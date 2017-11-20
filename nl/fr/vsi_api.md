---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Référence d'API
{: #api-reference} 

L'API {{site.data.keyword.slapi_full}} constitue l'interface de développement permettant aux développeurs et aux administrateurs système de gérer l'interaction avec le système dorsal d'{{site.data.keyword.cloud}}. Un grand nombre de fonctions du portail {{site.data.keyword.slportal_full}} sont également disponibles dans l'API {{site.data.keyword.slapi_short}}. Autrement dit, si une interaction est possible dans le portail {{site.data.keyword.slportal}}, elle peut également être exécutée dans l'API. Etant donné que vous pouvez interagir à l'aide d'un programme avec l'ensemble de l'environnement {{site.data.keyword.BluSoftlayer_full}} dans l'API, l'API {{site.data.keyword.slapi_short}} vous permet d'automatiser les tâches. Vous pouvez, par exemple, utiliser l'API *SoftLayer_Virtual_Guest/createObject* pour déployer une instance de serveur virtuel.
{:shortdesc}

L'API {{site.data.keyword.slapi_short}} est un système d'appel de procédure distante (RPC). Chaque appel implique l'envoi de données vers un noeud final d'API et la réception de données structurées. Le format utilisé pour l'envoi et la réception de données avec l'API {{site.data.keyword.slapi_short}} dépend de l'implémentation choisie pour l'API . L'API {{site.data.keyword.slapi_short}} utilise actuellement SOAP, XML-RPC ou REST pour la transmission des données.

Pour plus d'informations sur l'API {{site.data.keyword.slapi_short}} et les API de serveur virtuel, consultez les ressources suivantes dans {{site.data.keyword.sldn_full}} :
* [{{site.data.keyword.slapi_short}} Overview ![External link icon](../icons/launch-glyph.svg "External link icon")](https://sldn.softlayer.com/article/softlayer-api-overview){: new_window} 
* [Getting Started with the {{site.data.keyword.slapi_short}} ![External link icon](../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/article/getting-started){: new_window}
* [API Reference: SoftLayer_Virtual_Guest::createObject ![External link icon](../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/reference/services/softlayer_virtual_guest/createobject){: new_window}
* [API Reference: SoftLayer_Product_Order::placeOrder ![External link icon](../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/reference/services/SoftLayer_Product_Order/placeOrder){: new_window}

Pour des exemples d'utilisation d'API, voir les ressources suivantes :
* [{{site.data.keyword.slapi_short}} Python Client: Working with Virtual Servers ![External link icon](../icons/launch-glyph.svg "External link icon")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [{{site.data.keyword.slapi_short}} Examples - Release Notes ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/){: new_window}
* [Python examples ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/python/){: new_window}

## Exemples d'utilisation de serveurs virtuels dédiés
* [Get Dedicated Host Allocation ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/python/getdedihostallocation/){: new_window}
* [Get Dedicated Host Guests ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/python/getdedicatedhostguests/){: new_window}
* [Migrate a VSI between dedicated hosts ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/python/migratededicatedinstance/){: new_window}

## Exemples d'utilisation de serveurs virtuels publics
* [softlayer_virtual_guest API examples ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
