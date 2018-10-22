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

# Dedizierte Hosts und Instanzen verwalten
{: #managing-virtual-servers}

Auf der Seite 'Einheitendetails' können Sie Ihre dedizierten Hosts und Instanzen verwalten, Ihre Support-Tickets verfolgen und die Verfügbarkeit Ihres Hosts überwachen. Sie können Ihre dedizierten Hostinstanzen in der Einheitenliste auf zwei Arten aufrufen und anzeigen: als Teil des zugehörigen Hosts oder als einzelne Instanz.
{:shortdesc}

## Registerkarte für Hostkonfiguration
Auf der Registerkarte **Konfiguration** können Sie verschiedene Tasks für den dedizierten Host ausführen. Dazu gehört auch das Verwalten der dedizierten Hostinstanzen. Über das Dropdown-Menü 'Aktionen' können Sie den Host umbenennen oder abbrechen. Bevor ein Host abgebrochen werden kann, müssen zunächst alle zugeordneten dedizierten Hostinstanzen abgebrochen oder migriert werden. Andernfalls wird eine Fehlernachricht ausgegeben.

Anmerkungen zu einem Host und den zugehörigen Instanzen können verwaltet werden (z. B. 'Die Migration von myDallasHost auf myTorHost ist am XX/XX/XXXX geplant.'). In den Teilfenstern 'Allgemein', 'System' und 'Netz' der Seite finden Sie auf einen Blick Details zu dem Host. Beachten Sie, dass sich die Angaben im Teilfenster 'Speicher' auf die lokale Speicherkapazität beziehen.

Das Teilfenster 'Instanzen' enthält die Instanzen, die einem bestimmten Host zugeordnet sind, und bietet die Möglichkeit, Instanzen zu dem Host hinzuzufügen. Klicken Sie auf das Menü 'Aktionen' für eine Instanz, um die folgenden Aktionen für die betreffende Instanz auszuführen:

* Warmstart durchführen
* Ein- oder ausschalten
* Umbenennen
*	Prüfprotokolle anzeigen
*	Upgrade oder Downgrade durchführen
*	Abbrechen
*	Migrieren

## Registerkarte für Host-Tickets
Auf der Registerkarte 'Tickets' können Sie Support-Tickets für den Host und alle zugehörigen Instanzen öffnen, indem Sie auf 'Ticket öffnen' für diesen Link 'Einheit' klicken.

## Registerkarte für Hostzuordnungen
Auf der Registerkarte 'Zuordnungen' können Sie verfügbare Cores, Arbeitsspeicher und und lokalen Speicher für Ihren dedizierten Host anzeigen. Das blaue Segment im Kreisdiagramm gibt die genutzten Ressourcen an und das weiße Segment die verfügbaren Ressourcen.

## Registerkarte für dedizierte Hostinstanzen
Die Seite 'Einheitendetails' für dedizierte Hostinstanzen kann entweder über die Seite 'Einheitendetails des zugehörigen Hosts oder direkt über die Einheitenliste aufgerufen werden. Für dedizierte Hostinstanzen stehen weitere Registerkarten zur Verfügung; die Registerkarten 'Konfiguration' und 'Tickets' ähneln den Registerkarten auf der Hostebene. Über den Link 'Einheitenkonfiguration ändern' auf der Registerkarte 'Konfiguration' können Sie Änderungen an Ihrem System (z. B. Core, Arbeitsspeicher und lokaler Speicher) und an Ihrer Netzkonfiguration (Bandbreite und Uplink-Port-Geschwindigkeiten) vornehmen.

Für die Nutzung wird ein Zeitdiagramm angezeigt, das die CPU-Auslastung nach Datum darstellt. Das Diagramm bietet auch die Möglichkeit, die CPU-Auslastung für ein bestimmtes Datum bzw. eine bestimmte Uhrzeit anzuzeigen. Dies erleichtert Ihnen die Entscheidung, ob zusätzliche Verarbeitungskapazität bereitgestellt werden sollte.

Für die Bandbreite wird ebenfalls ein Zeitdiagramm dargestellt. In diesem Diagramm können Sie Parameter eingeben, um zu ermitteln, welcher Anteil der Bandbreite im Zeitverlauf genutzt wird. Auf der Registerkarte 'Speicher' wird der zusätzliche Block- oder Dateispeicher für die Instanz angezeigt.

# Dedizierten Host abbrechen
Sie können einen dedizierten Host jederzeit abbrechen. Bevor ein Host abgebrochen werden kann, müssen die dem Host zugeordneten dedizierten Instanzen entweder auf einen anderen dedizierten Host migriert oder ebenfalls abgebrochen werden. 
## Dedizierten Host über die Einheitenliste abbrechen
Führen Sie die folgenden Schritte aus, um einen dedizierten Host über die Einheitenliste abzubrechen.

1. Wählen Sie **Einheit** > **Einheitenliste** aus.
2. Suchen Sie den dedizierten Host, den Sie abbrechen möchten, und klicken Sie auf das Dropdown-Menü **Aktionen**.
3. Wählen Sie **Host abbrechen** aus. 
4. Ein Popup-Fenster mit mit einer Liste der dedizierten Instanzen, die dem Host zugeordnet sind, wird angezeigt. Sie müssen die Instanzen entweder migrieren oder abbrechen (falls nicht bereits geschehen), bevor Sie den Host abbrechen. Klicken Sie auf **OK**.

Eine Nachricht weist darauf hin, dass der dedizierte Host abgebrochen wird. Ein Link für das Support-Ticket zum Abbrechen des Hosts wird angezeigt.
## Dedizierten Host über die Seite 'Einheitendetails' abbrechen
Führen Sie die folgenden Schritte aus, um den dedizierten Host über die Seite 'Einheitendetails' abzubrechen.

1. Wählen Sie **Einheit** > **Einheitenliste** aus.
2. Suchen Sie den dedizierten Host, den Sie abbrechen möchten, und doppelklicken Sie auf den Host.
3. Stellen Sie sicher, dass alle dedizierten Instanzen, die dem dedizierten Host zugeordnet sind entweder migriert oder abgebrochen wurden.
4. Klicken Sie auf das Dropdown-Menü **Aktionen** und wählen Sie **Host abbrechen** aus.

Eine Nachricht weist darauf hin, dass der dedizierte Host abgebrochen wird. Ein Link für das Support-Ticket zum Abbrechen des Hosts wird angezeigt.

### Dedizierte Instanz abbrechen

Bevor Sie einen dedizierten host abbrechen können, müssen die dedizierten Instanzen abgebrochen werden, die dem Host zugeordnet sind. Dedizierte Instanzen können direkt über die Einheitenliste, die Seite 'Einheitendetails' des zugehörigen Hosts oder über die Seite 'Einheitendetails' der jeweiligen dedizierten Instanz abgebrochen werden. 

1. Wählen Sie die dedizierte Instanz aus, die Sie abbrechen möchten, und klicken Sie auf das Dropdown-Menü **Aktionen**.
2. Wählen Sie **Einheit abbrechen** aus.
3. Ein Warnhinweis wird angezeigt. Klicken Sie auf das Dropdown-Menü **Ursache**, wählen Sie den Grund für das Abbrechen der dedizierten Instanz aus und klicken Sie auf **Weiter**.

Eine Nachricht weist darauf hin, dass die dedizierte Instanz abgebrochen wird. Ein Link für das Support-Ticket zum Abbrechen der dedizierten Instanz wird angezeigt.

