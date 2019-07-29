---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Datenverkehrsspitzen mit der ressourcenbasierten automatischen Skalierung verwalten
{: #managing-resourced-based-auto-scaling}

Die Markteinführung eines neuen Produkts oder eine Verkaufsaktion für ein bereits vorhandenes Produkt kann zu Datenverkehrsspitzen auf Ihrer Website führen. Eine Datenverkehrsspitze kann sich auf die Antwortzeiten auswirken, die sich wiederum auf die Kundenerfahrung mit Ihrer Website auswirken. Das Feature für die automatische Skalierung von {{site.data.keyword.cloud}} ermöglicht es Ihnen, auf solche Datenverkehrsspitzen automatisch zu reagieren. Mit der ressourcenbasierten automatischen Skalierung können Sie diese Datenverkehrsspitzen besser kontrollieren.
{:shortdesc}

## Vorbereitungen
Navigieren Sie zuerst zum Einheitenmenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Tasks auszuführen.

* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Wenn Sie kein Kontoadministrator sind, muss Ihr Benutzerkonto über die Berechtigung zur Nutzung der automatischen Skalierung verfügen. Weitere Informationen zum Aktualisieren von Berechtigungen für die Nutzung der automatischen Skalierung finden Sie im Abschnitt zum [Einrichten von Benutzerberechtigungen für die automatische Skalierung](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen. 

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Gruppe für automatische Skalierung hinzufügen
{: #adding-auto-scale-group}

Beispiel: Eine E-Commerce-Site mit Standort in Dallas, Texas, benötigt drei virtuelle Server, um jederzeit online zu sein. Spitzen im Geschäftsbetrieb treten werktags im Zeitraum zwischen 9:00 Uhr und 17:00 Uhr auf, wenn das Unternehmen Onlineverkäufe durchführt. Um die Antwortzeiten der Website stabil zu halten, werden in diesem Zeitraum drei zusätzliche Server benötigt. Darüber hinaus sollten zwei weitere virtuelle Server bereitgestellt werden, um Zeiten abzudecken, in denen das durchschnittliche öffentliche Datenverkehrseingangsvolumen für zehn Minuten auf allen virtuellen Servern über 5 MB pro Sekunde beträgt. Fällt das Datenverkehrsvolumen wieder unter 5 MB pro Sekunde, dann soll die Ausführung dieser zusätzlichen virtuellen Server abgebrochen werden und die Server sollen entfernt werden. Dabei soll erreicht werden, dass Datenverkehrsspitzen mit maximal fünf virtuellen Servern bewältigt werden, wodurch die an Wochentagen eingesetzten virtuellen Server nicht durch den zusätzlichen Datenverkehr an Wochentagen beeinträchtigt werden. In den folgenden Schritten werden Sie durch die Einrichtung der automatischen Skalierung zur Unterstützung der ressourcenbasierten Skalierung geführt.

1. Wählen Sie im Menü **Einheiten** die Option **Automatische Skalierung** aus.
2. Wählen Sie **Gruppe für automatische Skalierung hinzufügen** aus.
3. Richten Sie eine Gruppe für die automatische Skalierung ein, indem Sie zuerst einen Wert für **Gruppenname** (z. B. 'Weekend Scale Up Group') eingeben und dann das Rechenzentrum auswählen.
4. Wählen Sie die Richtlinie für die Beendigung des Servers aus. Wenn Sie z. B. die Option für **Ältestes Datum** auswählen, dann wird der Server mit dem ältesten Bereitstellungsdatum beim Scale-down ausgewählt.
5. Geben Sie an, ob Ihre Gruppe eine Multi-VLAN-Skalierungsgruppe sein soll und wie die Auslastung bei einem Scale-down über die konfigurierten VLAN-Paare verteilt werden soll.
6. Wählen Sie die öffentlichen und privaten VLANs aus, auf denen Ihre Server bereitgestellt werden sollen. Wenn auf die Server über das öffentliche Internet zugegriffen werden soll (wenn das VLAN Web-Server ausführt), lassen Sie die Option **Nur privates Netz** inaktiviert.
7. Geben Sie für **Mindestanzahl der Mitglieder** den Wert '3' und für **Maximale Anzahl der Mitglieder** den Wert '6' an. Legen Sie für **Übergangszeitraum** den Wert '0' fest. Da Sie mit der zeitplanbasierten Skalierung arbeiten, werden keine Statistikdaten zur Auslösung der Skalierungsaktionen erfasst.

## Mitgliederkonfiguration für Ihre Gruppe definieren
{: #defining-member-configuration}

1. Suchen Sie die **Mitgliederkonfiguration** und geben Sie einen Wert für **Hostname** und **Domäne** für den Skalierungsserver ein. Nachfolgende Server, die zu der Gruppe hinzugefügt werden, verfügen über eindeutige Suffixe, die an den Hostnamen angefügt werden.
2. Geben Sie die Hardwarekonfiguration der Datenverarbeitungsinstanzen (Cores, RAM usw.) an. 
3. Wählen Sie ein Betriebssystem aus, wenn Sie das Mindestbetriebssystem installieren möchten. Sie können auch die Option **Öffentliches Image** oder **Privates Image** verwenden, um Ihre Instanzen bereitzustellen.
4. Wenn für die Instanzen weiterführende Schritte erforderlich sind, um zusätzliche Softwarekomponenten zu installieren, dann geben Sie die URL für ein **Nachinstallationsscript** an, um die Software zu installieren. (Wenn Sie eine Lastausgleichsfunktion für die Gruppe benutzen, dann werden die Nachinstallationsscripts ausgeführt, bevor ein Mitglied einer Lastausgleichsfunktion unterstellt wird.)

## Richtlinien einrichten
{: #setting-up-policies}

In dem Szenario verwendet die E-Commerce-Site die ressourcenbasierte Skalierung. Dazu werden zwei Richtlinien benötigt: Eine für eine relative Skalierungsaktion mit dem Wert '+3' für den erforderlichen Zeitrahmen und eine zweite für eine Absolutionsaktion mit dem Wert '3', wenn die Datenverkehrsspitze beendet ist. Die erste Richtlinie wird zum Hinzufügen von Ressourcen verwendet.

1. Blättern Sie abwärts zu **Richtlinien** und klicken Sie dann auf **Richtlinie hinzufügen**. Geben Sie einen Wert für **Richtlinienname** ('Weekday Scale Up') ein.
2. Wählen Sie unter **Übergangszeitraum** die Option für den Übergangszeitraum der Gruppe aus.
3. Klicken Sie auf **Auslöser hinzufügen** und geben Sie einen Wiederholungsauslöser an, indem Sie im ersten Dropdown-Menü **Jeden** auswählen, dann **Montag, Dienstag, Mittwoch, Donnerstag** und **Freitag** sowie in den nachfolgenden Dropdownfeldern **2:00 PM**\* hervorheben. (Im Kontrollkästchen **Erweiterte Bearbeitung** können Sie die Auslöserhäufigkeit in einer crontab-Notation angeben.)
4. Klicken Sie unter **Aktion** auf die Dropdown-Liste **Skalieren nach** und wählen Sie **Exakt** aus. Geben Sie im Feld **Mitglieder** den Wert '3' ein.
5. Klicken Sie erneut auf **Richtlinie hinzufügen**, um die zweite Richtlinie anzugeben, mit der die Server jeden Nachmittag entfernt werden. Der Übergangszeitraum stimmt mit dem Übergangszeitraum der Gruppe überein. Der Auslöser ist für jeden Montag, Dienstag, Mittwoch, Donnerstag und Freitag um 10:00 PM\* mit einer exakten Skalierungsaktion mit dem Wert '3' definiert. Die Zeit, die im Feld **Auslöser** eingegeben wird, basiert auf der UTC-Zeit. Deshalb müssen Sie für 9:00 AM Central Daylight Time den Wert 2:00 PM und für 5:00 PM Central Daylight Time den Wert 10:00 PM auswählen. Bei Verwendung der Central Standard Time (CST) müssten hingegen die Werte 1:00 PM und 9:00 PM angegeben werden, weil UTC/GMT die Sommerzeit nicht berücksichtigt. Einen Zeitumsetzer finden Sie auf der Website für den [World Time Server ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window}.
6. Richten Sie eine weitere Gruppe mit einem Übergangswert von '0' und dem Namen 'Traffic Burst Group' mit einer Mindestanzahl der Mitglieder von '0' und einer maximalen Anzahl von '5' ein. Verwenden Sie die gleichen Einstellungen für die Gruppen- und die Mitgliederkonfiguration, die auch für die Gruppe 'Weekday Scale Up' (außer Gruppenname) verwendet wird. 
7. Klicken Sie auf **Richtlinie hinzufügen**, um die zweite Richtlinie hinzuzufügen, die die beiden zusätzlichen Server steuert, wenn der öffentliche eingehende Datenverkehr auf allen virtuellen Servern für 10 Minuten durchschnittlich über 5 MB pro Sekunde liegt.
8. Geben Sie einen Wert für **Richtlinienname** ein, z. B. 'Traffic Burst Group'.
9. Wählen Sie unter **Übergangszeitraum** die Option für den Übergangszeitraum der Gruppe aus.
10. Klicken Sie auf **Auslöser hinzufügen**. Übernehmen sie im ersten Feld den Standardwert **Wenn mein** und wählen Sie im zweiten Feld **Eingehende Mb/s für öffentliches Netz** aus. Übernehmen Sie im dritten Feld das Standardzeichen (>). Geben Sie im vierten Feld den Wert **5** (5 MB) und im fünften Feld den Wert **600** ein und wählen Sie im letzten Feld **Sekunden** aus, um die Zeitdauer von 10 Minuten darzustellen.
11. Klicken Sie unter **Aktion** auf die Dropdown-Liste **Skalieren nach** und wählen Sie **Relativ** aus. Geben Sie im Feld **Mitglieder** den Wert '2' ein.
12. Klicken Sie erneut auf **Richtlinie hinzufügen**, um die zweite Richtlinie anzugeben, mit der die Server entfernt werden, wenn der Datenverkehr auf weniger als 5 Mbps\* abgenommen hat. Der Übergangszeitraum ist dann identisch mit dem Übergangszeitraum der Gruppe. Die Bedingung des Auslösers ist erfüllt, wenn der Wert für eingehende Mb/s für mein öffentliches Netz für einen Zeitraum von 600 Sekunden (10 Minuten) geringer als '5' (5 Mb/s) ist.

Wenn beide Gruppen erstellt werden, erstellt die Gruppe 'Weekday Scale Up' drei Server (Minimum). An Wochentagen werden um neun Uhr morgens (9:00 AM) Central Time drei weitere Server hinzugefügt und um fünf Uhr nachmittags (5:00 PM) Central Time werden diese Server wieder entfernt. Es gibt keine andere Möglichkeit zum Hinzufügen oder Entfernen der Mitglieder zur bzw. aus der Gruppe. In einer vollständig separaten Gruppe 'Traffic Burst Group' werden zwei Server für jeden Zeitraum von 10 Minuten hinzugefügt, in dem der eingehende öffentliche Datenverkehr für alle Mitglieder einen durchschnittlichen Wert von 5 MB pro Sekunde erreicht. Dieser Vorgang wird bis zum Gruppenmaximum '5' fortgesetzt. Bleibt der eingehende öffentliche Datenverkehr für einen Zeitraum von 10 Minuten unter diesem Wert, werden alle Server in dieser Gruppe entfernt.

