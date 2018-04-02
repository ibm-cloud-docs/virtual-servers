---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Virtuelle Server konfigurieren
{: #configuring-virtual-servers}

Stellen Sie sicher, dass der Zugriff auf Ihren virtuellen Server stets gemäß den Anforderungen Ihrer Umgebung konfiguriert wird.
{:shortdesc}

## Anmelden 
Melden Sie sich beim [{{site.data.keyword.slportal_full}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} mit den Berechtigungsnachweisen an, die Sie beim erstmaligen Erstellen Ihres Kontos per E-Mail erhalten haben.

## Virtuellen Server lokalisieren
Suchen Sie Ihren virtuellen Server in der Einheitenliste im {{site.data.keyword.slportal}}. Mithilfe der Einheitenliste können Sie Einheiten verwalten, Einheiten aktualisieren oder Diagramme für die Bandbreitennutzung erstellen. Weitere Informationen finden Sie unter [Virtuelle Server verwalten](../vsi/vsi_managing.html).

## IP-Adressen und Berechtigungsnachweise notieren
Bewahren Sie die IP-Adressen und Berechtigungsnachweise für den Server an einem sicheren Ort auf, an dem sie schnell und ohne Anmeldung beim {{site.data.keyword.slportal}} verfügbar sind. 
- Die IP-Adressen der einzelnen Einheiten können in der Einheitenliste angezeigt werden.
- Die Rootkennwörter für die einzelnen Einheiten können in der Snapshot-Ansicht der jeweiligen Einheit angezeigt werden. Klicken Sie auf den Pfeil neben dem Einheitennamen, um die Ansicht zu erweitern.
- Die IP-Adressen für mehrere Einheiten können über die Aktion 'CSV herunterladen' in der Einheitenliste angezeigt werden. Wählen Sie 'CSV herunterladen' im Dialogfenster für Einstellungen aus, um eine vollständige Liste der Einheiten und Details im Tabellenformat herunterzuladen.

## Berechtigungsnachweise für Software aktualisieren
Jeder Software, die beim Bereitstellungsprozess in Ihre Einheit geladen wurde, sind vorläufige Berechtigungsnachweise zugeordnet. Diese Berechtigungsnachweise können auf der Registerkarte 'Kennwörter' für jede Einheit im {{site.data.keyword.slportal}} angezeigt und verwaltet werden. Verwenden Sie diese vorläufigen Berechtigungsnachweise, um die Software zum ersten Mal aufzurufen. Als bewährtes Verfahren wird empfohlen, dass Sie Ihr Kennwort nach dem ersten Aufrufen der Software ändern. Verwenden Sie ein sicheres Kennwort, das eine Kombination aus Buchstaben, Zahlen und Sonderzeichen enthält.

Optional können Kennwortaktualisierungen auf der Registerkarte 'Kennwörter' für jede Einheit gespeichert werden. Beachten Sie jedoch, dass die im {{site.data.keyword.slportal}} gespeicherten Kennwörtern in der Anzeige 'Kennwörter' von jeder Person angezeigt werden können, die Zugriff auf das Konto hat und über entsprechende Berechtigungen verfügt.

Weitere Informationen zum Anzeigen und Verwalten Ihrer Softwareberechtigungsnachweise finden Sie unter [Infrastructure-Zugriff verwalten](../iam/mnginfra.html).

## Im privaten Netz auf eigene Server zugreifen
Das private Netz ist die Zentrale für Interaktionen mit Ihren Einheiten über Remote Desktop (RDP) mit SSH und KVM über IP. Das Tool für VPN-Zugriff ermöglicht Verbindungen in Ihrem privaten Netz mit dem nächsten SSL-VPN-Endpunkt oder mit einem Endpunkt Ihrer Wahl. Der VPN-Zugriff ist außerdem für Interaktionen mit vielen angebotenen Services erforderlich. Weitere Informationen finden Sie unter [Virtuelle private Netze (VPN) - Einführung](../infrastructure/iaas-vpn/getting-started.html).

## Überwachung einrichten
Die Überwachung dient primär als Ressource zum Überprüfen der Betriebszeit Ihres Servers und sie kann Anhaltspunkte für den geeigneten Zeitpunkt für Skalierungsmaßnahmen liefern. Die Standard Monitoring-Services und Nimsoft Monitoring decken unterschiedliche Überwachungsanforderungen ab. Standard Monitoring (gelegentlich auch als 'Basisüberwachung' bezeichnet) wird im Allgemeinen bei der Ping/Antwort-Methode mit einem langsamen Pingsignal oder einem Servicepingsignal verwendet, das über das {{site.data.keyword.slportal}} abgesetzt wird. Nimsoft Monitoring (auch als 'erweiterte Überwachung' bezeichnet) ist in drei Stufen (Basis, Erweitert und Premium) verfügbar. Dieser Service ist ebenfalls über das {{site.data.keyword.slportal}} zugänglich. Weitere Informationen finden Sie unter [Überwachung](../infrastructure/SLmonitoring/monitoring_index.html).

## System schützen
Mithilfe der verfügbaren Hardware-Firewalls können Sie sicherstellen, dass Ihr System stets geschützt ist. Hardware-Firewalls werden bei Bedarf ohne Ausfallszeit bereitgestellt. Wenn die Firewallregeln korrekt eingerichtet werden, kann Ihr System durch die Firewall vor unbeabsichtigten Aktivitäten geschützt werden. Nachdem Sie eine Firewall bestellt haben, muss sie aktiviert und mit Regeln ausgestattet werden.  

Weitere Informationen können Sie den folgenden Themensammlungen zur Sicherheit entnehmen.

* [Hardware-Firewalls (gemeinsam genutzt)](../infrastructure/hardware-firewall-shared/getting-started.html)
* [Hardware-Firewalls (dediziert)](../infrastructure/hardware-firewall-dedicated/getting-started.html)

Sicherheitsgruppen sind eine weitere Option zum Begrenzen des Datenaustauschs im Netz für Ihre virtuellen Server. Mithilfe von Sicherheitsgruppen können Sie eine Reihe von IP-Filterregeln aktivieren, die festlegen, wie eingehender und abgehender Datenverkehr für öffentliche und private Schnittstellen einer virtuellen Serverinstanz verarbeitet wird. Weitere Informationen finden Sie unter [Einführung in Sicherheitsgruppen](/docs/infrastructure/security-groups/sg_index.html).

## Sicherungen planen 
Sicherungen sorgen dafür, dass Ihre Daten sicher außerhalb Ihrer Einheit gespeichert werden, um Sie vor Datenverlust zu schützen. Die folgenden Sicherungsservices stehen zur Verfügung, um Ihre Daten an einer sicheren Position zu speichern, damit sie bei Bedarf erneut in Ihre Einheit geladen werden können:
- EVault Backup ist ein automatisiertes agentenbasiertes Sicherungssystem. Dabei handelt es sich um eine häufig genutzte und wartungsfreie Lösung zum Verwalten Ihrer Einheit. Diese Lösung ist über zusätzliche Plug-ins kompatibel mit Microsoft-Software wie Exchange und SQL. Benutzer von EVault interagieren mit diesem Service über die webbasierte EVault-Anwendung WebCC. Weitere Informationen finden Sie unter [Einführung in Backup-Services](../infrastructure/Backup/index.html).
- R1Soft Continuous Data Protection ist eine Backup-Software, die auf Ihrem Server oder Ihrer selbstverwalteten virtuellen Maschine installiert werden kann. Diese Software wird empfohlen, wenn Sie alle Ihre Sicherungen über eine einzige Schnittstelle verwalten möchten. Die Interaktion mit R1Soft CDP erfolgt über ein proprietäres Managementsystem, mit dem Agenten auf virtuellen Maschinen installiert und Datenbank-Plug-ins für zusätzliche Funktionen bereitgestellt werden können. Weitere Informationen finden Sie unter [Einführung in Backup-Services](../infrastructure/Backup/index.html).

## Nächste Schritte
Nachdem Ihr virtueller Server konfiguriert ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [Virtuellen Server verwalten](../vsi/vsi_managing.html).



