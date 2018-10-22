---



copyright:
  years: 2018
lastupdated: "2018-05-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Configuración de notificaciones para las reclamaciones de servidores virtuales transitorios

Los servidores virtuales transitorios son, por naturaleza, efímeros y se pueden terminar en cualquier momento, lo que podría provocar una pérdida de datos. Las notificaciones de reclamación automatizada pueden ayudarle a reducir la pérdida de datos. Cuando está suministrado, un servidor virtual transitorio se puede configurar para que reciba una notificación de que se está terminando **dos minutos** antes de la terminación real. La notificación le permite alertar mediante programación al servidor virtual transitorio para que finalice los procesos en curso o para que transfiera los datos necesarios fuera del servidor virtual transitorio.

La notificación `reclaim-scheduled` es un webhook, lo que significa que la notificación se envía mediante una solicitud POST HTTP a un punto final proporcionado por el usuario. Complete los pasos siguientes para configurar y utilizar el webhook:

1. Suministre una instancia de servidor virtual transitorio.
2. Configure el webhook.
3. Verifique las solicitudes del webhook.

## Suministro de una instancia de servidor virtual transitorio

Los servidores virtuales transitorios pueden suministrarse a través del [{{site.data.keyword.slportal_full}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} o a través de la [API de SLDN ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://sldn.softlayer.com){: new_window}. Para obtener más información, consulte [Suministro de instancias transitorias](/docs/vsi/vsi_provision_transient.html).

## Configuración del webhook

Para configurar el webhook, tiene que asignar los parámetros siguientes a la instancia de servidor virtual transitorio utilizando la API de SLDN:

   * **URI**: Un URI HTTP válido al que se envía la notificación `reclaim-scheduled`.
   * **Secreto**: Una serie que se utiliza como la clave de un algoritmo hash para firmar la solicitud. No revele a nadie este secreto.

El webhook debe estar configurado para cada servidor virtual transitorio suministrado. Sin embargo, el URI y el secreto no tienen que ser exclusivos.

Ambos parámetros son necesarios. Si el URI o el secreto se deben cambiar, vuelva a llamar al método con la nueva información.
{: tip}

El webhook del servidor virtual transitorio se puede configurar a través de la API de SLDN utilizando el método siguiente:

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

Para obtener más información, consulte la documentación del método de la API de SLDN para la [configuración del webhook ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window}.

### Cancelación de notificaciones reclaim-scheduled

Para cancelar las notificaciones `reclaim-scheduled`, llame al siguiente método de la API de SLDN:

  `SoftLayer_Virtual_Guest::deleteWebhook()`

Para obtener más información, consulte la documentación del método de la API de SLDN para la [cancelación de notificaciones ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window}.

## Verificación de las solicitudes del webhook

Para verificar las notificaciones `reclaim-scheduled` revise los elementos siguientes:

1. La indicación de fecha y hora de la solicitud

   Compruebe la hora en que se ha recibido la solicitud en la indicación de fecha y hora de las cabeceras de la solicitud. Si hay una diferencia de más de 30 segundos o similar, no acepte la solicitud. Esta acción puede ayudarle a evitar los ataques por reproducción.

2. El nonce que se encuentra en la cabecera "X-IBM-Nonce" de la solicitud

   Este valor es una serie que se genera aleatoriamente cuando se envía la solicitud. Puede elegir almacenar los nonces previamente recibidos para compararlos con el nonce incluido en la solicitud. Si el nonce en la solicitud se ha utilizado antes, no acepte la solicitud. Esta acción puede ayudarle a evitar los ataques por reproducción.

3. El código de autenticación de mensaje hash (HMAC) ubicado en la cabecera "Authorization" de la solicitud

   Este valor es una serie a la que se ha aplicado la función hash mediante el algoritmo HMAC-SHA256 que utiliza la serie secreta proporcionada como clave y que luego se ha codificado en Base64. Debe construir la serie, aplicarle la función hash, codificarla en Base64 y, a continuación, comparar el resultado con la firma en la cabecera "Authorization". Si no coinciden, no acepte la solicitud. Consulte la sección siguiente para ver detalles sobre la creación de la firma HMAC.

### Comparación de firmas HMAC

Para verificar la firma HMAC que se encuentra en la cabecera "Authorization" de la solicitud, debe crear una serie de comparación. Complete los pasos siguientes para crear la serie:

1. Cree la serie canónica.

  La serie canónica debe contener los datos siguientes:
  * Tipo de método: POST en este caso (debe estar en mayúsculas)
  * Tipo de contenido: Se encuentra en la cabecera "Content-Type".
  * Carga útil: El cuerpo de la solicitud. En este ejemplo se presupone que la serie JSON se ha decodificado en una matriz o diccionario asociativo nativo.  
  * Nonce: se encuentra en la cabecera "X-IBM-Nonce".

  Para crear la serie canónica, combine los datos de la serie canónica en el siguiente orden EXACTO sin delimitadores:

  Tipo de método + Tipo de contenido + Carga útil['id'] + Carga útil['serviceName'] + Carga útil['event'] + Carga útil['time stamp'] + Nonce

2. Aplique la función hash a la serie canónica.

  El algoritmo de hash que se ha utilizado en el webhook del servidor virtual transitorio es HMAC-SHA256, que es un algoritmo de has con clave. La clave que se debe utilizar es el secreto que se proporcionó cuando se configuró el webhook.

3. Codifique la serie canónica a Base64.

4. Compare la serie resultante con la firma en la cabecera 'Authorization'.  

  Utilice función de comparación de series seguras timing-attack. Si las series no coinciden, no acepte la solicitud.

## Anatomía de la carga útil de solicitud de notificación `reclaim-scheduled`

La solicitud que se ha enviado desde el webhook del servidor virtual transitorio es como cualquier solicitud HTTP en que tiene cabeceras y una carga útil. La carga útil es una serie con formato JSON con la forma siguiente:

**NOTA**: no hay ninguna garantía de que los nombres de clave estén en este orden específico.

	{
		'event': 'reclaim-scheduled',
		'id': <string - ID del invitado transitorio que se está reclamando>,
		'link': <string - enlace correspondiente a la llamada de API para devolver información sobre el invitado que se está captando>,
		'serviceName': <string - nombre de la clase de servicio de API>,
		'time stamp': <integer - indicación de fecha y hora del momento en que se planificó la reclamación>
	}


## Ejemplos de código para crear la firma de HMAC

Python:

```
# Se da por supuesto que las cabeceras de solicitud se almacenan en un diccionario llamado headers y que el
# contenido de JSON de la solicitud se ha descodificado en un diccionario llamado payload.

import base64
import hashlib
import hmac

secret = 'Su clave secreta'
canonical = 'POST' + headers['Content-Type'] + payload['id'] + payload['serviceName'] + payload['event'] \
	    + payload['timestamp'] + headers['X-IBM-Nonce']
signature = base64.b64encode(hmac.new(secret, canonical, hashlib.sha256).hexdigest())
match_flag = hmac.compare_digest(headers['Authorization'], signature)
```
{: screen}

PHP:

```
// Se da por supuesto que las cabeceras de solicitud se almacenan en una matriz asociativa denominada $headers y
// que el contenido JSON de la solicitud se ha descodificado en una matriz asociativa llamada $payload.

$secret = 'Su clave secreta';
$canonical = 'POST' . $headers['Content-Type'] . $payload['id'] . $payload['serviceName'] . $payload['event']
	     . payload['time stamp'] . $headers['X-IBM-Nonce'];
$signature = base64_encode(hash_hmac('sha256', $canonical, $secret));
$matchFlag = hash_equals($headers['Authorization'], $signature);
```
{: screen}

Node.js:

```
// Se da por supuesto que las cabeceras de solicitud se almacenan en variables denominadas content_type, nonce y auth_string.
// También se da por supuesto que el contenido de la solicitud es un objeto JSON denominado payload.

const crypto = require('crypto');

var canonical = 'POST' + content_type + payload.id + payload.serviceName + payload.event + payload.timestamp + nonce;
hmac = crypto.createHmac('sha256', secret).update(canonical);
signature = Buffer.from(hmac.digest('hex')).toString('base64');
matchFlag = crypto.timingSafeEqual(auth_string, signature);
```
{: screen}
