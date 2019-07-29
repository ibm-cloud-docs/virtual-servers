---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:note: .note}
{:new_window: target="_blank"}

# Platzierungsgruppen verwalten
{: #vsi_managing_placegroup}

Platzierungsgruppen können über die Seite für Platzierungsgruppen oder über die Seite mit den Einheitendetails in der {{site.data.keyword.cloud}}-Konsole verwaltet werden.
{:shortdesc}

## Platzierungsgruppen hinzufügen

Führen Sie die folgenden Schritte aus, um Platzierungsgruppen über die Seite für Platzierungsgruppen hinzuzufügen:
{:shortdesc}

1. Öffnen Sie die Seite für die [Platzierungsgruppen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. Klicken Sie auf der Seite für die Platzierungsgruppen auf **Neue Gruppe**.
3. Geben Sie einen Namen, einen Standort, einen Pod und eine Regel für die Platzierungsgruppe an und klicken Sie dann auf **Erstellen**.

Vorhandene Instanzen können nicht zu einer Platzierungsgruppe hinzugefügt werden; es ist nur möglich, eine virtuelle Serverinstanz zum Zeitpunkt der Bereitstellung zu einer Platzierungsgruppe hinzuzufügen. 
{:note}

## Platzierungsgruppen verwalten

Führen Sie die folgenden Schritte aus, um Platzierungsgruppen über die Seite für Platzierungsgruppen zu verwalten:
{:shortdesc}

1. Öffnen Sie die Seite für die [Platzierungsgruppen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. Im Abschnitt für die Platzierungsgruppen können Sie eine Reihe von Verwaltungsaufgaben durchführen.
     * Liste mit Platzierungsgruppen und Anzahl der zugewiesenen Instanzen anzeigen
     * Gruppe hinzufügen
     * Gruppe umbenennen
     * Instanz bereitstellen
     * Gruppe löschen
     
Zugewiesene Server müssen aus der Platzierungsgruppe entfernt werden, bevor die Platzierungsgruppe gelöscht werden kann. Zum Entfernen einer Instanz von einer Platzierungsgruppe muss die Instanz gelöscht oder freigegeben werden.
{:note}
