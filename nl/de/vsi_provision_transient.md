---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-21"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:note: .note}
{:important: .important}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Transiente Instanzen bereitstellen
{: #ordering-vs-transient}

## Vorbereitungen
Sie haben zwei Möglichkeiten, um Ihre transienten virtuellen Serverinstanzen bereitzustellen. Die erste Möglichkeit ist die Verwendung der {{site.data.keyword.cloud}}-Konsole und die zweite Möglichkeit ist das {{site.data.keyword.slportal}}. Für die Konsole und für das {{site.data.keyword.slportal}} sind eindeutige Anmelde-IDs erforderlich. Sie können sich folglich mit dem Benutzernamen und Kennwort für die Konsole nicht beim Portal anmelden und umgekehrt.
{:shortdesc}

Zum Bestellen virtueller Server über die {{site.data.keyword.cloud_notm}}-Konsole benötigen Sie ein Konto, für das ein Upgrade durchgeführt wurde. Weitere Informationen zum Upgrade Ihres Kontos finden Sie in [Nutzungsabhängiges Konto](/docs/account?topic=account-accounts#paygo).
{:note}

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie beginnen.

  1. Prüfen Sie die Bereitstellungsoptionen, die für Sie verfügbar sind. Weitere Informationen finden Sie in [Transiente virtuelle Server](/docs/vsi?topic=virtual-servers-about-vs-transient).

  2. Lesen Sie die Hinweise zur Kapazität der virtuellen Serverinstanz. Weitere Informationen finden Sie in [Hinweise zu Ressourcen für virtuelle Serverinstanzen](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).
  
  3. Öffnen Sie die Seite für die [virtuelle Serverinstanz ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?guestType=transient&cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} in der {{site.data.keyword.cloud_notm}}-Konsole.

## Transiente virtuelle Serverinstanz bereitstellen
{: #ordering-transient-instance}

Wenn Sie eine transiente virtuelle Serverinstanz bereitstellen möchten, dann sollten Sie sich mit den folgenden Informationen vertraut machen.

Sie müssen angemeldet sein, um alle verfügbaren Optionen anzuzeigen.
{:tip}

### Transiente Instanz

| Feld    | Details     |
| -------- | ----------- |
| Abrechnung  |Transiente Instanzen sind nur als Instanzen mit stündlicher Abrechnung verfügbar. Wenn Sie eine Instanz mit stündlicher Abrechnung nach zehn Tagen abbrechen, dann bezahlen Sie nur für die Stunden für diese zehn Tage. |
| Hostname | Kann Bezeichnungen enthalten, die aus alphanumerischen Zeichen und Gedankenstrichen bestehen, die durch Punkte getrennt sind. Bezeichnungen dürfen nicht rein numerisch sein, mit einem Gedankenstrich beginnen oder enden und keine aufeinanderfolgenden Gedankenstriche oder Punkte enthalten. |
| Domäne | Muss mindestens zwei Bezeichnungen enthalten, die aus alphanumerischen Zeichen und Gedankenstrichen bestehen können, die durch Punkte getrennt sind. Bezeichnungen dürfen nicht mit einem Gedankenstrich beginnen oder enden und keine aufeinanderfolgenden Gedankenstriche oder Punkte enthalten. Die letzte Bezeichnung darf ausschließlich Buchstaben enthalten. |
| Platzierungsgruppe | Sie können für Ihre Instanz eine Platzierungsgruppe auswählen. Wenn Sie eine Platzierungsgruppe hinzufügen, dann gibt die Verteilungsregel an, dass die Instanzen sich auf unterschiedlichen physischen Hardwarekomponenten befinden. Weitere Informationen finden Sie im Abschnitt zu den [Platzierungsgruppen](/docs/vsi?topic=virtual-servers-placement-groups). |
| Standort  | Standorte bestehen aus Regionen (speziellen geografischen Bereichen) und Zonen (fehlertoleranten Rechenzentren innerhalb einer Region). Wählen Sie den Standort aus, an dem Ihre Instanz erstellt werden soll. |
| Gängige Profile | Die Auswahl einer der Konfigurationen mit gängigen Profilen bietet Ihnen Unterstützung für die am häufigsten verwendeten Anwendungsfälle. Profile enthalten vorkonfigurierte Instanzen, die in wenigen Minuten einsatzbereit sind. |
| Alle Profile |Weitere Informationen zu den verfügbaren Profiloptionen für transiente Instanzen finden Sie in [Transiente virtuelle Server](/docs/vsi?topic=virtual-servers-about-vs-transient). |
| SSH-Schlüssel     | SSH-Schlüssel ermöglichen den Zugriff auf eine Instanz, ohne dass hierzu ein Kennwort der entsprechenden Clients für jeden öffentlichen Schlüssel verwendet werden muss, der in der Instanz implementiert ist. Wenn Sie einen SSH-Schlüssel hinzufügen möchten, dann geben Sie den öffentlichen Schlüssel Ihres SSH-Schlüssels an, den Sie zur Anmeldung bei Ihrer Instanz nach deren Bereitstellung verwenden können. |
| Image        |  Bei einem Image handelt es sich um das bereitgestellte Betriebssystem für Ihre Instanz. Dabei stehen einige kostenlose Optionen wie CentOS und Ubuntu zur Verfügung. Zahlungspflichtige Optionen wie Windows Server und Red Hat Enterprise Linux (RHEL) sind ebenfalls verfügbar. Wichtig: Beachten Sie, dass für Windows eine primäre Platte mit 100 GB erforderlich ist.|
{: caption="Tabelle 1. Optionen für transiente Instanzen" caption-side="top"}

### Add-ons für transiente Instanzen 

Wenn Sie Software-Add-ons auswählen, müssen diese Komponenten mit Ihrem Image kompatibel sein, um Fehler bei der Bestellung Ihrer Instanz zu vermeiden. Sie können beispielsweise kein Red Hat-Image mit einer Microsoft-Datenbank bereitstellen.
{:important}

| Feld     | Details     |
| --------- | ----------- |
| Datenbanksoftware      | Sie können eine zu installierende Datenbanksoftware auswählen. {{site.data.keyword.cloud_notm}} unterstützt jede Datenbanksoftware, die während des Bereitstellungsprozesses bereitgestellt wird. Nach der Bereitstellung des Servers können Sie auch eigene Datenbanksoftware installieren. |
| Services | Abhängig von Ihrer Imageauswahl werden bestimmte Services automatisch für Sie ausgewählt. Sie können sich für jedes der verbleibenden Service-Add-ons für Ihre Instanz entscheiden. |
| Bereitstellungsscript | Bereitstellungsscripts werden häufig verwendet, um eine kundenspezifische Konfiguration auf einen Server anzuwenden und die Automatisierung Ihrer Skalierungsstrategie zu unterstützen. Als Bereitstellungsscript kann jede Datei verwendet werden, die vom Betriebssystem ausgeführt werden kann (dazu gehören auch kombinierte Binärdateien und alle vom Betriebssystem unterstützten Sprachen). Bereitstellungsscripts können nicht für Images verwendet werden, für die eine Cloud-Initialisierung durchgeführt wurde. Weitere Informationen hierzu finden Sie in [Bereitstellungsscripts](/docs/vsi?topic=virtual-servers-provisioning-scripts). |
| Benutzerdaten    | Sie können Benutzerdaten hinzufügen, mit denen automatisch allgemeine Konfigurationstasks oder Scripts ausgeführt werden können. Benutzerdaten können für Images mit oder ohne Cloud-Initialisierung verwendet werden. |
{: caption="Tabelle 2. Add-ons für transiente Instanzen" caption-side="top"}

### Angehängte Speicherplatten

Wenn Sie zusätzlichen Speicher benötigen, können Sie Speicherplatten an Ihre Instanz anhängen. Der Typ der Speicherplatten, die für Sie verfügbar sind, hängt von dem von Ihnen ausgewählten Profil ab.  

### Netzschnittstelle

| Feld    | Details     |
| -------- | ----------- |
| Uplink-Port-Geschwindigkeiten | Sie können die Uplink-Geschwindigkeit für Ihre Instanz auswählen, die bis zu 1 GB/s betragen kann. Die virtuellen Uplinks werden durch redundante physische Uplinks zu den öffentlichen und dedizierten IBM Netzen abgesichert. Die Geschwindigkeiten der öffentlichen und dedizierten Uplinks sind zum Zeitpunkt der Bestellung immer gleich und können bei Bedarf erhöht oder verringert werden.|
| Private und öffentliche Sicherheitsgruppe  |Mithilfe von Sicherheitsgruppen können Sie eine Reihe von IP-Filterregeln aktivieren, die festlegen, wie eingehender und abgehender Datenverkehr für öffentliche und private Schnittstellen Ihrer Instanz verarbeitet wird. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu den IBM Sicherheitsgruppen](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups). |
| Privates und öffentliches VLAN | Ihre virtuelle Serverinstanz wird standardmäßig in einem automatisch zugewiesenen VLAN platziert. Sie können ein anderes VLAN auswählen, wenn bereits eines in dem von Ihnen ausgewählten Rechenzentrum vorhanden ist. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu VLANs](/docs/infrastructure/vlans?topic=vlans-about-vlans). |
| Privates und öffentliches Teilnetz | Das Auswählen eines Teilnetzes ist optional und nur durchzuführen, wenn Ihre Einheit eine IP-Adresse aus dem Teilnetz verwenden soll. Falls Sie ein Teilnetz auswählen, prüfen Sie, ob Sie über genug IP-Adressen zur Erfüllung der Anforderung verfügen. Wenn Sie nicht über genug IP-Adressen für Ihr Teilnetz verfügen, kann Ihre Bestellung verzögert oder abgebrochen werden. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu Teilnetzen und IPs](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
{: caption="Tabelle 3. Optionen für Netzschnittstellen" caption-side="top"}

### Add-ons für Netzschnittstellen

| Feld    | Details     |
| -------- | ----------- |
| Bandbreite | Die Bandbreitenzuordnung ist für transiente virtuelle Serverinstanzen nicht enthalten. |
| Hardware- und Software-Firewalls  |Firewall-Services verhindern unerwünschten Datenverkehr auf Ihren Servern, verringern die Wahrscheinlichkeit eines Angriffs und ermöglichen Ihnen die Zuordnung Ihrer Serverressourcen für den beabsichtigen Verwendungszweck. |
| Primäre IP-Adresse | Ihrer Instanz wird automatisch eine primäre IP-Adresse zugeordnet. |
| Öffentliche sekundäre IP-Adressen | Diese Teilnetze sind Ihnen für die Dauer der Nutzung Ihrer virtuellen Serverinstanz zugeordnet. Sie können das Teilnetz separat abbrechen, wenn Sie jedoch Ihre Instanz abbrechen, wird auch das Teilnetz entfernt. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu Teilnetzen und IPs](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
| IPv6-Adressen und öffentliche statische IPv6-Adressen | Sie können eine IPv6-Adresse oder öffentliche statische IPv6-Adressen für Ihre Instanz auswählen. |
| VPN-Management | Diese Option wird automatisch für Ihre Instanz mit unbegrenzten SSL-VPN-Benutzern ausgewählt. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zu VPN](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn). |
{: caption="Tabelle 4. Add-ons für Netzschnittstellen" caption-side="top"}

## Transiente virtuelle Serverinstanzen über das Kundenportal bereitstellen
Führen Sie die folgenden Schritte aus, um eine transiente virtuelle Serverinstanz über das {{site.data.keyword.slportal}} bereitzustellen:

  1. Melden Sie sich beim [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an.
  2. Suchen Sie den Bereich **Bestellung** und klicken Sie auf **Einheiten**.
  3. Klicken Sie unter *Öffentlicher virtueller Server* auf der Seite *Einheiten* auf **Transient** für das Angebot für virtuelle Server.
  4. Geben Sie auf der Seite *Cloud-Server konfigurieren* alle relevanten Informationan an.
  5. Klicken Sie auf **Zur Bestellung hinzufügen**, um fortzufahren.
  6. Bestätigen oder bearbeiten Sie die Domäneninformationen für den Server.
  7. Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
  8. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige bei Bedarf. Sie ist auch die Bestätigung für die Auftragsbestätigung für die Bereitstellung.

Sie können einen transienten virtuellen Server auch mithilfe der {{site.data.keyword.slapi_short}} bereitstellen. Ein Beispiel finden Sie unter [Transiente Instanz mit dem Objekt 'create' bereitstellen](/docs/vsi?topic=virtual-servers-api-rest-public#api-rest-transient).
{:tip}

## Nächste Schritte
Mehrere E-Mails werden an Ihren Administrator gesendet: Bestätigung der Bereitstellungsbestellung, Genehmigungs- und Bearbeitungsnachricht für die Bereitstellungsbestellung sowie Nachricht zur Fertigstellung der Bereitstellung. Über einen Link in der E-Mail, die die Fertigstellung der Bereitstellung mitteilt, gelangen Sie zu Ihrer Seite *Einheitendetails*.
 
Nachdem Ihr virtueller Server bereitgestellt wurde und einsatzbereit ist, können Sie Ihre virtuellen Server über die {{site.data.keyword.cloud_notm}}-Konsole oder über die {{site.data.keyword.slapi_short}} konfigurieren. Weitere Informationen finden Sie unter [Virtuelle Server konfigurieren](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
