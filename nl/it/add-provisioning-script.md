---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestione degli script di provisioning
{: #managing-a-provisioning-script}

Puoi utilizzare gli script di provisioning per specificare un URL di uno script che viene eseguito su un dispositivo di cui è appena stato eseguito il provisioning. Gli script di provisioning possono essere un qualsiasi file che può essere eseguito dal sistema operativo (SO), inclusi i file binari combinati o qualsiasi linguaggio supportato dal SO. Non hai limitazioni per il nome dello script; tuttavia, l'utilizzo di una convezione di denominazione simile per ogni script rende più facile l'identificazione. Gli script di provisioning devono essere associati a un nome del dominio completo e accessibili utilizzando i protocolli HTTP e HTTPS. Il tipo di protocollo utilizzato influenza la risposta automatizzata del sistema quando viene scaricato lo script di provisioning sul dispositivo.  
{:shortdesc}

* L'utilizzo del **protocollo HTTP** richiede che un amministratore esegua lo script manualmente dopo che è stato scaricato.
* L'utilizzo del **protocollo HTTPS** scarica ed esegue lo script automaticamente, se possibile. Se l'URL non è associato a uno script valido, lo script viene scaricato e non deve essere effettuata alcuna altra azione.

## Informazioni preliminari
Per prima cosa passa al menu del dispositivo e assicurati di disporre delle autorizzazioni account corrette per completare le attività.  

* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assicurati di avere tutte le autorizzazioni account necessarie e l'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione dell'infrastruttura classica **Manage Users**, può modificare le autorizzazioni.  

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione accesso dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access). 

## Aggiunta di uno script di provisioning
{: #add-provisioning-script}

1. Dal menu **Devices**, seleziona **Manage > Provisioning Scripts**.
2. Seleziona **Add Provisioning Script**. 
3. Immetti un nome di identificazione per lo script di provisioning nel campo **Name**.
4. Immetti il nome del dominio completo associato allo script nel campo **URL**.
5. Fai clic su **Add** per aggiungere lo script di provisioning all'account. 

## Modifica dei dettagli dello script di provisioning
{: #edit-provisioning-script-details}

1. Dal menu **Devices**, seleziona **Manage > Provisioning Scripts**.
2. Fai clic in un qualsiasi punto nella colonna **Name** o **URL** dello script di provisioning per aprire lo script per la modifica. 
3. Aggiorna il nome o l'URL.
   Quando aggiorni un URL, devi utilizzare un nome del dominio completo o la modifica non viene salvata.
   {:note}
4. Fai clic in un qualsiasi punto nella schermata per salvare la modifica.

## Passi successivi

Gli script di provisioning associati a un account possono essere modificati o rimossi in qualsiasi momento. Gli script di provisioning vengono salvati nella console {{site.data.keyword.cloud_notm}} finché non vengono rimossi e possono essere associati a un nuovo dispositivo ordinato tramite la console {{site.data.keyword.cloud_notm}}. Se lo script viene associato a un URL HTTP, viene scaricato nel nuovo dispositivo durante il provisioning e l'amministratore deve accedere al dispositivo ed eseguire lo script manualmente. Gli script associati agli URL HTTP vengono scaricati e, quando applicabile, eseguiti nel nuovo dispositivo senza la necessità di ulteriori interazioni. 

Se modifichi uno script, gli aggiornamenti validi vengono visualizzati nella schermata immediatamente. Le modifiche apportate agli script di provisioning esistenti non influenzano i dispositivi già forniti.

