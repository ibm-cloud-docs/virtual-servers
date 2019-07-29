---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Bereitstellungsscripts verwalten
{: #managing-a-provisioning-script}

Mit Bereitstellungsscripts können Sie eine URL für ein Script angeben, das in einer neu bereitgestellten Einheit ausgeführt werden soll. Als Bereitstellungsscript kann jede Datei verwendet werden, die vom Betriebssystem ausgeführt werden kann (dazu gehören auch kombinierte Binärdateien und alle vom Betriebssystem unterstützten Sprachen). Es gibt keine Beschränkungen für den Scriptnamen; zur Identifizierung der Scripts ist es jedoch einfacher, wenn für die einzelnen Scripts ähnliche Namenskonventionen verwendet werden. Bereitstellungsscripts muss ein vollständig qualifizierter Domänenname zugeordnet werden und auf sie muss der Zugriff mithilfe des Protokolls HTTP oder HTTPS möglich sein. Der verwendete Protokolltyp hat Auswirkung auf die automatische Antwort des Systems, wenn das Bereitstellungsscript in die Einheit heruntergeladen wird.  
{:shortdesc}

* Bei Verwendung des **HTTP-Protokolls** ist ein Administrator erforderlich, der das Script nach dem Herunterladen manuell ausführt.
* Bei Verwendung des **HTTPS-Protokolls** wird das Script (falls möglich) automatisch heruntergeladen und installiert. Wenn die URL keinem gültigen Script zugeordnet ist, wird das Script heruntergeladen und es muss keine weitere Aktion ausgeführt werden.

## Vorbereitungen
Navigieren Sie zuerst zum Einheitenmenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Tasks auszuführen. 

* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen. 

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Bereitstellungsscript hinzufügen
{: #add-provisioning-script}

1. Wählen Sie im Menü **Einheiten** die Option **Verwalten > Bereitstellungsscripts** aus.
2. Wählen Sie **Bereitstellungsscript hinzufügen** aus. 
3. Geben Sie für das Bereitstellungsscript im Feld **Name** einen identifizierenden Namen ein.
4. Geben Sie im Feld **URL** den vollständig qualifizierten Domänennamen ein, der dem Script zugeordnet ist.
5. Klicken Sie auf **Hinzufügen**, um das Bereitstellungsscript zum Konto hinzuzufügen. 

## Details des Bereitstellungsscripts bearbeiten
{: #edit-provisioning-script-details}

1. Wählen Sie im Menü **Einheiten** die Option **Verwalten > Bereitstellungsscripts** aus.
2. Klicken Sie in der Spalte **Name** oder **URL** für das Bereitstellungsscript an einer beliebigen Stelle, um das Script zur Bearbeitung zu öffnen.
3. Aktualisieren Sie den Namen oder die URL.
   Beim Aktualisieren einer URL müssen Sie einen vollständig qualifizierten Domänennamen verwenden, sonst wird die Änderung nicht gespeichert.
   {:note}
4. Klicken Sie auf eine beliebige Stelle in der Anzeige, um die Bearbeitung zu speichern.

## Nächste Schritte

Bereitstellungsscripts, die einem Konto zugeordnet sind, können jederzeit geändert oder entfernt werden. Bereitstellungsscripts werden solange in der {{site.data.keyword.cloud_notm}}-Konsole gespeichert, bis sie entfernt werden, und sie können jeder neuen Einheit zugeordnet werden, die über die {{site.data.keyword.cloud_notm}}-Konsole bestellt wird. Wenn das Script einer HTTP-URL zugeordnet ist, wird es während der Bereitstellung auf die neue Einheit heruntergeladen und der Administrator muss sich bei der Einheit anmelden und das Script manuell ausführen. Scripts, denen HTTPS-URLs zugeordnet sind, werden heruntergeladen und, falls zutreffend, auf der neuen Einheit ausgeführt, ohne dass hierzu weitere Aktionen erforderlich sind. 

Wenn Sie ein Script bearbeiten, werden gültige Aktualisierungen sofort auf dem Bildschirm angezeigt. Änderungen, die an vorhandenen Bereitstellungsscripts vorgenommen werden, haben keine Auswirkung auf bereits bereitgestellte Einheiten.

