---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Vue d'ensemble des références d'API 
{: #api-reference}

L'API {{site.data.keyword.slapi_full}} constitue l'interface de développement permettant aux développeurs et aux administrateurs système de gérer l'interaction avec le système dorsal d'{{site.data.keyword.cloud_notm}}. {{site.data.keyword.slapi_short}} optimise de nombreuses fonctionnalités de la console {{site.data.keyword.cloud_notm}}, ce qui signifie généralement que si une interaction est possible dans la console {{site.data.keyword.cloud_notm}}, elle peut également être exécutée dans l'API. Etant donné que vous pouvez interagir à l'aide d'un programme avec l'ensemble de l'environnement {{site.data.keyword.cloud_notm}} dans l'API, l'API {{site.data.keyword.slapi_short}} vous permet d'automatiser les tâches. Vous pouvez, par exemple, utiliser l'API *SoftLayer_Virtual_Guest/createObject* pour déployer une instance de serveur virtuel.
{:shortdesc}

L'API {{site.data.keyword.slapi_short}} est un système d'appel de procédure distante (RPC). Chaque appel implique l'envoi de données vers un noeud final d'API et la réception de données structurées. Le format utilisé pour l'envoi et la réception de données avec l'API {{site.data.keyword.slapi_short}} dépend de l'implémentation choisie pour l'API . L'API {{site.data.keyword.slapi_short}} utilise actuellement SOAP, XML-RPC ou REST pour la transmission des données.

Pour plus d'informations sur l'API {{site.data.keyword.slapi_short}} et les API de serveur virtuel, consultez les ressources suivantes dans {{site.data.keyword.sldn_full}} :
* [{{site.data.keyword.slapi_short}} Overview ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/reference/softlayerapi/){: new_window}
* [Getting Started with the {{site.data.keyword.slapi_short}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/article/getting-started/){: new_window}
* [API Reference: SoftLayer_Virtual_Guest::createObject ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/){: new_window}
* [API Reference: SoftLayer_Product_Order::placeOrder ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/){: new_window}

Pour des exemples d'utilisation d'API, voir les ressources suivantes :
* [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/article/understanding-ordering/){: new_window}
* [{{site.data.keyword.slapi_short}} Python Client: Working with Virtual Servers ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [{{site.data.keyword.slapi_short}} Examples - Release Notes ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/){: new_window}
* [Python examples ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/python/){: new_window}

## Exemples d'utilisation de serveurs virtuels dédiés
* [Get Dedicated Host Allocation ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/python/getDediHostAllocation/){: new_window}
* [Get Dedicated Host Guests ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/python/getDedicatedHostGuests/){: new_window}
* [Migrate a VSI between dedicated hosts ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/python/migrateDedicatedHost.py/){: new_window}

## Exemples d'utilisation de serveurs virtuels publics
* [Exemples d'API softlayer_virtual_guest ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
