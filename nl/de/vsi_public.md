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
Bei den {{site.data.keyword.BluVirtServers}}-Angeboten, die von IBM verwaltet werden, handelt es sich um Multi-Tenant-Bereitstellungen für virtuelle Server. Sie bieten schnelle Skalierbarkeit und mehr Kosteneffizienz durch vordefinierte Größen für alle Geschäftsanforderungen, damit Ihre Systeme schnell einsatzbereit sind.  
{:shortdesc}

Öffentliche virtuelle Server bieten zahlreiche Vorteile, einschließlich der folgenden:

* **Globale Verfügbarkeit** 

    Das Angebot für öffentliche virtuelle Server ist in Rechenzentrum weltweit verfügbar.

* **Konfigurationsauswahl, schnelle Bereitstellung und Skalierbarkeit** 

    Das Angebot für öffentliche virtuelle Server bietet Ihnen Optionen für begrenzte oder umfangreiche virtuelle Server, die verschiedene Workload-Anforderungen erfüllen können.

Beim Datenaustausch im Netz für öffentliche virtuelle Server, der VSI SAN und anderen netzgebundenen Speicher einschließt, gibt es keine Garantie. Beeinträchtigt der Netzverkehr einer virtuellen Serverinstanz zunehmend die Leistung anderer virtueller Server, wird die betreffende Instanz möglicherweise auf einem neuen Host gestartet oder im Extremfall vollständig inaktiviert. Diese Beeinträchtigung ist oft zu beobachten, wenn der Datenverkehr einen Umfang von 20.000 bis 30.000 Paketen pro Sekunde (PPS) erreicht. Für einen garantierten Netzbetrieb empfiehlt es sich, auf das Angebot für dedizierte virtuelle Server zurückzugreifen. Weitere Informationen finden Sie im Abschnitt zur Single-Tenant-Umgebung, dem [Angebot für dedizierte virtuelle Server](../vsi/vsi_dedicated.html). 

Öffentliche Instanzen befinden sich auf einem Hypervisor, der mit anderen Clients gemeinsam genutzt wird. Dabei sind die Prozessoren und der Speicher jedoch dem virtuellen Server zugeordnet (dediziert), um zuverlässige Serverleistung zu erzielen. 

Die folgenden öffentlichen virtuellen Server sind verfügbar. 

| Öffentliche virtuelle Server  | Beschreibung                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Ausgeglichen](../vsi/vsi_public_balanced.html) | Besonders geeignet für gemeinsame Cloud-Workloads, für die eine Balance zwischen Leistung und Skalierbarkeit erforderlich ist. NAS (Network-attached Storage) wird verwendet.|
| [Ausgeglichener lokaler Speicher](../vsi/vsi_public_balanced_local.html) | Besonders geeignet für große Datenbankcluster, für die eine E/A-Leistung mit niedrigen Latenzzeiten erforderlich ist.|
| [Compute](../vsi/vsi_public_compute.html) | Besonders geeignet für mittlere bis große Workloads im Webdatenverkehr.|
| [Speicher](../vsi/vsi_public_memory.html)  | Besonders geeignet für Speichercache- und Echtzeitanalyse-Workloads.
| [GPU](../vsi/vsi_public_gpu.html)  | Besonders geeignet für Workloads, die eine hohe Leistung erfordern.
{: caption="Tabelle 1. Unterstützte öffentliche virtuelle Server" caption-side="top"}

## Nächste Schritte

Nach dem Überprüfen und Festlegen der Version (Flavor) Ihres virtuellen Servers müssen Sie nun Ihren öffentlichen virtuellen Server bereitstellen. Lesen Sie zunächst die folgenden Informationen: 
1. [Optionen für die Bereitstellung](../vsi/vsi_public_selections.html)
2. [Öffentliche Instanzen bereitstellen](../vsi/vsi_provision_public.html)
