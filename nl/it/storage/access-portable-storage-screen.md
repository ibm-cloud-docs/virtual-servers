---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# Gestione dell'archiviazione portatile
{: #accessing-portable-storage}

I volumi di archiviazione portatile (PSV) sono una soluzione di archiviazione ausiliaria disponibile solo per {{site.data.keyword.virtualmachinesshort}}. Nella console {{site.data.keyword.cloud}}, puoi accedere ai volumi di archiviazione portatile e visualizzare tutti i PSV. Puoi anche collegare, scollegare, scambiare e modificare i volumi.
{:shortdesc}

Non puoi collegare o scambiare i volumi di archiviazione portatile per un'istanza del server virtuale di cui è stato eseguito il provisioning da un template dell'immagine crittografato.
{:note}

## Informazioni preliminari
Per prima cosa passa al menu dell'archiviazione o dei dispositivi e assicurati di disporre delle autorizzazioni account corrette per completare le attività. 

* Passa al menu del dispositivo o dell'archiviazione della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assicurati di avere tutte le autorizzazioni account necessarie e l'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione dell'infrastruttura classica **Manage Users**, può modificare le autorizzazioni.

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione accesso dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Collegamento dell'archiviazione portatile

1. Dal menu **Storage**, seleziona **Block Storage.**
2. Nella sezione **Portable storage**, seleziona l'opzione di collegamento per l'archiviazione portatile che vuoi utilizzare.
3. Nella schermata successiva, scegli il dispositivo che necessita dell'archiviazione e seleziona **Attach**.

## Gestione dell'archiviazione portatile collegata a un server

L'archiviazione portatile collegata a un server è elencata nella pagina *Device Details* del server.

1. Dal menu **Devices**, seleziona **Device List**.
2. Da **Device List**, seleziona l'istanza del server virtuale per visualizzarne i dettagli.
3. Fai clic sulla scheda **Storage** per visualizzare l'archiviazione portatile attualmente collegata all'istanza.
4. Nel menu **Actions**, puoi eseguire lo swap (**Swap**) o scollegare (**Detach**) l'archiviazione.
