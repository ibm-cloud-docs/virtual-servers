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

# Configuration des notifications pour la récupération des serveurs virtuels transitoires
{: #configuring-notifications-for-reclaims-of-transient-virtual-servers}

Les serveurs virtuels transitoires sont par nature éphémères et peuvent être arrêtés à tout moment, ce qui peut entraîner une perte de données. Des notifications de récupération automatisée peuvent aider à limiter la perte de données. Lors de sa mise à disposition, un serveur virtuel transitoire peut être configuré pour recevoir une notification indiquant qu'il est arrêté, **deux minutes** avant son arrêt effectif. La notification vous permet d'alerter, via un programme, le serveur virtuel transitoire et de lui demander d'arrêter le traitement en cours ou de transférer toutes les données nécessaires en dehors du serveur virtuel transitoire.

La notification `reclaim-scheduled` est une fonction de rappel webhook : une notification est envoyée par une demande HTTP POST vers un noeud final fourni par l'utilisateur. Procédez comme suit pour configurer et utiliser la fonction de rappel webhook :

1. Mettez à disposition une instance de serveur virtuel transitoire.
2. Configurez le webhook.
3. Vérifiez les demandes de webhook.

## Mise à disposition d'une instance de serveur virtuel transitoire
{: #provision-transient-virtual-server}

Les serveurs virtuels transitoires peuvent être mis à disposition via la console {{site.data.keyword.cloud_notm}}, {{site.data.keyword.slportal}} ou l'[API SLDN ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://sldn.softlayer.com){: new_window}. Pour plus d'informations, voir [Mise à disposition d'instances transitoires](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient).

## Configuration de la fonction de rappel webhook

Pour configurer la fonction webhook, vous devez affecter les paramètres suivants à l'instance de serveur virtuel transitoire en utilisant l'API SLDN :

   * **URI** - URI HTTP valide, vers laquelle la notification `reclaim-scheduled` est envoyée.
   * **Secret** - Chaîne qui est utilisée comme clé dans un algorithme de hachage pour signer la demande. Ne communiquez à personne la chaîne secrète.

La fonction de rappel webhook doit être configurée pour chaque serveur virtuel transitoire. Toutefois, l'URI et le secret n'ont pas besoin d'être uniques.

Les deux paramètres sont requis. Si l'URI ou le secret doivent être changés, appelez à nouveau la méthode avec les nouvelles informations.
{: tip}

La fonction de rappel webhook peut être définie via l'API SLDN en utilisant la méthode suivante :

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

Pour plus d'informations, voir la documentation relative à la méthode d'API SLDN pour la [configuration du webhook ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window}.

### Annulation des notifications reclaim-scheduled

Pour annuler les notifications `reclaim-scheduled`, appelez la méthode d'API SLDN suivante :

  `SoftLayer_Virtual_Guest::deleteWebhook()`

Pour plus d'informations, voir la documentation relative à la méthode d'API SLDN pour l'[annulation des notifications ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window}.

## Vérification des demandes webhook

Pour vérifier les notifications `reclaim-scheduled`, contrôlez les éléments suivants :

1. Horodatage de la demande

   Vérifiez l'heure de réception de la demande par rapport à l'horodatage dans les en-têtes de demande. S'il y a plus de 30 secondes de différence environ, n'acceptez pas la demande, afin de prévenir tout risque d'attaque par réinsertion.

2. Nonce trouvé dans l'en-tête "X-IBM-Nonce" de la demande

   Cette valeur est une chaîne qui est générée de façon aléatoire quand la demande est envoyée. Vous pouvez choisir de stocker les nonces reçus pour les comparer au nonce inclus dans la demande. Si le nonce de la demande a été utilisé auparavant, n'acceptez pas la demande afin de prévenir tout risque d'attaque par réinsertion.

3. Code HMAC (Hash Message Authentication Code) figurant dans l'en-tête "Authorization" de la demande

   Cette valeur est une chaîne qui a été hachée via l'algorithme HMAC-SHA256, qui utilise la chaîne secrète fournie en tant que clé, puis codée en Base64. Vous devez construire la chaîne, la hacher, la coder en Base64 puis comparer le résultat à la signature de l'en-tête "Authorization". En cas de non correspondance, n'acceptez pas la demande. Consultez les informations relatives à la création de la signature HMAC dans la section ci-dessous.

### Comparaison des signatures HMAC

Pour vérifier la signature HMAC qui se trouve dans l'en-tête "Authorization", vous devez créer une chaîne de comparaison. Procédez comme suit pour créer la chaîne :

1. Créez la chaîne canonique.

  La chaîne canonique doit contenir les données suivantes :
  * Type de méthode - POST dans ce cas (majuscules obligatoires)
  * Type de contenu - se trouve dans l'en-tête "Content-Type"
  * Contenu - corps de la demande. Cet exemple suppose que la chaîne JSON est décodée dans un tableau associatif natif ou dans un dictionnaire.  
  * Nonce - se trouve dans l'en-tête "X-IBM-Nonce"

  Pour créer la chaîne canonique, associez les données de la chaîne canonique dans l'ordre EXACT ci-après, sans délimiteurs :

  Type de méthode + Type de contenu + Contenu['id'] + Contenu['serviceName'] + Contenu['event'] + Contenu['time stamp'] + Nonce

2. Hachez la chaîne canonique.

  L'algorithme de hachage utilisé dans la fonction de rappel du serveur virtuel transitoire est HMAC-SHA256, soit un algorithme de hachage à clé. La clé à utiliser est le secret qui a été fourni quand la fonction webhook a été configurée.

3. Codez en Base64 la chaîne canonique de hachage.

4. Comparez la chaîne résultante à la signature de l'en-tête Authorization.  

  Utilisez une fonction de comparaison de chaînes permettant d'identifier les attaques temporelles. Si les chaînes ne correspondent pas, n'acceptez pas la demande.

## Anatomie du contenu de la demande de notification `reclaim-scheduled`

La demande qui est envoyée depuis la fonction de rappel du serveur virtuel transitoire est similaire à toute demande HTTP, en ce sens qu'elle dispose d'en-têtes et d'un contenu. Le contenu est une chaîne au format JSON, représentée ci-après :

**REMARQUE** : il n'est pas garanti que les noms de clé se présentent dans cet ordre spécifique.

	{
		'event': 'reclaim-scheduled',
		'id': <string - that is the ID of the transient guest being reclaimed>,
		'link': <string - link for an API call to return info about the guest being reaped>,
		'serviceName': <string - name of the API service class>,
		'time stamp': <integer - timestamp of when the reclaim was scheduled>
	}


## Exemples de code pour créer la signature HMAC

Python :

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

PHP :

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

Node.js :

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
