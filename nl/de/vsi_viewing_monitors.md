---



copyright:
  years: 2017
lastupdated: "2017-10-23"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Überwachung anzeigen und verwalten

Die Überwachung einer Einheit bietet Benutzern die Möglichkeit, durch das Absetzen von Service-Pingsignalen und langsamen Pingsignalen sicherzustellen, dass die Einheit online und reaktionsfähig ist.
{:shortdesc}

Wenn im vorgegebenen Zeitrahmen (1 Sekunde bei Service-Pingsignalen und 5 Sekunden bei langsamen Pingsignalen) kein Echo empfangen wird, wird eine Benachrichtigung an die für das
Konto angegebene E-Mail-Adresse gesendet. Der Status **Aktiv** im Feld **Status** gibt an, dass ein Echo empfangen wurde. Der Status **Inaktiv**
gibt an, dass kein Echo empfangen wurde. Wenn Sie bereits eine Basisüberwachung konfiguriert haben, können Sie mit den nachfolgenden Schritten die Überwachung für eine Einheit anzeigen und verwalten.

   <table>
   <CAPTION>Tabelle 1. Einheitenüberwachung anzeigen und verwalten</CAPTION>
   <THEAD>
   <TR>
   <th>Gewünschte Aktion</th>
   <th>Vorgehensweise</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Überwachungen anzeigen</td>
   <td>
   <ol>
   <li>Klicken Sie in der Einheitenliste auf den <b>Einheitennamen</b>, um auf die Einheit zuzugreifen.</li>
   <li>Klicken Sie auf die Registerkarte <b>Überwachung</b>. Alle aktuellen Pingsignale können auf der Landing-Page angezeigt werden. (Die Registerkarte <b>Überwachung</b> ist nur sichtbar, wenn mindestens eine Überwachung konfiguriert ist.)</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Überwachung hinzufügen</td>
   <td>
   <ol>
   <li>Klicken Sie in der Registerkarte <b>Überwachung</b> auf der Seite 'Einheitendetails' auf <b>Überwachungen verwalten</b> rechts auf der Seite, um die zugehörigen Überwachungen für diese Einheit zu verwalten.</li>
   <li>Klicken Sie auf der Seite 'Überwachungen' auf die Registerkarte <b>Überwachung hinzufügen</b>.</li>
   <li>Wählen Sie die zu überwachende IP-Adresse in der Dropdown-Liste <b>IP-Adresse</b> aus.</li>
   <li>Wählen Sie den Überwachungstyp in der Dropdown-Liste <b>Überwachungstyp</b> aus.</li>
   <li>Legen Sie die Benachrichtigungsoptionen fest. Wählen Sie in der Dropdown-Liste <b>Benachrichtigen</b> die Option <b>Benutzer benachrichtigen</b>  aus, um Benutzer über Probleme zu benachrichtigen, oder die Option <b>Keine Aktion</b>, um die Benutzerbenachrichtigung zu umgehen.</li>
   <li>Wählen Sie den Zeitrahmen für die Benutzerbenachrichtigung in der Dropdown-Liste <b>Wartezeit für Benachrichtigung</b> aus.</li>
   <li>Klicken Sie auf die Schaltfläche <b>Überwachung hinzufügen</b>, um die Überwachung für die Einheit hinzuzufügen. Die neue Überwachung wird in der Anzeige <b>Vorhandene Überwachungen bearbeiten</b> eingefügt.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Vorhandene Überwachung bearbeiten</td>
   <td>
   <ol>
   <li>Klicken Sie auf der Seite 'Überwachungen' unter der Überschrift <b>Vorhandene Überwachungen bearbeiten</b> auf beliebige Überwachungsdetails, um die Überwachung zum Bearbeiten zu öffnen.</li>
   <li>Aktualisieren Sie beliebige der folgenden Felder: Überwachungstyp, Benachrichtigen, Wartezeit für Benachrichtigung.</li>
   <li>Klicken Sie auf die Schaltfläche <b>Aktualisieren</b>, um die Details zu aktualisieren. Klicken Sie auf die Schaltfläche <b>Abbrechen</b>, um den Bearbeitungsvorgang abzubrechen.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Überwachung entfernen</td>
   <td>
   <ol>
   <li>Klicken Sie auf der Seite 'Überwachungen' unter der Überschrift <b>Vorhandene Überwachungen bearbeiten</b> auf das Symbol 'Entfernen' neben den Überwachungsdetails.</li>
   <li>Klicken Sie auf die Schaltfläche <b>Ja</b>, um die Überwachung zu entfernen. Klicken Sie auf die Schaltfläche <b>Nein</b>, um den Vorgang abzubrechen.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>
   
## Nächste Schritte
   
- Wenn eine neue Überwachung hinzugefügt wurde, wird sie auf der Registerkarte **Überwachung** angezeigt. Die Überwachung sendet alle fünf Minuten ein Pingsignal an die Einheit und erwartet eine Antwort entsprechend dem ausgewählten Pingsignaltyp. Wenn die erwartete Antwort nicht eintrifft, wird im angegebenen Zeitrahmen eine E-Mail an die für das Konto angegebene Benachrichtigungs-E-Mail-Adresse gesendet, falls die Benachrichtigungsoption ausgewählt wurde.
- Wenn eine Überwachung bearbeitet wurde, wird die Überwachung unter Beachtung der angegebenen Überwachungsdetails fortgesetzt. Wenn der Typ geändert wurde, wird ein geänderter Zeitrahmen für den Empfang des erwarteten Pingsignals verwendet. Wenn Benachrichtigungsoptionen geändert wurden, erfolgt die Benutzerbenachrichtigung über fehlgeschlagene Versuche gemäß den neuen Auswahlen. Die Überwachung ist in der Registerkarte **Überwachung** weiterhin zugänglich.
- Wenn eine Überwachung entfernt wurde, wird sie für die Einheit nicht mehr ausgeführt. Alle zugehörigen Prozesse für die Überwachung, die entfernt wurde, werden beendet, und die Überwachung wird auf der Registerkarte **Überwachung** nicht mehr angezeigt.
