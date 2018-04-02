---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


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
Sie können Ihre transienten virtuellen Serverinstanzen über das {{site.data.keyword.slportal_full}} bereitstellen.
{:shortdesc}

## Vorbereitungen
Überprüfen Sie die folgenden Voraussetzungen, bevor Sie beginnen.

  1. Stellen Sie sicher, dass Sie über gültige Berechtigungsnachweise für das {{site.data.keyword.slportal}} verfügen.

  2. Überprüfen Sie die Überlegungen zur Kapazität der virtuellen Serverinstanz.  Weitere Informationen finden Sie unter [Überlegungen zur Kapazität](ts_capacity_bp.html).

## Anmelden
Stellen Sie sicher, dass Sie beim {{site.data.keyword.slportal}} angemeldet sind:

  1. Öffnen Sie das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window}, indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben.

Die Hauptseite des {{site.data.keyword.slportal}}s wird geöffnet.

## Transiente virtuelle Serverinstanz bereitstellen
{: #ordering-transient-instance}
Nachdem Sie die Voraussetzungen erfüllt haben, stellen Sie eine transiente virtuelle Serverinstanz bereit. Sie können Ihre transienten Instanzen auf zwei Arten bereitstellen: über das Menü **Einheiten** oder das Symbol **Einheiten**.

### Transiente virtuelle Serverinstanz über das Symbol 'Einheiten' bereitstellen
Führen Sie die folgenden Schritte aus, um Ihre transiente virtuelle Serverinstanz über das Symbol *Einheiten* bereitzustellen:

1.  Suchen Sie im {{site.data.keyword.slportal}} den Abschnitt **Bestellung** und klicken Sie auf **Einheiten**.
2.  Klicken Sie unter *Öffentlicher virtueller Server* auf der Seite *Einheiten* auf **Transient** für das Angebot für virtuelle Server.
3.  Geben Sie auf der Seite *Cloud-Server konfigurieren* alle relevanten Informationan an.
4.  Klicken Sie auf **Zur Bestellung hinzufügen**, um fortzufahren.
5.  Bestätigen oder bearbeiten Sie die Domäneninformationen für den Server.
5.  Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
6.  Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Sie können diese Anzeige drucken. Sie ist die Auftragsbestätigung für Ihre Bereitstellung.

 Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der E-Mail, die die Fertigstellung der Bereitstellung mitteilt, gelangen Sie zu Ihrer Seite *Einheitendetails*.

### Transiente virtuelle Serverinstanz über das Menü 'Einheiten' bereitstellen
{: #ordering-transient-devices-menu}

Sie können Ihre transienten virtuellen Serverinstanzen auch über das Menü *Einheiten* auf der Hauptseite des {{site.data.keyword.slportal}}s bereitstellen.

1. Klicken Sie auf **Einheiten > Einheitenliste**.

   Auf der Seite 'Einheiten' werden alle Enheitentypen in Ihrem Konto angezeigt (dedizierte Hosts, virtuelle Server, Bare-Metal-Server und NetScaler-Controller für Anwendungsbereitstellung).
2. Klicken Sie auf den Link **Einheiten bestellen** in der rechten oberen Ecke.
3. Klicken Sie unter *Öffentlicher virtueller Server* auf der Seite *Einheiten* auf **Transient** für das Angebot für virtuelle Server.
4. Geben Sie auf der Seite *Cloud-Server konfigurieren* alle relevanten Informationan an.
5. Klicken Sie auf **Zur Bestellung hinzufügen**, um fortzufahren.
6. Bestätigen oder bearbeiten Sie die Domäneninformationen für den Server.
7. Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
8. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Sie können diese Anzeige drucken. Sie ist die Auftragsbestätigung für Ihre Bereitstellung.

Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der E-Mail, die die Fertigstellung der Bereitstellung mitteilt, gelangen Sie zu Ihrer Seite *Einheitendetails*.

Sie können einen transienten virtuellen Server auch mithilfe der {{site.data.keyword.slapi_short}} bereitstellen. Ein Beispiel finden Sie unter [Transiente Instanz mit dem Objekt 'create' bereitstellen](../vsi/vsi_provision_api.html#api-rest-transient).
{:tip}

## Nächste Schritte
Nachdem Ihr virtueller Server bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [Virtuellen Server verwalten](../vsi/vsi_managing.html).
