---



copyright:
  years: 2014, 2018
lastupdated: "2018-02-09"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Einheit aus dem Ersatzpool reaktivieren 
{: #reactivating-spare-pools}

Wenn eine Einheit dem Ersatzpool hinzugefügt wird, ändert sich ihr Status in der Einheitenliste von Aktiv (wodurch angezeigt wird, dass die Einheit für Standardinteraktionen auswählbar ist) in Ersatzpool. Einheiten, die zum Ersatzpool gehören, sind dieser Funktion zugeordnet und können nicht wie andere Einheiten für konventionelle, alltägliche Aufgaben genutzt werden. Wenn eine Einheit aus dem Ersatzpool entfernt werden soll, damit sie wieder ihre konventionelle Funktion übernehmen kann, muss sie reaktiviert werden. Führen Sie die folgenden Schritte aus, um eine Einheit zu reaktivieren.
{:shortdesc}

## Einheit aus dem Ersatzpool reaktivieren 

1. Öffnen Sie das [{{site.data.keyword.slportal_full}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window}, indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben.
2. Wählen Sie in der Navigationsleiste **Einheiten > Ersatzpool** aus, um die Anzeige *Ersatzpool* aufzurufen.
3. Wählen Sie für die gewünschte Einheit **Aktionen > Einheit reaktivieren** aus.
4. Klicken Sie auf **Ja**, um den Server zu reaktivieren. Klicken Sie auf **Nein**, um die Aktion abzubrechen.

## Nächste Schritte
Nachdem der Reaktivierungsprozess gestartet wurde, wird die Einheit offline geschaltet und die Firmware aktualisiert. Die Einheit ist dann für den normalen Betrieb verfügbar. Der Reaktivierungsprozess dauert ungefähr eine Stunde. Einheiten, die aus dem Ersatzpool entfernt werden, stehen für die Verwendung als Failover-Methode nicht mehr zur Verfügung. Die Einheit kann jederzeit wieder in den Ersatzpool aufgenommen werden, indem sie ihm wieder hinzugefügt wird. Weitere Informationen finden Sie unter [Einheit dem Ersatzpool hinzufügen](../vsi/adding_spare_pool.html).

