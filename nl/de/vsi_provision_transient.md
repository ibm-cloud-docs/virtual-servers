---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Transiente Instanzen bereitstellen
{: #ordering-vs-transient}
Sie können Ihre transienten virtuellen Serverinstanzen über den {{site.data.keyword.cloud}}-Katalog oder das {{site.data.keyword.slportal}} bereitstellen.
{:shortdesc}

## Vorbereitungen
Überprüfen Sie die folgenden Voraussetzungen, bevor Sie beginnen.

  1. Stellen Sie sicher, dass Sie über gültige Berechtigungsnachweise für den {{site.data.keyword.cloud_notm}}-Katalog oder für das {{site.data.keyword.slportal}} verfügen.

  **Hinweis:** Sie müssen über ein aktualisiertes Konto für den {{site.data.keyword.Bluemix_notm}}-Katalog verfügen, um virtuelle Server zu bestellen. Weitere Informationen zum Aktualisieren Ihres Kontos finden Sie unter [Zur IBMid wechseln](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).

  2. Überprüfen Sie die Überlegungen zur Kapazität der virtuellen Serverinstanz. Weitere Informationen finden Sie unter [Überlegungen zur Kapazität](/docs/vsi?topic=virtual-servers-capacity-considerations).

## Transiente virtuelle Serverinstanz bereitstellen
Wenn die Voraussetzungen erfüllt sind, können Sie mit dem Bereitstellen einer transienten virtuellen Serverinstanz beginnen. Sie können die Instanz über den {{site.data.keyword.cloud_notm}}-Katalog oder das {{site.data.keyword.slportal}} bereitstellen.

### Transiente virtuelle Serverinstanzen über den IBM Cloud-Katalog bereitstellen
Führen Sie die folgenden Schritte aus, um eine transiente virtuelle Serverinstanz über den {{site.data.keyword.cloud_notm}}-Katalog bereitzustellen:

  1. Melden Sie sich beim [{{site.data.keyword.cloud_notm}}-Katalog ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/catalog/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an.  
  2. Klicken Sie im Bereich für die Datenverarbeitungsinfrastruktur**** auf die Kachel **Virtuelle Server**.
  3. Wählen Sie die Option **Transienter virtueller Server** aus.
  4. Klicken Sie auf **Erstellen**.
  5. Geben Sie alle relevanten Informationen für die virtuelle Serverinstanz an.
  6. Überprüfen Sie die Bestellübersicht und klicken Sie auf das Kontrollkästchen für Servicevereinbarungen anderer Anbieter****.
  7. Klicken Sie auf **Bereitstellen**.

### Transiente virtuelle Serverinstanzen über das Kundenportal bereitstellen
Führen Sie die folgenden Schritte aus, um eine transiente virtuelle Serverinstanz über das {{site.data.keyword.slportal}} bereitzustellen:

  1. Melden Sie sich beim [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an.
  2. Suchen Sie den Bereich **Bestellung** und klicken Sie auf **Einheiten**.
  3. Klicken Sie unter *Öffentlicher virtueller Server* auf der Seite *Einheiten* auf **Transient** für das Angebot für virtuelle Server.
  4. Geben Sie auf der Seite *Cloud-Server konfigurieren* alle relevanten Informationan an.
  5. Klicken Sie auf **Zur Bestellung hinzufügen**, um fortzufahren.
  6. Bestätigen oder bearbeiten Sie die Domäneninformationen für den Server.
  7. Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
  8. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige bei Bedarf. Sie ist auch die Bestätigung für die Auftragsbestätigung für die Bereitstellung.

 Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der E-Mail, die die Fertigstellung der Bereitstellung mitteilt, gelangen Sie zu Ihrer Seite *Einheitendetails*.

Sie können einen transienten virtuellen Server auch mithilfe der {{site.data.keyword.slapi_short}} bereitstellen. Ein Beispiel finden Sie unter [Transiente Instanz mit dem Objekt 'create' bereitstellen](/docs/vsi?topic=virtual-servers-api-rest-public#api-rest-transient).
{:tip}

## Nächste Schritte
Nachdem Ihr virtueller Server bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [Virtuellen Server verwalten](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
