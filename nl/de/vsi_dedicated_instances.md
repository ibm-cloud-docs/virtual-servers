---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Dedizierte Instanzen bereitstellen

Sie haben zwei Möglichkeiten zum Bereitstellen Ihrer dedizierten Instanzen. Die erste Möglichkeit ist die Verwendung des {{site.data.keyword.Bluemix}}-Katalogs und die zweite Möglichkeit ist das {{site.data.keyword.slportal_full}}. Für den Katalog und für das {{site.data.keyword.slportal}} sind eindeutige Anmelde-IDs erforderlich. Sie können sich folglich mit dem Benutzernamen und Kennwort für den Katalog nicht beim Portal anmelden oder umgekehrt. In der Dokumentation [Bei {{site.data.keyword.Bluemix_notm}} anmelden](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} finden Sie Informationen zum Einrichten von Berechtigungsnachweisen für den {{site.data.keyword.Bluemix_notm}}-Katalog bzw. für das {{site.data.keyword.slportal}}.
{:shortdesc}

## Beim IBM Cloud-Katalog anmelden
Führen Sie die folgenden Schritte aus, um sich beim {{site.data.keyword.Bluemix_notm}}-Katalog anzumelden und mit dem Bereitstellen Ihrer dedizierten Instanzen zu beginnen. 

1. Öffnen Sie ein neues Browserfenster und geben Sie [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/){: new_window} ein.
2.	Klicken Sie auf den Link **Anmeldung** in der rechten oberen Ecke. 
3.	Geben Sie Ihre E-Mail-Adresse oder Ihre IBMiD ein und klicken Sie auf **Weiter**.
4.	Geben Sie Ihr Kennwort ein und klicken Sie auf **Anmelden**.
5.	Wählen Sie **Infrastruktur > Compute** aus.
6.  Klicken Sie auf die Kachel **Virtueller Server**.
7.	Wählen Sie die Option **Dedizierte virtuelle Server** aus.
8.  Klicken Sie auf **Erstellen**. 

Die Hauptseite des {{site.data.keyword.slportal}}s wird angezeigt.

## Beim Kundenportal anmelden
Führen Sie die folgenden Schritte aus, um sich beim {{site.data.keyword.slportal}} anzumelden und mit der Bestellung für Ihre dedizierten Instanzen zu beginnen.

1.	Öffnen Sie ein neues Browserfenster und geben Sie [https://control.softlayer.com](https://control.softlayer.com){: new_window} ein. 
2.	Geben Sie Ihren Benutzernamen und Ihr Kennwort ein und klicken Sie auf **Anmelden** ODER klicken Sie auf **Mit IBMid anmelden**.
3.	Geben Sie Ihre E-Mail-Adresse oder Ihre IBMiD ein und klicken Sie auf **Weiter**.
4.	Geben Sie Ihr Kennwort ein und klicken Sie auf **Anmelden**.

Die Hauptseite des {{site.data.keyword.slportal}}s wird angezeigt.

## Dedizierte Instanzen bereitstellen
{: #provision-dedicated-instances}
Sie können Ihre dedizierten Instanzen auf zwei Arten bereitstellen: über das Symbol **Einheiten** oder über das Menü **Einheiten**.

### Dedizierte Hostinstanzen über das Symbol 'Einheiten' bereitstellen
{: #ordering-dedicated-devices-menu}
Die erste Option zum Bereitstellen dedizierter Hostinstanzen ist die Verwendung des Symbols **Einheit** auf der Startseite des {{site.data.keyword.slportal}}s. Dieser Vorgang umfasst die folgenden Schritte.

1.	Klicken Sie auf das Symbol **Einheiten**. Das Fenster **SoftLayer-Produkt und Services bestellen** wird angezeigt. 
2.  Wählen Sie unter 'Dedizierte virtuelle Server' die Option **Stündlich** oder **Monatlich** aus. Die Seite *Cloud-Server konfigurieren* wird wieder angezeigt. 

3.	Geben Sie die folgenden Informationen ein:
       
    <table>
    <CAPTION>Tabelle 1. Optionen für dedizierte Hostinstanzen</CAPTION>
    <THEAD>
    <TR>
    <th>Feld</th>
    <th>Wert</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Menge</td>
    <td>Die Anzahl der dedizierten Instanzen, die bereitgestellt werden sollen.</td>
    </tr>
    <tr>
    <td>Platzierung</td>
    <td>
    <ul>
    <li>Automatisch zuordnen – {{site.data.keyword.Bluemix_notm}} ordnet Ihre Instanz automatisch einem Host in dem von Ihnen ausgewählten Rechenzentrum zu.</li>
    <li>Host angeben – Wird bei dedizierten Hostinstanzen verwendet. Weitere Informationen zu dedizierten Hosts und dedizierten Hostinstanzen finden Sie unter [Dedizierter virtueller Server](../vsi/vsi_dedicated.html).</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Rechenzentrum</td>
    <td>Wählen Sie das Rechenzentrum aus, in dem die Instanzen bereitgestellt werden sollen.</td>
    </tr>
    <tr>
    <td>Computing für Instanz</td>
    <td> Wählen Sie den Speicher und die CPU für jede Instanz in einer Bereitstellungsbestellung aus.</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> Wählen Sie den Arbeitsspeicher (Random Access Memory, RAM) für jede Instanz in einer Bereitstellungsbestellung aus.</td>
    </tr>
    <tr>
    <td>Betriebssystem</td>
    <td>Wählen Sie das Betriebssystem für die Instanz aus. Beachten Sie, dass eine Fehlernachricht ausgegeben wird, wenn ein Konflikt zwischen dem Server und dem Betriebssystem auftritt (z. B. beim Auswählen von Linux für einen Microsoft SQL-Server).</td>
    </tr>
    <tr>
    <td>Erster Plattenspeicher</td>
    <td>Wählen Sie für jede Instanz in einer Bestellung entweder 'SAN' oder 'Lokal' aus.</td>
    </tr>
    <tr>
    <td>Zusätzliche Plattenspeicher</td>
    <td>Sie können bis zu vier zusätzliche Bootdatenträger (SAN oder Lokal) für jede dedizierte Instanz bereitstellen.</td>
    </tr>
    <td>Netzoptionen</td>
    <td> Wählen Sie die geeigneten Optionen aus oder verwenden Sie die Standardwerte.</td>
    </tr>
    <tr>
    <td>Add-ons</td>
    <td> Wählen Sie die geeigneten Optionen aus oder verwenden Sie die Standardwerte.</td>
    </tr>
    <tr>
    </TBODY>
    </table> 

4.	Klicken Sie auf die Schaltfläche **Zur Bestellung hinzufügen**. Sie werden zur Seite 'Checkout' weitergeleitet.
5.  Geben Sie auf der Seite *Checkout* unter *Erweiterte Systemkonfiguration* die folgenden Informationen ein:

<table>
    <CAPTION>Tabelle 2. Erweiterte Systemkonfiguration für dedizierte Instanz</CAPTION>
    <THEAD>
    <TR>
    <th>Feld</th>
    <th>Wert</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>VLAN-Auswahl</td>
    <td>Fügen Sie den neuen Server zu einem VLAN unter Ihrem Konto hinzu, wenn Sie bereits mindestens einen Server bestellt haben.</td>
    </tr>
    <tr>
    <td>Bereitstellungsscripts</td>
    <td>Geben Sie ein Script an, mit dem bestimmte Schritte nach der Bereitstellung automatisiert werden können.</td>
    </tr>
    <tr>
    <td>SSH-Schlüssel</td>
    <td>Geben Sie einen öffentlichen Schlüssel für Ihren SSH-Schlüssel an, mit dem Sie sich bei Ihrem Server anmelden können, nachdem er bereitgestellt wurde.</td>
    </tr>
    <tr>
    <td>Benutzermetadaten</td>
    <td>Optionale Metadaten für angepasste Bereitstellungsscripts.</td>
    </tr>
    <tr>
    <td>Hostname</td>
    <td>Geben Sie einen permanenten oder temporären Namen für Ihren Server ein (z. B. server1).</td>
    </tr>
    <tr>
    <td>Domäne</td>
    <td>Geben Sie eine Unterdomäne ein, die nicht dem Namen einer Internetdomäne entspricht (z. B. test.acme.com).</td>
    </tr>
    </TBODY>
    </table>

6.  Klicken Sie auf die Kontrollkästchen **Bedingungen für Cloud-Service** und **Servicevereinbarung Dritter**.
7. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige bei Bedarf. Sie ist auch die Bestätigung für die Auftragsbestätigung für die Bereitstellung. 

    Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für Ihre Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu der zugehörigen Seite **Einheitendetails**, nachdem Sie sich bei {{site.data.keyword.Bluemix_notm}} angemeldet haben. Eine weitere Option ist die direkte Anmeldung beim {{site.data.keyword.slportal}}.

### Dedizierte Instanzen über das Menü 'Einheiten' bereitstellen

Die zweite Option ist das Bereitstellen Ihrer dedizierten Instanzen über das Menü **Einheiten** auf der Hauptseite des {{site.data.keyword.slportal}}s. Dieser Vorgang umfasst die folgenden Schritte.

1.	Klicken Sie auf **Einheiten > Einheitenliste**. 
 
    Auf der Seite *Einheiten* werden alle Einheitentypen in Ihrem Konto angezeigt (virtuelle Server, Bare-Metal-Server, dedizierte Hosts und NetScaler-Controller für Anwendungsbereitstellung). 

2.	Klicken Sie auf den Link **Einheiten bestellen** rechts auf der Seite.
    Das Fenster **SoftLayer-Produkt und Services bestellen** wird angezeigt.
3.	Führen Sie die Schritte unter [Dedizierte Instanzen über das Menü 'Einheiten' bereitstellen](#ordering-dedicated-devices-menu) ab Schritt 2 aus.

### Nächste Schritte
Nachdem Ihr virtueller Server bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [Virtuelle Server verwalten](../vsi/vsi_managing.html).
