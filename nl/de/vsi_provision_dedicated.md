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

# Dedizierte Hosts und Instanzen bereitstellen
{: #ordering-vs-dedicated}

Sie haben zwei Möglichkeiten zum Bereitstellen Ihrer dedizierten Instanzen. Die erste Möglichkeit ist die Verwendung des {{site.data.keyword.Bluemix}}-Katalogs und die zweite Möglichkeit ist das {{site.data.keyword.slportal_full}}. Für den Katalog und für das {{site.data.keyword.slportal}} sind eindeutige Anmelde-IDs erforderlich. Sie können sich folglich mit dem Benutzernamen und Kennwort für den Katalog nicht beim Portal anmelden oder umgekehrt. In der Dokumentation [Bei {{site.data.keyword.Bluemix_notm}} anmelden](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} finden Sie Informationen zum Einrichten von Berechtigungsnachweisen für den {{site.data.keyword.Bluemix_notm}}-Katalog bzw. für das {{site.data.keyword.slportal}}.
{:shortdesc}

## Beim IBM Cloud-Katalog anmelden
Führen Sie die folgenden Schritte aus, um sich beim {{site.data.keyword.Bluemix_notm}}-Katalog anzumelden und mit dem Bereitstellen Ihrer dedizierten Hosts und dedizierten Hostinstanzen zu beginnen. 

1. Öffnen Sie ein neues Browserfenster und geben Sie [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/){: new_window} ein.
2.	Klicken Sie auf den Link **Anmeldung** in der rechten oberen Ecke. 
3.	Geben Sie Ihre E-Mail-Adresse oder Ihre IBMiD ein und klicken Sie auf **Weiter**.
4.	Geben Sie Ihr Kennwort ein und klicken Sie auf **Anmelden**.
5.	Wählen Sie **Infrastruktur > Compute** aus.
6.  Klicken Sie auf die Kachel **Virtuelle Server**.
7.	Wählen Sie die Option **Dedizierte virtuelle Server** aus.
8.  Klicken Sie auf **Erstellen**. 

Die Hauptseite des {{site.data.keyword.slportal}}s wird angezeigt.

## Beim Kundenportal anmelden
Führen Sie die folgenden Schritte aus, um sich beim {{site.data.keyword.slportal}} anzumelden und die Bestellung für Ihre dedizierten Hosts und dedizierten Hostinstanzen zu erstellen.

1.	Öffnen Sie ein neues Browserfenster und geben Sie [https://control.softlayer.com](https://control.softlayer.com){: new_window} ein. 
2.	Geben Sie Ihren Benutzernamen und Ihr Kennwort ein und klicken Sie auf **Anmelden** ODER klicken Sie auf **Mit IBMiD anmelden**.
3.	Geben Sie Ihre E-Mail-Adresse oder Ihre IBMiD ein und klicken Sie auf **Weiter**.
4.	Geben Sie Ihr Kennwort ein und klicken Sie auf **Anmelden**.

Die Hauptseite des {{site.data.keyword.slportal}}s wird angezeigt.

## Dedizierten Host bereitstellen 
Führen Sie die folgenden Schritte aus, um Ihre dedizierten Hosts bereitzustellen.

1.	Klicken Sie auf das Symbol **Einheiten**.
2.  Klicken Sie auf den Link für **Dedizierter virtueller Server (Stündlich)** oder **Dedizierter virtueller Server (Monatlich)**. 

   **Hinweis:** Dedizierte Server sind private Server.

Die Seite *Cloud-Server konfigurieren* wird angezeigt. Auf dieser Seite können Sie eine dedizierte Instanz
bestellen, die entweder einem dedizierten Host zugeordnet ist oder nicht. Weitere Informationen zum Bestellen von Instanzen finden Sie unter [Dedizierte Hostinstanzen bereitstellen](#provision-dedicated-instances).

4.	Klicken Sie auf die Schaltfläche **Host erstellen** rechts im Formular.
5.	Geben Sie die folgenden Informationen ein:
    
    <table>
    <CAPTION>Tabelle 1. Auswahlen für die Bereitstellung dedizierter Hosts</CAPTION>
    <THEAD>
    <TR>
    <th>Feld</th>
    <th>Wert</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Menge</td>
    <td>Geben Sie an, wie viele dedizierte Hosts bestellt werden sollen. Beachten Sie, dass in jeder Bereitstellungsbestellung maximal zwei dedizierte Hosts bestellt werden können.</td>
    </tr>
    <tr>
    <td>Standort</td>
    <td>Wählen sie das {{site.data.keyword.cloud}}-Rechenzentrum aus, in dem Ihre Hosts platziert werden sollen. Die Liste der in Frage kommenden Rechenzentren finden Sie unter 'Informationen zu'.</td>
    </tr>
    <td>Dedizierter Host</td>
    <td>Die Standardeinstellung sind 56 Kerne X 242 RAM X 1,2 TB</td>
    </tr>
    </TBODY>
    </table>
    
    Die Zusammenfassung Ihrer Bestellung wird rechts neben der Seite *Konfiguration* angezeigt. 
    
6.  Klicken Sie auf die Schaltfläche **Zur Bestellung hinzufügen**.
7.  Bestätigen Sie Ihre Auswahlen auf der Seite *Checkout* und blättern Sie abwärts zu *Dedizierter Host - Erweiterte Systemkonfiguration*.
8.  Geben Sie die folgenden Informationen ein:

    <table>
    <CAPTION>Tabelle 2. Dedizierter Host - Erweiterte Systemkonfiguration</CAPTION>
    <THEAD>
    <TR>
    <th>Feld</th>
    <th>Wert</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>POD-Auswahl</td>
    <td>Klicken Sie auf die Dropdown-Liste und wählen Sie den POD aus, an dem Ihr dedizierter Host platziert werden soll.</td>
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

9.  Klicken Sie auf das Kontrollkästchen **Bedingungen für Cloud-Service**.
10. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige. Sie ist die

    Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für Ihre Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu der zugehörigen Seite **Einheitendetails**, nachdem Sie sich bei {{site.data.keyword.Bluemix_notm}} angemeldet haben. Eine weitere Option ist die direkte Anmeldung beim {{site.data.keyword.slportal}}.

## Dedizierte Hostinstanzen bereitstellen
{: #provision-dedicated-instances}
Sie können Ihre dedizierten Hostinstanzen auf zwei Arten bereitstellen: über das Menü **Einheiten** oder über das Symbol **Einheiten**.

### Dedizierte Hostinstanzen über das Menü 'Einheiten' bereitstellen
{: #ordering-dedicated-devices-menu}

Die erste Option ist das Bereitstellen Ihrer dedizierten Hostinstanzen über das Menü **Einheiten** auf der Hauptseite des {{site.data.keyword.slportal}}s. Dieser Prozess umfasst die folgenden Schritte.

1.	Klicken Sie auf **Einheiten > Einheitenliste**. 
 
    Auf der Seite *Einheiten* werden alle Einheitentypen in Ihrem Konto angezeigt (dedizierte Hosts, virtuelle Server, Bare-Metal-Server und NetScaler-Controller für Anwendungsbereitstellung). 

2.	Wählen Sie den Host für Ihre dedizierten Hostinstanzen durch Klicken auf den entsprechenden Link unter **Einheitenname** aus.
    
    Die Registerkarte **Konfiguration** auf der Seite *Einheitendetails* wird angezeigt. Auf der Registerkarte **Tickets** werden Ihre aktiven Support-Tickets aufgelistet; auf der Registerkarte **Zuordnungen** wird die Hauptspeichernutzung für Ihren ausgewählten Abrechnungszeitraum angezeigt. Weitere Informationen zu den Registerkarten finden Sie unter 'Über Einheitendetails Ihren dedizierten Hosts und Ihre Instanzen verwalten'.

3.	Blättern Sie abwärts zum Abschnitt **Instanzen**.

    Der Abrechnungsmodus für Ihren dedizierten Host (stündlich oder monatlich) legt die Abrechnung für Ihre dedizierten Hostinstanzen fest. Wenn Sie Hosts verwenden, die monatlich abgerechnet werden, können Sie dedizierte Hostinstanzen bereitstellen die auf Stundenbasis oder auf Monatsbasis abgerechnet werden. Beim Bereitstellen Ihrer Instanzen werden die beiden Links **Auf Stundenbasis hinzufügen** und **Auf Monatsbasis hinzufügen** angezeigt. Auf Stundenbasis abgerechnete Hosts können nur dedizierte Hostinstanzen bereitstellen, d. h. für sie wird nur der Link **Auf Stundenbasis hinzufügen** angezeigt. 

4.	Klicken Sie auf den Link **Auf Stundenbasis hinzufügen**, wenn Ihr Host stündlich oder monatlich abgerechnet wird. Klicken Sie auf den Link **Auf Monatsbasis hinzufügen**, wenn Ihr Host monatlich abgerechnet wird. Die Seite *Cloud-Server konfigurieren* wird wieder angezeigt. 

5.	Geben Sie die folgenden Informationen ein:
       
    <table>
    <CAPTION>Tabelle 3. Auswahlen für dedizierten Hostinstanzen</CAPTION>
    <THEAD>
    <TR>
    <th>Feld</th>
    <th>Wert</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Menge</td>
    <td>Die Anzahl der dedizierten Hostinstanzen, die auf einem einzigen Host implementiert werden sollen.</td>
    </tr>
    <tr>
    <td>Platzierung</td>
    <td>
    <ul>
    <li>Automatisch zuordnen – {{site.data.keyword.Bluemix_notm}} ordnet Ihre Instanz automatisch einem Host zu, d. h. Sie müssen den Host nicht selbst angeben. Ihre Instanz wird in einem Rechenzentrum platziert, das über freie Kapazität verfügt. Wenn Sie die Option für automatische Zuordnung verwenden, wird keine Kapazität auf Ihrem dedizierten Host belegt.</li>
    <li>Host angeben - Ihr dedizierter Host, der Ihrem Konto zugeordnet ist, wird unter 'Dedizierter Host' angezeigt. </li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Dedizierter Host</td>
    <td>Wählen Sie in der Liste den dedizierten Host aus, auf dem die Instanzen bereitgestellt werden sollen.</td>
    </tr>
    <tr>
    <td>Datenverarbeitungsinstanz</td>
    <td> Wählen Sie den Hauptspeicher und die CPU für jede Instanz in einer Bereitstellungsbestellung aus.</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> Wählen Sie den RAM für jede Instanz in einer Bereitstellungsbestellung aus.</td>
    </tr>
    <tr>
    <td>Betriebssystem</td>
    <td>Wählen Sie das Betriebssystem für die Instanz aus. Beachten Sie, dass eine Fehlernachricht ausgegeben wird, wenn ein Konflikt zwischen dem Server und dem Betriebssystem auftritt (z. B. beim Auswählen von Linux für einen Microsoft SQL-Server).</td>
    </tr>
    <tr>
    <td>Erster Datenträger</td>
    <td>Wählen Sie für jede Instanz in einer Bestellung entweder 'SAN' oder 'Lokal' aus.</td>
    </tr>
    <tr>
    <td>Weitere Datenträger</td>
    <td>Sie können bis zu vier zusätzliche Bootdatenträger (SAN oder Lokal) für jede dedizierte Hostinstanz bereitstellen.</td>
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

6.	Klicken Sie auf die Schaltfläche **Zur Bestellung hinzufügen**.
7.  Geben Sie auf der Seite *Checkout* unter *Erweiterte Systemkonfiguration* die folgenden Informationen ein:

<table>
    <CAPTION>Tabelle 4. Dedizierte Hostinstanz - Erweiterte Systemkonfiguration</CAPTION>
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

8.  Klicken Sie auf die Kontrollkästchen **Bedingungen für Cloud-Service** und **Servicevereinbarung Dritter**.
9. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige. Sie ist die Auftragsbestätigung für Ihre Bereitstellungsbestellung.


Sie werden per E-Mail benachrichtigt, sobald Ihre dedizierten Hostinstanzen bereitgestellt sind.

### Dedizierte Hostinstanzen über das Symbol 'Einheiten' bereitstellen
Die zweite Option zum Bereitstellen dedizierter Hostinstanzen ist die Verwendung des Symbols **Einheiten** auf der Startseite des {{site.data.keyword.slportal}}s. Dieser Prozess umfasst die folgenden Schritte.

1.	Klicken Sie auf das Symbol **Einheiten** und wählen Sie die Option **Stündlich** oder **Monatlich** unter 'Dedizierte virtuelle Server' aus.
2.	Führen Sie die Schritte unter [Dedizierte Hostinstanzen über das Menü 'Einheiten' bereitstellen](#ordering-dedicated-devices-menu) ab Schritt 5 aus.

### Nächste Schritte
Nachdem Ihr virtueller Server bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [Virtuelle Server verwalten](../vsi/vsi_managing.html).


