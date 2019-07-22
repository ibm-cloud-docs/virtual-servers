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

# Panoramica sulla guida di riferimento API 
{: #api-reference}

{{site.data.keyword.slapi_full}} è l'interfaccia di sviluppo che consente agli sviluppatori e agli amministratori di sistema di interagire direttamente con il sistema di backend di {{site.data.keyword.cloud_notm}}. {{site.data.keyword.slapi_short}} potenzia molte delle funzioni disponibili nella console {{site.data.keyword.cloud_notm}}, che in genere significa che se un'interazione è possibile nella console {{site.data.keyword.cloud_notm}}, può essere eseguita anche nella API. Poiché puoi interagire a livello di programmazione con tutte le parti dell'ambiente {{site.data.keyword.cloud_notm}} all'interno della API, {{site.data.keyword.slapi_short}} ti consente di automatizzare le attività. Ad esempio, puoi utilizzare la API *SoftLayer_Virtual_Guest/createObject* per distribuire un'istanza del server virtuale.
{:shortdesc}

{{site.data.keyword.slapi_short}} è un sistema di chiamata di procedura remota. Ogni chiamata implica l'invio di dati verso un endpoint della API e la ricezione dei dati strutturati come ritorno. Il formato utilizzato per inviare e ricevere i dati con {{site.data.keyword.slapi_short}} dipende da quale implementazione API scegli. {{site.data.keyword.slapi_short}} attualmente utilizza SOAP, XML-RPC o REST per la trasmissione dei dati.

Per ulteriori informazioni sull'{{site.data.keyword.slapi_short}} e sulle API del server virtuale, consulta le seguenti risorse in {{site.data.keyword.sldn_full}}:
* [Panoramica di {{site.data.keyword.slapi_short}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/reference/softlayerapi/){: new_window}
* [Introduzione a {{site.data.keyword.slapi_short}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/article/getting-started/){: new_window}
* [Riferimento API: SoftLayer_Virtual_Guest::createObject ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/){: new_window}
* [Riferimento API: SoftLayer_Product_Order::placeOrder ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/){: new_window}

Per gli esempi di utilizzo della API, consulta le seguenti risorse:
* [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/article/understanding-ordering/){: new_window}
* [Client {{site.data.keyword.slapi_short}} Python: gestione dei server virtuali ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [Esempi di {{site.data.keyword.slapi_short}} - Note sulla release ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/){: new_window}
* [Python examples ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/python/){: new_window}

## Esempi di utilizzo dei server virtuali dedicati
* [Get Dedicated Host Allocation ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/python/getDediHostAllocation/){: new_window}
* [Get Dedicated Host Guests ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/python/getDedicatedHostGuests/){: new_window}
* [Migrate a virtual server instance between dedicated hosts ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/python/migrateDedicatedHost.py/){: new_window}

## Esempi di utilizzo dei server virtuali pubblici
* [softlayer_virtual_guest API examples ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
