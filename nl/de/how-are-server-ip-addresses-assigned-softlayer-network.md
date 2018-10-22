---

copyright:
  years: 2018
lastupdated: "2018-08-01"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Server-IP-Adressen zuweisen
{: #assigning-server-ip-addresses}

In {{site.data.keyword.cloud}} werden virtuelle Serverinstanzen mit einer IPv4-Adresse im privaten Netz konfiguriert, soweit angefordert, auch mit einer öffentlichen (mit dem Internet verbundenen) IPv4-Adresse. Darüber hinaus können Sie eine IPv6-Adresse im öffentlichen Netz anfordern. Diese IP-Adressen werden als _primäre IP-Adressen_ bezeichnet.
{:shortdesc}

Zusätzliche IP-Adressen können nach dem Erwerb sekundärer Teilnetze über das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com) an virtuelle Serverinstanzen gebunden werden. Auf diese Weise erworbene und von Ihnen verwaltete IP-Adressen werden als _sekundäre IP-Adressen_ bezeichnet.

Weitere Informationen zu den für den Bezug von IP-Adressen verfügbaren Optionen finden Sie im Abschnitt [Teilnetze und IP-Adressen](https://console.bluemix.net/docs/infrastructure/subnets/).

## Sekundäre IP-Adressen binden

Nach dem Erwerb eines sekundären Teilnetzes und der Einrichtung der Weiterleitung müssen Sie das Betriebssystem konfigurieren, damit neu erworbene IP-Adressen verwendet werden können. De Konfigurationsschritte für die neuen IP-Adressen variieren bei den einzelnen Betriebssystemen. Auf die erforderliche Konfiguration wird jedoch im Allgemeinen als Einrichtung eines 'Schnittstellenalias' verwiesen. Weitere Konfigurationsdetails finden Sie in der Dokumentation zu Ihrem Betriebssystem.
