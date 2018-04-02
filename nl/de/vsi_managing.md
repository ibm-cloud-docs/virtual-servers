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


# Virtuelle Server verwalten
{: #managing-virtual-servers}

Mithilfe der Einheitenliste können Sie virtuelle Server und andere Einheiten wie Bare-Metal-Server und WLAN-Firewalls verwalten.
{:shortdesc}

Für virtuelle Server wird in der Einheitenliste der Einheitentyp *Virtuell* angegeben. Für Bare-Metal-Server wird der Einheitentyp *Server* angegeben. Für dedizierte Hosts wird der Einheitentyp *Dedizierter virtueller Host* angegeben. Viele der verfügbaren Interaktionen sind für alle Einheitentypen gleich, aber jeder Einheitentyp verfügt außerdem über einheitenspezifische Interaktionen.

In der Einheitenliste sind die folgenden Verwaltungstasks für virtuelle Server verfügbar:
* Warmstart -  Die Einheit sofort ausschalten und anschließend wieder einschalten.
* Ein-/ausschalten - Die Einheit über Fernzugriff ein- oder ausschalten.
* Umbenennen - Einen Eineitennamen ändern oder aktualisieren.
* Abbrechen - Die Verwendung einer Einheit beenden. Die Verwendung von Einheiten kann sofort oder an einem Rechnungsstichtag abgebrochen werden. Nach dem Bestätigen des Abbruchs Ihrer Einheit kann die Aktion nicht rückgängig gemacht werden. Beim sofortigen Abbrechen wird keine Rückerstattung von Gebühren gewährt.

Führen Sie die folgenden Schritte aus, um Verwaltungstasks für Ihre virtuellen Server über die Einheitenliste im Kundenportal auszuführen:  
1. Melden Sie sich beim [{{site.data.keyword.slportal_full}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an. 
2. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus.
3. Klicken Sie auf **Aktionen** für die Einheit, die Sie verwalten möchten, und wählen Sie die gewünschte Verwaltungstask aus.

**Tipps:** 
* Für die Interaktion mit Servern im {{site.data.keyword.slportal}} können Sie sowohl die Snapshot-Ansicht (eine Zusammenfassung für Ihre Einheit) als auch die Anzeige der Einheitendetails (eine ausführliche Liste) verwenden. Klicken Sie zum Anzeigen von oder Interagieren mit Ihrem Server in der Snapshot-Ansicht auf den Pfeil neben dem Einheitennamen, um die Ansicht zu erweitern. Klicken Sie zum Anzeigen von oder Interagieren mit Ihrem Server in der Ansicht 'Einheitendetails' auf den Einheitennamen des Servers.
* Sie können über die Registerkarte **Konfiguration** jederzeit Anmerkungen zu einer Einheit hinzufügen. Anmerkungen können beim Ermitteln von Details der Einheit, ihrer Verwendung und der für sie ausgeführten Aktionen helfen.

## Weitere Schritte
* **Warmstart durchführen**

    Ein Warmstart ist eine der grundlegendsten Einheitenaktionen. Der Warmstart einer Einheit führt zum sofortigen Ausschalten und dann Wiedereinschalten Ihrer Einheit und wird aus zahlreichen Gründen durchgeführt, wobei es sich häufig um für die Einheit oder die Geschäftsanforderungen des einzelnen Benutzers spezifische Gründe handelt. Warmstarts von Einheiten können sowohl aus der Einheitenliste als auch aus der Einheitenansicht einer einzelnen Einheit ausgeführt werden. Für virtuelle Server kann jederzeit ein Warmstart durchgeführt werden.  

* **Ein-/ausschalten**

    Wenn die Einheit ausgeschaltet wird, bleibt sie im Status 'ausgeschaltet' und muss durch Wiederholung der oben beschriebenen Schritte manuell eingeschaltet werden. Benutzer können nicht mit einer Einheit interagieren, wenn sie ausgeschaltet ist. Sobald die Einheit eingeschaltet wurde, kann normale Interaktion stattfinden. Sie bleibt eingeschaltet, bis weitere Aktionen unternommen werden.

* **Umbenennen**

  Nach dem Umbenennen der Einheit wird der Name im {{site.data.keyword.slportal}} automatisch aktualisiert. Verwenden Sie beim Durchführen einer Suche im {{site.data.keyword.slportal}} den neuen Einheitennamen, wenn Sie nach zur Einheit zugehörigem Inhalt suchen. Wiederholen Sie die oben genannten Schritte, um die Einheit zu einem beliebigen Zeitpunkt erneut umzubenennen.

* **Abbrechen**

  Nach dem Bestätigen des Abbruchs beginnt der Abbruchprozess für die Einheit. Falls ein sofortiger Abbruch angefordert wurde, wird die Einheit sofort abgebrochen. Falls ein Abbruch am Rechnungsstichtag angefordert wurde, bleibt die Einheit bis zum nächsten Rechnungsstichtag aktiv. Nach ihrem Abbruch wird die Einheit nicht mehr in der Einheitenliste im {{site.data.keyword.slportal}} angezeigt. Rechnungspositionen werden ebenfalls aus Rechnungen entfernt, wenn alle ggf. ausstehenden Posten für die Einheit bezahlt wurden. Falls Sie Fragen zu einer Rechnung für eine abgebrochene Einheit haben, öffnen Sie ein Ticket und wählen Sie als Ticketthema 'Abrechnungsanforderung' aus. Beim sofortigen Abbrechen wird keine Rückerstattung von Gebühren gewährt.
  
## Nächste Schritte
Weitere Informationen zum erneuten Konfigurieren eines vorhanden virtuellen Servers finden Sie unter [Vorhandenen virtuellen Server neu konfigurieren](../vsi/vsi_reconfigure.html).

