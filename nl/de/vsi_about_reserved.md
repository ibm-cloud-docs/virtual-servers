---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-25"

keywords: reserved virtual servers, cost savings, guaranteed capacity 
subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Reservierte virtuelle Server
{: #about-reserved-virtual-servers}

Das {{site.data.keyword.BluVirtServers}}-Angebot für reservierte Instanzen ist eine hervorragende Option für alle, die nach garantierten Ressourcen für spätere Bereitstellungen sowie zum Einsparen von Kosten suchen. Sie können eine 1- oder 3-jährige Laufzeit für die reservierte Kapazität wählen. Im Rahmen dieser reservierten Kapazität können Sie eine Gruppe von bis zu 20 virtuellen Serverinstanzen einer bestimmten Größe wählen und diese Instanzen bereitstellen, sobald sie benötigt werden. Diese Kapazität wird Ihnen über die Laufzeit Ihres Vertrags im POD und Rechenzentrum Ihrer Wahl garantiert.

Reservierte virtuelle Serverinstanzen bieten viele Vorzüge, z. B.:

* **Garantierte Kapazität**

    Wenn Sie Kapazität reservieren, wird Ihnen diese Kapazität für die Laufzeit Ihres Vertrags garantiert. 
    
* **Globale Verfügbarkeit**
    
    Das Angebot für reservierte virtuelle Server ist in Rechenzentren auf der ganzen Welt verfügbar.

* **Zuverlässige Bereitstellung**
   
   Innerhalb der reservierten Kapazitäten können Sie virtuelle Serverinstanzen nach Bedarf bereitstellen und freigeben.

* **Kosteneinsparungen**
    
    Die Auswahl einer 1- oder 3-jährigen Vertragslaufzeit ermöglicht konstante monatliche Zahlungen und Kosteneinsparungen gegenüber Rechnungsstellungszyklen für virtuelle Server auf Stunden- oder Monatsbasis.

Reservierte virtuelle Serverinstanzen sind öffentliche Instanzen, die SAN-gestützten Speicher verwenden. Für dieses Angebot sind die folgenden Familien von öffentlichen Instanzen verfügbar.

| Familien  | Beschreibung                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Ausgeglichen](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Besonders geeignet für gemeinsame Cloud-Workloads, für die eine Balance zwischen Leistung und Skalierbarkeit erforderlich ist. NAS (Network-attached Storage) wird verwendet.|
| [Compute](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Besonders geeignet für mittlere bis große Workloads im Webdatenverkehr.|
| [Speicher](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Besonders geeignet für Speichercache- und Echtzeitanalyse-Workloads. |
{: caption="Tabelle 1. Optionen für Produktfamilie öffentlicher virtueller Server" caption-side="top"}

## Einschränkungen 

Vor dem Reservieren von Kapazität und Bereitstellen virtueller Serverinstanzen sind die folgenden Einschränkungen zu beachten:
  
  * Ein Upgrade oder Downgrade für Ihre Instanzen ist nicht möglich.
  * Reservierte Kapazität kann nicht storniert werden. Sie können jedoch virtuelle Serverinstanzen im Rahmen der betreffenden Kapazität freigeben.
    
## Benachrichtigungen

Einen Monat vor Ablauf des Vertrags über die reservierte virtuelle Serverkapazität erhalten Sie eine entsprechende E-Mail-Benachrichtigung.

## Nächste Schritte

Nach Abwägung der verfügbaren Optionen und einer entsprechenden Entscheidung können Sie nun mit der Bereitstellung der reservierten Kapazität und Instanzen fortfahren. Lesen Sie zunächst die folgenden Informationen:

   1. [Reservierte Kapazität und Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)
   2. [Häufig gestellte Fragen (FAQs): Reservierte Kapazität und Instanzen](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances)
