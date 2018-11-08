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


# Eventi del programma di traccia dell'attività 
{: #at_events}

In qualità di responsabile della sicurezza, revisore o gestore, puoi utilizzare il servizio {{site.data.keyword.cloudaccesstrailfull}} per tracciare come gli utenti e le applicazioni interagiscono con
le istanze del server virtuale (VSI) in {{site.data.keyword.Bluemix}}. Il proprietario dell'account e gli utenti collegati
all'account possono attivare gli eventi del server virtuale registrati in {{site.data.keyword.cloudaccesstrailshort}}.
{:shortdesc}

Il servizio {{site.data.keyword.cloudaccesstrailshort}} registra le attività avviate dall'utente che modificano lo stato di un servizio in
{{site.data.keyword.Bluemix_notm}}. Per ulteriori informazioni, vedi
[Informazioni su {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov ).

Per iniziare a monitorare le azioni del tuo utente, vedi
[{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla). 

Un iniziatore può essere un utente, un servizio o un'applicazione. Perché un utente possa generare gli eventi, deve avere l'accesso alle risorse dell'**Infrastruttura** nella console {{site.data.keyword.Bluemix}}. 
{: tip}

## Eventi di accesso
{: #login}

La seguente tabella elenca l'azione che genera un evento di accesso:

| Azione | Descrizione |
|----------|---------|
| `audit-log.user.login`  | Viene generato un evento quando un iniziatore accede a {{site.data.keyword.Bluemix}} tramite l'IU {{site.data.keyword.Bluemix}} o {{site.data.keyword.slportal}}. | 
{: caption="Tabella 1. Azione di accesso" caption-side="top"} 


## Eventi dell'istanza del server virtuale
{: #vsi}

Puoi controllare un'istanza del server virtuale (VSI) attraverso il suo ciclo di vita utilizzando il servizio {{site.data.keyword.cloudaccesstrailshort}}.

La seguente tabella elenca le azioni che generano un evento:

| Azione | Descrizione |
|----------|---------|
| `audit-log.vsi.provision`             | Viene generato un evento quando un iniziatore esegue il provisioning di una VSI.  | 
| `audit-log.vsi-port.disable`          | Viene generato un evento quando un iniziatore disabilita una porta in una VSI. | 
| `audit-log.vsi-port.enable`           | Viene generato un evento quando un iniziatore abilita la porta in una VSI. | 
| `audit-log.vsi-port-speed.update`     | Viene generato un evento quando un iniziatore aggiorna la velocità della porta in una VSI. |
| `audit-log.vsi-image-template.create` | Viene generato un evento quando un iniziatore crea un template di immagini per una VSI.  |
| `audit-log.vsi.power-off`             | Viene generato un evento quando un iniziatore disattiva una VSI.  |
| `audit-log.vsi.soft-power-off`        | Viene generato un evento quando un iniziatore esegue un arresto semplice di una VSI. |
| `audit-log.vsi.force-power-off`       | Viene generato un evento quando un iniziatore forza un arresto di una VSI. |
| `audit-log.vsi.reboot`                | Viene generato un evento quando un iniziatore riavvia una VSI. | 
| `audit-log.vsi.soft-reboot`           | Viene generato un evento quando un iniziatore esegue un riavvio semplice di una VSI. | 
| `audit-log.vsi.hard-reboot`           | Viene generato un evento quando un iniziatore esegue un riavvio forzato di una VSI. | 
| `audit-log.vsi.power-on`              | Viene generato un evento quando un iniziatore attiva una VSI. | 
| `audit-log.vsi.rename`                | Viene generato un evento quando un iniziatore ridenomina una VSI. | 
| `audit-log.vsi.rescue`                | Viene generato un evento quando un iniziatore recupera una VSI. | 
| `audit-log.vsi-security-group.add`    | Viene generato un evento quando un iniziatore aggiunge un gruppo di sicurezza a una VSI. | 
| `audit-log.vsi-security-group.remove` | Viene generato un evento quando un iniziatore rimuove un gruppo di sicurezza da una VSI. | 
| `audit-log.vsi.reload`                | Viene generato un evento quando un iniziatore esegue un ricaricamento del sistema operativo (SO) di una VSI. | 
| `audit-log.vsi.boot`                  | Viene generato un evento quando un iniziatore avvia una VSI da un'immagine. | 
| `audit-log.vsi.reclaim`               | Viene generato un evento quando un iniziatore annulla una VSI. | 
| `audit-log.vsi.pause`                 | Viene generato un evento quando un iniziatore mette in pausa una VSI. | 
{: caption="Tabella 2. Azioni VSI" caption-side="top"} 



## Visualizzazione degli eventi
{: #ui}

Gli eventi {{site.data.keyword.cloudaccesstrailshort}} sono disponibili nel **dominio dell'account** {{site.data.keyword.cloudaccesstrailshort}}
disponibile nella regione {{site.data.keyword.Bluemix_notm}} in cui vengono generati gli eventi. Per ulteriori informazioni, consulta [Visualizzazione degli
eventi dell'account](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events).

Gli eventi {{site.data.keyword.cloudaccesstrailshort}} vengono inoltrati automaticamente al servizio {{site.data.keyword.cloudaccesstrailshort}}
nella stessa regione in cui si è verificata l'azione.
