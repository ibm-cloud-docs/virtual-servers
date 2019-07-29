---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Virtuelle Server verwalten
{: #managing-virtual-servers}

Sie können virtuelle Server zusammen mit anderen Einheiten über die Liste mit den Einheitendetails verwalten.
{:shortdesc}


## Vorbereitungen
Navigieren Sie zuerst zum Einheitenmenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Tasks auszuführen.

* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen.

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Einheitentypen
In der Liste mit den Einheitendetails werden die folgenden Einheitentypen angezeigt:

| Einheit  | Einheitentyp  |
| ------  | ------------ | 
| Virtuelle Server | Virtuell |
| Bare Metal Server | Server |
| Dedizierte Hosts | Dedizierter virtueller Host | 
{: caption="Tabelle 1. Einheitentypen" caption-side="top"}

Welche Aktionen für Sie angezeigt werden, hängt vom Einheitentyp und von den Berechtigungen ab, die Ihrem Benutzerkonto erteilt wurden.

Führen Sie die folgenden Schritte aus, um Verwaltungstasks für Ihre virtuellen Server auszuführen.

1. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus.
2. Klicken Sie für die Einheit, die Sie verwalten möchten, auf **Aktionen** und wählen Sie die gewünschte Task aus.

* Für die Interaktion mit Servern in der {{site.data.keyword.cloud_notm}}-Konsole können Sie sowohl die Snapshot-Ansicht (eine Zusammenfassung für Ihre Einheit) als auch die Seite mit den Einheitendetails (eine ausführliche Liste) verwenden. Klicken Sie zum Anzeigen der Daten und zum Interagieren mit Ihrem Server in der Snapshot-Ansicht auf den Pfeil neben dem Einheitennamen, um die Ansicht zu erweitern. Klicken Sie zum Anzeigen der Daten und zum Interagieren mit Ihrem Server auf der Seite mit den Einheitendetails auf den Einheitennamen des Servers.

* Sie können über die Registerkarte **Konfiguration** jederzeit Anmerkungen zu einer Einheit hinzufügen. Anmerkungen können beim Ermitteln von Details der Einheit, ihrer Verwendung und der für sie ausgeführten Aktionen helfen.
 {:tip}

## Warmstart durchführen
Ein Warmstart ist eine der grundlegendsten Einheitenaktionen. Der Warmstart einer Einheit führt zum sofortigen Ausschalten und dann Wiedereinschalten Ihrer Einheit und wird aus zahlreichen Gründen durchgeführt, wobei es sich häufig um für die Einheit oder die Geschäftsanforderungen des einzelnen Benutzers spezifische Gründe handelt. Warmstarts von Einheiten können sowohl aus der Einheitenliste als auch aus der Einheitenansicht einer einzelnen Einheit ausgeführt werden. Für virtuelle Server kann jederzeit ein Warmstart durchgeführt werden.

Ein Warmstart ist sehr hilfreich, wenn ein Problem auftritt, bei dem der Server aufgrund eines Konfigurationsfehlers nicht ins Betriebssystem gebootet werden kann. Der Bootvorgang kann auch in den Rescue-Kernel ausgeführt werden. Nach dem Booten in den Rescue-Kernel können Sie die Laufwerke Ihres Servers anhängen und anschließend das Konfigurationsproblem beheben. Nachdem Sie das Problem behoben haben, können Sie für den Server über die Befehlszeile einen Warmstart durchführen. Daraufhin wird der Server in den Standardkernel Ihres Servers gebootet.
{:tip}

## Ein-/ausschalten
Wenn die Einheit ausgeschaltet wird, bleibt sie im Status 'ausgeschaltet' und muss durch Wiederholung der oben beschriebenen Schritte manuell eingeschaltet werden. Benutzer können nicht mit einer Einheit interagieren, wenn sie ausgeschaltet ist. Wenn der virtuelle Server das Feature für das Aussetzen der Abrechnung unterstützt, wird die Abrechnung für einige Rechenressourcen ausgesetzt. Sie können in einer Instanz erst wieder alle Verwaltungsaktionen ausführen, wenn die Abrechnung wiederaufgenommen wird. Weitere Informationen finden Sie in [Abrechnung aussetzen](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing). Informationen darüber, ob die virtuelle Serverinstanz das Feature für das Aussetzen der Abrechnung unterstützt, finden Sie in [Feature für das Aussetzen der Abrechnung anzeigen](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature#viewing-suspend-billing-feature). Sobald die Einheit eingeschaltet wurde, kann normale Interaktion stattfinden. Sie bleibt eingeschaltet, bis weitere Aktionen unternommen werden.

## Umbenennen
Nach dem Umbenennen der Einheit wird der Name in der {{site.data.keyword.cloud_notm}}-Konsole automatisch aktualisiert. Verwenden Sie beim Durchführen einer Suche in der {{site.data.keyword.cloud_notm}}-Konsole den neuen Einheitennamen, wenn Sie nach zur Einheit zugehörigem Inhalt suchen. Wiederholen Sie die oben genannten Schritte, um die Einheit zu einem beliebigen Zeitpunkt erneut umzubenennen.

## Abbrechen
Wenn Sie die Ausführung einer Einheit abbrechen, dann beenden Sie die Nutzung der betreffenden Einheit. Die Verwendung von Einheiten kann sofort oder an einem Rechnungsstichtag abgebrochen werden. Nach dem Bestätigen des Abbruchs Ihrer Einheit kann die Aktion nicht rückgängig gemacht werden. Beim sofortigen Abbrechen wird keine Rückerstattung von Gebühren gewährt.

Nach dem Bestätigen des Abbruchs beginnt der Abbruchprozess für die Einheit. Falls ein sofortiger Abbruch angefordert wurde, wird die Einheit sofort abgebrochen. Falls ein Abbruch am Rechnungsstichtag angefordert wurde, bleibt die Einheit bis zum nächsten Rechnungsstichtag aktiv. Nach ihrem Abbruch wird die Einheit nicht mehr in der Einheitenliste in der {{site.data.keyword.cloud_notm}}-Konsole angezeigt. Rechnungspositionen werden ebenfalls aus Rechnungen entfernt, wenn alle ggf. ausstehenden Posten für die Einheit bezahlt wurden. Falls Sie Fragen zu einer Rechnung für eine abgebrochene Einheit haben, öffnen Sie ein Ticket und wählen Sie als Ticketthema 'Abrechnungsanforderung' aus. Beim sofortigen Abbrechen wird keine Rückerstattung von Gebühren gewährt.

## Nächste Schritte
Weitere Informationen zum erneuten Konfigurieren eines vorhanden virtuellen Servers finden Sie unter [Vorhandenen virtuellen Server neu konfigurieren](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).
