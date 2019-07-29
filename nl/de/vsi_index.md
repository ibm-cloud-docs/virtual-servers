---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-29"

keywords: virtual servers, provisioning process, IBM Cloud Virtual Servers

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Lernprogramm zur Einführung
{: #getting-started-tutorial}

{{site.data.keyword.BluVirtServers}} können in wenigen Minuten bereitgestellt werden. Die virtuellen Server werden
aus den virtuellen Serverimages Ihrer Wahl und in der geografischen Region bereitgestellt, die für Ihre Workloads geeignet ist.
{:shortdesc}

Lernen Sie unsere virtuellen Server in einer virtuellen privaten Cloud kennen! Weitere Informationen finden Sie in [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started).
{:tip}

Wenn Sie einen virtuellen Server in der klassischen Infrastruktur erstellen, können Sie zwischen einer öffentlichen Umgebung (Multi-Tenant-Funktionalität) und einer dedizierten Umgebung (Einzel-Tenant-Funktionalität) wählen. Abhängig von der gewählten Umgebung müssen Sie dann auch auf Stundenbasis abzurechnende, auf Monatsbasis abzurechnende oder transiente virtuelle Server auswählen. Im Falle öffentlicher virtueller Server wählen Sie auch aus, ob SAN-basierter Speicher oder lokaler Speicher verwendet werden soll.

## Vorbereitungen

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie beginnen.

  1. Sie müssen über ein aktualisiertes Konto verfügen, um virtuelle Server zu bestellen. Dieser Prozess kann einige Zeit
dauern und Ihre Anfrage muss genehmigt werden, damit Sie fortfahren können. Weitere Informationen zum Aktualisieren Ihres Kontos finden Sie unter [Zur IBMid wechseln](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
  2. Überprüfen Sie Ihre Bereitstellungsoptionen und treffen Sie die gewünschte Auswahl. Weitere Informationen finden
Sie in den folgenden Abschnitten:

|              Bereitstellungsoptionen                           |  Beschreibung                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Öffentlicher virtueller Server](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)            | Von IBM verwaltete Multi-Tenant-Bereitstellungen für virtuelle Server|
|[Transienter virtueller Server](/docs/vsi?topic=virtual-servers-about-vs-transient)| Von IBM verwaltete Multi-Tenant-Bereitstellungen für virtuelle Server, angeboten zu reduzierten Kosten und am besten geeignet für flexible Workloads |
|[Reservierter virtueller Server](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers)  | Von IBM verwaltete Multi-Tenant-Bereitstellungen für virtuelle Server mit garantierter Kapazität über einen vereinbarten Zeitraum |
|[Dedizierter virtueller Server](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers)      | Von IBM verwaltete Einzel-Tenant-Bereitstellungen für virtuelle Server            |
{: caption="Tabelle 1. Bereitstellungsoptionen" caption-side="top"}   

## Virtuellen Server bereitstellen

Nachdem Sie sich für eine Bereitstellungsoption entschieden haben, können Sie mit dem Bereitstellungsprozess beginnen.

|              Bereitstellungsanweisungen                                        |  Beschreibung                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Öffentliche Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-public)                | Öffentliche Instanzen mit verschiedenen Optionen bereitstellen             |
|[Transiente Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-transient)                | Transiente Instanzen mit verschiedenen Optionen bereitstellen            |
|[Reservierte Kapazität und Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances)            | Reservierte Kapazität und Instanzen mit verschiedenen Optionen bereitstellen |
|[Dedizierte Hosts und Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)| Private Instanzen oder dedizierte Instanzen auf dedizierten Hosts bereitstellen|
{: caption="Tabelle 2. Informationen zur Bereitstellung" caption-side="top"}

## Nächste Schritte

Nachdem Ihr virtueller Server bereitgestellt wurde und einsatzbereit ist, können Sie Ihre virtuellen Server über die
{{site.data.keyword.cloud_notm}}-Konsole oder über die {{site.data.keyword.slapi_short}} konfigurieren. Weitere Informationen finden Sie unter [Virtuelle Server konfigurieren](/docs/vsi?topic=virtual-servers-configuring-virtual-servers).
