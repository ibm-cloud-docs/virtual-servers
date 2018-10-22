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

# Configurazione delle notifiche per i recuperi dei server virtuali temporanei

I server virtuali temporanei sono per loro natura temporanei e possono essere terminati in qualsiasi momento, che potrebbe comportare la perdita di dati. Le notifiche di recupero automatizzate possono essere utili a ridurre la perdita di dati. Quando ne viene eseguito il provisioning, un server virtuale temporaneo può essere configurato per ricevere una notifica che sta per essere terminato, **due minuti** prima della terminazione effettiva. La notifica ti consente di avvisare in modo programmatico il server virtuale temporaneo di finire qualsiasi elaborazione in corso o di trasferire tutti i dati necessari al di fuori di esso.

La notifica `reclaim-scheduled` è un webhook, il che significa che la notifica viene inviata da una richiesta HTTP POST a un endpoint fornito dall'utente. Completa la seguente procedura per configurare e utilizzare il webhook:

1. Esegui il provisioning di un'istanza del server virtuale temporanea. 
2. Configura il webhook.
3. Verifica le richieste del webhook.

## Provisioning di un'istanza del server virtuale temporanea

I server virtuali temporanei possono essere forniti tramite [{{site.data.keyword.slportal_full}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} o tramite [SLDN API ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://sldn.softlayer.com){: new_window}. Per ulteriori informazioni, vedi [Provisioning delle istanze temporanee](/docs/vsi/vsi_provision_transient.html).

## Configurazione del webhook

Per configurare il webhook, devi assegnare i seguenti parametri all'istanza del server virtuale temporaneo utilizzando l'API SLDN:

   * **URI** - Un URI HTTP valido a cui viene inviata la notifica `reclaim-scheduled`.
   * **Segreto** - Una stringa utilizzata come la chiave dell'algoritmo hash per firmare la richiesta. Non comunicare la stringa segreta a nessuno.

Il webhook deve essere configurato per ogni server virtuale temporaneo fornito. Tuttavia, non è necessario che l'URI e il segreto siano univoci.

Entrambi i parametri sono obbligatori. Se l'URI o il segreto devono essere modificati, richiama nuovamente il metodo con le nuove informazioni.
{: tip}

Il webhook del server virtuale temporaneo può essere configurato tramite l'API SLDN utilizzando il seguente metodo:

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

Per ulteriori informazioni, consulta la documentazione del metodo API SLDN per [configurare il webhook ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window}.

### Annullamento delle notifiche reclaim-scheduled

Per annullare le notifiche `reclaim-scheduled`, richiama il seguente metodo API SLDN:

  `SoftLayer_Virtual_Guest::deleteWebhook()`

Per ulteriori informazioni, consulta la documentazione del metodo API SLDN per [annullare le notifiche ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window}.

## Verifica delle richieste del webhook

Per verificare le notifiche `reclaim-scheduled`, controlla i seguenti elementi:

1. La data/ora della richiesta

   Controlla l'ora in cui è stata ricevuta la richiesta con la data/ora nelle intestazioni della richiesta. Se è diversa per più di 30 secondi circa, non accettare la richiesta. Questa azione può essere utile per evitare attacchi di tipo replay.

2. Il nonce trovato nell'intestazione "X-IBM-Nonce" della richiesta

   Questo valore è una stringa generata in modo casuale quando viene inviata la richiesta. Puoi scegliere di archiviare precedentemente i nonce ricevuti per confrontarli con quello incluso nella richiesta. Se il nonce nella richiesta è già stato utilizzato, non accettare la richiesta. Questa azione può essere utile per evitare attacchi di tipo replay.

3. L'Hash Message Authentication Code (HMAC) ubicato nell'intestazione "Authorization" della richiesta.

   Questo valore è una stringa distribuita in modo casuale utilizzando l'algoritmo HMAC-SHA256 che utilizza la stringa del segreto fornita come chiave e quindi codificata in Base64. Devi creare la stringa, distribuirla in modo casuale, codificarla in Base64 e quindi confrontare il risultato con la firma dell'intestazione "Authorization". Se non corrispondono, non accettare la richiesta. Vedi la seguente sezione per i dettagli sulla creazione della firma HMAC.

### Confronto delle firme HMAC

Per verificare la firma HMAC ubicata nell'intestazione "Authorization" della richiesta, devi creare una stringa di confronto. Completa la seguente procedura per creare la stringa:

1. Crea la stringa canonica.

  La stringa canonica deve contenere i seguenti dati:
  * Tipo di metodo - POST in questo caso (deve essere maiuscolo)
  * Tipo di contenuto - Trovato nell'intestazione "Content-Type"
  * Payload - Il corpo della richiesta. Questo esempio presuppone che la stringa JSON è stata decodificata in un dizionario o un array associativo nativo.  
  * Nonce - Trovato nell'intestazione "X-IBM-Nonce"

  Per creare la stringa canonica, combina i dati della stringa canonica nel seguente ordine ESATTO senza delimitatori:

  Tipo di metodo + Tipo di contenuto + Payload['id'] + Payload['serviceName'] + Payload['event'] + Payload['time stamp'] + Nonce

2. Hash della stringa canonica

  L'algoritmo di hash utilizzato nel webhook del server virtuale temporaneo è HMAC-SHA256, che è un algoritmo di hash con chiave. La chiave da utilizzare è il segreto che è stato fornito quando è stato configurato il webhook.

3. Codifica la stringa canonica distribuita in modo casuale in Base64.

4. Confronta la stringa risultante con la firma nell'intestazione 'Authorization'.  

  Utilizza una funzione di confronto della stringa sicura di attacco di timing. Se le stringhe non corrispondono, non accettare la richiesta.

## Anatomia del payload della richiesta della notifica `reclaim-scheduled`

La richiesta inviata dal webhook del server virtuale temporaneo è come qualsiasi altra richiesta HTTP con intestazioni e un payload. Il payload è una stringa formattata JSON nel seguente formato:

**NOTA**: non c'è alcuna garanzia che i nomi della chiave sono in questo ordine specifico.

	{
		'event': 'reclaim-scheduled',
		'id': <string - that is the ID of the transient guest being reclaimed>,
		'link': <string - link for an API call to return info about the guest being reaped>,
		'serviceName': <string - name of the API service class>,
		'time stamp': <integer - timestamp of when the reclaim was scheduled>
	}


## Esempi di codice per la creazione della firma HMAC

Python:

```
# Assume che le intestazioni della richiesta siano archiviate in un dizionario denominato intestazioni e che il contenuto JSON
# della richiesta sia stato codificato in un dizionario denominato payload.

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
// Assume che le intestazioni della richiesta siano archiviate in un array associativo denominato $headers e che
// il contenuto JSON della richiesta è stato codificato in un array associativo denominato $payload.

$secret = 'Your secret key';
$canonical = 'POST' . $headers['Content-Type'] . $payload['id'] . $payload['serviceName'] . $payload['event']
	     . payload['time stamp'] . $headers['X-IBM-Nonce'];
$signature = base64_encode(hash_hmac('sha256', $canonical, $secret));
$matchFlag = hash_equals($headers['Authorization'], $signature);
```
{: screen}

Node.js:

```
// Assume che le intestazioni della richiesta siano archiviate in variabili denominate content_type, nonce e auth_string.
// Assume inoltre che il contenuto della richiesta sia un oggetto JSON denominato payload.

const crypto = require('crypto');

var canonical = 'POST' + content_type + payload.id + payload.serviceName + payload.event + payload.timestamp + nonce;
hmac = crypto.createHmac('sha256', secret).update(canonical);
signature = Buffer.from(hmac.digest('hex')).toString('base64');
matchFlag = crypto.timingSafeEqual(auth_string, signature);
```
{: screen}
