---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Dedizierte Hostinstanz auf einen anderen Host migrieren
{: #migrating-dedicated-host}

Sie können Ihre dedizierten Hostinstanzen im selben POD von einem Host auf einen anderen migrieren. Wählen Sie die zu migrierende Instanz entweder auf der Seite 'Einheitendetails' des Hosts oder auf der Seite 'Einheitendetails' der Instanz aus. Dabei ist zu beachten, dass jeweils nur zwei Instanzen gleichzeitig migriert werden können. Die erforderliche Zeit hängt vom Datenträger ab. SAN-Datenträger können schneller migriert werden, da lokale Platten beim Migrieren kopiert werden müssen. Die zu migrierenden Instanzen werden für die Dauer der Migration offline geschaltet. Der Host bleibt online, damit die übrigen dedizierten Hostinstanzen verfügbar bleiben.
{:shortdesc}

Führen Sie die folgenden Schritte aus, um dedizierte Hostinstanzen über die Seite 'Einheitendetails' des *ursprünglichen dedizierten Hosts*auf einen anderen dedizierten Host in demselben POD zu migrieren.

1. Öffnen Sie das [{{site.data.keyword.slportal_full}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/), indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben.
2. Klicken Sie auf **Einheit > Einheitenliste** und wählen Sie entweder den Host oder die gehostete Instanz in der Liste aus.
3. Klicken Sie auf die Dropdown-Liste **Aktionen** neben der dedizierten Instanz, die Sie migrieren möchten.
4. Wählen Sie **Migrieren** aus und geben Sie den Host ein, auf den die Instanz migriert werden soll. Dabei ist zu beachten, dass sich der Zielhost im selben POD wie der Quellenhost befinden muss.
5. Klicken Sie auf die Schaltfläche **Migrieren**.

Die Migration wird sofort durchgeführt. Während der Migration wird die dedizierte Instanz offline geschaltet, bis sie sich auf dem neuen Host befindet. Sie können die Seite 'Einheitendetails' des Zielhosts aufrufen, um sicherzustellen, dass die Instanz ordnungsgemäß migriert wurde.

Führen Sie die folgenden Schritte aus, um dedizierte Hostinstanzen über die Seite 'Einheitendetails' der *dedizierten Hostinstanz* auf einen anderen dedizierten Host in demselben POD zu migrieren.

1. Öffnen Sie das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/), indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben.
2. Klicken Sie auf **Einheit > Einheitenliste** und wählen Sie in der Liste die gehostete Instanz aus, die migriert werden soll.
3. Klicken Sie auf den Link **Migrieren** rechts auf der Seite.
4. Wählen Sie den Zielhost aus, auf den die Instanz  migriert werden soll. Dabei ist zu beachten, dass sich der Zielhost im selben POD wie der Quellenhost befinden muss.
5. Klicken Sie auf die Schaltfläche **Migrieren**.

Die Migration wird sofort durchgeführt. Während der Migration wird die dedizierte Instanz offline geschaltet, bis sie sich auf dem neuen Host befindet. Sie können die Seite 'Einheitendetails' des Zielhosts aufrufen, um sicherzustellen, dass die Instanz ordnungsgemäß migriert wurde.

## Nächste Schritte
Vergewissern Sie sich nach dem Migrieren einer dedizierten Hostinstanz, dass die Migration erfolgreich durchgeführt wurde, indem Sie überprüfen, dass auf der Seite 'Einheitendetails' des neuen dedizierten Hosts ein grünes Symbol für den Status angezeigt wird.
