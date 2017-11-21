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


# Häufig gestellte Fragen (FAQs): Server (allgemein)

## Worin besteht der Unterschied zwischen "Aus Image starten" und "Aus Image laden"?
Die Funktionen "Aus Image starten" und "Aus Image laden" wenden vorhandene Imagevorlagen auf eine Einheit an, um das vorhandene Betriebssystem entweder zu ersetzen oder zu ergänzen. Mit dieser Maßnahme soll ein bestehendes Problem behoben werden. Der Hauptunterschied zwischen dem Start- und dem Ladeprozess ist der Typ des verwendeten Images. Stellen Sie vor dem Ausführen des Prozesses "Aus Image starten" oder "Aus Image laden" sicher, dass Sie alle Daten gesichert haben, die möglicherweise wiederhergestellt werden sollen.

   * "Aus Image starten" ist eine Methode zum Booten einer Einheit mithilfe eines ISO-Images, das von {{site.data.keyword.BluSoftlayer_full}} für die Systemwiederherstellung bereitgestellt wird, oder eines ISO-Images, das mit der Funktion *Image importieren* im {{site.data.keyword.slportal_full}} hochgeladen wurde. Das ISO-Image kann eine bereinigte Version des Betriebssystems der Einheit oder ein Wiederherstellungsdatenträger sein, die bzw. der verwendet werden kann, um ein Problem in der Einheit zu beheben.
   * "Aus Image laden" ist eine Methode zum erneuten Laden des Betriebssystems unter Verwendung einer Imagevorlage, die entweder aus einer Einheit erfasst oder mit der Funktion *Image importieren* im {{site.data.keyword.slportal}} hochgeladen wurde. Bei der Methode *Aus Image laden* wird eine VHD zum erneuten Laden verwendet. Dabei werden alle Daten auf der Einheit gelöscht und das vorhandene Betriebssystem sowie die Dateien werden durch eine (unbenutzte) Originalversion des ausgewählten Images ersetzt.

## Warum kann ich keine Verbindung zur KVM-Konsole herstellen?
Wenn Sie keine Verbindung zur KVM-Konsole herstellen können, prüfen Sie die nachfolgenden Tipps zur Fehlerbehebung, die beim Beheben des Problems nützlich sein können. Falls weitere Probleme auftreten sollten, wenden Sie sich an den Support. Weitere Informationen zur Kontaktaufnahme mit dem Support finden Sie unter [Hilfe und Unterstützung anfordern](../vsi/vsi_ts_index.html).

   * Die KVM-Konsole ist ein Java-Applet. Vor dem Zugriff auf die Konsole muss Java installiert werden. Weitere Informationen zum Installieren von Java finden Sie unter [Java kostenlos herunterladen ![Symbol für extrernen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.java.com/en/download/){: new_window}.   
   * Wenn Java installiert ist, stellen Sie sicher, dass eine Verbindung über VPN hergestellt wurde. Falls keine Verbindung besteht und Sie versuchen, eine Verbindung zur KVM-Konsole herzustellen, weist eine Warnung darauf hin, dass eine VPN-Verbindung erforderlich ist.
   * Die KVM-Konsole öffnet während des Verbindungsprozesses möglicherweise ein oder mehrere Popup-Fenster. Aktivieren Sie Pop-up-Fenster vom {{site.data.keyword.slportal}} um sicherzustellen, dass eine Verbindung hergestellt werden kann.
   * Möglicherweise wird der Fehler "Java-Anwendungen werden durch Ihre Sicherheitseinstellungen blockiert" angezeigt. Für Bare-Metal-iKVM-Einheiten müssen Sie eine Ausnahme für die IP-Adresse der IPMI-Einheit hinzufügen. Für VSI-Einheiten müssen "https://control.softlayer.com" und die IP-Adresse der KVM-Konsole zugelassen werden. Weitere Informationen finden Sie unter [Warum werden Java-Anwendungen beim aktuellen Java-Release durch Ihre Sicherheitseinstellungen blockiert? ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.java.com/en/download/help/java_blocked.xml){: new_window}.
   * Wenn die oben genannten Bedingungen erfüllt sind und der Fehler "Missing required Permissions manifest in main.jar" angezeigt wird, dann wurden im Java Control Panel keine Java-Applets aktiviert. Diese Einstellung wurde von Oracle in Java SE v7 als Sicherheitsvorkehrung eingeführt. Aktivieren Sie Applets im Control Panel, um dieses Problem zu beheben.

     **Anmerkung:** Wenn Sie Mac OS X in Verbindung mit Google Chrome verwenden, lesen Sie die Angaben unter "Informationen und Systemvoraussetzungen zum Installieren und Verwenden von Mac Java 7" auf der Java-Website.

   * Wenn bei dem Versuch, eine Verbindung zu einer VSI über die Java-Standardversion herzustellen, nur Fehler angezeigt werden, können Sie alternativ versuchen, VNC zu verwenden. Weitere Informationen zur Verwendung von VNC finden Sie unter [Über VNC mit Ihrer VSI verbinden ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://knowledgelayer.softlayer.com/articles/connect-your-vsi-using-vnc){: new_window}.

Wenn Sie alle oben angegebenen Prüfschritte durchgeführt haben und weiterhin keine Verbindung zur KVM-Konsole herstellen können, wenden Sie sich an den Support, um weitere Unterstützung bei der Fehlerbehebung zu erhalten. Wenn zwar eine Verbindung zur Konsole hergestellt wurde, jedoch Probleme beim Verbinden mit der Einheit aufgetreten sind, stellen Sie sicher, dass gültige Berechtigungsnachweise für den Zugriff auf die Einheit verwendet werden. Wenden Sie sich gegebenenfalls an den Kontoadministrator, um Berechtigungsnachweise zu überprüfen.

## Ich habe mein Kennwort für den Server nicht mehr. Wie kann ich das Kennwort wiederherstellen?
Wenn das Root- oder Administratorkennwort für Ihren Server plötzlich nicht mehr funktioniert, sollten Sie zunächst einige Punkte überprüfen, bevor Sie sich an den Support wenden.

   * Haben Sie das Kennwort kopiert und eingefügt? Falls nicht, versuchen Sie es. Fügen Sie das Kennwort probeweise in einem Texteditor ein, um sicherzustellen, dass keine unbeabsichtigten Leerzeichen mit kopiert werden.
   * Wenn der Server über eine Komponente cPanel verfügt: Besteht die Möglichkeit, dass Ihre IP-Adresse nach fehlgeschlagenen Anmeldeversuchen durch cPHulk gesperrt wurde? Wenn dies zutrifft, können Sie über KVM oder IPMI auf den Server zugreifen und Ihre IP-Adresse in die Whitelist eintragen, indem Sie cPHulk mit "/scripts/cphulkdwhitelist", gefolgt von Ihrer IP-Adresse eingeben.
   * Hat jemand in letzter Zeit versucht, das Kennwort für den Server durch Ändern des Kennworts im {{site.data.keyword.slportal}} zu ändern? Beim Ändern des Kennworts im {{site.data.keyword.slportal}} wird nur das für Sie angezeigte Kennwort geändert. Dies hat keine Auswirkung auf das vom Server verwendete Kennwort. Wenn dies der Fall ist, verständigen Sie den Support. Der Support kann in der Regel das ursprüngliche gültige Kennwort wiederherstellen.

Wenn die angegebenen Punkte überprüft wurden und weiterhin kein Serverzugriff mit dem Kennwort möglich ist, öffnen Sie ein Support-Ticket und fordern Sie das Zurücksetzen des Kennworts an. Der Support muss einen Neustart des Servers durchführen, um das Kennwort zurückzusetzen. Halten Sie sich bereit, den Neustart zu bestätigen und/oder benennen Sie einen Wartungszeitrahmen, in dem der Neustart erfolgen kann. Das Zurücksetzen des Kennworts dauert in den meisten Fällen nicht länger als 15 Minuten. Um ein Ticket zu öffnen, navigieren Sie im {{site.data.keyword.slportal}} zu **Support > Ticket hinzufügen** und verwenden Sie den Eintrag *"Neustarts und Konsolenzugriff"*.

## Werden LVM-Partitionen als gültiges Dateisystem unterstützt?
LVM (Logical Volume Management) ermöglicht die logische Verwaltung von Dateisystemen in Linux. In der {{site.data.keyword.BluSoftlayer}}-Umgebung wird LVM nicht als bootfähiges Partitionierungsschema unterstützt. Virtuelle Serverinstanzen können nicht mit LVM bestellt werden und das Bereitstellen von Images, die LVM als bootfähige Partition verwenden, schlägt fehl. Wenn Sie LVM auf der Bootpartition benötigen, finden Sie im Bare-Metal-Angebot Unterstützung für LVM beim Booten unter bestimmten Betriebssystemen. Bei entsprechender Betriebssystemunterstützung und -konfiguration können sekundäre VSI-Platten für LVM-Partitionen verwendet werden. Dabei ist jedoch zu beachten, dass LVM kein unterstütztes Dateisystem für flexible Images oder Imagevorlagen ist. Wenn Sie weitere Fragen haben, öffnen Sie ein Support-Ticket, um Unterstützung anzufordern.

## Vorkonfigurierte 161.26.0.0/16-Routen auf Kunden-Hosts
{{site.data.keyword.BluSoftlayer}} aktiviert auf allen neu bereitgestellten Servern eine neue Route, um zukünftige Produkte zu unterstützen.
   * Die Route verweist auf eine beliebige Adresse für das private Back-End-Netz im Bereich 161.26.0.0/16 (161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255).
   * Dieser IP-Block wird der {{site.data.keyword.BluSoftlayer_notm}} von IANA zugewiesen und nicht im öffentlichen Internet zugänglich gemacht.
   * Über diesen IP-Bereich werden nur Systeme der {{site.data.keyword.BluSoftlayer_notm}} adressiert.
   * ACLs auf Kundenservern, virtuellen Servern und Vyatta-Gateways müssen aktualisiert werden, damit Kunden-Hosts Infrastrukturservices verwenden können, die mit IP-Adressen aus diesem Bereich konfiguriert sind.

## Vorgehensweise beim Hinzufügen der neuen Routenwahl für verschiedene Betriebssysteme

   <table>
   <CAPTION>Tabelle 1. Routen für Betriebssysteme hinzufügen</CAPTION>
   <THEAD>
   <TR>
   <th>Betriebssystem</th>
   <th>Schritte</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Windows 2003 Standard und Enterprise</td>
   <td>
   Fügen Sie die persistente Route hinzu, indem Sie in der Befehlszeile Folgendes eingeben:
   <blockquote>route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p</blockquote>
   <b>Hinweis:</b> Ersetzen Sie 10.0.0.1 durch die IP-Adresse Ihres privaten Gateways.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Server Core
   </td>
   <td>
   Fügen Sie die persistente Route hinzu, indem Sie in der Befehlszeile Folgendes eingeben:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Hinweis:</b> Ersetzen Sie 10.0.0.1 durch die IP-Adresse Ihres privaten Gateways.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Web, Standard, Enterprise und Datacenter</td>
   <td>
   Fügen Sie die persistente Route hinzu, indem Sie in der Befehlszeile Folgendes eingeben:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Hinweis:</b> Ersetzen Sie 10.0.0.1 durch die IP-Adresse Ihres privaten Gateways.
   </td>
   </tr>
    <tr>
   <td>RedHat, Fedora und CentOS</td>
   <td>
   Erstellen bzw. bearbeiten Sie die folgende Datei, um eine neue Route zu erstellen: <i>/etc/sysconfig/network-scripts/route-eth0</i>
   <p>Nach dem Erstellen dieser Datei müssen Sie in der Datei die folgenden Angaben hinzufügen: <i>161.26.0.0/16 via 10.0.0.1</i>
   </p>
   <b>Hinweis:</b> Ersetzen Sie 10.0.0.1 durch die IP-Adresse Ihres privaten Gateways.
   </td>
   </tr>
   <tr>
   <td>Ubuntu und Debian</td>
   <td>
   Fügen Sie am Ende Ihrer Datei <i>/etc/network/interfaces</i> die folgende Zeile hinzu:
   <blockquote>
   up route add -net 161.26.0.0/16 gw 10.0.0.1
   </blockquote>
   <b>Hinweis:</b> Ersetzen Sie 10.0.0.1 durch die IP-Adresse Ihres privaten Gateways.
   </td>
   </tr>
   <tr>
   <td>Vyatta</td>
   <td><i>set protocols static route 161.26.0.0/16 next-hop 172.16.0.26</i>
   <p>
   <b>Hinweis:</b> Ersetzen Sie 172.16.0.26 durch das Gateway des Teilnetzes, in dem sich die Maschine befindet (dies sollte das Gateway sein, das auch für die Route 10.0.0./8 definiert ist).</p>
   </td>
   </tr>
   <tr>
   <td>ESXi</td>
   <td>Verwenden Sie den folgenden Befehl, um die Route zum ESXi-Host hinzuzufügen:
   <blockquote>
   esxcfg-route -a 161.26.0.0/16 10.0.0.1
   </blockquote>
   <b>Hinweis:</b> Ersetzen Sie 10.0.0.1 durch die IP-Adresse Ihres privaten Gateways.</td>
   </tr>
   <tr>
   <td>CoreOS</td>
   <td>Erstellen Sie in /etc/systemd/network eine Datei für statische Routen mit dem Namen 10-static.network, die Folgendes enthält:
   <blockquote>
   [Route]
   Gateway=10.0.0.1
   Destination=161.26.0.0/16
   </blockquote>
   <b>Hinweis:</b> Ersetzen Sie 10.0.0.1 durch die IP-Adresse Ihres privaten Gateways.</td>
   </tr>
   </TBODY>
   </table>
   
   <a name="top"></a>

## Kann das Überwachungssystem einen automatischen Warmstart auslösen UND einen Support-Techniker verständigen, wenn der Server nicht mehr reagiert?

Ja, wenn Sie den Service **Automatischer Warmstart nach Überwachungsfehler** bestellt haben, können Sie das Überwachungssystem so einrichten, dass automatisch ein Warmstart des Servers eingeleitet und ein Ticket für einen Support-Techniker geöffnet wird, wenn ein Überwachungsalert ausgegeben wird. Der zusätzliche Service **NOC-Überwachung** bietet die Möglichkeit, dass Sie persönlich benachrichtigt werden, wenn ein Überwachungsproblem auftritt. Weitere Informationen zu diesen beiden Angeboten enthält die Seite [Serverüberwachung ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://www.softlayer.com/services/monitoring/){:new_window}.


