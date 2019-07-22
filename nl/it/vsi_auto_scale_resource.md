---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestione dei picchi di traffico con il ridimensionamento automatico basato sulle risorse 
{: #managing-resourced-based-auto-scaling}

Il lancio di un nuovo prodotto o una svendita di un prodotto esistente può causare un picco di traffico sul tuo sito web. Un picco del traffico può influenzare il tuo tempo di risposta, cosa che si ripercuote sull'esperienza dei tuoi clienti con il tuo sito web. Il ridimensionamento automatico di {{site.data.keyword.cloud}} ti consente di rispondere automaticamente ai picchi di traffico. Puoi utilizzare il ridimensionamento automatico basato sulle risorse per controllare questi picchi di traffico.
{:shortdesc}

## Informazioni preliminari
Per prima cosa passa al menu del dispositivo e assicurati di disporre delle autorizzazioni account corrette per completare le attività.

* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assicurati di avere tutte le autorizzazioni account necessarie e l'accesso al dispositivo. Se non sei l'amministratore dell'account, il tuo account utente deve includere l'autorizzazione per utilizzare il ridimensionamento automatico. Per ulteriori informazioni sull'aggiornamento delle autorizzazioni per utilizzare il ridimensionamento automatico, vedi [Configurazione delle autorizzazioni dell'utente per il ridimensionamento automatico](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Solo il proprietario dell'account o un utente con l'autorizzazione dell'infrastruttura classica **Manage Users**, può modificare le autorizzazioni. 

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione accesso dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Aggiunta di un gruppo di ridimensionamento automatico 
{: #adding-auto-scale-group}

Ad esempio, un sito web di e-commerce che si trova a Dallas, in Texas, richiede che tre server virtuali siano sempre online. L'attività commerciale ha un picco tra le 9 e le 17 ogni giorno della settimana quando la società propone delle svendite online. Per aiutare a sostenere i tempi di risposta del sito web, sono necessari tre ulteriori server virtuali aggiuntivi durante questi orari. Inoltre, quando il traffico in entrata pubblico ha una media superiore ai 5 MB al secondo in tutti i server virtuali per 10 minuti, deve essere eseguito il provisioning di altri due server virtuali. Quando il traffico scende sotto i 5 MB al secondo, questi server virtuali aggiuntivi devono essere annullati e rimossi. L'obiettivo è quello di disporre di non più di cinque server virtuali che gestiscono l'aumento di traffico, evitando così che i server virtuali dei giorni infrasettimanali risentano del traffico infrasettimanale aggiuntivo. La seguente procedura ti guida nella modalità di configurazione del ridimensionamento automatico per supportare il ridimensionamento basato sulle risorse. 

1. Dal menu **Devices**, seleziona **Auto Scale**.
2. Seleziona **Add Auto Scale Group**.
3. Configura un gruppo di ridimensionamento automatico immettendo come prima cosa un nome del gruppo (**Group Name**), ad esempio, Weekend Scale Up Group, e seleziona quindi il data center.
4. Seleziona la politica di terminazione del server. Ad esempio, se scegli **Oldest**, quando si esegue la riduzione viene scelto il server con la data di provisioning meno recente.
5. Indica se il tuo gruppo è un gruppo di ridimensionamento a più VLAN e come bilanciare la riduzione sulle coppie VLAN configurate 
6. Seleziona le VLAN pubbliche e private su cui desideri che venga eseguito il provisioning dei tuoi server. Se si deve accedere ai server da internet pubblico (se la VLAN sta eseguendo dei server web), lascia l'opzione **Private Network Only** non selezionata. 
7. Imposta **Minimum Member Counts** su 3 e **Maximum Member Counts** su 6. Imposta **Cooldown Period** su 0. Perché questo è un ridimensionamento basato sulle pianificazioni, non viene eseguita alcuna raccolta di statistiche per attivare le azioni di ridimensionamento. 

## Definizione della configurazione del membro per il tuo gruppo
{: #defining-member-configuration}

1. Individua **Member Configuration** e immetti un nome host (**Hostname**) e un dominio (**Domain**) per il server di ridimensionamento. I server successivi aggiunti al gruppo hanno dei suffissi univoci accodati al nome host. 
2. Specifica la configurazione hardware delle istanze di calcolo (core, RAM e così via). 
3. Seleziona un sistema operativo se vuoi installare il sistema operativo minimo. Puoi anche utilizzare un'immagine pubblica (**Public Image**) o un'immagine privata (**Private Image**) per eseguire il provisioning delle tue istanze.
4. Se le istanze richiedono dei passi supplementari per installare del software aggiuntivo, specifica l'URL di uno script di post-installazione (**Post-Install Script**) per installare il software. (Se utilizzi un programma di bilanciamento del carico per il gruppo, gli script post-installazione vengono eseguiti prima che un membro venga posizionato dietro un programma di bilanciamento del carico).

## Configurazione delle politiche
{: #setting-up-policies}

Nello scenario, il sito web di e-commerce sta utilizzando il ridimensionamento basato sulle risorse. Sono necessarie due politiche: una per avere un'azione di ridimensionamento relativo di +3 per il periodo di tempo necessario e una seconda per avere un'azione di annullamento di 3 quando il picco è finito. La prima politica consiste nell'aggiungere le risorse.

1. Scorri verso il basso fino a **Policies** e fai clic su **Add Policy**. Immetti il nome della politica (**Policy Name**), (Weekday Scale Up).
2. Seleziona l'opzione di periodo di raffreddamento del gruppo per il periodo di raffreddamento (**Cooldown Period**).
3. Fai clic su **Add Trigger** e specifica un trigger che si ripete selezionando **Every** nel primo menu a discesa ed evidenzia quindi **Monday, Tuesday, Wednesday, Thursday,** e **Friday** e **2:00 PM**\* dalle successive caselle a discesa. (La casella di spunta **Advanced Edit** ti consente di immettere la frequenza del trigger in un'annotazione simile a crontab). 
4. Fai clic sulla casella a discesa **Scale By** in **Action** e seleziona **Exact**. Immetti 3 nel campo **Members**.
5. Fai nuovamente clic su **Add Policy** per specificare la seconda politica che rimuove i server ogni pomeriggio. Il periodo di raffreddamento è uguale a quello del gruppo. Il trigger è ogni lunedì (Monday), martedì (Tuesday), mercoledì (Wednesday), giovedì (Thursday) e venerdì (Friday) alle 22 (10:00 PM\*), con un'azione di ridimensionamento esatto di 3. L'ora immessa nel campo **Triggers** è basata sull'ora UTC, ecco perché devi selezionare le 14 (2:00 PM) per le 9 del mattino (9:00 AM) dell'Ora legale fuso centrale e le 22 (10:00 PM) per le 17 (5:00 PM) dell'Ora legale fuso centrale. Durante l'Ora solare fuso centrale, le ore sono le 13 (1:00 PM) e le 21 (9:00 PM) perché UTC/GMT non riconosce l'ora legale. Consulta il sito [World Time Server ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} per un convertitore orario. 
6. Configura un altro gruppo con un tempo di raffreddamento (cooldown) pari a zero (0) e con un nome, ad esempio, Traffic Burst Group, con un conteggio minimo di membri pari a 0 e un massimo pari a 5. Utilizza le stesse impostazioni per la configurazione di gruppo e membri del gruppo Weekday Scale Up, fatta eccezione per il nome gruppo. 
7. Fai clic su **Add Policy** per aggiungere la seconda politica che controlla i due server aggiuntivi quando il traffico in entrata pubblico ha una media superiore ai 5 MB al secondo in tutti i server virtuali per 10 minuti. 
8. Immetti il nome della politica (**Policy Name**), ad esempio, Traffic Burst Group. 
9. Seleziona l'opzione di periodo di raffreddamento del gruppo per il periodo di raffreddamento (**Cooldown Period**).
10. Fai clic su **Add Trigger**. Lascia il valore **If my** predefinito nella prima casella e seleziona **Public Network Incoming Mbps** per la seconda casella.Lascia il segno > predefinito nella terza casella. Nella quarta casella, immetti **5** (5 MB), immetti **600** nella quinta casella e seleziona **Seconds** nell'ultima casella per rappresentare 10 minuti.
11. Fai clic sulla casella a discesa **Scale By** in **Action** e seleziona **Relative**. Immetti 2 nel campo **Members**.
12. Fai nuovamente clic su **Add Policy** per specificare la seconda politica che rimuove i server quando il traffico è sceso a meno di 5 Mbps\*Il periodo di raffreddamento sarà uguale a quello del gruppo. Il trigger è: se il valore di Mbps in entrata della mia rete pubblica è inferiore a 5 (5 Mbps) per un periodo di 600 secondi (10 minuti).

Quando vengono creati entrambi i gruppi, il gruppo Weekday Scale Up crea tre server (il minimo). Durante i giorni della settimana, alle 9:00 del mattino del Fuso centrale, vengono aggiunti altri tre server e alle 17 dello stesso fuso i server vengono rimossi. Non c'è alcun altro modo per aggiungere o rimuovere i membri da tale gruppo. In un gruppo Traffic Burst Group completamente separato, due server vengono aggiunti per ogni 10 minuti in cui il traffico pubblico in entrata su tutti i membri ha una media di 5 MB al secondo, fino a raggiungere il valore massimo del gruppo, che è pari a cinque. Dopo che il traffico pubblico in entrata rimane sotto tale quantità per 10 minuti, tutti i server in questo gruppo vengono rimossi.

