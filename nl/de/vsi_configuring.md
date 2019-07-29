---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Virtuelle Server konfigurieren
{: #configuring-virtual-servers}

Wenn Sie Zugriff auf Ihren virtuellen Server haben, sollten Sie Ihr Kennwort ändern und prüfen, ob die Einrichtung von SSH für eine Authentifizierungslösung mit höherer Sicherheit sinnvoll ist. Es stehen zahlreiche weitere Optionen zur Konfiguration Ihres virtuellen Servers zur Verfügung, um die Anforderungen Ihrer Umgebung zu erfüllen.
{:shortdesc}

## Anmelden
Melden Sie sich bei der [{{site.data.keyword.cloud}}-Konsole ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/classic?){: new_window} mit den Berechtigungsnachweisen an, die Sie bei der Ersterstellung Ihres Kontos per E-Mail erhalten haben. Alternativ hierzu können Sie sich auch beim [{{site.data.keyword.slportal}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){:new_window} anmelden.

## Virtuellen Server lokalisieren
Suchen Sie Ihren virtuellen Server in der Einheitenliste in der {{site.data.keyword.cloud_notm}}-Konsole. Mithilfe der Einheitenliste können Sie Einheiten verwalten, Einheiten aktualisieren oder Diagramme für die Bandbreitennutzung erstellen. Weitere Informationen finden Sie unter [Virtuelle Server verwalten](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).

## Kennwort ändern
Ändern Sie Ihr Kennwort und verwenden Sie hierbei die Richtlinien für sichere Kennwörter. Weitere Informationen hierzu finden Sie im Abschnitt zum [Anzeigen und Verwalten von Benutzernamen und Kennwörtern für Einheiten](/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device#view-update-user-name-password-for-device).

## SSH konfigurieren
SSH bietet eine bessere Sicherheitslösung als die Kennwortauthentifizierung. Weitere Informationen hierzu finden Sie im Abschnitt mit der [Einführung zu SSH-Schlüsseln](/docs/infrastructure/ssh-keys?topic=ssh-keys-getting-started-tutorial#getting-started-tutorial).

## IP-Adressen und Berechtigungsnachweise notieren
Bewahren Sie die IP-Adressen und Berechtigungsnachweise für den Server an einem sicheren Ort auf, an dem sie schnell und ohne Anmeldung bei der {{site.data.keyword.cloud_notm}}-Konsole verfügbar sind.
- Die IP-Adressen der einzelnen Einheiten können in der Einheitenliste angezeigt werden.
- Die Rootkennwörter für die einzelnen Einheiten können in der Snapshot-Ansicht der jeweiligen Einheit angezeigt werden. Klicken Sie auf den Pfeil neben dem Einheitennamen, um die Ansicht zu erweitern.
- Die IP-Adressen für mehrere Einheiten können über die Aktion 'CSV herunterladen' in der Einheitenliste angezeigt werden. Wählen Sie 'CSV herunterladen' im Dialogfenster für Einstellungen aus, um eine vollständige Liste der Einheiten und Details im Tabellenformat herunterzuladen.

## Berechtigungsnachweise für Software aktualisieren
Jeder Software, die beim Bereitstellungsprozess in Ihre Einheit geladen wurde, sind vorläufige Berechtigungsnachweise zugeordnet. Diese Berechtigungsnachweise können auf der Registerkarte 'Kennwörter' für jede Einheit in der {{site.data.keyword.cloud_notm}}-Konsole angezeigt und verwaltet werden. Verwenden Sie diese vorläufigen Berechtigungsnachweise, um die Software zum ersten Mal aufzurufen. Als bewährtes Verfahren wird empfohlen, dass Sie Ihr Kennwort nach dem ersten Aufrufen der Software ändern. Verwenden Sie ein sicheres Kennwort, das eine Kombination aus Buchstaben, Zahlen und Sonderzeichen enthält.

Optional können Kennwortaktualisierungen auf der Registerkarte 'Kennwörter' für jede Einheit gespeichert werden. Beachten Sie jedoch, dass die in der {{site.data.keyword.cloud_notm}}-Konsole gespeicherten Kennwörter in der Anzeige 'Kennwörter' von jeder Person angezeigt werden können, die Zugriff auf das Konto hat und über entsprechende Berechtigungen verfügt.

Weitere Informationen zum Anzeigen und Verwalten Ihrer Softwareberechtigungsnachweise finden Sie im Abschnitt zum [Verwalten des Zugriffs auf die klassische Infrastruktur](/docs/vsi?topic=iam-mngclassicinfra).

## Im privaten Netz auf eigene Server zugreifen
Das private Netz ist die Zentrale für Interaktionen mit Ihren Einheiten über Remote Desktop (RDP) mit SSH und KVM über IP. Das Tool für VPN-Zugriff ermöglicht Verbindungen in Ihrem privaten Netz mit dem nächsten SSL-VPN-Endpunkt oder mit einem Endpunkt Ihrer Wahl. Der VPN-Zugriff ist außerdem für Interaktionen mit vielen angebotenen Services erforderlich. Weitere Informationen finden Sie unter [Virtuelle private Netze (VPN) - Einführung](/docs/infrastructure/iaas-vpn?topic=VPN-gettingstarted-with-virtual-private-networking).

## Überwachung einrichten
Die Überwachung dient primär als Ressource zum Überprüfen der Betriebszeit Ihres Servers und sie kann Anhaltspunkte für den geeigneten Zeitpunkt für Skalierungsmaßnahmen liefern. Die Standard Monitoring-Services und Nimsoft Monitoring decken unterschiedliche Überwachungsanforderungen ab. Standard Monitoring (gelegentlich auch als 'Basisüberwachung' bezeichnet) wird im Allgemeinen bei der Ping/Antwort-Methode mit einem langsamen Pingsignal oder einem Servicepingsignal verwendet, das über die {{site.data.keyword.cloud_notm}}-Konsole abgesetzt wird. Nimsoft Monitoring (auch als 'erweiterte Überwachung' bezeichnet) ist in drei Tiers (Basis, Erweitert und Premium) verfügbar. Dieser Service ist ebenfalls über die {{site.data.keyword.cloud_notm}}-Konsole zugänglich. Weitere Informationen finden Sie unter [Überwachung](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring#monitoring).

## Sicherheitsgruppen konfigurieren
Sie können Sicherheitsgruppen verwenden, um den Netzdatenverkehr auf Ihren virtuellen Servern zu begrenzen. Mithilfe von Sicherheitsgruppen können Sie eine Reihe von IP-Filterregeln aktivieren, die festlegen, wie eingehender und abgehender Datenverkehr für öffentliche und private Schnittstellen einer virtuellen Serverinstanz verarbeitet wird. Weitere Informationen finden Sie unter [Einführung in Sicherheitsgruppen](/docs/infrastructure/security-groups?topic=security-groups-getting-started).

## Firewalls konfigurieren
Für einen höheren Schutz stehen auch Hardware-Firewalls zur Verfügung. Hardware-Firewalls werden bei Bedarf ohne Ausfallszeit bereitgestellt. Wenn die Firewallregeln korrekt eingerichtet werden, kann Ihr System durch die Firewall vor unbeabsichtigten Aktivitäten geschützt werden. Nachdem Sie eine Firewall bestellt haben, muss sie aktiviert und mit Regeln ausgestattet werden.

Weitere Informationen finden Sie in den folgenden Abschnitten.

* [Hardware-Firewalls (gemeinsam genutzt)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Hardware-Firewalls (dediziert)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)

## Sicherungen planen
Sicherungen sorgen dafür, dass Ihre Daten sicher außerhalb Ihrer Einheit gespeichert werden, um Sie vor Datenverlust zu schützen. Die folgenden Sicherungsservices stehen zur Verfügung, um Ihre Daten an einer sicheren Position zu speichern, damit sie bei Bedarf erneut in Ihre Einheit geladen werden können:
- {{site.data.keyword.backup_notm}} ist ein automatisiertes agentenbasiertes Sicherungssystem. Dabei handelt es sich um eine häufig genutzte und wartungsfreie Lösung zum Verwalten Ihrer Einheit. Diese Lösung ist über zusätzliche Plug-ins kompatibel mit Microsoft-Software wie Exchange und SQL. {{site.data.keyword.backup_notm}}-Benutzer interagieren mit diesem Service über die webbasierte {{site.data.keyword.backup_notm}}-Anwendung WebCC. Weitere Informationen finden Sie in [Einführung in {{site.data.keyword.backup_notm}}-Services](/docs/infrastructure/Backup?topic=Backup-getting-started).
- R1Soft Continuous Data Protection ist eine Backup-Software, die auf Ihrem Server oder Ihrer selbstverwalteten virtuellen Maschine installiert werden kann. Diese Software wird empfohlen, wenn Sie alle Ihre Sicherungen über eine einzige Schnittstelle verwalten möchten. Die Interaktion mit R1Soft CDP erfolgt über ein proprietäres Managementsystem, mit dem Agenten auf virtuellen Maschinen installiert und Datenbank-Plug-ins für zusätzliche Funktionen bereitgestellt werden können. Weitere Informationen finden Sie in [Einführung in {{site.data.keyword.backup_notm}}-Services](/docs/infrastructure/Backup?topic=Backup-getting-started).

## Nächste Schritte
Nachdem Ihr virtueller Server konfiguriert ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [Virtuellen Server verwalten](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
