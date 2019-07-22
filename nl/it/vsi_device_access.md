---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Gestione accesso dispositivo
{: #managing-device-access}

Per accedere e gestire i dettagli di un dispositivo specifico, devi disporre delle autorizzazioni corrette concesse al tuo account utente.  Dopo che l'amministratore dell'account ha concesso al tuo account utente l'accesso a un dispositivo, puoi visualizzare i dettagli del dispositivo utilizzando la console {{site.data.keyword.cloud}} o la {{site.data.keyword.slapi_short}}.  Le informazioni o le azioni che puoi visualizzare dipendono dal tipo di dispositivo, così come le autorizzazioni concesse al tuo account utente.
{:shortdesc}

Se il tuo account ha dispositivi a cui non ti è stato concesso l'accesso, visualizzerai il nome "Dispositivo sconosciuto" quando tenterai di accedere a tali dispositivi.
{:note}

Puoi assegnare l'accesso al dispositivo a qualsiasi utente nel tuo account, ma non a te stesso. Solo un amministratore dell'account dispone dell'accesso a tutti i dispositivi sui propri account cliente e può configurare l'accesso per tutti gli utenti nei loro account. 

Devi disporre delle seguenti autorizzazioni per accedere ai dettagli del dispositivo per i server virtuali pubblici o dedicati.

* **Visualizza i dettagli dei server virtuali** - Ti consente di visualizzare gli indirizzi IP, il tipo di sistema operativo, le password e altro per un server virtuale specificato.  Ti consente inoltre di aggiornare le password del server virtuale nel portale. Devi disporre di questo accesso per visualizzare le istanze pubbliche, dedicate e le istanze host dedicato.

* **Visualizza i dettagli dell'host dedicato virtuale** - Ti consente di visualizzare gli indirizzi IP, il tipo di sistema operativo, le password e altro per un host dedicato specificato.  Ti consente inoltre di migrare le istanze dedicate in un host dedicato differente. Devi disporre di questo accesso per visualizzare gli host dedicati.


## Aggiunta di autorizzazioni ai tuoi utenti
Se sei l'amministratore dell'account e vuoi concedere l'autorizzazione agli utenti per visualizzare i dettagli del server virtuale e dell'host dedicato, completa la seguente procedura.

1. Accedi alla pagina [Accesso (IAM) ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/iam#/users){: new_window} nella console {{site.data.keyword.cloud}}. 
2. Nella scheda **Utenti**, seleziona **Visualizzato da: Miei utenti dell'infrastruttura classica**.
3. Seleziona un utente e fai quindi clic sulla scheda **Infrastruttura classica**.
4. Espandi la categoria **Dispositivi** nella scheda **Autorizzazioni** e seleziona **Visualizza dettagli server virtuale** e **Visualizza dettagli host dedicato virtuale**.
5. Fai clic su **Applica**.

### Aggiunta di autorizzazioni al livello di dispositivo specifico 
Se vuoi fornire agli utenti l'accesso a un livello di dispositivo specifico, completa la seguente procedura:

1. Nella scheda **Utenti**, seleziona **Visualizzato da: Miei utenti dell'infrastruttura classica**. 
2. Seleziona un utente e fai quindi clic sulla scheda **Infrastruttura classica**.
3. Nella sezione **Seleziona tipo** nella scheda **Dispositivi**, seleziona l'autorizzazione appropriata: **Tutti i server bare metal**, **Tutti gli host dedicati** o **Tutti i server virtuali**. 
4. Nella sezione **Abilita accesso futuro** nella scheda **Dispositivi**, seleziona l'autorizzazione appropriata: **Accesso al server bare metal automatico**, **Accesso all'host dedicato automatico** o **Accesso al server virtuale automatico**. Questa autorizzazione consente ai tuoi utenti di avere sempre accesso al tipo di dispositivo quando vengono aggiunti dei nuovi dispositivi. 
5. Fai clic su **Imposta** per applicare le nuove autorizzazioni.

## Aggiunta di autorizzazioni ai tuoi utenti nel portale clienti 
Se sei l'amministratore dell'account e vuoi concedere l'autorizzazione agli utenti per visualizzare i dettagli del server virtuale e dell'host dedicato, completa la seguente procedura.

1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.
2. Seleziona **Account > Utenti** dalla barra di navigazione per accedere alla schermata degli utenti.
3. Fai clic sul nome utente pertinente per accedere al profilo utente.
4. Fai clic sull'icona **Autorizzazioni portale** per accedere alla schermata delle autorizzazioni del portale.
5. Nella scheda **Dispositivo**, seleziona **Visualizza dettagli server virtuale** e **Visualizza dettagli host dedicato virtuale** per aggiungere queste autorizzazioni al profilo dell'utente.

### Aggiunta di autorizzazioni al livello di dispositivo specifico nel portale clienti
Per fornire l'accesso a un livello del dispositivo specifico, continua con le seguenti istruzioni.

1. Fai clic sull'icona **Accesso dispositivo** per accedere alla schermata di accesso al dispositivo.
2. Fai clic sulla scheda **Accesso rapido**. 
3. Dall'elenco a discesa **Tipo di dispositivo**, seleziona **Tutti i server virtuali** e **Tutti gli host dedicati**.
4. Seleziona la casella di spunta **Concedi l'accesso automaticamente quando vengono aggiunti nuovi dispositivi** se l'utente associato deve avere sempre accesso a questo tipo di dispositivo.
5. Verifica che siano stati selezionati i dispositivi corretti.
6. Fai clic su **Aggiorna accesso dispositivo**.

Puoi anche utilizzare il servizio API SoftLayer_User_Customer::addBulkDedicatedHostAccess per fornire un accesso utente a uno o più host dedicati. Per ulteriori informazioni, consulta [Adding Bulk Dedicated Host Access ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/reference/services/SoftLayer_User_Customer/addBulkDedicatedHostAccess/){: new_window}.  
{:note}

## Passi successivi
Le autorizzazioni utente vengono aggiornate immediatamente dopo l'invio delle modifiche. Se le autorizzazioni sono state concesse, l'utente può visualizzare o interagire con le funzioni selezionate. Se le autorizzazioni sono state rimosse, l'utente non può più visualizzare o interagire con le funzioni selezionate. Le autorizzazioni possono essere nuovamente aggiornate in qualsiasi momento.

