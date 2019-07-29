---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# Virtuelle Serverinstanz über Drittanbieterimage bereitstellen
{: #ordering-3P}

Sie können eine virtuelle Serverinstanz über ein Image bereitstellen, das von einem Drittanbieter erstellt wurde. Drittanbieterimages stehen über den Link für Cloud-Images im {{site.data.keyword.cloud}}-Katalog zur Verfügung.
{:shortdesc}

## Vorbereitungen
Bevor Sie beginnen, müssen Sie sicherstellen, dass die Berechtigungsnachweise für Ihren {{site.data.keyword.cloud_notm}}-Katalog eingerichtet wurden.

Zum Bestellen virtueller Server über den {{site.data.keyword.Bluemix_notm}}-Katalog benötigen Sie ein Konto, für das ein Upgrade durchgeführt wurde. Weitere Informationen zum Aktualisieren Ihres Kontos finden Sie unter [Zur IBMid wechseln](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

## Image für virtuellen Server auswählen
1. Melden Sie sich beim [{{site.data.keyword.cloud_notm}}-Katalog ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/catalog/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an.
2. Suchen Sie im Abschnitt **Cloud-Images** das Drittanbieterimage, das Sie bereitstellen möchten, und klicken Sie darauf.
3. Überprüfen Sie die Details des angepassten Images und klicken Sie dann auf **Weiter**. Daraufhin wird die Seite **Virtuelle Serverinstanz - Angepasstes Image** angezeigt, in der Ihr angepasstes Image vorausgewählt ist.

## Bereitstellungsoptionen überprüfen und auswählen
Weitere Informationen finden
Sie in den folgenden Abschnitten:

|              Bereitstellungsoptionen                           |  Beschreibung                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Öffentlicher virtueller Server](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)            | Von IBM verwaltete Multi-Tenant-Bereitstellungen für virtuelle Server|
|[Transienter virtueller Server](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)| Von IBM verwaltete Multi-Tenant-Bereitstellungen für virtuelle Server, angeboten zu reduzierten Kosten und am besten geeignet für flexible Workloads |
|[Reservierter virtueller Server](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | Von IBM verwaltete Multi-Tenant-Bereitstellungen für virtuelle Server mit garantierter Kapazität über einen vereinbarten Zeitraum |
|[Dedizierter virtueller Server](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)      | Von IBM verwaltete Einzel-Tenant-Bereitstellungen für virtuelle Server            |
{: caption="Tabelle 1. Bereitstellungsoptionen" caption-side="top"}

## Virtuellen Server bereitstellen
Nachdem Sie sich für eine Bereitstellungsoption entschieden haben, können Sie mit dem Bereitstellungsprozess beginnen. Weitere Informationen hierzu finden Sie in den folgenden Abschnitten.

Da Sie den Bereitstellungsprozess mit einem angepassten Image gestartet haben, kann der Imagetyp während des Bereitstellungsprozesses nicht geändert werden.
{:note}

|              Bereitstellungsanweisungen                                        |  Beschreibung                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Öffentliche Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                | Öffentliche Instanzen mit verschiedenen Optionen bereitstellen             |
|[Transiente Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                | Transiente Instanzen mit verschiedenen Optionen bereitstellen            |
|[Reservierte Kapazität und Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | Reservierte Kapazität und Instanzen mit verschiedenen Optionen bereitstellen |
|[Dedizierte Hosts und Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)| Private Instanzen oder dedizierte Instanzen auf dedizierten Hosts bereitstellen|
{: caption="Tabelle 2. Informationen zur Bereitstellung" caption-side="top"}


## Nächste Schritte
Nachdem Ihr virtueller Server bereitgestellt wurde und einsatzbereit ist, können Sie Ihre virtuellen Server über die
{{site.data.keyword.cloud_notm}}-Konsole oder über die {{site.data.keyword.slapi_short}} konfigurieren. Weitere Informationen finden Sie unter [Virtuelle Server konfigurieren](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
