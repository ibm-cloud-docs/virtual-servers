---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Migrazione di un'istanza host dedicato a un altro host
{: #migrating-dedicated-host}

Puoi migrare le tue istanze host dedicato da un host a un altro nello stesso POD. Seleziona l'istanza da migrare dalla pagina dei dettagli del dispositivo dell'host o dell'istanza. Tieni presente che possono venire migrate solo due istanze alla volta e il tempo necessario per la migrazione dipende dal disco. I dischi SAN vengono migrati più velocemente perché i dischi locali richiedono la copia del disco. Le istanze di migrazione sono offline durante la migrazione; l'host rimane attivo per qualsiasi altra istanza host dedicato.
{:shortdesc}

## Informazioni preliminari
Per prima cosa passa al menu del dispositivo e assicurati di disporre delle autorizzazioni account corrette per completare le attività.

* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assicurati di avere tutte le autorizzazioni account necessarie e l'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione dell'infrastruttura classica **Manage Users**, può modificare le autorizzazioni.

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione accesso dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Migrazione dall'host dedicato
Utilizza le seguenti istruzioni per migrare le istanze dell'host dedicato a un altro host dedicato nello stesso POD dalla pagina dei dettagli del dispositivo dell'*host dedicato originale*. 

1. Dal menu **Devices**, seleziona **Device List**.
2. Seleziona l'host e l'istanza host dall'elenco.
3. Fai clic sull'elenco a discesa **Actions** accanto all'istanza dedicata da migrare.
4. Seleziona **Migrate** e immetti l'host in cui viene migrata l'istanza; ricorda, l'host di destinazione deve essere nello stesso POD dell'host originale.
5. Fare clic su **Migrate** per iniziare la migrazione. 

La migrazione inizia immediatamente. Durante la migrazione, l'istanza dedicata è offline finché non migrata al proprio nuovo host. Puoi visualizzare la pagina dei dettagli del dispositivo dell'host di destinazione per assicurarti che l'istanza sia stata migrata correttamente.

## Migrazione dall'istanza dedicata
Utilizza le seguenti istruzioni per migrare le istanze dell'host dedicato a un altro host dedicato nello stesso POD dalla pagina dei dettagli dell'*istanza host dedicato*.

1. Dal menu **Devices**, seleziona **Device List**.
2. Seleziona l'istanza host da migrare dall'elenco.
3. Fai clic su **Migrate**.
4. Seleziona l'host di destinazione a cui migrare l'istanza; ricorda, l'host di destinazione deve essere nello stesso POD dell'host originale.
5. Fare clic su **Migrate** per iniziare la migrazione.

La migrazione inizia immediatamente. Durante la migrazione, l'istanza dedicata è offline finché non migrata al proprio nuovo host. Puoi visualizzare la pagina dei dettagli del dispositivo dell'host di destinazione per assicurarti che l'istanza sia stata migrata correttamente.

## Passi successivi
Dopo aver migrato un'istanza host dedicato, controlla che la migrazione abbia funzionato verificando se il suo stato è verde nella pagina dei dettagli del dispositivo del nuovo host dedicato.

