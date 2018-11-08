---

copyright:
  years: 2016, 2018

lastupdated: "2018-09-12"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Activity Tracker-Ereignisse 
{: #at_events}

Als Sicherheitsbeauftragter, Auditor oder Manager können Sie mit dem Service '{{site.data.keyword.cloudaccesstrailfull}}' die Interaktion
von Benutzern und Anwendungen mit virtuellen Serverinstanzen in {{site.data.keyword.Bluemix}} verfolgen. Der Kontoeigner sowie Benutzer, die
mit dem Konto verknüpft sind, können Ereignisse für virtuelle Server auslösen, die in {{site.data.keyword.cloudaccesstrailshort}} angemeldet sind.
{:shortdesc}

Über den Service '{{site.data.keyword.cloudaccesstrailshort}}' werden von Benutzern initiierte Aktivitäten aufgezeichnet, die den Status eines Service in
{{site.data.keyword.Bluemix_notm}} ändern. Weitere Informationen finden Sie im Abschnitt mit [Informationen zu {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov ).

Weitere Informationen zum Einstieg in die Überwachung von Benutzeraktionen finden Sie in [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla). 

Ereignisse können von einem Benutzer, einem Service oder einer Anwendung initiiert werden. Benutzer können Ereignisse nur generieren, wenn sie über einen Zugriff auf ****Infrastrukturressourcen in der {{site.data.keyword.Bluemix}}-Konsole verfügen. 
{: tip}

## Anmeldeereignisse
{: #login}

Die folgende Tabelle enthält die Aktion, über die ein Anmeldeereignis generiert wird:

| Aktion | Beschreibung |
|----------|---------|
| `audit-log.user.login`  | Ein Ereignis wird generiert, wenn sich ein Initiator über die {{site.data.keyword.Bluemix}}-UI oder das {{site.data.keyword.slportal}} in {{site.data.keyword.Bluemix}} anmeldet. | 
{: caption="Tabelle 1. Anmeldeaktion" caption-side="top"} 


## Ereignisse für virtuelle Serverinstanzen
{: #vsi}

Sie können während des gesamten Lebenszyklus einer virtuellen Serverinstanz (VSI) mit dem Service '{{site.data.keyword.cloudaccesstrailshort}}' ein Audit durchführen.

In der folgenden Tabelle werden die Aktionen aufgeführt, über die ein Ereignis generiert wird:

| Aktion | Beschreibung |
|----------|---------|
| `audit-log.vsi.provision`             | Ein Ereignis wird generiert, wenn ein Initiator eine VSI bereitstellt.  | 
| `audit-log.vsi-port.disable`          | Ein Ereignis wird generiert, wenn ein Initiator einen Port in einer VSI inaktiviert. | 
| `audit-log.vsi-port.enable`           | Ein Ereignis wird generiert, wenn ein Initiator einen Port in einer VSI aktiviert. | 
| `audit-log.vsi-port-speed.update`     | Ein Ereignis wird generiert, wenn ein Initiator die Portgeschwindigkeit in einer VSI aktualisiert. |
| `audit-log.vsi-image-template.create` | Ein Ereignis wird generiert, wenn ein Initiator eine Imagevorlage für eine VSI erstellt.  |
| `audit-log.vsi.power-off`             | Ein Ereignis wird generiert, wenn ein Initiator eine VSI ausschaltet.  |
| `audit-log.vsi.soft-power-off`        | Ein Ereignis wird generiert, wenn ein Initiator eine normale Abschaltung einer VSI durchführt. |
| `audit-log.vsi.force-power-off`       | Ein Ereignis wird generiert, wenn ein Initiator eine erzwungene Abschaltung einer VSI durchführt. |
| `audit-log.vsi.reboot`                | Ein Ereignis wird generiert, wenn ein Initiator eine VSI neu startet. | 
| `audit-log.vsi.soft-reboot`           | Ein Ereignis wird generiert, wenn ein Initiator einen Warmstart für eine VSI durchführt. | 
| `audit-log.vsi.hard-reboot`           | Ein Ereignis wird generiert, wenn ein Initiator einen Kaltstart für eine VSI durchführt. | 
| `audit-log.vsi.power-on`              | Ein Ereignis wird generiert, wenn ein Initiator eine VSI einschaltet. | 
| `audit-log.vsi.rename`                | Ein Ereignis wird generiert, wenn ein Initiator eine VSI umbenennt. | 
| `audit-log.vsi.rescue`                | Ein Ereignis wird generiert, wenn ein Initiator eine Rettungsaktion für eine VSI durchführt. | 
| `audit-log.vsi-security-group.add`    | Ein Ereignis wird generiert, wenn ein Initiator eine Sicherheitsgruppe zu einer VSI hinzufügt. | 
| `audit-log.vsi-security-group.remove` | Ein Ereignis wird generiert, wenn ein Initiator eine Sicherheitsgruppe in einer VSI entfernt. | 
| `audit-log.vsi.reload`                | Ein Ereignis wird generiert, wenn ein Initiator das Betriebssystem für eine VSI erneut lädt. | 
| `audit-log.vsi.boot`                  | Ein Ereignis wird generiert, wenn ein Initiator eine VSI über ein Image bootet. | 
| `audit-log.vsi.reclaim`               | Ein Ereignis wird generiert, wenn ein Initiator den Betrieb einer VSI abbricht. | 
| `audit-log.vsi.pause`                 | Ein Ereignis wird generiert, wenn ein Initiator den Betrieb einer VSI unterbricht. | 
{: caption="Tabelle 2. VSI-Aktionen" caption-side="top"} 



## Ereignisse anzeigen
{: #ui}

Die {{site.data.keyword.cloudaccesstrailshort}}-Ereignisse stehen in der {{site.data.keyword.cloudaccesstrailshort}}-**Kontodomäne** zur
Verfügung, die in der {{site.data.keyword.Bluemix_notm}}-Region verfügbar ist, in der die Ereignisse generiert wurden. Weitere Informationen hierzu finden Sie im Abschnitt [Kontoereignisse
anzeigen](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events).

{{site.data.keyword.cloudaccesstrailshort}}-Ereignisse werden automatisch an den Service '{{site.data.keyword.cloudaccesstrailshort}}'
in der Region weitergeleitet, in der die Aktion stattgefunden hat.
