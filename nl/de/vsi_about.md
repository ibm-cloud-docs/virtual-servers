---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-29"

keywords: scalable virtual servers, virtual servers, key features

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Informationen zu virtuellen Servern
{: #about-virtual-servers}

{{site.data.keyword.BluVirtServers}} sind skalierbare virtuelle Server, die mit Cores und Speicherzuordnungen erworben werden. Dieses Angebot ist besonders nützlich, wenn Sie innerhalb von Minuten zusätzliche Computerressourcen benötigen, denn es bietet Zugriff auf Funktionen wie Imagevorlagen. Der Hypervisor wird vollständig von {{site.data.keyword.cloud_notm}} verwaltet und Sie können Konfigurations- und Verwaltungstasks sowohl in der {{site.data.keyword.cloud_notm}}-Konsole als auch über die {{site.data.keyword.slapi_short}} ausführen. Virtuelle Server werden in denselben VLANs bereitgestellt wie physische Server. Dies bedeutet, dass Sie Workloads auf mehrere virtuelle Server und Bare Metal Server-Systeme verteilen können, ohne die Interoperabilität zu beeinträchtigen. Virtuelle Server können bei der Bestellung vollständig angepasst werden und bieten außerdem Skalierungsmöglichkeiten, um Ihre wachsenden Computing-Anforderungen auch in Zukunft zu erfüllen.
{:shortdesc}

Wenn Sie einen virtuellen Server erstellen, können Sie zwischen einer öffentlichen Umgebung (Multi-Tenant-Funktionalität) und einer dedizierten Umgebung (Einzel-Tenant-Funktionalität) wählen. Sie können auch zwischen stündlicher und monatlicher Abrechnung sowie zwischen leistungsstarken lokalen Platten und SAN-Speicher im Unternehmen wählen.

## Schlüsselfunktionen
Nachfolgend sind die Schlüsselfunktionen aufgelistet, die von virtuellen Servern bereitgestellt werden.

### Nahtlose Integration
Virtuelle Server werden im selben Pod und Netz bereitgestellt wie Bare Metal Server und Netz-Appliances. Damit erhalten Sie die nötige Flexibilität, um die optimale Technologie für jede Workload zu verwenden. Häufig werden mehrere virtuelle Server hinter einer Einrichtung für den Lastausgleich bereitgestellt, um den Webdatenverkehr zu verarbeiten. Diese Server können über direkten Zugriff der Ebene 2 auf das private Netz für Bare-Metal-Datenbankserver und für andere anspruchsvolle Workloads verfügen.

### Vollständig anpassbar
Die können jeden virtuellen Server durch eine Reihe von Optionen genau auf Ihren Bedarf abstimmen. Es gibt keine vordefinierten Paketvoraussetzungen, d. h. Sie können jeden Server genau an die zu unterstützende Workload anpassen.

### Schnelle Bereitstellung
Virtuelle Server werden innerhalb von 5 Minuten bereitgestellt. Dies bedeutet für Sie eine sehr geringe Wartezeit zwischen Bestellung und Bereitstellung.

### Fernverwaltung
Wie alle unsere Services bieten auch die virtuellen Server die Möglichkeit der Verwaltung über Fernzugriff. Sie können alle Details Ihrer Einheiten über die {{site.data.keyword.cloud_notm}}-Konsole oder über die {{site.data.keyword.slapi_short}} anzeigen und verwalten. Außerdem können Sie über die bereitgestellten KVM-Funktionen mit dem Server interagieren oder nach dem Anmelden beim Server über die öffentliche oder private Schnittstelle alle Verwaltungsfunktionen steuern.

### Einfache Skalierbarkeit
Nach dem Bereitstellen Ihres virtuellen Servers können Sie Ihre Instanzen schnell und einfach aufwärts oder abwärts skalieren sowie bei Bedarf zusätzliche Instanzen hinzufügen oder entfernen. Nachdem eine Imagevorlage des Servers entsprechend konfiguriert und optimiert wurde, können Sie weitere virtuelle Server erstellen, die auf dieser Vorlage basieren.
