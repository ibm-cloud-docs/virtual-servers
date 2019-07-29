---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-29"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Portgeschwindigkeit verringern
{: #downgrading-port-speeds}

Sie können die Portgeschwindigkeiten für Ihre virtuelle Serverinstanz temporär verringern (ein Downgrade durchführen), ohne ein Ticket zu öffnen. Sie können nur soweit die Geschwindigkeit verringern, die Verbindung trennen oder die Verbindung wiederherstellen, wie Sie bereits bezahlen. Sie können mit dieser Option keine Erhöhung durchführen. Die Änderungen bleiben in der Konsole erhalten, bis Sie sie wieder ändern. Hieraus ergibt sich keine geänderte Rechnungsstellung, und das temporäre Downgrading Ihres Servers verringert nicht Ihren Rechnungsbetrag. Wenn Sie Ihre Portgeschwindigkeit permanent ändern möchten, müssen Sie ein Vertriebsticket öffnen.
{:shortdesc}

## Vorbereitungen
Navigieren Sie zuerst zum Einheitenmenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Task auszuführen. 

* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen. 

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Portgeschwindigkeit verringern
Führen Sie die folgenden Schritte aus, um die Portgeschwindigkeiten mit einem Downgrade zu verringern.

1. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus.
2. Wählen Sie den zu aktualisierenden Server aus.
3. Rufen Sie auf der Registerkarte **Übersicht** die Option **Netzdetails** auf.
4. Wählen Sie das Dropdown-Menü in **Geschwindigkeit** (entweder für ein öffentliches oder ein privates Netz) aus, um die Portgeschwindigkeit mit einem Downgrade zu verringern oder die Verbindung zu trennen.

Wenn Sie aus irgendeinem Grund Portgeschwindigkeiten ändern oder Ihre Portverbindungen trennen, müssen Sie manuell den Server ändern.
{:tip}
