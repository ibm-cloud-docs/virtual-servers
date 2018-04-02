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

# Öffentliche Instanzen bereitstellen
{: #ordering-vs-public}

## Vorbereitungen
Sie haben zwei Möglichkeiten, um Ihre öffentlichen virtuellen Serverinstanzen bereitzustellen. Die erste Möglichkeit ist die Verwendung des {{site.data.keyword.Bluemix}}-Katalogs und die zweite Möglichkeit ist das {{site.data.keyword.slportal_full}}. Für den Katalog und für das {{site.data.keyword.slportal}} sind eindeutige Anmelde-IDs erforderlich. Sie können sich mit dem Benutzernamen und Kennwort für den Katalog daher nicht beim Portal anmelden und umgekehrt.
{:shortdesc}

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie beginnen.

  1. Stellen Sie sicher, dass Sie über gültige Berechtigungsnachweise für den {{site.data.keyword.Bluemix_notm}}-Katalog oder für das {{site.data.keyword.slportal}} verfügen. 
  
     **Hinweis:** Sie müssen über ein aktualisiertes Konto für den {{site.data.keyword.Bluemix_notm}}-Katalog verfügen, um virtuelle Server zu bestellen. Weitere Informationen zum Aktualisieren Ihres Kontos finden Sie unter [Zur IBMid wechseln](https://console.bluemix.net/docs/admin/softlayerlink.html).
  
  2. Machen Sie sich mit den Bereitstellungsoptionen vertraut, die Ihnen zur Verfügung stehen (falls dies noch nicht geschehen ist). Weitere Informationen finden Sie unter [Bereitstellungsoptionen: Öffentlicher virtueller Server](../vsi/vsi_public.html).

## Anmelden 
Stellen Sie sicher, dass Sie angemeldet sind (entweder beim {{site.data.keyword.Bluemix_notm}}-Katalog oder beim {{site.data.keyword.slportal}}): 

  <table>
   <CAPTION>Tabelle 1.Anmeldeposition auswählen</CAPTION>
   <THEAD>
   <TR>
   <th>Anmeldung mit...</th>
   <th>Vorgehensweise</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud-Katalog</td>
   <td>
   <ol>
   <li>Öffnen Sie ein neues Browserfenster und geben Sie <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a> ein.</li>
   <li>Klicken Sie auf den Link <b>Anmeldung</b> in der rechten oberen Ecke. </li>
   <li>Geben Sie Ihre E-Mail-Adresse oder Ihre IBMid ein und klicken Sie auf <b>Weiter</b>.</li>
   <li>Geben Sie Ihr Kennwort ein und klicken Sie auf <b>Anmelden</b>.</li>
   <li>Wählen Sie <b>Infrastruktur</b> > <b>Compute</b> aus.</li>
   <li>Klicken Sie auf die Kachel <b>Virtuelle Server</b>.</li>
   <li>Wählen Sie die Option <b>Öffentliche virtuelle Server</b> aus.</li>
   <li>Klicken Sie auf <b>Erstellen</b>. Die Hauptseite des {{site.data.keyword.slportal}}s wird geöffnet.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Kundenportal</td>
   <td>
   <ol>
   <li>Öffnen Sie ein neues Browserfenster und geben Sie <a href="https://control.softlayer.com">https://control.softlayer.com</a> ein.</li>
   <li>Geben Sie Ihren Benutzernamen und Ihr Kennwort ein und klicken Sie auf <b>Anmeldung</b>. Oder klicken Sie auf <b>Melden Sie sich mit der IBMid an</b>. Geben Sie anschließend Ihre E-Mail-Adresse oder Ihre IBMid ein und klicken Sie auf <b>Weiter</b>. Geben Sie Ihr Kennwort ein und klicken Sie auf <b>Anmelden</b>. Die Hauptseite des {{site.data.keyword.slportal}}s wird geöffnet.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Öffentliche virtuelle Serverinstanz bereitstellen
{: #ordering-public-instance}
Nachdem Sie die Voraussetzungen erfüllt haben, können Sie mit dem Bereitstellen einer öffentlichen virtuellen Serverinstanz beginnen. Sie können Ihre öffentlichen Instanzen auf zwei Arten bereitstellen: mit dem Menü **Einheiten** oder mit dem Symbol **Einheiten**.

### Öffentliche virtuelle Serverinstanz über das Symbol 'Einheiten' bereitstellen
Führen Sie die folgenden Schritte aus, um Ihre öffentliche virtuelle Serverinstanz über das Symbol *Einheiten* bereitzustellen:

1.  Suchen Sie im {{site.data.keyword.slportal}} den Abschnitt **Bestellung** und klicken Sie auf **Einheiten**.
2.  Klicken Sie auf der Seite 'Einheiten' auf **Stundenbasis** oder **Monatsbasis** für eines der Angebote für virtuelle Server.
3.  Geben Sie auf der Seite *Cloud-Server konfigurieren* alle relevanten Informationan an.
4.  Klicken Sie auf die Schaltfläche **Zur Bestellung hinzufügen**, um fortzufahren.
5.  Bestätigen oder bearbeiten Sie die Domäneninformationen für den Server.
5.  Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
6.  Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige. Sie ist die Auftragsbestätigung für Ihre Bereitstellungsbestellung.

 Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu der zugehörigen Seite *Einheitendetails*, nachdem Sie sich bei {{site.data.keyword.Bluemix_notm}} angemeldet haben. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.

### Öffentliche virtuelle Serverinstanz über das Menü 'Einheiten' bereitstellen
{: #ordering-public-devices-menu}

Sie können Ihre öffentlichen virtuellen Serverinstanzen auch über das Menü *Einheiten* auf der Hauptseite des {{site.data.keyword.slportal}}s bereitstellen. 

1. Klicken Sie auf **Einheiten > Einheitenliste**.

   Auf der Seite 'Einheiten' werden alle Enheitentypen in Ihrem Konto angezeigt (dedizierte Hosts, virtuelle Server, Bare-Metal-Server und NetScaler-Controller für Anwendungsbereitstellung).
2. Klicken Sie auf den Link **Einheiten bestellen** in der rechten oberen Ecke.
3. Klicken Sie auf der Seite 'Einheiten' auf **Stundenbasis** oder **Monatsbasis** für eines der Angebote für virtuelle Server.
4. Geben Sie auf der Seite *Cloud-Server konfigurieren* alle relevanten Informationan an.
5. Klicken Sie auf die Schaltfläche **Zur Bestellung hinzufügen**, um fortzufahren.
6. Bestätigen oder bearbeiten Sie die Domäneninformationen für den Server.
7. Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
8. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige. Sie ist die Auftragsbestätigung für Ihre Bereitstellungsbestellung.

Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu der zugehörigen Seite *Einheitendetails*, nachdem Sie sich bei {{site.data.keyword.Bluemix_notm}} angemeldet haben. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.

### Nächste Schritte
Nachdem Ihr virtueller Server bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [Virtuellen Server verwalten](../vsi/vsi_managing.html).
