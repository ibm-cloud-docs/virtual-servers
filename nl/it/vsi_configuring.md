---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Configurazione di server virtuali
{: #configuring-virtual-servers}

Quando hai accesso al tuo server virtuale, assicurati di configurarlo in modo che soddisfi i bisogni del tuo ambiente.
{:shortdesc}

## Accedi 
Accedi al [{{site.data.keyword.slportal_full}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} con le credenziali che hai ricevuto in un'email quando il tuo account è stato inizialmente creato.

## Individua il tuo server virtuale
Trova il tuo server virtuale nell'elenco dei dispositivi nel {{site.data.keyword.slportal}}. Dall'elenco dei dispositivi, puoi gestire i dispositivi, aggiornarli o generare i grafici dell'utilizzo della larghezza di banda. Per ulteriori informazioni, vedi [Gestione dei server virtuali](../vsi/vsi_managing.html).

## Registra gli indirizzi IP e le credenziali
Mantieni un log degli indirizzi IP e delle credenziali per il server in una posizione sicura in modo da potervi accedere rapidamente senza dover accedere al {{site.data.keyword.slportal}}. 
- Indirizzi IP del dispositivo individuali possono essere visualizzati dall'elenco dei dispositivi.
- Password root del dispositivo individuali possono essere visualizzate nella vista dell'istantanea del dispositivo. Fai clic sulla freccia accanto al nome del dispositivo per espandere la vista.
- Più indirizzi IP del dispositivo possono essere visualizzati utilizzando l'azione di scaricamento CSV nell'elenco dei dispositivi. Seleziona Scarica CSV dall'ingranaggio delle impostazioni per scaricare un elenco completo di dispositivi e di dettagli nel formato foglio di calcolo.

## Aggiorna le credenziali software
A tutto il software che è stato caricato nel tuo dispositivo durante il processo di provisioning sono state assegnate delle credenziali temporanee. Queste credenziali sono visualizzate e gestite nella scheda Password di ciascun dispositivo nel {{site.data.keyword.slportal}}. Utilizza queste credenziali temporanee per accedere al tuo software per la prima volta. Come procedura consigliata, modifica la password del tuo software dopo aver eseguito l'accesso per la prima volta. Utilizza un password sicura che consiste di una combinazione di lettere, numeri e simboli.

Facoltativamente, gli aggiornamenti delle password possono essere memorizzati nella scheda Password per ciascun dispositivo; tuttavia, ricorda che quando memorizzi le password nel {{site.data.keyword.slportal}}, qualsiasi persona con accesso all'account e autorizzazioni appropriate può visualizzare le password memorizzate nella schermata Password.

Per ulteriori informazioni sulla visualizzazione e gestione delle tue credenziali software, consulta [Gestione dell'accesso all'infrastruttura](../iam/mnginfra.html).

## Accedi al tuo server nella rete privata
La rete privata è il precursore dell'interazione con i tuoi dispositivi tramite desktop remoto (RDP) utilizzando SSH e KVM su IP. Lo strumento di accesso VPN consente il collegamento alla rete privata dall'endpoint VPN SSL più vicino o dall'endpoint di tua scelta. L'accesso VPN è inoltre necessario per interagire con diversi servizi offerti. Per ulteriori informazioni, consulta [Introduzione a VPN (Virtual Private Networking)](../infrastructure/iaas-vpn/getting-started.html).

## Configurazione del monitoraggio
Il monitoraggio viene principalmente utilizzato come una risorsa per controllare l'attività del tuo server, ma può anche essere utile per sapere quando ridimensionare. I servizi di monitoraggio standard e Nimsoft sono disponibili per coprire varie esigenze di monitoraggio. Il monitoraggio standard, talvolta definito “Monitoraggio di base,” viene generalmente utilizzato nel metodo ping-and-respond (effettua ping e rispondi), attraverso l'uso di un ping lento o di servizio iniziato mediante il {{site.data.keyword.slportal}}. Il monitoraggio Nimsoft conosciuto anche come “Monitoraggio avanzato” è disponibile in tre livelli: Di base, Avanzato e Premium. Si può accedere a questo servizio anche tramite il {{site.data.keyword.slportal}}. Per ulteriori informazioni, vedi [Monitoraggio](../infrastructure/SLmonitoring/monitoring_index.html).

## Proteggi il tuo sistema
I firewall hardware sono disponibili per assicurarti che il tuo sistema sia sempre protetto. Viene eseguito il provisioning dei firewall hardware su richiesta senza tempo di inattività. Se le regole sono state stabilite correttamente, un firewall può proteggere il tuo server da attività non desiderata. Dopo aver ordinato un firewall, deve essere abilitato e devono essere configurate le regole. Per ulteriori informazioni su come ottenere il massimo dai firewall.

Per ulteriori informazioni, consulta le seguenti raccolte di argomenti di sicurezza. 

* [Firewall hardware (condivisi)](../infrastructure/hardware-firewall-shared/getting-started.html)
* [Firewall hardware (dedicati)](../infrastructure/hardware-firewall-dedicated/getting-started.html)

I gruppi di sicurezza rappresentano un'altra opzione per limitare il traffico di rete sui tuoi server virtuali. Puoi utilizzare i gruppi di sicurezza per attivare una serie di regole di filtro IP che definiscono come gestire il traffico in entrata e in uscita per le interfacce pubbliche e private di un'istanza del server virtuale. Per ulteriori informazioni, vedi [Introduzione ai gruppi di sicurezza](/docs/infrastructure/security-groups/sg_index.html).

## Pianifica backup 
I backup garantiscono che i tuoi dati vengano archiviati in modo sicuro al di fuori del dispositivo e protetti se persi. I seguenti servizi di backup sono disponibili per archiviare i tuoi dati in un'ubicazione sicura nel caso tu abbia mai bisogno di ricaricare le tue informazioni nel tuo dispositivo:
- Il backup EVault è un sistema di backup basato sull'agent automatizzato. Questa è una soluzione “configura e dimentica” popolare per la gestione del tuo dispositivo. È compatibile con il software Microsoft inclusi Exchange e SQL tramite ulteriori plugin. Gli utenti EVault interagiscono con questo servizio tramite l'applicazione basata sul web WebCC di EVault. Per ulteriori informazioni, vedi [Introduzione ai servizi di backup](../infrastructure/Backup/index.html).
- R1Soft Continuous Data Protection (CDP) è un software di backup che può essere installato nel tuo server o nella macchina virtuale autogestita. È raccomandato se vuoi una sola interfaccia per gestire tutti i tuoi backup. Interagisci con CDP R1Soft tramite il tuo sistema di gestione proprietario, che permette l'installazione degli agent sulle macchine virtuali e offre i plugin del database per ulteriori funzioni. Per ulteriori informazioni, vedi [Introduzione ai servizi di backup](../infrastructure/Backup/index.html).

## Passi successivi
Dopo aver configurato il tuo server virtuale, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione del tuo server virtuale](../vsi/vsi_managing.html).



