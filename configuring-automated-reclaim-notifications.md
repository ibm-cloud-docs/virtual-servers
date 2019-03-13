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

# Configuring notifications for reclaims of transient virtual servers
{: #configuring-notifications-for-reclaims-of-transient-virtual-servers}

Transient virtual servers are by their nature ephemeral and they can be terminated at any time, which might lead to lost data. Automated reclaim notifications can help reduce lost data. When provisioned, a transient virtual server can be configured to receive a notification that it is being terminated **two minutes** before the actual termination. The notification enables you to programmatically alert the transient virtual server to finish any processing that is in progress or to transfer any necessary data off the transient virtual server.

The `reclaim-scheduled` notification is a webhook, which means the notification is sent by an HTTP POST request to a user-provided endpoint. Complete the following steps to set up and use the webhook:

1. Provision a transient virtual server instance.
2. Set up the webhook.
3. Verify the webhook requests.

## Provisioning a transient virtual server instance

Transient virtual servers can be provisioned through the [{{site.data.keyword.slportal_full}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} or through the [SLDN API ![External link icon](../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com){: new_window}. For more information, see [Provisioning transient instances](/docs/vsi?topic=virtual-servers-ordering-vs-transient).

## Setting up the webhook

To set up the webhook, you need to assign the following parameters to the transient virtual server instance by using the SLDN API:

   * **URI** - A valid HTTP URI to which the `reclaim-scheduled` notification is sent.
   * **Secret** - A string that is used as the key to a hash algorithm to sign the request. Do not communicate the secret string to anyone else.

The webhook must be set up for each provisioned transient virtual server. However, the URI and the secret do not need to be unique.

Both parameters are required. If the URI or secret must be changed, call the method again with the new information.
{: tip}

The transient virtual server webhook can be set up through the SLDN API by using the following method:

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

For more information, see the SLDN API method documentation for [webhook set-up ![External link icon](../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window}.

### Canceling reclaim-scheduled notifications

To cancel the `reclaim-scheduled` notifications, call the following SLDN API method:

  `SoftLayer_Virtual_Guest::deleteWebhook()`

For more information, see the SLDN API method documentation for [canceling notifications ![External link icon](../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window}.

## Verifying the webhook requests

To verify `reclaim-scheduled` notifications, review the following items:

1. The time stamp of the request

   Check the time that the request was received against the time stamp in the request headers. If it is off by more than 30 seconds or so, do not accept the request. This action can help prevent replay attacks.

2. The nonce found in the request's "X-IBM-Nonce" header

   This value is a string that is randomly generated when the request is sent. You can choose to store previously received nonces to compare against the nonce included in the request. If the nonce in the request was used before, do not accept the request. This action can help prevent replay attacks.

3. Hash Message Authentication Code (HMAC) located in the request's "Authorization" header

   This value is a string that is hashed by using the HMAC-SHA256 algorithm that uses the provided secret string as the key, and then encoded into Base64. You need to construct the string, hash it, encode it to Base64, and then compare the result to the signature in the "Authorization" header. If they do not match, do not accept the request. See next section for details on creating the HMAC signature.

### Comparing the HMAC signatures

To verify the HMAC signature that is located in the request's "Authorization" header, you need to create a comparison string. Complete the following steps to create the string:

1. Create the canonical string.

  The canonical string must contain the following data:
  * Method Type - POST in this case (must be uppercase)
  * Content Type - Found in the "Content-Type" header
  * Payload - The body of the request. This example assumes that the JSON string is decoded into a native associative array or dictionary.  
  * Nonce - Found in the "X-IBM-Nonce" header

  To create the canonical string, combine the canonical string data in the following EXACT order with no delimiters:

  Method Type + Content Type + Payload['id'] + Payload['serviceName'] + Payload['event'] + Payload['time stamp'] + Nonce

2. Hash the canonical string.

  The hashing algorithm that is used in the transient virtual server webhook is HMAC-SHA256, which is a keyed hashing algorithm. The key to use is the secret that was provided when the webhook was set up.

3. Encode the hashed canonical string to Base64.

4. Compare the resulting string to the signature in the 'Authorization' header.  

  Use a timing-attack safe string comparison function. If the strings do not match, do not accept the request.

## Anatomy of the `reclaim-scheduled` notification request payload

The request that is sent from the transient virtual server webhook is like any HTTP request in that it has headers and a payload. The payload is a JSON formatted string in the following form:

**NOTE**: There is no guarantee that the key names are in this specific order.

	{
		'event': 'reclaim-scheduled',
		'id': <string - that is the ID of the transient guest being reclaimed>,
		'link': <string - link for an API call to return info about the guest being reaped>,
		'serviceName': <string - name of the API service class>,
		'time stamp': <integer - timestamp of when the reclaim was scheduled>
	}


## Code examples for creating the HMAC signature

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
