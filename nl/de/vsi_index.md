---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Einführung in virtuelle Server
{{site.data.keyword.BluVirtServers}} können in wenigen Minuten bereitgestellt werden. Die virtuellen Server werden
aus den virtuellen Serverimages Ihrer Wahl und in der geografischen Region bereitgestellt, die für Ihre Workloads geeignet ist.
{:shortdesc}

Wenn Sie einen virtuellen Server erstellen, können Sie zwischen einer öffentlichen Umgebung (Multi-Tenant-Funktionalität) und einer dedizierten Umgebung (Einzel-Tenant-Funktionalität) wählen. Abhängig von der gewählten Umgebung müssen Sie dann auch auf Stundenbasis abzurechnende, auf Monatsbasis abzurechnende oder transiente virtuelle Server auswählen. Im Falle öffentlicher virtueller Server wählen Sie auch aus, ob SAN-basierter Speicher oder lokaler Speicher verwendet werden soll.

## Vorbereitungen

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie beginnen.

  1. Sie müssen über ein aktualisiertes Konto verfügen, um virtuelle Server zu bestellen. Dieser Prozess kann einige Zeit
dauern und Ihre Anfrage muss genehmigt werden, damit Sie fortfahren können. Weitere Informationen zum Aktualisieren Ihres Kontos finden Sie unter [Zur IBMid wechseln](https://console.bluemix.net/docs/admin/softlayerlink.html).
  2. Überprüfen Sie Ihre Bereitstellungsoptionen und treffen Sie die gewünschte Auswahl. Weitere Informationen finden
Sie in den folgenden Abschnitten:

|              Bereitstellungsoptionen                           |  Beschreibung                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Öffentlicher virtueller Server](../vsi/vsi_public.html)            | Von IBM verwaltete Multi-Tenant-Bereitstellungen für virtuelle Server|
|[Transienter virtueller Server](../vsi/vsi_about_transient.html)| Von IBM verwaltete Multi-Tenant-Bereitstellungen für virtuelle Server, angeboten zu reduzierten Kosten und am besten geeignet für flexible Workloads |
|[Dedizierter virtueller Server](../vsi/vsi_dedicated.html)      | Von IBM verwaltete Einzel-Tenant-Bereitstellungen für virtuelle Server            |
{: caption="Tabelle 1. Bereitstellungsoptionen" caption-side="top"}   

## Virtuellen Server bereitstellen

Nachdem Sie sich für eine Bereitstellungsoption entschieden haben, können Sie mit dem Bereitstellungsprozess beginnen.

|              Bereitstellungsanleitung                                         |  Beschreibung                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Öffentliche Instanzen bereitstellen](../vsi/vsi_provision_public.html)                | Öffentliche Instanzen mit verschiedenen Optionen bereitstellen             |
|[Transiente Instanzen bereitstellen](../vsi/vsi_provision_transient.html)                | Transiente Instanzen mit verschiedenen Optionen bereitstellen            |
|[Dedizierte Hosts und Instanzen bereitstellen](../vsi/vsi_provision_dedicated.html)| Private Instanzen oder dedizierte Instanzen auf dedizierten Hosts bereitstellen|
{: caption="Tabelle 2. Informationen zur Bereitstellung" caption-side="top"}

## Nächste Schritte

Nachdem Ihr virtueller Server bereitgestellt wurde und verfügbar ist, können Sie Ihre virtuellen Server über das
{{site.data.keyword.slportal_full}} oder über die {{site.data.keyword.slapi_full}} konfigurieren. Weitere Informationen finden Sie unter [Virtuelle Server konfigurieren](../vsi/vsi_configuring.html).
