---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Datenverkehrsspitzen mit der zeitplanbasierten automatischen Skalierung verwalten
{: #managing-schedule-based-auto-scaling}

Webdatenverkehrsspitzen können sich positiv oder auch negativ auswirken. Solche Lastspitzen bedeuten einerseits, dass mehr Personen Ihre Site nutzen. Andererseits verursachen sie jedoch eine Bedarfsspitze auf Ihrem System, die sich negativ auf Ihre Antwortzeiten auswirken kann. Das Feature für die automatische Skalierung von {{site.data.keyword.cloud}} bietet Ihnen die Möglichkeit, für Ihre Server automatisch ein Scale-up oder Scale-down durchzuführen, um so eine Anpassung Ihrer Systemleistung an die geltenden Geschäftsanforderungen vorzunehmen. Mit der zeitplanbasierten automatischen Skalierung können Sie diese Datenverkehrsspitzen kontrollieren.
{:shortdesc}

## Vorbereitungen
Navigieren Sie zuerst zum Einheitenmenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Tasks auszuführen.

* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Wenn Sie kein Kontoadministrator sind, muss Ihr Benutzerkonto über die Berechtigung zur Nutzung der automatischen Skalierung verfügen. Weitere Informationen zum Aktualisieren von Berechtigungen für die Nutzung der automatischen Skalierung finden Sie im Abschnitt zum [Einrichten von Benutzerberechtigungen für die automatische Skalierung](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen. 

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Gruppe für automatische Skalierung hinzufügen
{: #add-auto-scale-group}

In diesem Szenario kommt es während der Wochenenden auf einer Social Media-Website in Dallas, Texas, zu Lastspitzen. Zwischen Montag und Freitag werden auf der Site mindestens zwei virtuelle Server benötigt. An den Wochenenden werden allerdings zwei weitere virtuelle Server benötigt, um den erhöhten an diesen Tagen vermehrten Datenverkehr abzufangen. In den folgenden Schritten werden Sie durch die Einrichtung der automatischen Skalierung zur Unterstützung der zeitplanbasierten Skalierung geführt.

1. Wählen Sie im Menü **Einheiten** die Option **Automatische Skalierung** aus.
2. Wählen Sie **Gruppe für automatische Skalierung hinzufügen** aus.
3. Richten Sie eine Gruppe für die automatische Skalierung ein, indem Sie zuerst einen Wert für **Gruppenname** (z. B. 'Weekend Scale Up Group') eingeben und dann das Rechenzentrum auswählen.
4. Wählen Sie die Richtlinie für die Beendigung des Servers aus. Wenn Sie z. B. die Option für **Ältestes Datum** auswählen, dann wird der Server mit dem ältesten Bereitstellungsdatum beim Scale-down ausgewählt.
5. Geben Sie an, ob Ihre Gruppe eine Multi-VLAN-Skalierungsgruppe sein soll und wie die Auslastung bei einem Scale-down über die konfigurierten VLAN-Paare verteilt werden soll.
6. Wählen Sie die öffentlichen und privaten VLANs aus, auf denen Ihre Server bereitgestellt werden sollen. Wenn auf die Server über das öffentliche Internet zugegriffen werden soll (wenn das VLAN Web-Server ausführt), lassen Sie die Option **Nur privates Netz** inaktiviert.
7. Geben Sie für **Mindestanzahl der Mitglieder** den Wert '2' und für **Maximale Anzahl der Mitglieder** den Wert '4' an. Legen Sie für **Übergangszeitraum** den Wert '0' fest. Da Sie mit der zeitplanbasierten Skalierung arbeiten, werden keine Statistikdaten zur Auslösung der Skalierungsaktionen erfasst.

## Mitgliederkonfiguration für Ihre Gruppe definieren
{: #define-member-configuration}

1. Suchen Sie die **Mitgliederkonfiguration** und geben Sie einen Wert für **Hostname** und **Domäne** für den Skalierungsserver ein. Nachfolgende Server, die zu der Gruppe hinzugefügt werden, verfügen über eindeutige Suffixe, die an den Hostnamen angefügt werden.
2. Geben Sie die Hardwarekonfiguration der Datenverarbeitungsinstanzen (Cores, RAM usw.) an. 
3. Wählen Sie ein Betriebssystem aus, wenn Sie das Mindestbetriebssystem installieren möchten. Sie können auch ein öffentliches Image oder ein privates Image verwenden, um Ihre Instanzen bereitzustellen.
4. Wenn für die Instanzen weiterführende Schritte erforderlich sind, um zusätzliche Softwarekomponenten zu installieren, dann geben Sie die URL für ein Nachinstallationsscript an, um die Software zu installieren. (Wenn Sie eine Lastausgleichsfunktion für die Gruppe benutzen, dann werden die Nachinstallationsscripts ausgeführt, bevor ein Mitglied einer Lastausgleichsfunktion unterstellt wird.)

## Richtlinien einrichten
{: #set-up-policies}

In diesem Szenario wird auf der Social Media-Website die zeitplanbasierte Skalierung verwendet. Es sind zwei Richtlinien erforderlich: eine, um für die Server am Freitagnachmittag ein Scale-up durchzuführen, und eine zweite, um am Sonntagabend für die Server ein Scale-down durchzuführen. Die erste Richtlinie wird zum Durchführen eines Scale-ups für die Server verwendet.

1. Suchen Sie die **Richtlinien** und klicken Sie dann auf **Richtlinie hinzufügen**. Geben Sie einen Wert für **Richtlinienname** ('Friday Scale Up') ein.
2. Wählen Sie unter **Übergangszeitraum** die Option für den Übergangszeitraum der Gruppe aus.
3. Klicken Sie auf **Auslöser hinzufügen** und geben Sie einen Wiederholungsauslöser an, indem Sie im ersten Dropdown-Menü **Jeden** und dann **Freitag** sowie in den nachfolgenden Dropdown-Menüs **10:00 PM**\* auswählen. (Im Kontrollkästchen **Erweiterte Bearbeitung** können Sie die Auslöserhäufigkeit in einer crontab-Notation angeben.)
4. Klicken Sie unter **Aktion** auf die Dropdown-Liste **Skalieren nach** und wählen Sie **Relativ** aus. Geben Sie im Feld **Mitglieder** den Wert '2' ein.
5. Klicken Sie erneut auf **Richtlinie hinzufügen**, um die zweite Richtlinie anzugeben, mit der für die Server am Sonntagabend ein Scale-down durchgeführt wird. Der Übergangszeitraum stimmt mit dem Übergangszeitraum der Gruppe überein. Der Auslöser tritt jeden Sonntag um 1:00 Uhr morgens (1:00 AM*) mit einer relativen Skalierungsaktion mit dem Wert '-2' auf.
6. Die Zeit, die im Feld **Auslöser** eingegeben wird, basiert auf der UTC-Zeit. Deshalb müssen Sie für 5:00 PM Central Daylight Time den Wert 10:00 PM und für 8:00 PM Central Daylight Time den Wert 1:00 AM auswählen. Bei Verwendung der Central Standard Time (CST) müssten hingegen die Werte 9:00 AM und 12:00 AM angegeben werden, weil UTC/GMT die Sommerzeit nicht berücksichtigt. Einen Zeitumsetzer finden Sie auf der Website für den [World Time Server ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window}.

## Lokale Lastausgleichsfunktion hinzufügen

Wenn Sie eine lokale Lastausgleichsfunktion eingerichtet haben, können Sie sie zum Lastausgleich Ihrer Gruppe für die automatische Skalierung verwenden.

1. Suchen Sie **Lokale Lastausgleichsfunktionen** und klicken Sie dann auf **Lastausgleichsfunktion hinzufügen**.
2. Klicken Sie auf **VIP-Einstellungen anzeigen** (öffnet eine separate Seite), um die für Ihr Konto verfügbaren lokalen Lastausgleichsfunktionen anzuzeigen und bei Bedarf neue zu bestellen. Eine Lastausgleichsfunktion muss über eine zugeordnete Servicegruppe verfügen, die mit einer Gruppe für die automatische Skalierung verwendet werden kann. Vergewissern Sie sich, dass sich die Lastausgleichsfunktion im Rechenzentrum Ihrer Gruppe für die automatische Skalierung befindet.
3. Klicken Sie auf der Seite **Gruppe für die automatische Skalierung hinzufügen** auf **Lastausgleichsfunktion hinzufügen**, klicken Sie dann auf den Dropdown-Pfeil für die virtuelle IP und wählen Sie Ihre Lastausgleichsfunktion aus.
4. Klicken Sie auf die Dropdown-Pfeile für **Servicegruppe**, **Service-Port** und **Typ der Statusprüfung für Service** und wählen Sie dann die entsprechenden Werte aus.
5. Klicken Sie auf **Gruppe hinzufügen**, um Ihre Gruppe zu speichern.
6. Nachdem alle Rechenzentren, Netze und sonstigen Komponenten korrekt angegeben wurden, wird Ihre Gruppe für die automatische Skalierung erstellt. Klicken Sie in der Anzeige **Alle Gruppen anzeigen** auf die gewünschte Gruppe, um die Gruppendetails anzuzeigen.

Das Einrichten einer zeitplanbasierten Skalierung führt dazu, dass zwei Mitglieder automatisch bereitgestellt werden, um die Mindestanforderungen der Website zu erfüllen. Immer am Freitag um 17:00 Uhr (5:00 PM) Central Time werden zwei weitere Mitglieder automatisch bereitgestellt, sobald der Auslöser der ersten Richtlinie angewendet wird. Sonntags um 20:00 Uhr (8:00 PM) Central Time werden diese beiden Mitglieder in Übereinstimmung mit dem Auslöser der zweiten Richtlinie wieder freigegeben. Wenn Sie eine Lastausgleichsfunktion angeben, werden alle Mitglieder, die entweder zum Erstellungszeitpunkt oder am Freitag erstellt wurden, der Lastausgleichsfunktion unterstellt, nachdem das angepasste Nachinstallationsscript ausgeführt wurde.
