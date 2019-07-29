---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Dedizierte Hostinstanz auf einen anderen Host migrieren
{: #migrating-dedicated-host}

Sie können Ihre dedizierten Hostinstanzen im selben POD von einem Host auf einen anderen migrieren. Wählen Sie die zu migrierende Instanz entweder auf der Seite mit den Einheitendetails des Hosts oder auf der Seite mit den Einheitendetails der Instanz aus. Dabei ist zu beachten, dass jeweils nur zwei Instanzen gleichzeitig migriert werden können. Die erforderliche Zeit hängt vom Datenträger ab. SAN-Datenträger können schneller migriert werden, da lokale Platten beim Migrieren kopiert werden müssen. Die zu migrierenden Instanzen werden für die Dauer der Migration offline geschaltet. Der Host bleibt online, damit die übrigen dedizierten Hostinstanzen verfügbar bleiben.
{:shortdesc}

## Vorbereitungen
Navigieren Sie zuerst zum Einheitenmenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Tasks auszuführen.

* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen.

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Migration über den dedizierten Host ausführen
Führen Sie die folgenden Schritte aus, um dedizierte Hostinstanzen über die Seite mit den Einheitendetails des *ursprünglichen dedizierten Hosts* auf einen anderen dedizierten Host in demselben POD zu migrieren. 

1. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus.
2. Wählen Sie in der Liste entweder den Host oder die gehostete Instanz aus.
3. Klicken Sie auf die Dropdown-Liste **Aktionen** neben der dedizierten Instanz, die Sie migrieren möchten.
4. Wählen Sie **Migrieren** aus und geben Sie den Host ein, auf den die Instanz migriert werden soll. Dabei ist zu beachten, dass sich der Zielhost im selben POD wie der Quellenhost befinden muss.
5. Klicken Sie auf **Migrieren**, um mit der Migration zu beginnen. 

Die Migration beginnt sofort. Während der Migration wird die dedizierte Instanz offline geschaltet, bis sie sich auf dem neuen Host befindet. Sie können die Seite 'Einheitendetails' des Zielhosts aufrufen, um sicherzustellen, dass die Instanz ordnungsgemäß migriert wurde.

## Migration über die dedizierte Instanz ausführen
Führen Sie die folgenden Schritte aus, um dedizierte Hostinstanzen über die Seite mit den Einheitendetails der *dedizierten Hostinstanz* auf einen anderen dedizierten Host in demselben POD zu migrieren.

1. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus.
2. Wählen Sie in der Liste die gehostete Instanz aus, die migriert werden soll.
3. Klicken Sie auf **Migrieren**.
4. Wählen Sie den Zielhost aus, auf den die Instanz  migriert werden soll. Dabei ist zu beachten, dass sich der Zielhost im selben POD wie der Quellenhost befinden muss.
5. Klicken Sie auf **Migrieren**, um mit der Migration zu beginnen.

Die Migration beginnt sofort. Während der Migration wird die dedizierte Instanz offline geschaltet, bis sie sich auf dem neuen Host befindet. Sie können die Seite mit den Einheitendetails des Zielhosts aufrufen, um sicherzustellen, dass die Instanz ordnungsgemäß migriert wurde.

## Nächste Schritte
Vergewissern Sie sich nach dem Migrieren einer dedizierten Hostinstanz, dass die Migration erfolgreich durchgeführt wurde, indem Sie überprüfen, dass auf der Seite mit den Einheitendetails des neuen dedizierten Hosts ein grünes Symbol für den Status angezeigt wird.

