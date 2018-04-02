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


# Vorhandenen virtuellen Server neu konfigurieren
{: #reconfiguring-virtual-servers}

Sie können die Konfiguration eines bereitgestellten virtuellen Servers jederzeit erweitern oder reduzieren.  

**Wichtiger Hinweis:** Für öffentliche virtuelle Server werden mehrere vordefinierte Versionen (Flavors) angeboten. Für einen begrenzten Zeitraum können Sie alle virtuellen Server ändern, die verfügbar waren, bevor vordefinierte Versionen angeboten wurden. Anschließend müssen Sie die vorhandenen Instanzen migrieren oder abbrechen und neu bestellen. 

Bei einem virtuellen Server, der vordefinierte Versionen verwendet, können die festgelegten Werte für Kern, RAM und Datenträgergröße nicht geändert werden. Wählen Sie stattdessen eine andere Version mit den gewünschten vordefinierten Werten für Kerne, RAM und Datenträgergröße aus. Die von Ihnen ausgewählte Version des virtuellen Servers entscheidet darüber, welche Werte für Kerne, Arbeitsspeicher und Datenträgergröße verwendet werden.  

Dedizierte virtuelle Server können flexibler angepasst werden, d. h. Sie können die Werte für Kerne, RAM und Datenträgergröße ändern.

Führen Sie die folgenden Schritte aus, um die Konfiguration für einen vorhandenen virtuellen Server zu ändern.
{:shortdesc}

## Vorhandenen virtuellen Server mit vordefinierten Versionen ändern
1. Öffnen Sie das [{{site.data.keyword.slportal_full}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/), indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben. 
2. Klicken Sie in der Einheitenliste auf den Namen des virtuellen Servers, den Sie neu konfigurieren möchten.
3. Auf der Registerkarte **Konfiguration** können Sie auf **Ändern** oder auf **Einheitenkonfiguration ändern** klicken, um die folgenden Einstellungen zu ändern. 
  <dl>
  <dt>Größe</dt>
  <dd>Wählen Sie eine neue Größe aus.</dd>
  <p><note>Hinweis: Beim Ändern einer Version, die lokalen Speicher verwendet, können Sie keine Version auswählen, die fernen Speicher verwendet. Ebenso kann beim Ändern einer Version, die fernen Speicher verwendet, keine Version ausgewählt werden, die lokalen Speicher verwendet.
  </note></p>
  </dl>
4. Nachdem Sie die gewünschten Änderungen für den virtuellen Server angegeben haben, müssen Sie die Konfigurationsaktualisierung abschließen.
  <dl>
  
  <dt>Aktualisierungsdatum</dt>
  <dd>Klicken Sie auf das Kontrollkästchen 'Sofort', um die Aktualisierung sofort durchzuführen, oder geben Sie einen Zeitpunkt an, an dem die Aktualisierung wirksam werden soll.</dd>

  <dt>Aktualisierungszeitpunkt</dt>
  <dd>Geben Sie das Datum (JJJJ-MM-TT) an, an dem die Aktualisierung wirksam werden soll.</dd>

  <dt>Anmerkungen</dt>
  <dd>Geben Sie die gewünschten Anmerkungen für Ihre Einheit ein. </dd>
  </dl>

5. Klicken Sie auf **Weiter**.
6. Prüfen Sie, ob die Angaben in Ihrer Auftragsbestätigung korrekt sind.  Klicken Sie auf **Bearbeiten**, um Ihre Aktualisierung zu bearbeiten.
7. Klicken Sie auf **Bestätigen**, um Ihre Bestellung zu bestätigen und die Änderungen auf Ihre Einheit anzuwenden.

## Vorhandenen virtuellen Server (vor der Einführung vordefinierter Versionen) oder dedizierten virtuellen Server ändern
1. Klicken Sie in der Einheitenliste auf den Namen des virtuellen Servers, den Sie neu konfigurieren möchten.
2. Auf der Registerkarte **Konfiguration** können Sie auf den Link für **Kern- oder RAM-Aktualisierung** klicken, um die folgenden Einstellungen zu ändern. 
  
|   Aktualisierungsoptionen       |  Beschreibung                                                                                                |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| Aktualisierungsdatum            | Geben Sie das Datum (JJJJ-MM-TT) an, an dem die Aktualisierung wirksam werden soll.                                                |
| Aktualisierungszeitpunkt            | Wählen Sie über die Dropdown-Felder die Uhrzeit aus, zu der die Aktualisierung aktiv werden soll oder klicken Sie auf das Kontrollkästchen **Sofort** für eine sofortige Aktualisierung.                                                                                        |
| Kerne                   | Wählen Sie gegebenenfalls die Anzahl der Kerne für die Aktualisierung aus. |
| RAM                     | Wählen Sie gegebenenfalls die gewünschte RAM-Größe aus, die für die Aktualisierung auf Ihre Einheit angewendet werden soll.   |
| Uplink-Port-Geschwindigkeiten      | Wählen Sie gegebenenfalls die neuen Uplink-Port-Geschwindigkeiten für Ihre Einheit aus. |
| Öffentliche Bandbreite        | Wählen Sie gegebenenfalls das gewünschte Volumen (in GB) für die öffentliche Bandbreite Ihrer Einheit aus.   |
| Erster Datenträger – Fünfter Datenträger | Wählen Sie gegebenenfalls die Option für den Plattenspeicherplatz/Speicher für Ihren ersten Datenträger aus. Weitere Informationen finden Sie unten im Abschnitt **Hinweise zu Datenträgern**.                                                                                                                               |
| Anmerkungen                   | Geben Sie die gewünschten Anmerkungen für Ihre Einheit ein.                                                                 |
{: caption="Tabelle 1. Bereitstellungsoptionen" caption-side="top"}   
  
  **Hinweise zu Datenträgern:**
  * Sowohl lokaler Speicher als auch SAN-Speicher sind verfügbar.  Überprüfen Sie Ihre Auswahl noch einmal um sicherzustellen, dass Ihre Speicheroption richtig ist.
  * Wenn Sie bei öffentlichen virtuellen Servern den lokalen Speicher aktualisieren und mehr Kerne oder RAM benötigen, wird möglicherweise der sekundäre Datenträger entfernt. Wenn Sie eine Version eines virtuellen Servers ändern, bei der lokaler Speicher verwendet wird, ist die Version bereits voreingestellt und es können keine Versionen ausgewählt werden, die nicht vergleichbar sind.
3. Klicken Sie auf **Weiter**.
4. Prüfen Sie, ob die Angaben in Ihrer Auftragsbestätigung korrekt sind.  Klicken Sie auf **Bearbeiten**, um Ihre Aktualisierung zu bearbeiten.
5. Klicken Sie auf **Bestätigen**, um Ihre Bestellung zu bestätigen und die Änderungen auf Ihre Einheit anzuwenden.
