---



copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Gestione accesso dispositivo
{: #managing-device-access}

Per accedere e gestire i dettagli di un dispositivo specifico, devi disporre delle autorizzazioni corrette concesse al tuo account utente.  Dopo che l'amministratore dell'account ha concesso al tuo account utente l'accesso a un dispositivo, puoi visualizzare i dettagli del dispositivo utilizzando il {{site.data.keyword.slportal_full}} o la API.  Le informazioni o le azioni che puoi visualizzare dipendono dal tipo di dispositivo, così come le autorizzazioni concesse al tuo account utente.
{:shortdesc}

**Nota:** se il tuo account ha dispositivi a cui non ti è stato concesso l'accesso, visualizzerai il nome "Dispositivo sconosciuto" quando tenterai di accedere a tali dispositivi.

Puoi assegnare l'accesso al dispositivo a qualsiasi utente nel tuo account, ma non a te stesso. Solo un amministratore dell'account dispone dell'accesso a tutti i dispositivi sui propri account cliente e può configurare l'accesso per tutti gli utenti nei loro account. 

Devi disporre delle seguenti autorizzazioni per accedere ai dettagli del dispositivo per i server virtuali pubblici o dedicati.

**Visualizza i dettagli dei server virtuali**

Ti consente di visualizzare gli indirizzi IP, il tipo di sistema operativo, le password e altro per un server virtuale specificato.  Ti consente inoltre di aggiornare le password del server virtuale nel portale. Un utente deve disporre di questo accesso per visualizzare le istanze pubbliche, dedicate e le istanze host dedicate.

**Visualizza i dettagli dell'host dedicato virtuale**

Ti consente di visualizzare gli indirizzi IP, il tipo di sistema operativo, le password e altro per un host dedicato specificato.  Ti consente inoltre di migrare le istanze dedicate in un host dedicato differente. Un utente deve disporre di questo accesso per visualizzare gli host dedicati.

## Aggiunta dell'autorizzazione per visualizzare le istanze del server virtuale.
Utilizza le seguenti istruzioni per aggiungere le autorizzazioni *Visualizza i dettagli del Virtual Server* per ognuno dei tuoi utenti secondari. Solo un amministratore dell'account può concedere le autorizzazioni ad altri utenti nel propri account.  

1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.
2. Seleziona **Account > Utenti** dalla barra di navigazione per accedere alla schermata degli utenti.
3. Fai clic sul nome utente pertinente per accedere al profilo utente.
4. Fai clic sull'icona **Autorizzazioni portale** per accedere alla schermata delle autorizzazioni del portale.
5. Nella scheda *Dispositivo*, seleziona **Visualizza i dettagli del Virtual Server** per aggiungere questa autorizzazione al profilo dell'utente.

Per fornire l'accesso a un livello del dispositivo specifico, continua con le seguenti istruzioni.

1. Fai clic sull'icona **Accesso dispositivo** per accedere alla schermata di accesso al dispositivo.
2. Fai clic sulla scheda **Accesso rapido**. 
   Nota: un'altra opzione è di selezionare invece un dispositivo individuale.
3. Dall'elenco a discesa *Tipo di dispositivo*, seleziona **Tutti i server virtuali**.
4. Seleziona la casella di spunta **Concedi l'accesso automaticamente quando vengono aggiunti nuovi dispositivi** se l'utente associato deve avere sempre accesso a questo tipo di dispositivo.
5. Verifica che siano stati selezionati i dispositivi corretti.
6. Fai clic su **Aggiorna accesso dispositivo**.

## Aggiunta dell'autorizzazione per visualizzare gli host dedicati
Utilizza le seguenti istruzioni per aggiungere le autorizzazioni *Visualizza i dettagli dell'host dedicato virtuale* per ognuno dei tuoi utenti secondari. Solo un amministratore dell'account può concedere le autorizzazioni ad altri utenti nel propri account.

1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.
2. Seleziona **Account > Utenti** dalla barra di navigazione per accedere alla schermata degli utenti.
3. Fai clic sul nome utente pertinente per accedere al profilo utente.
4. Fai clic sull'icona **Autorizzazioni portale** per accedere alla schermata delle autorizzazioni del portale.
5. Nella scheda *Dispositivo*, seleziona **Visualizza i dettagli dell'host dedicato virtuale** per aggiungere questa autorizzazione al profilo dell'utente.

Per fornire l'accesso a un livello del dispositivo specifico, continua con le seguenti istruzioni.

1. Fai clic sull'icona **Accesso dispositivo** per accedere alla schermata di accesso al dispositivo.
2. Fai clic sulla scheda **Accesso rapido**. 
   Nota: un'altra opzione è di selezionare invece dispositivi individuali.
3. Dall'elenco a discesa *Tipo di dispositivo*, seleziona **Tutti gli host dedicati**.
4. Seleziona la casella di spunta **Concedi l'accesso automaticamente quando vengono aggiunti nuovi dispositivi** se l'utente associato deve avere sempre accesso a questo tipo di dispositivo.
5. Verifica che siano stati selezionati i dispositivi corretti.
6. Fai clic su **Aggiorna accesso dispositivo**.

**Nota:** puoi inoltre utilizzare il servizio API SoftLayer_User_Customer::addBulkDedicatedHostAccess per fornire un accesso utente a uno o più host dedicati. Per ulteriori informazioni, consulta [Adding Bulk Dedicated Host Access ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/reference/services/SoftLayer_User_Customer/addBulkDedicatedHostAccess/){: new_window}.  

## Passi successivi
Le autorizzazioni utente vengono aggiornate immediatamente dopo l'invio delle modifiche. Se le autorizzazioni sono state concesse, l'utente può visualizzare o interagire con le funzioni selezionate. Se le autorizzazioni sono state rimosse, l'utente non può più visualizzare o interagire con le funzioni selezionate. Le autorizzazioni possono essere nuovamente aggiornate in qualsiasi momento.
