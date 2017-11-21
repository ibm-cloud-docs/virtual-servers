---



copyright:
  years: 2017
lastupdated: "2017-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

#  Betriebssystem erneut laden
Das erneute Laden des Betriebssystems kann in einer Einheit jederzeit durchgeführt werden, um den ursprünglichen Betriebszustand der Einheit wiederherzustellen. Bei diesem Vorgang werden alle in der Einheit gespeicherten Daten verloren und die Einheit wird wieder in den ursprünglichen, "unbenutzten" Werkszustand versetzt, der beim Konfigurieren des erneuten Ladens angegeben wurde. Bei erneuten Laden des Betriebssystems werden alle Daten in der Einheit gelöscht, von denen zuvor keine Sicherungskopie erstellt wurde, d. h. die Daten werden endgültige gelöscht und können nicht mehr abgerufen werden.
{:shortdesc}

**Wichtig:** Wenn Sie keine Daten verlieren möchten, sicheren Sie alle Daten, bevor das Betriebssystem erneut geladen wird.

## Erneutes Laden durchführen
1. Klicken Sie in der **Einheitenliste** auf den Server, für den das Betriebssystem erneut geladen werden soll.
2. Wählen Sie im Menü **Aktionen** links oben auf der Seite die Option **Betriebssystem erneut laden** aus.
3. Legen Sie fest, ob die vorhandene Konfiguration oder eine neue Konfiguration für die Einheit erneut geladen werden soll.

   <table>
   <CAPTION>Tabelle 1. Optionen für erneutes Laden des Betriebssystems</CAPTION>
   <THEAD>
   <TR>
   <th>Typ</th>
   <th>Schritte</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Beim erneuten Laden eine neue Konfiguration verwenden</td>
   <td>
   <ol>
   <li>Klicken Sie auf <b>Bearbeiten</b> für die Kategorie, die aktualisiert werden soll.</li>
   <li>Wählen Sie in der Dropdown-Liste <i>Software auswählen</i> auf die neue Software, die auf die Einheit angewendet werden soll.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Beim erneuten Laden die vorhandene Konfiguration verwenden</td>
   <td>Fahren Sie mit dem nächsten Schritt fort.</td>
   </tr>
   </TBODY>
   </table>

4. Legen Sie fest, ob ein Script nach der Bereitstellung ausgeführt werden soll, nachdem die Einheit bereitgestellt wurde.

   Wenn Sie ein Script nach der Installation anwenden möchten, wählen Sie das Script in der Dropdown-Liste für vorhandene Scripts aus oder geben Sie die qualifizierte URL für das neue Script ein.  Fahren Sie andernfalls mit dem nächsten Schritt fort.

5. Legen Sie für physische Einheiten fest, ob installierte Partitionen hinzugefügt, entfernt oder beibehalten werden sollen.
   
   <table>
   <CAPTION>Tabelle 2. Aktionsoptionen für Partitionen</CAPTION>
   <THEAD>
   <TR>
   <th>Partitionsaktion</th>
   <th>Schritte</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Installierte Partitionen hinzufügen</td>
   <td>
   <ul>
   <li>Klicken Sie auf den Link <b>Weitere Partition hinzufügen</b>.</li>
   <li>Geben Sie den Namen der Partition korrekt ein.</li>
   <li>Geben Sie die Größe für die Partition ein (in GB). Bei Bedarf können Sie die Vergrößerungsoption auswählen, damit die Partition erweitert wird, bis Sie den verbleibenden Plattenspeicher ausfüllt.
   <p><b>Hinweis:</b> Die Vergrößerungsoption kann jeweils nur für eine Partition ausgewählt werden. Die betreffende Partition belegt mehr als die angegebene Größe und füllt die gesamte verfügbare Kapazität aus. Beim Berechnen der Kapazität für die vergrößerte Partition wird die kumulierte Größe aller übrigen Partitionen von der Gesamtkapazität abgezogen, die im Abschnitt für installierte Partitionen angegeben ist.</p>
   </li>
   </ul>
   </td>
   </tr>
   <tr>
   <td>Installierte Partitionen löschen</td>
   <td>Klicken Sie auf das Symbol <b>Löschen</b>, um die Partition zu löschen.</td>
   </tr>
   <tr>
   <td>Partitionen unverändert beibehalten</td>
   <td>Fahren Sie mit dem nächsten Schritt fort.</td>
   </tr>
   </TBODY>
   </table>
    
6. Legen Sie fest, ob ein oder mehrere SSH-Schlüssel auf die Einheit angewendet werden soll(en).

7. Wählen Sie die Kontrollkästchen für die gewünschten Optionen aus, die während oder nach dem erneuten Laden des Betriebssystems auf die Einheit angewendet werden sollen.

   **Hinweis:** Die Optionen variieren je nach Einheit. Nicht alle Optionen sind für jede Einheit verfügbar.

8. Klicken Sie auf die Schaltfläche **Vorherige Konfiguration erneut laden**, um das Popup-Fenster zum Überprüfen aufzurufen. Klicken Sie auf die Schaltfläche **Abbrechen**, um die Änderungen für die Einheit zu verwerfen und die Anzeige zu schließen.

9. Überprüfen Sie, dass alle Details im Abschnitt für die neue Konfiguration korrekt angegeben sind.  

10. Klicken Sie auf die Schaltfläche **Erneutes Laden des Betriebssystems bestätigen**, um die Aktion zu bestätigen und das erneute Laden des Betriebssystems zu starten. Klicken Sie auf die Schaltfläche **Abbrechen**, um die Aktion abzubrechen.

## Weitere Schritte
Nachdem das erneute Laden des Betriebssystems gestartet ist, wird die betreffende Einheit offline geschaltet und der Vorgang wird durchgeführt.
Der Zeitraum, in dem das erneute Laden des Betriebssystems ausgeführt wird, variiert entsprechend der aktuellen und der neuen Konfiguration der Einheit.
Während des Konfigurationsprozesses wird in jeder Bildschirmanzeige die Mindestzeit für das erneute Laden des Betriebssystems angezeigt.
Der angegebene Zeitrahmen ist ein vom System berechneter, unverbindlicher Schätzwert. Wenn das erneute Laden länger als 24 Stunden
dauert, wenden Sie sich an das Support-Team. Sobald die Einheit wieder online ist, wird die in den Einstellungen für das erneute Laden
des Betriebssystems angegebene neue Konfiguration verwendet. Alle zuvor in der Einheit gespeicherten Daten gehen verloren. Sie können jedoch
wiederhergestellt werden, wenn vor dem erneuten Laden eine Datensicherung für die Einheit erstellt wurde.
Wenn Daten nicht gesichert wurden, können Sie nicht mehr abgerufen werden.
 
Informationen zum erneuten Registrieren Ihrer Einheit bei eVault finden Sie unter [Re-registering your device with eVault ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
