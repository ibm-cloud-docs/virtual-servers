---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-26"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Informationen zur ausgesetzten Abrechnung (Beta)
{: #requirements}

Bei Ausschalten eines virtuellen Servers, der die Funktion für ausgesetzte Abrechnung unterstützt, fallen für bestimmte Rechenressourcen keine Kosten an. Die Abrechnung stoppt bei Ausschalten des Servers automatisch. Die Funktion für ausgesetzte Abrechnung unterstützt Sie bei der Kostenreduzierung und bewirkt, dass Sie einen virtuellen Server nicht erneut bereitstellen müssen, wenn sie seine Ressourcen wieder benötigen. Die ausgesetzte Abrechnung wird nur für neue Bereitstellungen, nicht für vorhandene Instanzen, unterstützt.{:shortdesc}

Damit Sie auf die Funktion für ausgesetzte Abrechnung zugreifen können, müssen Sie die virtuelle Serverinstanz mithilfe der {{site.data.keyword.slapi_short}} bereitstellen, in der sie das Paket für die ausgesetzte Abrechnung angeben. Die neue virtuelle Serverinstanz muss mithilfe der folgenden Einstellungen konfiguriert werden:

* Stündliches SAN
* Eine der folgenden Familien:
  * Ausgewogen (Balanced)
  * Berechnen (Compute)
  * Speicher (Memory)
* Eines der folgenden {{site.data.keyword.cloud}}-Rechenzentren:

| Rechenzentren |         |
| ------------ | ------- | 
|SEO01         |  WDC01  |
|SAO01         |  WDC04  |
|TOK02         |  WDC06  |
|DAL01         |  WDC07  |
|DAL05         |  LON02  |
|DAL06         |  LON04  |
|DAL09         |  LON06  |
|DAL10         |  FRA02  |
|DAL12         |  FRA04  |
|DAL13         |  FRA05  |
{: caption="Tabelle 1. Unterstützte Rechenzentren" caption-side="top"}

Sie können die Funktion für ausgesetzte Abrechnung als eine schnellere Alternative zum Bereitstellen bzw. Aufheben der Bereitstellung von virtuellen Serverinstanzen verwenden.
{:tip}

## Bereitstellung

In der Betaversion müssen Sie für die Bereitstellung einer virtuellen Serverinstanz, die die Funktion für ausgesetzte Abrechnung unterstützt, die {{site.data.keyword.slapi_short}} verwenden. API-Beispiele finden Sie in [Öffentliche Instanz mit dem Objekt 'placeOrder' bereitstellen](../vsi/vsi_provision_api.html#provisioning-a-public-instance-using-place-order-object). 

Sie müssen während des Bereitstellungsprozesses auch die bestimmte ID für das Paket für ausgesetzte Abrechnung angeben. Sie können in der {{site.data.keyword.slapi_short}} mithilfe des Schlüsselnamens (keyName) `SUSPEND_CLOUD_SERVER` eine Abfrage nach der ID des Pakets für ausgesetzte Abrechnung ausführen. Sie finden ein Beispiel für eine Suche nach Serverpaketen in [Bestellung mithilfe der {{site.data.keyword.slapi_short}}-Bestellungs-CLI verstehen und erstellen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Details zur Abrechnung

Es ist wichtig zu verstehen, welche Kosten bei Ausschalten der virtuellen Serverinstanz weiterhin anfallen und welche Kosten nicht mehr anfallen.

| Ressource                     | Abrechnung stoppt | Abrechnung läuft weiter |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          |          X        |                  |
| RAM                           |          X        |                  |
| Portgeschwindigkeit           |          X        |                  |
| Lizenzen des Betriebssystems  |          X        |                  |
| Überwachung von Add-ons       |          X        |                  |
| Sekundäre öffentl. IP-Adressen|                   |         X        |
| Speicher                      |                   |         X        |
{: caption="Tabelle 1. Details zur Abrechnung von Ressourcen" caption-side="top"}   

**Hinweis:** Wenn Sie eine virtuelle Serverinstanz bereitstellen, die die Funktion für ausgesetzte Abrechnung unterstützt, wird die Verwendungsdauer sowohl bei Verwendung als auch bei Aussetzen pro Minute berechnet. Auch wenn Sie die Funktion für ausgesetzte Abrechnung nie durch Ausschalten der Instanz aufrufen, wird die Abrechnungssumme pro Minute des Lebenszyklus der Instanz berechnet. 

### Mindestnutzungsgebühr
Bei virtuellen Serverinstanzen, die die Funktion für ausgesetzte Abrechnung unterstützen, fällt pro Monat eine Mindestnutzungsgebühr an. Nutzungszeiten, die 25 Prozent übersteigen, werden in Rechnung gestellt. Wenn die Nutzung geringer ist als 25 Prozent, werden Ihnen für 25 Prozent der Stunden, während denen die Instanz in Ihrem aktuellen Rechnungsstellungszyklus vorhanden war, Gebühren berechnet. 

### Rechnung
Wenn Sie die Abrechnung auf einem virtuellen Server aussetzen, enthält Ihre Rechnung einige Änderungen. Die entsprechenden Gebühren werden nun als nutzungsabhängige Einzeldaten aufgeführt. Beispielsweise werden folgende Zusatzpunkte aufgeführt, die in Stunden die Zeit der Verfügbarkeit und der Nutzung sowie die Gesamtzahl der in Rechnung gestellten Stunden darstellen:

```
Nutzung der Datenverarbeitungsinstanz...
RAM-Nutzung...
Betriebssystemnutzung...
```
{:screen}

## Ressourcendetails

### Speicher

Wenn Sie die Abrechnung in einer virtuellen Serverinstanz aussetzen, bleibt der zugeordnete Speicher bestehen; Sie können jedoch nicht auf Daten zugreifen, während die virtuelle Serverinstanz ausgeschaltet ist. Wenn Sie die Abrechnung in der Instanz wiederaufnehmen, können Sie auf Ihre Daten zugreifen und es beginnt wieder die normale Abrechnung.

### IP-Adressen

Alle öffentlichen IP-Adressen werden für Sie beibehalten, wenn die Abrechnung für Ihre virtuelle Serverinstanz ausgesetzt ist.

Sie können über die {{site.data.keyword.slapi_short}} oder im {{site.data.keyword.slportal_full}} durch Öffnen der Seite mit den Einheitendetails anzeigen, ob Ihre Einheit gestoppt ist; außerdem können Sie das relevante Datum anzeigen, an dem der Status geändert wurde.

### Einschränkungen

Die Anzahl der unterstützten gleichzeitig ausgeführten Instanzen ist Teil Ihres kontoweiten Einheitenkontingents. Weitere Informationen zu Einschränkungen bei gleichzeitig ausgeführten Instanzen finden Sie unter [FAQs: Virtuelle Server](vsi_faqs_vs.html#concurrent).

## Nächste Schritte
Nach der Bereitstellung eines virtuellen Servers, der die ausgesetzte Abrechnung unterstützt, können Sie in der Einheit mit dem Aussetzen und Wiederaufnehmen der Abrechnung beginnen.
Wenn die Abrechnung in einer virtuellen Serverinstanz ausgesetzt ist, können erst nach dem Wiederaufnehmen der Abrechnung für die Einheit wieder alle Aktionen ausgeführt werden.

Zum Aussetzen der Abrechnung in einer virtuellen Serverinstanz schalten Sie den virtuellen Server aus. Weitere Informationen finden Sie unter [Virtuelle Server verwalten](vsi_managing.html).
