---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-25"

keywords: virtual server, suspend billing feature, virtual server instances, suspend billing

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:table: .aria-labeledby="caption"}

# Informationen zur ausgesetzten Abrechnung
{: #requirements}

Bei Ausschalten eines virtuellen Servers, der das Feature für das Aussetzen der Abrechnung unterstützt, fallen für bestimmte Rechenressourcen keine Kosten an. Die Abrechnung stoppt bei Ausschalten des Servers automatisch. Die Funktion für ausgesetzte Abrechnung unterstützt Sie bei der Kostenreduzierung und bewirkt, dass Sie einen virtuellen Server nicht erneut bereitstellen müssen, wenn sie seine Ressourcen wieder benötigen.
{:shortdesc}

Die meisten virtuellen Serverinstanzen, die vor dem 01. November 2018 erstellt wurden, unterstützten das Feature für das Aussetzen der Abrechnung nicht. Informationen darüber, ob die virtuelle Serverinstanz das Feature für das Aussetzen der Abrechnung unterstützt, finden Sie in [Feature für das Aussetzen der Abrechnung anzeigen](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature).

Dieses Feature ist in Rechenzentren auf der ganzen Welt verfügbar. Wenn Sie eine virtuelle Serverinstanz bereitstellen möchten, die das Feature für das Aussetzen der Abrechnung unterstützt, muss die virtuelle Serverinstanz mit den folgenden Einstellungen konfiguriert werden:

* Stündliches SAN
* Öffentliche Profile einer der folgenden Familien:
  * Ausgewogen (Balanced)
  * Berechnung (Compute)
  * Speicher (Memory)

Sie können das Feature für das Aussetzen der Abrechnung als eine schnellere Alternative zum Bereitstellen und Freigeben von virtuellen Serverinstanzen verwenden.
{:tip}

Die Abrechnung wird nur ausgesetzt, wenn Sie die virtuelle Serverinstanz über das {{site.data.keyword.slportal_full}}, die CLI oder die {{site.data.keyword.slapi_short}} ausschalten. Wenn Sie die virtuelle Serverinstanz direkt über das Betriebssystem ausschalten, wird die Abrechnung für die betreffende Instanz nicht ausgesetzt.
{:note}

## Bereitstellungsdetails

Sie können eine virtuelle Serverinstanz, die das Feature für das Aussetzen der Abrechnung unterstützt, über den {{site.data.keyword.cloud_notm}}-Katalog (cloud.ibm.com), die Befehlszeilenschnittstelle (CLI) oder die {{site.data.keyword.slapi_short}} bereitstellen. Eine virtuelle Serverinstanz, die das Feature für das Aussetzen der Abrechnung unterstützt, kann nicht über das {{site.data.keyword.slportal}} (control.softlayer.com) bereitgestellt werden. Weitere Informationen zum Bereitstellen von öffentlichen virtuellen Serverinstanzen finden Sie in [Öffentliche Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public).

Zum Bestellen virtueller Server über den {{site.data.keyword.cloud_notm}}-Katalog benötigen Sie ein Konto, für das ein Upgrade durchgeführt wurde. Weitere Informationen zum Aktualisieren Ihres Kontos finden Sie unter [Zur IBMid wechseln](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

### Bereitstellung über die SoftLayer-API
Sie können eine virtuelle Serverinstanz, die das Feature für das Aussetzen der Abrechnung unterstützt, über die {{site.data.keyword.slapi_short}} bereitstellen. API-Beispiele finden Sie in [Öffentliche Instanz mit dem Objekt 'placeOrder' bereitstellen](/docs/vsi?topic=virtual-servers-api-rest-public#provisioning-a-public-instance-using-place-order-object).

Sie müssen während des Bereitstellungsprozesses die spezifische Paket-ID für ausgesetzte Abrechnung angeben. Sie können in der {{site.data.keyword.slapi_short}} mithilfe des Schlüsselnamens (keyName) `SUSPEND_CLOUD_SERVER` eine Abfrage nach der ID des Pakets für ausgesetzte Abrechnung ausführen. Sie finden ein Beispiel für eine Suche nach Serverpaketen in [Bestellung mithilfe der {{site.data.keyword.slapi_short}}-Bestellungs-CLI verstehen und erstellen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Details zur Abrechnung

Es ist wichtig zu verstehen, welche Kosten bei Ausschalten der virtuellen Serverinstanz weiterhin anfallen und welche Kosten nicht mehr anfallen.

| Ressource                      | Abrechnung stoppt   | Abrechnung läuft weiter |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          |          X        |                  |
| RAM                           |          X        |                  |
| Portgeschwindigkeit                    |          X        |                  |
| Lizenzen des Betriebssystems     |          X        |                  |
| Überwachung von Add-ons          |          X        |                  |
| Sekundäre öffentl. IP-Adressen |                   |         X        |
| Speicher                       |                   |         X        |
{: caption="Tabelle 1. Details zur Abrechnung von Ressourcen" caption-side="top"}   

Wenn Sie eine virtuelle Serverinstanz bereitstellen, die das Feature für das Aussetzen der Abrechnung unterstützt, wird die Verwendungsdauer sowohl bei Verwendung als auch bei Aussetzen pro Minute berechnet. Auch wenn Sie das Feature für das Aussetzen der Abrechnung nie durch Ausschalten der Instanz aufrufen, wird die Abrechnungssumme pro Minute des Lebenszyklus der Instanz berechnet.
{:note}

### Mindestnutzungsgebühr
Bei virtuellen Serverinstanzen, die das Feature für das Aussetzen der Abrechnung unterstützen, kann in einigen Fällen eine Mindestnutzungsgebühr anfallen. Nutzungszeiten, die 25 Prozent übersteigen, werden in Rechnung gestellt. Wenn die Nutzung geringer ist als 25 Prozent, werden Ihnen für 25 Prozent der Stunden, während denen die Instanz in Ihrem aktuellen Rechnungsstellungszyklus vorhanden war, Gebühren berechnet.

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

Wenn für eine virtuelle Serverinstanz die Abrechnung ausgesetzt wird, bleibt die Abrechnung für den zugehörigen Speicher bestehen, es besteht jedoch kein Zugriff auf die gespeicherten Daten, während die virtuelle Serverinstanz ausgeschaltet ist. Wenn Sie die Abrechnung für die Instanz wiederaufnehmen, können Sie wieder auf Ihre Daten zugreifen.

### IP-Adressen

Alle öffentlichen IP-Adressen werden für Sie beibehalten, wenn die Abrechnung für Ihre virtuelle Serverinstanz ausgesetzt ist.

### Einschränkungen

Virtuelle Serverinstanzen, für die die Abrechnung ausgesetzt ist, zählen weiterhin zum Einheitenkontingent des Kontos. Weitere Informationen zu Einschränkungen bei Instanzen finden Sie in [FAQs: Virtuelle Server](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#concurrent).

## Nächste Schritte
Nach der Bereitstellung eines virtuellen Servers, der die ausgesetzte Abrechnung unterstützt, können Sie in der Einheit mit dem Aussetzen und Wiederaufnehmen der Abrechnung beginnen.

Wenn die Abrechnung für eine virtuelle Serverinstanz ausgesetzt ist, können erst nach dem Wiederaufnehmen der Abrechnung für die Einheit wieder alle Aktionen ausgeführt werden. Sie können über die {{site.data.keyword.slapi_short}} oder im {{site.data.keyword.slportal}} durch Öffnen der Seite mit den Einheitendetails anzeigen, ob Ihre Einheit gestoppt ist; außerdem können Sie das relevante Datum anzeigen, an dem der Status geändert wurde.

Zum Aussetzen der Abrechnung in einer virtuellen Serverinstanz schalten Sie den virtuellen Server aus. Weitere Informationen finden Sie unter [Virtuelle Server verwalten](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
