---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

keywords: public virtual servers, network traffic, virtual server deployment

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Öffentliche virtuelle Server
{: #about-public-virtual-servers}

Bei den {{site.data.keyword.BluVirtServers}}-Angeboten, die von IBM verwaltet werden, handelt es sich um Multi-Tenant-Bereitstellungen für virtuelle Server. Sie bieten schnelle Skalierbarkeit und mehr Kosteneffizienz durch vordefinierte Größen für alle Geschäftsanforderungen, damit Ihre Systeme schnell einsatzbereit sind.
{:shortdesc}

Öffentliche virtuelle Server bieten zahlreiche Vorteile, einschließlich der folgenden:

* **Globale Verfügbarkeit** 

    Das Angebot für öffentliche virtuelle Server ist in Rechenzentrum weltweit verfügbar.

* **Konfigurationsauswahl, schnelle Bereitstellung und Skalierbarkeit** 

    Das Angebot für öffentliche virtuelle Server bietet Ihnen Optionen für begrenzte oder umfangreiche virtuelle Server, die verschiedene Workload-Anforderungen erfüllen können.

Beim Datenaustausch im Netz für öffentliche virtuelle Server, der VSI SAN und anderen netzgebundenen Speicher einschließt, gibt es keine Garantie. Beeinträchtigt der Netzverkehr einer virtuellen Serverinstanz zunehmend die Leistung anderer virtueller Server, wird die betreffende Instanz möglicherweise auf einem neuen Host gestartet oder im Extremfall vollständig inaktiviert. Diese Beeinträchtigung ist oft zu beobachten, wenn der Datenverkehr einen Umfang von 20.000 bis 30.000 Paketen pro Sekunde (PPS) erreicht.  Für einen garantierten Netzbetrieb empfiehlt es sich, auf das Angebot für dedizierte virtuelle Server zurückzugreifen. Weitere Informationen finden Sie im Abschnitt zur Single-Tenant-Umgebung, dem [Angebot für dedizierte virtuelle Server](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers).

Für dieses Angebot sind die folgenden Familien von öffentlichen Instanzen verfügbar. 

| Familien  | Beschreibung                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Ausgeglichen](/docs/vsi?topic=virtual-servers-balanced#balanced) | Besonders geeignet für gemeinsame Cloud-Workloads, für die eine Balance zwischen Leistung und Skalierbarkeit erforderlich ist. NAS (Network-attached Storage) wird verwendet. |
| [Ausgeglichener lokaler Speicher](/docs/vsi?topic=virtual-servers-balanced-local-storage#balanced-local-storage) | Am besten geeignet für umfangreiche Datenbankworkloads mit hohen Anforderungen in Bezug auf die E/A-Leistung und sehr geringen Latenzzeiten. |
| [Compute](/docs/vsi?topic=virtual-servers-compute#compute) | Besonders geeignet für mittlere bis große Workloads im Webdatenverkehr.|
| [Speicher](/docs/vsi?topic=virtual-servers-memory#memory)  | Besonders geeignet für Speichercache- und Echtzeitanalyse-Workloads. |
| [GPU](/docs/vsi?topic=virtual-servers-gpu#gpu)  | Besonders geeignet für Workloads, die eine hohe Leistung erfordern.
{: caption="Tabelle 1. Optionen für Produktfamilie öffentlicher virtueller Server" caption-side="top"}

Einige dieser Produktfamilien sind auch für IBM Cloud Virtual Servers for VPC verfügbar. Weitere Informationen finden Sie in [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started).
{:tip}

## Nächste Schritte

Nach dem Überprüfen und Festlegen des Profils Ihres virtuellen Servers müssen Sie nun Ihren öffentlichen virtuellen Server bereitstellen. Informationen zur Vorgehensweise finden Sie in [Öffentliche Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public).
