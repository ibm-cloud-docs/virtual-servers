---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Imagevorlagen
{: #image-templates}

Mit den {{site.data.keyword.BluVirtServers}}-Imagevorlagen können Sie ein Image für eine Einheit erfassen und die zugehörige Konfiguration mit minimalen Änderungen im Bestellvorgang replizieren.
{:shortdesc}

Imagevorlagen stellen eine Option für die Imageerstellung für alle {{site.data.keyword.BluVirtServers_short}} unabhängig vom Betriebssystem bereit. Imagevorlagen ermöglichen die Imageerfassung für einen vorhandenen virtuellen Server und das Erstellen eines neuen virtuellen Servers basierend auf dem erfassten Image. Imagevorlagen sind nicht kompatibel mit Bare Metal Server-Systemen.

## Funktionsweise von Imagevorlagen
Die beiden Hauptaktionen für jede Imagevorlage sind das Erstellen und das Bereitstellen. Wenn Sie das Erstellen eines Images anfordern, schaltet das automatisierte System der {{site.data.keyword.BluSoftlayer_full}} Ihren Server offline. Während der Server offline ist, wird eine komprimierte Sicherung Ihrer Daten erstellt, die Konfigurationsdaten werden aufgezeichnet und die Imagevorlage wird im SAN der {{site.data.keyword.BluSoftlayer_notm}} gespeichert. In der Bereitstellungsphase der Imagevorlage erstellt das automatisierte System einen neuen Server mithilfe der aus dem ausgewählten Image gesammelten Daten. Im Bereitstellungsprozess wird das Volumen angepasst, die kopierten Daten werden wiederhergestellt und schließlich werden Konfigurationsänderungen (z. B. Netzkonfigurationen) für den neuen Host vorgenommen.

Weitere Informationen zu Imagevorlagen finden Sie unter [Einführung in Imagevorlagen](/docs/infrastructure/image-templates?topic=image-templates-getting-started-with-image-templates).
