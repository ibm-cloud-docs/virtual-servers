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

# Auswahlen für die Bereitstellung
Beim Bereitstellen eines öffentlichen virtuellen Servers müssen Sie die folgenden Auswahlen treffen.

## Standort
Sie können auswählen, in welchem Rechenzentrum die Bereitstellung erfolgen soll. Bei neuen Bereitstellungen ermittelt {{site.data.keyword.Bluemix}} automatisch den am besten geeigneten POD (basierend auf der Verfügbarkeit) und erstellt die entsprechenden öffentlichen und privaten VLANs. Bei Ergänzungen für vorhandene Umgebungen können Sie POD, VLAN und Teilnetz auswählen, die für Ihre Zwecke geeignet sind.

## Prozessoren / RAM
Beim Bestellen können Sie zwischen den angebotenen Optionen für Kernprozessoren auswählen. Dabei sind Standards für virtuelle Serverbereitstellungen zu beachten. Jeder physische Kern im Server wird per Hyper-Threading verbunden und als zwei virtuelle CPUs (vCPUs) oder Kerne dargestellt. Das Angebot für virtuelle Server bietet 2,0 GHz oder mehr pro Kern sowie bis zu 56 verfügbare Kerne auf einem einzelnen virtuellen Server.

Die Zuordnung des Arbeitsspeichers (RAM) ist sehr leicht nachvollziehbar. Die von Ihnen ausgewählte RAM-Kapazität wird Ihrem virtuellen Server in vollem Umfang dediziert zur Verfügung gestellt (bis zu 242 GB für einen einzelnen virtuellen Server).

**Hinweis:** Für öffentliche und dedizierte Instanzen gelten geringfügig abweichende Konfigurationsgrenzwerte. Sehr hohe Zuordnungen für Kerne oder Arbeitsspeicher schränken die verfügbaren Optionen ein.

## Betriebssystem

Sie können auch auswählen, welches Betriebssystem auf dem Server bereitgestellt werden soll. Dabei stehen einige kostenlose Optionen wie CentOS und Ubuntu zur Verfügung. Zahlungspflichtige Optionen wie Windows Server und Red Hat Enterprise Linux (RHEL) sind ebenfalls verfügbar. Wichtig: Beachten Sie, dass für Windows ein primärer Datenträger mit 100 MB erforderlich ist.

Für Bestandskunden ist außerdem die Bereitstellung über eine Imagevorlage im {{site.data.keyword.slportal_full}} möglich (navigieren Sie zu **Einheiten -> Verwalten -> Images** und wählen Sie **Virtuellen Server bestellen** im Menü *Aktionen* aus. Daraufhin wird automatisch das entsprechende Betriebssystem für die Bestellung ausgewählt. Alternativ können Sie basierend auf einem Standardimage bestellen und danach jederzeit eine Imagevorlage erneut laden.

## Speicher

Sie können für jeden virtuellen Server zwischen den Optionen 'SAN' und 'Lokal' wählen. Der SAN-Speicher bzw. der lokale Speicher kann nach Bedarf durch weitere Produkte ergänzt werden. SAN-Speicher und lokaler Speicher sind für den virtuellen Server als lokale Datenträger zugänglich. Nach allen Änderungen der Datenträger (z. B. anhängen, abhängen, migrieren usw.) muss der virtuelle Server neu gestartet werden. Weitere Informationen finden Sie unter [Speicheroptionen](../vsi/storage/vsi_about_storage.html).

## Stündliche und monatliche Abrechnung

Für einen virtuellen Server können Sie die Abrechnung auf Stundenbasis oder auf Monatsbasiss auswählen. Der Hauptunterschied (abgesehen von den Gebühren) besteht darin, dass stündlich abgerechnete Server keine Bandbreitenzuordnung beinhalten. Am Ende des Abrechnungszeitraums werden die genutzte Bandbreite und die Anzahl der Stunden, in denen jeder Server für das Konto aktiv war, berechnet. Eine laufende Summe wird im {{site.data.keyword.slportal}} auf der Seite mit der Ansicht für virtuelle Server zusammen mit einem Link zu einer Detailseite mit den einzelnen Artikelpositionen, Stundenanzahlen und laufenden Kosten für jeden Artikel angezeigt.

## Bandbreite

Das Angebot beinhaltet 250 GB für monatlich abgerechnete virtuelle Server mit einen öffentlichen Uplink. Größere Zuordnungen können Sie zu einem reduzierten Satz im Vergleich zum Überschreitungstarif erwerben.

## Portgeschwindigkeit

Sie können die Uplink-Geschwindigkeit für den virtuellen Server auswählen (bis zu 1 GB/s). Die virtuellen Uplinks werden durch redundante physische Uplinks zu den öffentlichen und dedizierten IBM Netzen abgesichert. Die Geschwindigkeiten der öffentlichen und dedizierten Uplinks sind zum Zeitpunkt der Bestellung immer gleich und können bei Bedarf erhöht oder verringert werden.

## Software

Sie können Software auswählen, die bei der Bereitstellung von {{site.data.keyword.Bluemix_notm}} installiert werden soll. {{site.data.keyword.Bluemix_notm}} bietet Unterstützung für jede Software, die während des Bereitstellungsprozesses installiert wird. Nach dem Bereitstellen des Servers können Sie eigene Software installieren.

## Sicherheit

Vor der Bereitstellung sollten Sie sich mit den Sicherheitsoptionen befassen. Als Teil des Bestellprozesses können Sie eine einheitenspezifische Hardware- oder Software-Firewall auswählen, um Ihr System zu schützen. Alternativ können Sie dedizierte Firewallanwendungen in der Umgebung bereitstellen und den virtuellen Server in einem geschützten VLAN bereitstellen. 

**Hinweis:** Ein virtueller Server kann nicht durch zwei Firewall-Anwendungen in derselben Schnittstelle geschützt werden. 

Außerdem können Sie mithilfe von Sicherheitsgruppen eine Reihe von IP-Filterregeln aktivieren, die festlegen, wie eingehender und abgehender Datenverkehr für die öffentlichen und privaten Schnittstellen einer virtuellen Serverinstanz abgewickelt wird.

Weitere Informationen finden Sie unter [Firewalls](vsi_security_options.html) und [Einführung in Sicherheitsgruppen](/docs/infrastructure/security-groups/sg_index.html).

## Überwachung

Sie können aus einer Vielzahl von Überwachungsoptionen für den virtuellen Server auswählen. Zu den verfügbaren Optionen gehört die Standardüberwachung, die mit Pingsignalen und TCP-Serviceantworten (TCP = Transmission Control Protocol) sowie mit optionalen Antworten bei Störungen arbeitet. Sie können auch die erweiterte Überwachung hinzufügen, die den Nimsoft-Softwareagenten nutzt und umfangreichere Überwachungsfunktionen für den virtuellen Server und die installierte Software bereitstellt.

Weitere Informationen finden Sie unter [Überwachungskomponenten anzeigen und verwalten](vsi_viewing_monitors.html).

## Sicherung

Während des Bestellprozesses können Sie Evault-Sicherungen hinzufügen. Sie können auch eine R1soft-Lizenz für Ihre vorhandene R1soft-Sicherungsumgebung erwerben oder die Sicherungslösung eines Drittanbieters verwenden.

Weitere Informationen finden Sie unter [Einheit erneut bei eVault registrieren![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.

## Scripts nach der Bereitstellung

Bei jeder Bestellung eines virtuellen Servers können Scripts nach der Bereitstellung zugeordnet werden. Dies ermöglicht die Ausführung eines vom Kunden entwickelten Scripts, nachdem die Bereitstellungstasks abgeschlossen sind. Solche Scripts werden häufig verwendet, um eine kundenspezifische Konfiguration auf einen Server anzuwenden und die Automatisierung Ihrer Skalierungsstrategie zu unterstützen.

Weitere Informationen finden Sie unter [Angepasstes Bereitstellungsscript hinzufügen](vsi_add_script.html).

## Weitere Schritte
Wenn Sie mit dem Bereitstellen Ihres öffentlichen virtuellen Servers beginnen möchten, finden Sie weitere Informationen unter [Öffentliche Instanzen bereitstellen](vsi_provision_public.html).
