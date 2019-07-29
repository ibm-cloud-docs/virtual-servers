---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-17"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Öffentliche Instanzen bereitstellen
{: #ordering-vs-public}

## Vorbereitungen
Sie haben zwei Möglichkeiten, um Ihre öffentlichen virtuellen Serverinstanzen bereitzustellen. Die erste Möglichkeit ist die Verwendung der {{site.data.keyword.cloud}}-Konsole und die zweite Möglichkeit ist das {{site.data.keyword.slportal}}. Für die Konsole und für das {{site.data.keyword.slportal}} sind eindeutige Anmelde-IDs erforderlich. Sie können sich folglich mit dem Benutzernamen und Kennwort für die Konsole nicht beim Portal anmelden und umgekehrt.
{:shortdesc}

Zum Bestellen virtueller Server über die {{site.data.keyword.cloud_notm}}-Konsole benötigen Sie ein Konto, für das ein Upgrade durchgeführt wurde. Weitere Informationen zum Upgrade Ihres Kontos finden Sie in [Nutzungsabhängiges Konto](/docs/account?topic=account-accounts#paygo).
{:note}

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie beginnen.

  1. Prüfen Sie die Bereitstellungsoptionen, die für Sie verfügbar sind. Weitere Informationen finden Sie in [Öffentliche virtuelle Server](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers).

  2. Lesen Sie die Hinweise zur Kapazität der virtuellen Serverinstanz. Weitere Informationen finden Sie in [Hinweise zu Ressourcen für virtuelle Serverinstanzen](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).
  
  3. Öffnen Sie die Seite für die [virtuelle Serverinstanz ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} in der {{site.data.keyword.cloud_notm}}-Konsole.

## Öffentliche virtuelle Serverinstanz bereitstellen  
{: #ordering-public-instance}

Wenn Sie eine virtuelle Serverinstanz bereitstellen möchten, dann sollten Sie sich mit den folgenden Informationen vertraut machen.

Sie müssen angemeldet sein, um alle verfügbaren Optionen anzuzeigen.
{:tip}

### Öffentliche Instanz

| Feld    | Details     |
| -------- | ----------- |
| Abrechnung  | Abhängig von Ihrer virtuellen Serverinstanz können Sie entweder die stündliche oder die monatliche Abrechnung auswählen. Der Hauptunterschied (abgesehen von den Gebühren) besteht darin, dass nach Stunden abgerechnete Instanzen keine Bandbreitenzuordnung beinhalten. Am Ende des Abrechnungszeitraums werden die genutzte Bandbreite und die Anzahl der Stunden, in denen jede Instanz für das Konto aktiv war, berechnet. Wenn Sie beispielsweise eine Instanz mit stündlicher Abrechnung nach zehn Tagen abbrechen, dann bezahlen Sie nur für die Stunden für diese zehn Tage. Wenn Sie eine Instanz mit monatlicher Abrechnung nach zehn Tagen abbrechen, bezahlen Sie für den ganzen Monat. Wenn Sie an der Nutzung des Features für das Aussetzen der Abrechnung interessiert sind, das nur für Instanzen mit stündlicher Abrechnung zur Verfügung steht, dann finden Sie weiterführende Informationen im Abschnitt mit den [Informationen zum Aussetzen der Abrechnung](/docs/vsi?topic=virtual-servers-about-suspend-billing). |
| Hostname | Kann Bezeichnungen enthalten, die aus alphanumerischen Zeichen und Gedankenstrichen bestehen, die durch Punkte getrennt sind. Bezeichnungen dürfen nicht rein numerisch sein, mit einem Gedankenstrich beginnen oder enden und keine aufeinanderfolgenden Gedankenstriche oder Punkte enthalten. |
| Domäne | Muss mindestens zwei Bezeichnungen enthalten, die aus alphanumerischen Zeichen und Gedankenstrichen bestehen können, die durch Punkte getrennt sind. Bezeichnungen dürfen nicht mit einem Gedankenstrich beginnen oder enden und keine aufeinanderfolgenden Gedankenstriche oder Punkte enthalten. Die letzte Bezeichnung darf ausschließlich Buchstaben enthalten. |
| Platzierungsgruppe | Sie können für Ihre Instanz eine Platzierungsgruppe auswählen. Wenn Sie eine Platzierungsgruppe hinzufügen, dann gibt die Verteilungsregel an, dass die Instanzen sich auf unterschiedlichen physischen Hardwarekomponenten befinden. Weitere Informationen finden Sie im Abschnitt zu den [Platzierungsgruppen](/docs/vsi?topic=virtual-servers-placement-groups). |
| Standort  | Standorte bestehen aus Regionen (speziellen geografischen Bereichen) und Zonen (fehlertoleranten Rechenzentren innerhalb einer Region). Wählen Sie den Standort aus, an dem Ihre virtuelle Serverinstanz erstellt werden soll. |
| Gängige Profile | Die Auswahl einer der Konfigurationen mit gängigen Profilen bietet Ihnen Unterstützung für die am häufigsten verwendeten Anwendungsfälle. Profile enthalten vorkonfigurierte Instanzen, die in wenigen Minuten einsatzbereit sind. |
| Alle Profile | Weitere Informationen zu den verfügbaren Profiloptionen für öffentliche Instanzen finden Sie in [Öffentliche virtuelle Server](/docs/vsi?topic=virtual-servers-about-public-virtual-servers). |
| SSH-Schlüssel     | SSH-Schlüssel ermöglichen den Zugriff auf eine Instanz, ohne dass hierzu ein Kennwort der entsprechenden Clients für jeden öffentlichen Schlüssel verwendet werden muss, der in der Instanz implementiert ist. Wenn Sie einen SSH-Schlüssel hinzufügen möchten, dann geben Sie den öffentlichen Schlüssel Ihres SSH-Schlüssels an, den Sie zur Anmeldung bei Ihrer Instanz nach deren Bereitstellung verwenden können. |
| Image        |  Bei einem Image handelt es sich um das bereitgestellte Betriebssystem für Ihre Instanz. Dabei stehen einige kostenlose Optionen wie CentOS und Ubuntu zur Verfügung. Zahlungspflichtige Optionen wie Windows Server und Red Hat Enterprise Linux (RHEL) sind ebenfalls verfügbar. Wichtig: Beachten Sie, dass für Windows eine primäre Platte mit 100 GB erforderlich ist.|
{: caption="Tabelle 1. Optionen für öffentliche Instanzen" caption-side="top"}

### Add-ons für öffentliche Instanzen 

Wenn Sie Betriebssysteme, Steuerkonsolen oder Software-Add-ons auswählen, müssen diese Komponenten mit Ihrem Image kompatibel sein, um Fehler bei der Bestellung Ihrer Instanz zu vermeiden. Sie können beispielsweise kein Red Hat-Image mit einer Microsoft-Datenbank bereitstellen.
{:important}

| Feld     | Details     |
| --------- | ----------- |
| Betriebssystem-Add-ons | Wenn Sie die monatliche Abrechnung auswählen, dann haben Sie die Wahl zwischen den folgenden Image-Add-ons:<br><br> **R1Soft Server Backup Manager** bietet leistungsfähige Funktionen für die Serversicherung von Platte auf Platte sowie die zentrale Verwaltung und ein Datenrepository. Wenn Sie das R1Soft-Add-on auswählen, dann müssen Sie ein R1Soft Backup Agent-Paket erwerben, bei dem es sich um ein CDP-Add-on im Abschnitt **Services** handelt. Werden diese Komponenten nicht gemeinsam ausgewählt, dann führt dies zu einem Fehler in Ihrer Bestellung. Weitere Informationen zu R1Soft und IBM Cloud finden Sie im Abschnitt zum [R1Soft Server Backup Manager ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/cloud/backup-and-restore?mhq=R1Soft%20Server%20Backup%20Manager&mhsrc=ibmsearch_a){: new_window}.<br><br>**Veeam Backup and Replication** kombiniert Funktionen für automatisierte Sicherungen mit Funktionen für die Wiederherstellung und Replikation. Veeam bietet außerdem Funktionen für die erweiterte Überwachung, Berichterstellung und Kapazitätsplanung. Weitere Informationen zu Veeam Backup and Replication finden Sie im Abschnitt zu [Veeam Backup and Replication mit IBM Speicher ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www-356.ibm.com/partnerworld/gsd/solutiondetails.do?solution=54724&lc=en&stateCd=P&tab=2){: new_window}.<br><br>**VMware vCenter** dient zur Automatisierung der Bereitstellung der zugrunde liegenden VMware vSphere- und VMware vCenter Server-Ebenen, die Sie für eine flexible und anpassbare VMware-Lösung benötigen. Weitere Informationen zu vCenter on IBM Cloud finden Sie im Abschnitt mit den [Informationen zu vCenter Server on IBM Cloud ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/downloads/cas/L7RKPZND?mhq=vmware%20vcenter&mhsrc=ibmsearch_a){: new_window}.|
| Steuerkonsolensoftware | Wenn Sie die monatliche Abrechnung auswählen, dann können Sie eine Steuerkonsole für das Web-Hosting hinzufügen. |
| Datenbanksoftware      | Sie können eine zu installierende Datenbanksoftware auswählen. {{site.data.keyword.cloud_notm}} unterstützt jede Datenbanksoftware, die während des Bereitstellungsprozesses bereitgestellt wird. Nach der Bereitstellung des Servers können Sie auch eigene Datenbanksoftware installieren. |
| Services | Abhängig von Ihrem Abrechnungstyp und der Imageauswahl werden bestimmte Services automatisch für Sie ausgewählt. Sie können sich für jedes der verbleibenden Service-Add-ons für Ihre Instanz entscheiden. |
| Bereitstellungsscript | Bereitstellungsscripts werden häufig verwendet, um eine kundenspezifische Konfiguration auf einen Server anzuwenden und die Automatisierung Ihrer Skalierungsstrategie zu unterstützen. Als Bereitstellungsscript kann jede Datei verwendet werden, die vom Betriebssystem ausgeführt werden kann (dazu gehören auch kombinierte Binärdateien und alle vom Betriebssystem unterstützten Sprachen). Bereitstellungsscripts können nicht für Images verwendet werden, für die eine Cloud-Initialisierung durchgeführt wurde. Weitere Informationen hierzu finden Sie in [Bereitstellungsscripts](/docs/vsi?topic=virtual-servers-provisioning-scripts). |
| Benutzerdaten    | Sie können Benutzerdaten hinzufügen, mit denen automatisch allgemeine Konfigurationstasks oder Scripts ausgeführt werden können. Benutzerdaten können für Images mit oder ohne Cloud-Initialisierung verwendet werden. |
{: caption="Tabelle 2. Add-ons für öffentliche Instanzen" caption-side="top"}

### Angehängte Speicherplatten

Wenn Sie zusätzlichen Speicher benötigen, können Sie Speicherplatten an Ihre Instanz anhängen. Der Typ der Speicherplatten, die für Sie verfügbar sind, hängt von dem von Ihnen ausgewählten Profil ab. Zum Beispiel verwenden ausgeglichene lokale Profile und einige der GPU-Profile lokale Speicherplatten. Wenn Sie die monatliche Abrechnung auswählen, dann können Sie {{site.data.keyword.backup_notm}} hinzufügen und die Option auswählen, die Ihren Anforderungen am besten entspricht. Weitere Informationen hierzu finden Sie im Abschnitt zu den [{{site.data.keyword.backup_notm}}-Services](/docs/infrastructure/Backup?topic=Backup-getting-started).

### Netzschnittstelle

| Feld    | Details     |
| -------- | ----------- |
| Uplink-Port-Geschwindigkeiten | Sie können die Uplink-Geschwindigkeit für Ihre Instanz auswählen, die bis zu 1 GB/s betragen kann. Die virtuellen Uplinks werden durch redundante physische Uplinks zu den öffentlichen und dedizierten IBM Netzen abgesichert. Die Geschwindigkeiten der öffentlichen und dedizierten Uplinks sind zum Zeitpunkt der Bestellung immer gleich und können bei Bedarf erhöht oder verringert werden. |
| Private und öffentliche Sicherheitsgruppe  |Mithilfe von Sicherheitsgruppen können Sie eine Reihe von IP-Filterregeln aktivieren, die festlegen, wie eingehender und abgehender Datenverkehr für öffentliche und private Schnittstellen Ihrer Instanz verarbeitet wird. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu den IBM Sicherheitsgruppen](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups). |
| Privates und öffentliches VLAN | Ihre virtuelle Serverinstanz wird standardmäßig in einem automatisch zugewiesenen VLAN platziert. Sie können ein anderes VLAN auswählen, wenn bereits eines in dem von Ihnen ausgewählten Rechenzentrum vorhanden ist. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu VLANs](/docs/infrastructure/vlans?topic=vlans-about-vlans). |
| Privates und öffentliches Teilnetz | Das Auswählen eines Teilnetzes ist optional und nur durchzuführen, wenn Ihre Einheit eine IP-Adresse aus dem Teilnetz verwenden soll. Falls Sie ein Teilnetz auswählen, prüfen Sie, ob Sie über genug IP-Adressen zur Erfüllung der Anforderung verfügen. Wenn Sie nicht über genug IP-Adressen für Ihr Teilnetz verfügen, kann Ihre Bestellung verzögert oder abgebrochen werden. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu Teilnetzen und IPs](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
{: caption="Tabelle 3. Optionen für Netzschnittstellen" caption-side="top"}

### Add-ons für Netzschnittstellen

| Feld    | Details     |
| -------- | ----------- |
| Bandbreite | Im Angebot für Instanzen mit monatlicher Abrechnung mit öffentlichem Uplink sind 250 GB enthalten. Größere Zuordnungen können Sie zu einem reduzierten Satz im Vergleich zum Überschreitungstarif erwerben. |
| Hardware- und Software-Firewalls  |Firewall-Services verhindern unerwünschten Datenverkehr auf Ihren Servern, verringern die Wahrscheinlichkeit eines Angriffs und ermöglichen Ihnen die Zuordnung Ihrer Serverressourcen für den beabsichtigen Verwendungszweck. |
| Primäre IP-Adresse | Ihrer Instanz wird automatisch eine primäre IP-Adresse zugeordnet. |
| Öffentliche sekundäre IP-Adressen | Diese Teilnetze sind Ihnen für die Dauer der Nutzung Ihrer virtuellen Serverinstanz zugeordnet. Sie können das Teilnetz separat abbrechen, wenn Sie jedoch Ihre Instanz abbrechen, wird auch das Teilnetz entfernt. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu Teilnetzen und IPs](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
| IPv6-Adressen und öffentliche statische IPv6-Adressen | Sie können eine IPv6-Adresse oder öffentliche statische IPv6-Adressen für Ihre Instanz auswählen. |
| VPN-Management | Diese Option wird automatisch für Ihre Instanz mit unbegrenzten SSL-VPN-Benutzern ausgewählt. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu VPN](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn). |
{: caption="Tabelle 4. Add-ons für Netzschnittstellen" caption-side="top"}


## Öffentliche Instanz über das Kundenportal bereitstellen
Führen Sie die folgenden Schritte aus, um Ihre öffentliche virtuelle Serverinstanz über das {{site.data.keyword.slportal}} bereitzustellen:

  1. Melden Sie sich beim [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an.
  2. Suchen Sie den Bereich **Bestellung** und klicken Sie auf **Einheiten**.
  3. Klicken Sie auf der Seite 'Einheiten' auf **Stündliches SAN**, **Stündlich lokal**, **Monatlich** oder **Transient** für eines der Angebote für virtuelle Server.
  4. Geben Sie auf der Seite *Cloud-Server konfigurieren* alle relevanten Informationan an.
  5. Klicken Sie auf **Zur Bestellung hinzufügen**, um fortzufahren.
  6. Bestätigen oder bearbeiten Sie die Domäneninformationen für den Server.
  7. Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
  8. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige bei Bedarf. Sie ist auch die Bestätigung für die Auftragsbestätigung für die Bereitstellung.

## Nächste Schritte
Mehrere E-Mails werden an Ihren Administrator gesendet: Bestätigung der Bereitstellungsbestellung, Genehmigungs- und Bearbeitungsnachricht für die Bereitstellungsbestellung sowie Nachricht zur Fertigstellung der Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zur zugehörigen Seite *Einheitendetails*, nachdem Sie sich bei {{site.data.keyword.Bluemix_notm}} angemeldet haben.

Nachdem Ihr virtueller Server bereitgestellt wurde und einsatzbereit ist, können Sie Ihre virtuellen Server über die
{{site.data.keyword.cloud_notm}}-Konsole oder über die {{site.data.keyword.slapi_short}} konfigurieren. Weitere Informationen finden Sie unter [Virtuelle Server konfigurieren](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
