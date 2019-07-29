---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Dedizierte Instanzen bereitstellen
{: #provisioning-dedicated-instances}

Sie haben zwei Möglichkeiten zum Bereitstellen Ihrer dedizierten Instanzen. Die erste Möglichkeit ist die Verwendung des {{site.data.keyword.Bluemix}}-Katalogs und die zweite Möglichkeit ist das {{site.data.keyword.slportal_full}}. Für den Katalog und für das {{site.data.keyword.slportal}} sind eindeutige Anmelde-IDs erforderlich. Sie können sich folglich mit dem Benutzernamen und Kennwort für den Katalog nicht beim Portal anmelden oder umgekehrt. [Bei {{site.data.keyword.Bluemix_notm}} registrieren](/docs/account?topic=account-signup#signup) enthält Informationen zum Einrichten des {{site.data.keyword.Bluemix_notm}}-Katalogs oder der {{site.data.keyword.slportal}}-Berechtigungsnachweise.
{:shortdesc}

## Dedizierte virtuelle Serverinstanzen bereitstellen
{: #provision-dedicated-instances}
Sie können die dedizierte virtuelle Serverinstanz über den {{site.data.keyword.cloud_notm}}-Katalog oder das {{site.data.keyword.slportal}} bereitstellen.

### Dedizierte virtuelle Serverinstanz über den IBM Cloud-Katalog bereitstellen
Führen Sie die folgenden Schritte aus, um eine dedizierte virtuelle Serverinstanz über den {{site.data.keyword.cloud_notm}}-Katalog bereitzustellen:

  1. Melden Sie sich beim [{{site.data.keyword.cloud_notm}}-Katalog ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/catalog/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an.
  2. Klicken Sie im Bereich für die Datenverarbeitungsinfrastruktur**** auf die Kachel **Virtuelle Server**.
  3. Wählen Sie die Option **Dedizierter virtueller Server** aus.
  4. Klicken Sie auf **Erstellen**.
  5. Wählen Sie im Abschnitt **Dedizierter Host** die Option **Automatisch zuweisen** aus. Daraufhin weist {{site.data.keyword.cloud_notm}} die Instanz automatisch einem Host im ausgewählten Rechenzentrum zu.

     **Hinweis**: Wählen Sie für dedizierte Hosts **Host angeben** oder **Host erstellen** aus. Weitere Informationen zu dedizierten Hosts und Hostinstanzen finden Sie in [Dedizierte virtuelle Server](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers).

  5. Geben Sie alle relevanten Informationen für die dedizierte virtuelle Serverinstanz an.
  6. Überprüfen Sie die Bestellübersicht und klicken Sie auf das Kontrollkästchen für Servicevereinbarungen anderer Anbieter****.
  7. Klicken Sie auf **Bereitstellen**.

### Dedizierte virtuelle Serverinstanz über das Kundenportal bereitstellen
Führen Sie die folgenden Schritte aus, um eine dedizierte virtuelle Serverinstanz über das {{site.data.keyword.slportal}} bereitzustellen:

1. Melden Sie sich beim [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an.
2. Suchen Sie den Bereich **Bestellung** und klicken Sie auf **Einheiten**. Das Fenster **SoftLayer-Produkt und Services bestellen** wird angezeigt.
3.  Wählen Sie unter 'Dedizierte virtuelle Server' die Option **Stündlich** oder **Monatlich** aus. Die Seite *Cloud-Server konfigurieren* wird wieder angezeigt.

4.	Geben Sie die folgenden Informationen ein:

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
    <li>Host angeben – Wird bei dedizierten Hostinstanzen verwendet. Weitere Informationen zu dedizierten Hosts und dedizierten Hostinstanzen finden Sie in [Dedizierte virtuelle Server](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers).</li>
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
    <td>Erster Datenträger</td>
    <td>Wählen Sie für jede Instanz in einer Bestellung entweder 'SAN' oder 'Lokal' aus.</td>
    </tr>
    <tr>
    <td>Zusätzliche Datenträger</td>
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

5.	Klicken Sie auf die Schaltfläche **Zur Bestellung hinzufügen**. Sie werden zur Seite 'Checkout' weitergeleitet.
6.  Geben Sie auf der Seite *Checkout* unter *Erweiterte Systemkonfiguration* die folgenden Informationen ein:

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

7.  Klicken Sie auf die Kontrollkästchen **Bedingungen für Cloud-Service** und **Servicevereinbarung Dritter**.
8. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige bei Bedarf. Sie ist auch die Bestätigung für die Auftragsbestätigung für die Bereitstellung.

    Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für Ihre Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu der zugehörigen Seite **Einheitendetails**, nachdem Sie sich bei {{site.data.keyword.Bluemix_notm}} angemeldet haben. Eine weitere Option ist die direkte Anmeldung beim {{site.data.keyword.slportal}}.

## Nächste Schritte
Nachdem Ihr virtueller Server bereitgestellt wurde und verfügbar ist, können Sie Ihre virtuellen Server über das
{{site.data.keyword.slportal_full}} oder über die {{site.data.keyword.slapi_full}} konfigurieren. Weitere Informationen finden Sie unter [Virtuelle Server konfigurieren](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
