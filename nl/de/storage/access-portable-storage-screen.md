---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# Portierbaren Speicher verwalten
{: #accessing-portable-storage}

Portierbare Speicherdatenträger (Portable Storage Volumes; PSVs) stellen eine Zusatzspeicherlösung ausschließlich für {{site.data.keyword.virtualmachinesshort}} dar. In der {{site.data.keyword.cloud}}-Konsole können Sie auf portierbare Speicherdatenträger zugreifen und alle PSVs anzeigen. Die Datenträger können auch an- und abgehängt, ausgetauscht und bearbeitet werden.
{:shortdesc}

Das Anhängen oder Austauschen portierbarer Speicherdatenträger an eine bzw. in einer virtuellen Serverinstanz, die über eine verschlüsselte Imagevorlage bereitgestellt wurde, ist nicht möglich.
{:note}

## Vorbereitungen
Navigieren Sie zuerst zum Speicher- oder Einheitenmenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Tasks auszuführen.

* Navigieren Sie zum Speicher- oder Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen.

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Portierbaren Speicher anhängen

1. Wählen Sie im Menü **Speicher** die Option **Blockspeicher** aus.
2. Wählen Sie im Abschnitt **Portierbarer Speicher** die Option zum Anhängen des portierbaren Speichers aus, den Sie verwenden wollen.
3. Wählen Sie in der nächsten Anzeige die Einheit aus, für die der Speicher benötigt wird, und wählen Sie dann **Anhängen** aus.

## An einen Server angehängten portierbaren Speicher verwalten

An einen Server angehängter portierbarer Speicher wird auf der Seite *Einheitendetails* des Servers aufgelistet.

1. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus.
2. Wählen Sie in der **Einheitenliste** eine virtuelle Serverinstanz aus, um die zugehörigen Details anzuzeigen.
3. Klicken Sie auf die Registerkarte **Speicher**, um den portierbaren Speicher anzuzeigen, der momentan an die Instanz angehängt ist.
4. Im Menü **Aktionen** können Sie für den Speicher die Optionen **Tauschen** oder **Zuordnung aufheben** auswählen.
