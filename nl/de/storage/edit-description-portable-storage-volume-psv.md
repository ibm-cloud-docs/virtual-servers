---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Beschreibung für portierbaren Speicher bearbeiten
{: #editing-a-portable-storage-description}

Sie können portierbare Speicherdatenträger (Portable Storage Volumes; PSVs) in der {{site.data.keyword.cloud}}-Konsole anzeigen. Auf der Seite für portierbaren Speicher werden die Beschreibung, die Position und die Kapazität des PSV sowie der Einheitenname angezeigt, dem der PSV zugeordnet ist. Sie können die Beschreibung jederzeit aktualisieren. Aktualisieren Sie die Beschreibungen portierbarer Speicherdatenträger mithilfe einer eindeutigen Kennung, die Bezug zur Verwendung des Speicherdatenträgers hat.
{:shortdesc}

## Vorbereitungen
Navigieren Sie zuerst zum Speichermenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Task auszuführen.

* Navigieren Sie zum Speichermenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen.

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Beschreibung für portierbaren Speicher bearbeiten

1. Wählen Sie im Menü **Speicher** die Option **Blockspeicher** aus.
2. Suchen Sie im Abschnitt **Portierbarer Speicher** den portierbaren Speicherdatenträger, der bearbeitet werden soll. Verwenden Sie das Tool zum **Filtern des portierbaren Speichers**, um einen Datenträger schnell zu finden.
3. Klicken Sie auf den Abschnitt **Beschreibung** für den portierbaren Speicherdatenträger, um die Beschreibung zum Bearbeiten zu öffnen.
4. Geben Sie den Inhalt im Feld **Beschreibung** ein bzw. überarbeiten Sie ihn, je nach Bedarf.
5. Klicken Sie auf eine beliebige Stelle in der Zeile, die den PSV enthält, um die bearbeitete Beschreibung zu speichern.

## Nächste Schritte

Nach dem Bearbeiten der Beschreibung für einen PSV verbleibt dieser an seiner ursprünglichen Position in der Liste, bis Sie die Seite für portierbaren Speicher verlassen. Wenn Sie die Seite erneut öffnen, wird der PSV basierend auf der alphabetischen Reihenfolge der Beschreibung an einer neuen Position angezeigt. Wenn Sie den PSV nach dem erneuten Starten der Anzeige in dieser Liste nicht finden können, halten Sie die Taste **STRG** gedrückt und klicken Sie auf die Schaltfläche zum **Aktualisieren**, um den Browser-Cache zu löschen und versuchen Sie es erneut. Die Beschreibung kann durch Wiederholung der oben genannten Schritte jederzeit erneut geändert werden.
