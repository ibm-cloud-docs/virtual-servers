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

# Betriebssystem mithilfe einer Imagevorlage erneut laden
Ähnlich wie beim Standardprozess zum erneuten Laden des Betriebssystems, bietet auch das erneute Laden mithilfe einer Imagevorlage den Benutzern die Möglichkeit eine Einheit anhand einer bereits vorhandenen Imagevorlage wiederherzustellen oder zu rekonfigurieren, die dem verwendeten Konto im Kundenportal zugeordnet ist. Beim Standardverfahren zum erneuten Laden des Betriebssystems können die Konfigurationsoptionen für die Einheit einzeln ausgewählt werden. Beim erneuten Laden aus einer Imagevorlage wird jedoch die Konfiguration aus der Imagevorlage übernommen. Auch bei dieser Methode können Sie vor dem Durchführen des erneuten Ladens Zusatzeinrichtungen hinzufügen.
Führen Sie die folgenden Schritte aus, um das erneute Laden eines Betriebssystems aus einer Imagevorlage mithilfe der Funktion 'Aus Image laden' im Kundenportal durchzuführen.
{:shortdesc}

## Erneutes Laden mithilfe einer Imagevorlage durchführen
1. Sichern Sie alle in der Einheit gespeicherten Daten.
  
   **Hinweis:** Beim erneuten Laden des Betriebssystems werden alle Daten auf der Festplatte gelöscht. Wenn die Daten vor dem erneuten Laden des Betriebssystems nicht gesichert wurden, können sie nicht mehr abgerufen werden. Bluemix (SoftLayer) erstellt keine Sicherungen der auf Einheiten des Kunden gespeicherten Daten und haftet nicht für Datenverluste durch das erneute Laden des Betriebssystems.
  
2. Wählen Sie auf der Seite 'Einheitenliste' die Option **Aus Image laden** im Menü **Aktionen** für die gewünschte Einheit aus.

3. Wählen Sie das Kontrollkästchen für das gewünschte Image aus, um die Imagevorlage anzugeben, die in die Einheit geladen werden soll.

   **Hinweis:** Bevor das erneute Laden abgeschlossen wird, wird die Imagevorlage in das Rechenzentrum kopiert, das die Einheit enthält, falls es sich noch nicht in dem Rechenzentrum befindet. Wenn die Imagevorlage in das betreffende Rechenzentrum kopiert werden muss, fällt möglicherweise eine zusätzliche Gebühr an, sofern die Vorlage nicht an der Speicherposition gelöscht wird, nachdem das erneute Laden des Betriebssystems erfolgt ist.
  
4. Legen Sie fest, ob Zusatzeinrichtungen hinzugefügt werden sollen. Alle von Ihnen ausgewählten Zusatzeinrichtungen werden beim erneuten Laden zu der Einheit hinzugefügt.
   
   <table>
   <CAPTION>Tabelle 1. Zusatzeinrichtungen</CAPTION>
   <THEAD>
   <TR>
   <th>Zusatzeinrichtungen</th>
   <th>Schritte</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   </tr>
   <tr>
   <td>Ja, ich möchte Zusatzeinrichtungen hinzufügen</td>
   <td>
   <ol>
   <li>Klicken Sie auf <b>Ausgewähltes Image laden</b>.</li>
   <li>Überprüfen Sie die Imagekonfiguration und fahren Sie fort oder brechen Sie den Vorgang ab.</li>
   <li>Klicken Sie auf <b>Erneutes Laden des Betriebssystems bestätigen</b>, um den Vorgang zu bestätigen und das erneute Laden des Betriebssystems zu starten.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Nein, ich möchte keine Zusatzeinrichtungen hinzufügen</td>
   <td>Klicken Sie auf <b>Zusatzeinrichtungen anzeigen</b>.</td>
   </tr>
   </TBODY>
   </table>

5. Konfigurieren Sie die gewünschten Zusatzeinrichtungen. Weitere Details finden Sie in den nachfolgenden Informationen.
   
   <dl>
   <dt>Script nach der Installation</dt>
   <dd>Fügt ein vorhandenes oder ein neues Script nach der Installation hinzu.</dd>
   <dt>SSH-Schlüssel</dt>
   <dd>Fügt einen SSH-Schlüssel für die Einheit bei der Aktion für erneutes Laden hinzu. </dd>
   <dt>IPMI-Kennwort zurücksetzen</dt>
   <dd> Diese Option ist nur für physische Einheiten verfügbar. </dd>
   <dt>BIOS-Upgrades für Steuerplatine anwenden</dt>
   <dd>Diese Option ist nur für physische Einheiten verfügbar. </dd>
   <dt>Firmware-Updates für alle Festplattenlaufwerke anwenden</dt>
   <dd>Diese Option ist nur für physische Einheiten verfügbar.</dd>
   <dt>Nach erneuten Laden des Betriebssystems zum Ersatzpool hinzufügen</dt>
   <dd>Diese Option ist nur auf physischen Einheiten verfügbar und muss intern genehmigt werden, damit sie für ein Konto verfügbar ist.</dd>
   <dt>Alle Festplatten löschen</dt>
   <dd> Diese Option ist nur auf physischen Einheiten verfügbar und erfordert spezielle Benutzerberechtigungen, die vom Kontoadministrator erteilt werden.</dd>
   <dt>Neuladen des Betriebssystems unter Beibehaltung der Platte</dt>
   <dd>Behält alle Daten auf dem aktuellen primären Datenträger bei, wenn das Betriebssystem erneut geladen wird. Bei Verwendung dieser Option wird das primäre Laufwerk in eine portierbare Speichereinheit umgewandelt. Diese Option ist nur für virtuelle Einheiten verfügbar und sie verursache zusätzliche Gebühren gemäß dem Abrechnungsmuster (stündlich oder monatlich) der Einheit. Durch Abbrechen der portierbaren Speichereinheit können die Gebühren nach dem Erstellen der Einheit jederzeit beendet werden.</dd>
   </dl>

6. Klicken Sie auf **Ausgewähltes Image laden**.

7. Überprüfen Sie die Konfiguration und klicken Sie auf **Weiter**, um die nächste Anzeige aufzurufen, oder klicken Sie auf **Abbrechen**, um den Vorgang abzubrechen.

   **Hinweis:** Wenn Sie auf **Weiter** klicken, werden alle Netzports für die Einheit systematisch beendet und die Einheit ist bis zu 15 Minuten lang nicht verfügbar. Während dieser Zeit kann die Aktion durch Klicken auf **Abbrechen** jederzeit abgebrochen werden. Wenn der nächste Schritt nicht innerhalb von 15 Minuten nach dem Klicken auf **Weiter** abgeschlossen wird, muss der vorangegangene Schritt erneut ausgeführt werden. Auf diese Weise wird sichergestellt, dass zwischen dem Bestätigen der Konfiguration und dem Start des erneuten Ladevorgangs für das Betriebssystems keine zusätzlichen Daten in der Einheit hinzugefügt werden.

8. Klicken Sie auf **Erneutes Laden des Betriebssystems bestätigen**, um den Vorgang zu bestätigen und das erneute Laden des Betriebssystems zu starten. Klicken Sie auf **Abbrechen**, um den Vorgang abzubrechen.

## Weitere Schritte
Nachdem das erneute Laden des Betriebssystems gestartet ist, wird die betreffende Einheit offline geschaltet und der Vorgang wird durchgeführt.
Der Zeitraum, in dem das erneute Laden des Betriebssystems ausgeführt wird, variiert entsprechend der aktuellen und der neuen Konfiguration der Einheit.
Wenn das erneute Laden länger als 24 Stunden dauert, verständigen Sie das Support-Team. Sobald die Einheit wieder online ist, wird die in den Einstellungen für das erneute Laden
des Betriebssystems angegebene neue Konfiguration verwendet. Alle zuvor in der Einheit gespeicherten Daten gehen verloren. Sie können jedoch
wiederhergestellt werden, wenn vor dem erneuten Laden eine Datensicherung für die Einheit erstellt wurde. Wenn Daten nicht gesichert wurden, können Sie nicht mehr abgerufen werden.

 Informationen zum erneuten Registrieren Ihrer Einheit bei eVault finden Sie unter [Re-registering your device with eVault ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
