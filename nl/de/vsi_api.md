---

copyright:
  years: 2017
lastupdated: "2017-10-25"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# API-Referenz
{: #api-reference}

Die {{site.data.keyword.slapi_full}} ist die Entwicklungsschnittstelle, die Entwicklern und Systemadministratoren die direkte Interaktion mit dem Back-End-System von {{site.data.keyword.cloud}} ermöglicht. Die {{site.data.keyword.slapi_short}} ermöglicht viele der Funktionen im {{site.data.keyword.slportal_full}}, d. h. jede Interaktion, die im {{site.data.keyword.slportal}} möglich ist, kann in der Regel auch in der API ausgeführt werden. Da Sie innerhalb der API programmgesteuert mit allen Teilen der {{site.data.keyword.BluSoftlayer_full}}-Umgebung interagieren können, eröffnet {{site.data.keyword.slapi_short}} Ihnen die Möglichkeit zum Automatisieren von Tasks. Sie können zum Beispiel die API *SoftLayer_Virtual_Guest/createObject* verwenden, um eine virtuelle Instanz bereitzustellen.
{:shortdesc}

Die {{site.data.keyword.slapi_short}} ist ein System für ferne Prozeduraufrufe (Remote Procedure Calls). Bei jedem Aufruf werden Daten an einen API-Endpunkt gesendet und strukturierte Daten als Antwort zurückgegeben. Das Format zum Senden und Empfangen von Daten in der {{site.data.keyword.slapi_short}} hängt von der API-Implementierung ab, die Sie auswählen. Die {{site.data.keyword.slapi_short}} unterstützt derzeit SOAP, XML-RPC oder REST für die Datenübertragung.

Weitere Informationen zur {{site.data.keyword.slapi_short}} und zu APIs für virtuelle Server finden Sie in den folgenden Ressourcen von {{site.data.keyword.sldn_full}}:
* [{{site.data.keyword.slapi_short}} - Übersicht ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/reference/softlayerapi/){: new_window}
* [Einführung in die {{site.data.keyword.slapi_short}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/article/getting-started/){: new_window}
* [API-Referenz: SoftLayer_Virtual_Guest::createObject ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/){: new_window}
* [API-Referenz: SoftLayer_Product_Order::placeOrder ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/){: new_window}

API-Verwendungsbeispiele finden Sie in den folgenden Ressourcen:
* [Bestellung mithilfe der {{site.data.keyword.slapi_short}}-Bestellungs-CLI verstehen und erstellen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/article/understanding-ordering/){: new_window}
* [{{site.data.keyword.slapi_short}} - Python-Client: Mit virtuellen Servern arbeiten ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [{{site.data.keyword.slapi_short}}-Beispiele - Releaseinformationen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/){: new_window}
* [Python-Beispiele ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/python/){: new_window}

## Verwendungsbeispiele für dedizierte virtuelle Server
* [Zuordnung für dedizierten Host abrufen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/python/getDediHostAllocation/){: new_window}
* [Gastmaschinen für dedizierten Host abrufen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/python/getDedicatedHostGuests/){: new_window}
* [Virtuelle Serverinstanz zwischen dedizierten Hosts migrieren ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/python/migrateDedicatedHost.py/){: new_window}

## Verwendungsbeispiele für öffentliche virtuelle Server
* [API-Beispiele für softlayer_virtual_guest ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
