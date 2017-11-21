---



copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Imagevorlagen
Mit den {{site.data.keyword.BluVirtServers}}-Imagevorlagen können Sie ein Image für eine Einheit erfassen und die zugehörige Konfiguration mit minimalen Änderungen im Bestellvorgang replizieren.
{:shortdesc}

Standard-Imagevorlagen stellen eine Option für die Imageerstellung für alle {{site.data.keyword.BluVirtServers_short}} unabhängig vom Betriebssystem bereit. Standard-Imagevorlagen ermöglichen die Imageerfassung für einen vorhandenen virtuellen Server und das Erstellen eines neuen virtuellen Servers basierend auf dem erfassten Image. Standard-Imagevorlage sind nicht kompatibel mit Bare-Metal-Servern.

## Funktionsweise von Imagevorlagen
Die beiden Hauptaktionen für jede Imagevorlage sind das Erstellen und das Bereitstellen. Wenn Sie das Erstellen eines Images anfordern, schaltet das automatisierte System der {{site.data.keyword.BluSoftlayer_full}} Ihren Server offline. Während der Server offline ist, wird eine komprimierte Sicherung Ihrer Daten erstellt, die Konfigurationsdaten werden aufgezeichnet und die Imagevorlage wird im SAN der {{site.data.keyword.BluSoftlayer_notm}} gespeichert. In der Bereitstellungsphase der Imagevorlage erstellt das automatisierte System einen neuen Server mithilfe der aus dem ausgewählten Image gesammelten Daten. Im Bereitstellungsprozess wird das Volumen angepasst, die kopierten Daten werden wiederhergestellt und schließlich werden Konfigurationsänderungen (z. B. Netzkonfigurationen) für den neuen Host vorgenommen.

## Private Images

Private Images sind Images, die von einem Benutzer auf dem Konto erstellt werden oder Images, die auf einem anderen Konto erstellt und gemeinsam genutzt werden. Standardmäßig sind alle Images, die erstellt werden, private Images. 

## Öffentliche Images

Öffentliche Images sind vorkonfigurierte Maschinen, die von {{site.data.keyword.BluSoftlayer_notm}} gepostet oder von Kunden öffentlich gemacht werden und für alle {{site.data.keyword.BluSoftlayer_notm}}-Kunden zur Verfügung stehen. Virtuelle Server, die über öffentliche Imagevorlagen bereitgestellt werden, sind im Allgemeinen mit bestimmten Kombinationen einer Vielfalt von Konfiguriationsspezifikationen für optimale Leistung konfiguriert.

Weitere Informationen zu Imagevorlagen finden Sie unter [Einführung in Imagevorlagen](/docs/infrastructure/image-templates/image_index.html).
