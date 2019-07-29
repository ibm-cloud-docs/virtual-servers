---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Benachrichtigungen für das Zurückfordern transienter virtueller Server konfigurieren
{: #configuring-notifications-for-reclaims-of-transient-virtual-servers}

Transiente virtuelle Server sind ihrer Art nach ephemer und können jederzeit beendet werden; dies führt möglicherweise zu Datenverlust. Hierbei können automatisierte Benachrichtigungen über ein Zurückfordern dazu beitragen, den Datenverlust zu verringern. Ist ein transienter, virtueller Server bereitgestellt, kann er so konfiguriert werden, dass **zwei Minuten** vor der tatsächlichen Beendigung eine Nachricht ausgegeben wird. Die Benachrichtigung ermöglicht es Ihnen, über ein Programm dafür zu sorgen, dass die gesamte aktuelle Verarbeitung beim transienten virtuellen Server beendet wird oder erforderliche Daten des transienten virtuellen Servers an andere Server übertragen werden.

Die Benachrichtigung `reclaim-scheduled` ist ein Webhook; dies bedeutet, die Benachrichtigung wird über die HTTP-Anforderung POST an einen vom Benutzer bereitgestellten Endpunkt gesendet. Führen Sie für die Einrichtung und Verwendung des Webhooks folgende Schritte aus:

1. Transiente virtuelle Serverinstanz bereitstellen
2. Webhook einrichten
3. Webhookanforderungen überprüfen

## Transiente virtuelle Serverinstanz bereitstellen
{: #provision-transient-virtual-server}

Transiente virtuelle Server können über die {{site.data.keyword.cloud_notm}}-Konsole, über das {{site.data.keyword.slportal}} oder über die [SLDN-API ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://sldn.softlayer.com){: new_window} bereitgestellt werden. Weitere Informationen finden Sie unter [Transiente Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient).

## Webhook einrichten

Zum Einrichten des Webhooks müssen Sie der transienten virtuellen Serverinstanz mithilfe der SLDN-API folgende Parameter zuordnen:

   * **URI** – Ein gültiger HTTP-URI, an den die Benachrichtigung `reclaim-scheduled` gesendet wird.
   * **Secret** – Eine Zeichenfolge, die als Schlüssel für einen Hashalgorithmus verwendet wird, um die Anforderung zu signieren. Teilen Sie diese geheime Zeichenfolge niemandem mit.

Der Webhook muss für jeden einzelnen der bereitgestellten transienten virtuellen Server eingerichtet werden. URI und geheimer Schlüssel müssen jedoch nicht für jeden Server eindeutig sein.

Beide Parameter sind erforderlich. Falls URI oder geheimer Schlüssel geändert werden müssen, rufen Sie die Methode mit den neuen Informationen erneut auf.
{: tip}

Der Webhook für den transienten virtuellen Server kann anhand der folgenden Methode über die SLDN-API eingerichtet werden:

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

Weitere Informationen finden Sie in der Dokumentation zur SLDN-API-Methode für die [Webhookeinrichtung ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window}.

### reclaim-scheduled-Benachrichtigungen stornieren

Zum Stornieren der `reclaim-scheduled`-Benachrichtigungen rufen Sie folgende SLDN-API-Methode auf:

  `SoftLayer_Virtual_Guest::deleteWebhook()`

Weitere Informationen finden Sie in der Dokumentation zur SLDN-API-Methode unter [Benachrichtigungen stornieren ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window}.

## Anforderungen des Webhooks überprüfen

Überprüfen Sie die `reclaim-scheduled`-Benachrichtigungen anhand folgender Punkte:

1. Die Zeitmarke der Anforderung

   Überprüfen Sie die Zeit, zu der die Anforderung empfangen wurde, anhand der Zeitmarke in den Anforderungsheadern. Liegt hier eine Abweichung von mehr als ca. 30 Sekunden vor, akzeptieren Sie die Anforderung nicht. Auf diese Weise können Attacken durch Nachrichtenaufzeichnung und -wiederholung verhindert werden.

2. Die generierte Zufallszahl im Header 'X-IBM-Nonce' der Anforderung

   Dieser Wert ist eine Zeichenfolge, die beim Senden der Anforderung zufällig generiert wird. Sie können auswählen, dass zuvor empfangene generierte Zufallszahlen gespeichert und mit der in der Anforderung enthaltenen generierten Zufallszahl verglichen werden. Wurde die in der Anforderung enthaltene generierte Zufallszahl zuvor bereits verwendet, akzeptieren Sie die Anforderung nicht. Auf diese Weise können Attacken durch Nachrichtenaufzeichnung und -wiederholung verhindert werden.

3. Der im Header 'Authorization' der Anforderung vorhandene, hashverschlüsselte Nachrichtenauthentifizierungscode (HMAC – Hash Message Authentication Code)

   Dieser Wert ist eine Zeichenfolge, die mithilfe des Algorithmus HMAC-SHA256, bei dem die geheime Zeichenfolge als Schlüssel verwendet wird, hashverschlüsselt und anschließend mit Base64 codiert wird. Sie müssen die Zeichenfolge erstellen, sie in einen Hashwert umwandeln, diesen mit Base64 codieren und das Ergebnis mit der Signatur im Header 'Authorization' vergleichen. Besteht keine Übereinstimmung, akzeptieren Sie die Anforderung nicht. Details zum Erstellen der HMAC-Signatur enthält der nächste Abschnitt.

### HMAC-Signaturen vergleichen

Zum Überprüfen der HMAC-Signatur, die im Header 'Authorization' der Anforderung enthalten ist, müssen Sie eine Vergleichszeichenfolge erstellen. Führen Sie zum Erstellen der Zeichenfolge folgende Schritte aus:

1. Erstellen Sie die kanonische Zeichenfolge.

  Die kanonische Zeichenfolge muss folgende Daten enthalten:
  * Method Type (Methodentyp) – in diesem Fall: POST (Großschreibung obligatorisch)
  * Content Type (Inhaltstyp) – im Header 'Content-Type' vorhanden
  * Payload (Nutzdaten) – Der Hauptteil der Anforderung. Bei diesem Beispiel wird vorausgesetzt, dass die JSON-Zeichenfolge in eine native assoziative Feldgruppe oder ein Wörterbuch decodiert wird.  
  * Nonce (Generierte Zufallszahl) – im Header 'X-IBM-Nonce' vorhanden

  Zum Erstellen der kanonischen Zeichenfolge kombinieren Sie die kanonischen Zeichenfolgedaten in exakt der folgenden Reihenfolge ohne Trennzeichen:

  Method Type + Content Type + Payload['id'] + Payload['serviceName'] + Payload['event'] + Payload['time stamp'] + Nonce

2. Wandeln Sie die kanonische Zeichenfolge in einen Hashwert um.

  Der im Webhook des transienten virtuellen Servers verwendete Hashalgorithmus lautet HMAC-SHA256 und basiert auf einer kryptographischen Hashfunktion. Der zu verwendende Schlüssel ist der geheime Schlüssel, der beim Einrichten des Webhooks angegeben wurde.

3. Hashverschlüsselte kanonische Zeichenfolge mit Base64 codieren.

4. Vergleichen Sie die sich ergebende Zeichenfolge mit der Signatur im Header 'Authorization'.  

  Verwenden Sie für den Zeichenfolgevergleich eine Funktion, die gegen Attacken auf Zeitabläufe gesichert ist. Stimmen die Zeichenfolgen nicht überein, akzeptieren Sie die Anforderung nicht.

## Aufbau der Nutzdaten in der Benachrichtigungsanforderung `reclaim-scheduled`

Die Anforderung, die vom Webhook des transienten virtuellen Servers gesendet wird, weist wie alle HTTP-Anforderungen Header und Nutzdaten auf. Die Nutzdaten sind eine Zeichenfolge mit JSON-Formatierung, die das folgende Format aufweist:

**HINWEIS**: Es gibt keine Garantie, dass die Schlüsselnamen in dieser bestimmten Reihenfolge auftreten.

	{
		'event': 'reclaim-scheduled',
		'id': <string - ID der transienten Gastmaschine, die zurückgefordert wird>,
		'link': <string - Link für einen API-Aufruf zur Rückgabe von Informationen zu der Gastmaschine, die zurückgefordert wird>,
		'serviceName': <string - Name der API-Serviceklasse>,
		'time stamp': <integer - Zeitmarke für den Zeitpunkt, an dem die Rückforderung angesetzt wurde>
	}


## Codebeispiele für die Erstellung der HMAC-Signatur

Python:

```
# Hier wird vorausgesetzt, dass die Anforderungsheader in einem Wörterbuch mit dem Namen 'Header' gespeichert werden und dass der JSON-Inhalt
# der Anforderung in ein Wörterbuch mit der Bezeichnung 'payload' (Nutzdaten) decodiert wird.

import base64
import hashlib
import hmac

secret = 'Ihr geheimer Schlüssel'
canonical = 'POST' + headers['Content-Type'] + payload['id'] + payload['serviceName'] + payload['event'] \
	    + payload['timestamp'] + headers['X-IBM-Nonce']
signature = base64.b64encode(hmac.new(secret, canonical, hashlib.sha256).hexdigest())
match_flag = hmac.compare_digest(headers['Authorization'], signature)
```
{: screen}

PHP:

```
// Hier wird vorausgesetzt, dass die Anforderungsheader in einer assoziativen Feldgruppe mit der Bezeichnung $headers gespeichert
// werden und dass der JSON-Inhalt der Anforderung in eine assoziative Feldgruppe mit der Bezeichnung $payload entschlüsselt wird.

$secret = 'Ihr geheimer Schlüssel';
$canonical = 'POST' . $headers['Content-Type'] . $payload['id'] . $payload['serviceName'] . $payload['event']
	     . payload['time stamp'] . $headers['X-IBM-Nonce'];
$signature = base64_encode(hash_hmac('sha256', $canonical, $secret));
$matchFlag = hash_equals($headers['Authorization'], $signature);
```
{: screen}

Node.js:

```
// Hier wird vorausgesetzt, dass die Anforderungsheader in Variablen mit den Namen 'content_type', 'nonce' und 'auth_string' gespeichert werden.
// Hier wird auch vorausgesetzt, dass der Inhalt der Anforderung ein JSON-Objekt mit der Bezeichnung 'payload' ist.

const crypto = require('crypto');

var canonical = 'POST' + content_type + payload.id + payload.serviceName + payload.event + payload.timestamp + nonce;
hmac = crypto.createHmac('sha256', secret).update(canonical);
signature = Buffer.from(hmac.digest('hex')).toString('base64');
matchFlag = crypto.timingSafeEqual(auth_string, signature);
```
{: screen}
