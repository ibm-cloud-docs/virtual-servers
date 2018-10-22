---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-03"


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
Sie haben zwei Möglichkeiten, um Ihre öffentlichen virtuellen Serverinstanzen bereitzustellen. Die erste Möglichkeit ist die Verwendung des {{site.data.keyword.Bluemix}}-Katalogs und die zweite Möglichkeit ist das {{site.data.keyword.slportal}}. Für den Katalog und für das {{site.data.keyword.slportal}} sind eindeutige Anmelde-IDs erforderlich. Sie können sich mit dem Benutzernamen und Kennwort für den Katalog daher nicht beim Portal anmelden und umgekehrt.
{:shortdesc}

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie beginnen.

  1. Stellen Sie sicher, dass Sie über gültige Berechtigungsnachweise für den {{site.data.keyword.Bluemix_notm}}-Katalog oder für das {{site.data.keyword.slportal}} verfügen.

     **Hinweis:** Sie müssen über ein aktualisiertes Konto für den {{site.data.keyword.Bluemix_notm}}-Katalog verfügen, um virtuelle Server zu bestellen. Weitere Informationen zum Aktualisieren Ihres Kontos finden Sie unter [Zur IBMid wechseln](https://console.bluemix.net/docs/admin/softlayerlink.html).

  2. Machen Sie sich mit den Bereitstellungsoptionen vertraut, die Ihnen zur Verfügung stehen (falls dies noch nicht geschehen ist). Weitere Informationen finden Sie unter [Bereitstellungsoptionen: Öffentlicher virtueller Server](../vsi/vsi_public.html).

  3. Überprüfen Sie die Überlegungen zur Kapazität der virtuellen Serverinstanz.  Weitere Informationen finden Sie unter [Überlegungen zur Kapazität](ts_capacity_bp.html).

## Öffentliche virtuelle Serverinstanz bereitstellen
{: #ordering-public-instance}

Wenn die Voraussetzungen erfüllt sind, können Sie mit dem Bereitstellen einer öffentlichen virtuellen Serverinstanz beginnen. Sie können die öffentliche Instanz über den {{site.data.keyword.cloud_notm}}-Katalog oder das {{site.data.keyword.slportal}} bereitstellen.

### Öffentliche virtuelle Serverinstanz über den IBM Cloud-Katalog bereitstellen
Führen Sie die folgenden Schritte aus, um eine öffentliche virtuelle Serverinstanz über {{site.data.keyword.cloud_notm}} bereitzustellen:

  1. Melden Sie sich beim [{{site.data.keyword.cloud_notm}}-Katalog ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/catalog/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an. 
  2. Klicken Sie im Bereich für die Datenverarbeitungsinfrastruktur**** auf die Kachel **Virtuelle Server**.
  3. Wählen Sie die Option **Öffentlicher virtueller Server** aus.
  4. Klicken Sie auf **Erstellen**.
  5. Geben Sie alle relevanten Informationen für die virtuelle Serverinstanz an. 
  6. Überprüfen Sie die Bestellübersicht und klicken Sie auf das Kontrollkästchen für Servicevereinbarungen anderer Anbieter****. 
  7. Klicken Sie auf **Bereitstellen**.
  
### Öffentliche virtuelle Serverinstanz über das Kundenportal bereitstellen
Führen Sie die folgenden Schritte aus, um Ihre öffentliche virtuelle Serverinstanz über das {{site.data.keyword.slportal}} bereitzustellen:

  1. Melden Sie sich beim [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an.
  2. Suchen Sie den Bereich **Bestellung** und klicken Sie auf **Einheiten**. 
  3. Klicken Sie auf der Seite 'Einheiten' auf **Stündliches SAN**, **Stündlich lokal**, **Monatlich** oder **Transient** für eines der Angebote für virtuelle Server.
  4. Geben Sie auf der Seite *Cloud-Server konfigurieren* alle relevanten Informationan an.
  5. Klicken Sie auf die Schaltfläche **Zur Bestellung hinzufügen**, um fortzufahren.
  6. Bestätigen oder bearbeiten Sie die Domäneninformationen für den Server.
  7. Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
  8. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige bei Bedarf. Sie ist auch die Bestätigung für die Auftragsbestätigung für die Bereitstellung. 

 Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu der zugehörigen Seite *Einheitendetails*, nachdem Sie sich bei {{site.data.keyword.Bluemix_notm}} angemeldet haben. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.

## Nächste Schritte
Nachdem Ihr virtueller Server bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [Virtuellen Server verwalten](../vsi/vsi_managing.html).
