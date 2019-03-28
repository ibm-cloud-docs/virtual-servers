---

copyright:
  years: 2018
lastupdated: "2018-05-11"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Configurando notificações para recuperações de servidores virtuais temporários
{: #configuring-notifications-for-reclaims-of-transient-virtual-servers}

Servidores virtuais temporários são, por natureza, efêmeros e podem ser finalizados a qualquer momento, o que pode levar à perda de dados. As notificações de recuperação automatizadas podem ajudar a reduzir a perda de dados. Quando provisionado, um servidor virtual temporário pode ser configurado para receber uma notificação indicando que ele está sendo finalizado **dois minutos** antes da finalização real. A notificação permite alertar programaticamente o servidor virtual temporário para concluir qualquer processamento em andamento ou transferir quaisquer dados necessários para fora do servidor virtual temporário.

A notificação `reclaim-scheduled` é um webhook, o que significa que a notificação é enviada por uma solicitação de POST HTTP para um terminal fornecido pelo usuário. Conclua as etapas a seguir para configurar e usar o webhook:

1. Forneça uma instância do servidor virtual temporário.
2. Configure o webhook.
3. Verifique as solicitações do webhook.

## Provisionando uma instância de servidor virtual temporária
{: #provision-transient-virtual-server}

Servidores virtuais temporários podem ser provisionados por meio do [{{site.data.keyword.slportal_full}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} ou por meio da [API SLDN ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://sldn.softlayer.com){: new_window}. Para obter mais informações, consulte [Provisionando instâncias temporárias](/docs/vsi?topic=virtual-servers-ordering-vs-transient).

## Configurando o webhook

Para configurar o webhook, é necessário designar os parâmetros a seguir para a instância temporária do servidor virtual usando a API SLDN:

   * **URI** - um URI HTTP válido para o qual a notificação `reclaim-scheduled` é enviada.
   * **Segredo** - uma sequência que é usada como a chave para um algoritmo hash assinar a solicitação. Não comunique a sequência secreta para ninguém.

O webhook deve ser configurado para cada servidor virtual temporário provisionado. No entanto, o URI e o segredo não precisam ser exclusivos.

Ambos os parâmetros são necessários. Se o URI ou o segredo tiver que ser mudado, chame o método novamente com as novas informações.
{: tip}

O webhook do servidor virtual temporário pode ser configurado por meio da API SLDN usando o método a seguir:

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

Para obter mais informações, consulte a documentação do método da API SLDN para a configuração de webhook do [
![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window}.

### Cancelando as notificações reclaim-scheduled

Para cancelar as notificações `reclaim-scheduled`, chame o seguinte método da API SLDN:

  `SoftLayer_Virtual_Guest::deleteWebhook()`

Para obter mais informações, consulte a documentação do método da API SLDN para [cancelamento de notificações ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window}.

## Verificando as solicitações de webhook

Para verificar as notificações `reclaim-scheduled`, revise os seguintes itens:

1. O registro de data e hora da solicitação

   Verifique a hora em que a solicitação foi recebida com relação ao registro de data e hora nos cabeçalhos da
solicitação. Se estiver desligado por mais de aproximadamente 30 segundos, não aceite a solicitação. Essa ação pode
ajudar a evitar os ataques de reprodução.

2. O nonce localizado no cabeçalho "X-IBM-Nonce" da solicitação

   Esse valor é uma sequência que é gerada aleatoriamente quando a solicitação é enviada. É possível escolher armazenar nonces recebidos anteriormente para comparar ao nonce incluído na solicitação. Se o nonce na solicitação foi usado anteriormente, não aceite a solicitação. Essa ação pode
ajudar a evitar os ataques de reprodução.

3. Hash Message Authentication Code (HMAC) localizado no cabeçalho "Authorization" da solicitação

   Esse valor é uma sequência feita em hash usando o algoritmo HMAC-SHA256 que usa a sequência secreta fornecida como a chave e, em seguida, codificada em Base64. É necessário construir a sequência, fazer hash dela, codificá-la em Base64 e, então, comparar o resultado com a assinatura no cabeçalho "Authorization". Se não corresponderem, não aceite a solicitação. Consulte a próxima seção para obter detalhes sobre como criar a assinatura HMAC.

### Comparando as assinaturas HMAC

Para verificar a assinatura HMAC que está localizada no cabeçalho "Autorização" da solicitação, é necessário criar
uma sequência de comparação. Conclua as etapas a seguir para criar a sequência:

1. Crie a sequência canônica.

  A sequência canônica deve conter os seguintes dados:
  * Tipo de método: POST nesse caso (deve estar em letras maiúsculas)
  * Tipo de conteúdo - localizado no cabeçalho "Content-Type"
  * Carga útil - o corpo da solicitação. Esse exemplo assume que a sequência JSON é decodificada em uma matriz
ou dicionário associativo nativo.  
  * Nonce - localizado no cabeçalho "X-IBM-Nonce"

  Para criar a sequência canônica, combine os dados de sequência canônica na ordem EXATA a seguir sem
delimitadores:

  Tipo de método + Tipo de conteúdo + Carga útil['ID'] + Carga útil['nome do serviço'] + Carga
útil['evento'] + Carga útil['registro de data e hora'] + Nonce

2. Faça hash da sequência canônica.

  O algoritmo hash que é usado no webhook do servidor virtual temporário é HMAC-SHA256, que é um algoritmo hash
com chave. A chave a ser usada é o segredo que foi fornecido quando o webhook foi configurado.

3. Codifique a sequência canônica em hash para Base64.

4. Compare a sequência resultante com a assinatura no cabeçalho 'Authorization'.  

  Use uma função segura de comparação de sequência de ataque de tempo. Se as sequências não corresponderem, não aceite a solicitação.

## Anatomia da carga útil da solicitação de notificação `reclaim-scheduled`

A solicitação que é enviada do webhook do servidor virtual temporário é como qualquer solicitação HTTP
quanto aos cabeçalhos e uma carga útil. A carga útil é uma sequência formatada em JSON no formato a seguir:

**NOTA**: não há garantia de que os nomes de chave estejam nessa ordem específica.

	{
		'event': 'reclaim-scheduled',
		'id': <sequência: que é o ID do guest temporário que está sendo recuperado>,
		'link': <sequência: link para uma chamada API para retornar as informações sobre o guest que está sendo
removido>, 		'serviceName': <sequência: nome da classe de serviço API>,
		'time stamp': <número inteiro: registro de data e hora de quando a recuperação foi planejada>
	}


## Exemplos de código para criação da assinatura HMAC

Python:

```
# This assumes that the request headers are stored in a dictionary called headers and that the JSON
# content of the request has been decoded into a dictionary called payload.

import base64
import hashlib
import hmac

secret = 'Your secret key'
canonical = 'POST' + headers['Content-Type'] + payload['id'] + payload['serviceName'] + payload['event'] \
	    + payload['timestamp'] + headers['X-IBM-Nonce']
signature = base64.b64encode(hmac.new(secret, canonical, hashlib.sha256).hexdigest())
match_flag = hmac.compare_digest(headers['Authorization'], signature)
```
{: screen}

PHP:

```
// This assumes that the request headers are stored in an associative array called $headers and that
// the JSON content of the request is decoded into an associative array called $payload.

$secret = 'Your secret key';
$canonical = 'POST' . $headers['Content-Type'] . $payload['id'] . $payload['serviceName'] . $payload['event']
	     . payload['time stamp'] . $headers['X-IBM-Nonce'];
$signature = base64_encode(hash_hmac('sha256', $canonical, $secret));
$matchFlag = hash_equals($headers['Authorization'], $signature);
```
{: screen}

Node.js:

```
// This assumes that the request headers are stored in variables that are named content_type, nonce, and auth_string.
// This also assumes that the content of the request is a JSON object called payload.

const crypto = require('crypto');

var canonical = 'POST' + content_type + payload.id + payload.serviceName + payload.event + payload.timestamp + nonce;
hmac = crypto.createHmac('sha256', secret).update(canonical);
signature = Buffer.from(hmac.digest('hex')).toString('base64');
matchFlag = crypto.timingSafeEqual(auth_string, signature);
```
{: screen}
