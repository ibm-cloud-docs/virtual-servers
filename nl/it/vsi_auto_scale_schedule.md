---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestione dei picchi di traffico con il ridimensionamento automatico basato sulle pianificazioni 
{: #managing-schedule-based-auto-scaling}

I picchi di traffico web possono essere sia un bene che un male. I picchi sono un bene nel senso che più persone stanno utilizzando il tuo sito; potrebbero essere un male a causa del fatto che un aumento dell'attività può ripercuotersi sui tuoi tempi di risposta. Il ridimensionamento automatico di {{site.data.keyword.cloud}} ti consente di ridimensionare automaticamente i tuoi server, aumentandoli o riducendoli, per supportare le tue esigenze di business. Puoi utilizzare il ridimensionamento automatico basato sulle pianificazioni per controllare questi picchi di traffico.
{:shortdesc}

## Informazioni preliminari
Per prima cosa passa al menu del dispositivo e assicurati di disporre delle autorizzazioni account corrette per completare le attività.

* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assicurati di avere tutte le autorizzazioni account necessarie e l'accesso al dispositivo. Se non sei l'amministratore dell'account, il tuo account utente deve includere l'autorizzazione per utilizzare il ridimensionamento automatico. Per ulteriori informazioni sull'aggiornamento delle autorizzazioni per utilizzare il ridimensionamento automatico, vedi [Configurazione delle autorizzazioni dell'utente per il ridimensionamento automatico](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Solo il proprietario dell'account o un utente con l'autorizzazione dell'infrastruttura classica **Manage Users**, può modificare le autorizzazioni. 

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione accesso dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Aggiunta di un gruppo di ridimensionamento automatico
{: #add-auto-scale-group}

In questo scenario, un sito web social che si trova a Dallas, Texas, riscontra dei picchi di attività durante i fine settimana, Due server virtuali sono il minimo richiesto dal sito dal lunedì al venerdì; tuttavia, sono necessari due ulteriori server virtuali ogni fine settimana per tenere conto del traffico aumentato. La seguente procedura ti giuda nella modalità di configurazione del ridimensionamento automatico per supportare il ridimensionamento basato sulle pianificazioni.

1. Dal menu **Devices**, seleziona **Auto Scale**.
2. Seleziona **Add Auto Scale Group**.
3. Configura un gruppo di ridimensionamento automatico immettendo come prima cosa un nome del gruppo (**Group Name**), ad esempio, Weekend Scale Up Group, e seleziona quindi il data center.
4. Seleziona la politica di terminazione del server. Ad esempio, se scegli **Oldest**, quando si esegue la riduzione viene scelto il server con la data di provisioning meno recente.
5. Indica se il tuo gruppo è un gruppo di ridimensionamento a più VLAN e come bilanciare la riduzione sulle coppie VLAN configurate. 
6. Seleziona le VLAN pubbliche e private su cui desideri che venga eseguito il provisioning dei tuoi server. Se si deve accedere ai server da internet pubblico (se la VLAN sta eseguendo dei server web), lascia l'opzione **Private Network Only** non selezionata.
7. Imposta **Minimum Member Counts** su 2 e **Maximum Member Counts** su 4. Imposta **Cooldown Period** su 0. Perché questo è un ridimensionamento basato sulle pianificazioni, non viene eseguita alcuna raccolta di statistiche per attivare le azioni di ridimensionamento. 

## Definizione della configurazione del membro per il tuo gruppo
{: #define-member-configuration}

1. Individua **Member Configuration** e immetti un nome host (**Hostname**) e un dominio (**Domain**) per il server di ridimensionamento. I server successivi aggiunti al gruppo hanno dei suffissi univoci accodati al nome host.
2. Specifica la configurazione hardware delle istanze di calcolo (core, RAM e così via). 
3. Seleziona un sistema operativo se vuoi installare il sistema operativo minimo. Puoi anche utilizzare un'immagine pubblica o privata per eseguire il provisioning delle tue istanze. 
4. Se le istanze richiedono dei passi supplementari per installare del software aggiuntivo, specifica l'URL di uno script di post installazione (post-install script) per installare il software. (Se utilizzi un programma di bilanciamento del carico per il gruppo, gli script post-installazione vengono eseguiti prima che un membro venga posizionato dietro un programma di bilanciamento del carico).

## Configurazione delle politiche
{: #set-up-policies}

In questo scenario, il sito web social sta utilizzando il ridimensionamento basato sulle pianificazioni. Sono necessarie due politiche: una per aumentare i server di venerdì pomeriggio e una seconda per ridurre i server di domenica sera. La prima politica consiste nell'aumentare i server.

1. Individua **Policies** e fai clic su **Add Policy**. Immetti il nome della politica (**Policy Name**), (Friday Scale Up).
2. Seleziona l'opzione di periodo di raffreddamento del gruppo per il periodo di raffreddamento (**Cooldown Period**).
3. Fai clic su **Add Trigger** e specifica un trigger che si ripete selezionando **Every** nel primo menu a discesa e seleziona quindi **Friday** e **10:00 PM**\* dai successivi menu a discesa. (La casella di spunta **Advanced Edit** ti consente di immettere la frequenza del trigger in un'annotazione simile a crontab).
4. Fai clic sulla casella a discesa **Scale By** in **Action** e seleziona **Relative**. Immetti 2 nel campo **Members**.
5. Fai nuovamente clic su **Add Policy** per specificare la seconda politica che riduce i server di domenica sera. Il periodo di raffreddamento è uguale a quello del gruppo. Il trigger è ogni domenica all'una di notte (1:00 AM*) con un'azione di ridimensionamento relativo di -2.
6. L'ora immessa nel campo **Triggers** è basata sull'ora UTC, ecco perché devi selezionare le 22 (10:00 PM) per le 17 (5:00 PM) dell'Ora legale fuso centrale e l'1 di notte (1:00 AM) per le 20 (8:00 PM) dell'Ora legale fuso centrale. Durante l'Ora solare fuso centrale, le ore sono le 9 (9:00 AM) e mezzanotte (12:00 AM) perché UTC/GMT non riconosce l'ora legale. Consulta il sito [World Time Server ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} per un convertitore orario.

## Aggiunta di un programma di bilanciamento del carico locale

Se hai un programma di bilanciamento del carico locale configurato, puoi utilizzarlo per bilanciare il carico del tuo gruppo di ridimensionamento automatico.

1. Individua **Local Load Balancers** e fai clic su **Add Load Balancer**. 
2. Fai clic su **View VIP Settings** (si apre una pagina separata) per visualizzare i programmi di bilanciamento del carico locali disponibili nel tuo account e ordinarne di nuovi, se necessario. Un programma di bilanciamento del carico deve avere un gruppo di servizi associato per essere utilizzato con un gruppo di ridimensionamento automatico. Assicurati che il programma di bilanciamento del carico si trovi nel data center del tuo gruppo di ridimensionamento automatico. 
3. Fai clic su **Add Load Balancer** nella pagina **Add Auto Scale Group**, fai clic sulla freccia a discesa per Virtual IP e seleziona il tuo programma di bilanciamento del carico. 
4. Fai clic sulle frecce a discesa per **Service Group**, **Service Port** e **Service Health Check Type** e seleziona i valori appropriati. 
5. Fai clic su **Add Group** per salvare il tuo gruppo. 
6. Se tutti i tuoi data center, le tue reti e così via sono specificati correttamente, il tuo gruppo di ridimensionamento automatico viene creato. Fai clic sul gruppo nella schermata **View All Groups** per visualizzare i dettagli del tuo gruppo. 

Il risultato della configurazione di un ridimensionamento basato sulle pianificazioni consiste in due membri di cui viene eseguito automaticamente il provisioning per soddisfare il requisito minimo del sito web. Di venerdì alle 17 (5:00 PM) del Fuso centrale, viene automaticamente eseguito il provisioning di due membri supplementari quando si attiva il primo trigger della politica. Quindi, di domenica alle 20 (8:00 PM) del Fuso centrale, i due membri vengono reclamati grazie al secondo trigger della politica. Se specifichi un programma di bilanciamento del carico, tutti i membri creati alla creazione, oppure di venerdì, si trovano dietro il programma di bilanciamento del carico dopo che per essi è stato eseguito lo script di post-installazione personalizzato. 
