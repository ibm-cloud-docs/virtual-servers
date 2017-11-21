---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Öffentliche virtuelle Server
Bei den {{site.data.keyword.BluVirtServers}}-Angeboten, die von IBM verwaltet werden, handelt es sich um Multi-Tenant-Bereitstellungen für virtuelle Server. Sie bieten schnelle Skalierbarkeit und mehr Kosteneffizienz durch vordefinierte Größen für alle Geschäftsanforderungen, damit Ihre Systeme schnell einsatzbereit sind. Öffentliche virtuelle Server bieten zahlreiche Vorteile, einschließlich der folgenden:

* **Globale Verfügbarkeit** 

    Das Angebot für öffentliche virtuelle Server ist in Rechenzentrum weltweit verfügbar.

* **Konfigurationsauswahl, schnelle Bereitstellung und Skalierbarkeit** 

    Das Angebot für öffentliche virtuelle Server bietet Ihnen Optionen für begrenzte oder umfangreiche virtuelle Server, die verschiedene Workload-Anforderungen erfüllen können.

**Hinweis:** Wenn Sie an einer Single-Tenant-Umgebung interessiert sind, sollten Sie das Angebot [Dedizierter virtueller Server](../vsi/vsi_dedicated.html) in Betracht ziehen.
{:shortdesc}

Öffentliche Instanzen befinden sich auf einem Hypervisor, der mit anderen Clients gemeinsam genutzt wird. Dabei sind die Prozessoren und der Speicher jedoch dem virtuellen Server zugeordnet (dediziert), um zuverlässige Serverleistung zu erzielen. 

Die folgenden öffentlichen virtuellen Server sind verfügbar. 

| Öffentliche virtuelle Server  | Beschreibung                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Ausgeglichen](../vsi/vsi_public_balanced.html) | Besonders geeignet für gemeinsame Cloud-Workloads, für die eine Balance zwischen Leistung und Skalierbarkeit erforderlich ist. NAS (Network-attached Storage) wird verwendet.|
| [Ausgeglichener lokaler Speicher](../vsi/vsi_public_balanced_local.html) | Besonders geeignet für große Datenbankcluster, für die eine E/A-Leistung mit niedrigen Latenzzeiten erforderlich ist.|
| [Compute](../vsi/vsi_public_compute.html) | Besonders geeignet für mittlere bis große Workloads im Webdatenverkehr.|
| [Speicher](../vsi/vsi_public_memory.html)  | Besonders geeignet für Speichercache- und Echtzeitanalyse-Workloads.
{: caption="Tabelle 1. Unterstützte öffentliche virtuelle Server" caption-side="top"}

## Nächste Schritte

Nach dem Überprüfen und Festlegen der Version (Flavor) Ihres virtuellen Servers müssen Sie nun Ihren öffentlichen virtuellen Server bereitstellen. Lesen Sie zunächst die folgenden Informationen: 
1. [Auswahlen für die Bereitstellung](../vsi/vsi_public_selections.html)
2. [Öffentliche Instanzen bereitstellen](../vsi/vsi_provision_public.html)
