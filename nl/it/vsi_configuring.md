---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Configurazione di server virtuali
{: #configuring-virtual-servers}

Quando hai accesso al tuo server virtuale, assicurati di modificare la tua password e considera di configurare SSH per una soluzione di autenticazione più sicura. Esistono molte altre opzioni per la configurazione del tuo server virtuale per soddisfare le esigenze del tuo ambiente.
{:shortdesc}

## Accedi
Accedi alla [console {{site.data.keyword.cloud}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/classic?){: new_window} con le credenziali che hai ricevuto in un'email quando il tuo account è stato inizialmente creato. In alternativa, puoi accedere al [{{site.data.keyword.slportal}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){:new_window}.

## Individua il tuo server virtuale
Trova il tuo server virtuale nell'elenco dei dispositivi nella console {{site.data.keyword.cloud_notm}}. Dall'elenco dei dispositivi, puoi gestire i dispositivi, aggiornarli o generare i grafici dell'utilizzo della larghezza di banda. Per ulteriori informazioni, vedi [Gestione dei server virtuali](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).

## Modifica della tua password
Modifica la tua password utilizzando delle linee guida per la password complesse. Vedi [Visualizzazione e gestione dei nomi utente e delle password del dispositivo](/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device#view-update-user-name-password-for-device).

## Configura SSH
SSH fornisce una migliore soluzione di sicurezza rispetto all'autenticazione tramite password. Vedi [Introduzione alle chiavi SSH](/docs/infrastructure/ssh-keys?topic=ssh-keys-getting-started-tutorial#getting-started-tutorial).

## Registra gli indirizzi IP e le credenziali
Mantieni un log degli indirizzi IP e delle credenziali per il server in una posizione sicura in modo da potervi accedere rapidamente senza dover accedere alla console {{site.data.keyword.cloud_notm}}.
- Indirizzi IP del dispositivo individuali possono essere visualizzati dall'elenco dei dispositivi.
- Password root del dispositivo individuali possono essere visualizzate nella vista dell'istantanea del dispositivo. Fai clic sulla freccia accanto al nome del dispositivo per espandere la vista.
- Più indirizzi IP del dispositivo possono essere visualizzati utilizzando l'azione di scaricamento CSV nell'elenco dei dispositivi. Seleziona Scarica CSV dall'ingranaggio delle impostazioni per scaricare un elenco completo di dispositivi e di dettagli nel formato foglio di calcolo.

## Aggiorna le credenziali software
A tutto il software che è stato caricato nel tuo dispositivo durante il processo di provisioning sono state assegnate delle credenziali temporanee. Queste credenziali sono visualizzate e gestite nella scheda Password di ciascun dispositivo nella console {{site.data.keyword.cloud_notm}}. Utilizza queste credenziali temporanee per accedere al tuo software per la prima volta. Come procedura consigliata, modifica la password del tuo software dopo aver eseguito l'accesso per la prima volta. Utilizza un password sicura che consiste di una combinazione di lettere, numeri e simboli.

Facoltativamente, gli aggiornamenti delle password possono essere memorizzati nella scheda Password per ciascun dispositivo; tuttavia, ricorda che quando memorizzi le password nella console {{site.data.keyword.cloud_notm}}, qualsiasi persona con accesso all'account e autorizzazioni appropriate può visualizzare le password memorizzate nella schermata Password.

Per ulteriori informazioni sulla visualizzazione e gestione delle tue credenziali software, consulta [Gestione dell'accesso all'infrastruttura classica](/docs/vsi?topic=iam-mngclassicinfra).

## Accedi al tuo server nella rete privata
La rete privata è il precursore dell'interazione con i tuoi dispositivi tramite desktop remoto (RDP) utilizzando SSH e KVM su IP. Lo strumento di accesso VPN consente il collegamento alla rete privata dall'endpoint VPN SSL più vicino o dall'endpoint di tua scelta. L'accesso VPN è inoltre necessario per interagire con diversi servizi offerti. Per ulteriori informazioni, consulta [Introduzione a VPN (Virtual Private Networking)](/docs/infrastructure/iaas-vpn?topic=VPN-gettingstarted-with-virtual-private-networking).

## Configurazione del monitoraggio
Il monitoraggio viene principalmente utilizzato come una risorsa per controllare l'attività del tuo server, ma può anche essere utile per sapere quando ridimensionare. I servizi di monitoraggio standard e Nimsoft sono disponibili per coprire varie esigenze di monitoraggio. Il monitoraggio standard, talvolta definito “Monitoraggio di base,” viene generalmente utilizzato nel metodo ping-and-respond (effettua ping e rispondi), attraverso l'uso di un ping lento o di servizio iniziato mediante la console {{site.data.keyword.cloud_notm}}. Il monitoraggio Nimsoft conosciuto anche come “Monitoraggio avanzato” è disponibile in tre livelli: Di base, Avanzato e Premium. Si può accedere a questo servizio anche tramite la console {{site.data.keyword.cloud_notm}}. Per ulteriori informazioni, vedi [Monitoraggio](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring#monitoring).

## Configura i gruppi di sicurezza
Puoi utilizzare i gruppi di sicurezza per limitare il traffico di rete sui tuoi server virtuali. Utilizza i gruppi di sicurezza per attivare una serie di regole di filtro IP che definiscono come gestire il traffico in entrata e in uscita per le interfacce pubbliche e private di un'istanza del server virtuale. Per ulteriori informazioni, vedi [Introduzione ai gruppi di sicurezza](/docs/infrastructure/security-groups?topic=security-groups-getting-started).

## Configura i firewall
Sono disponibili dei firewall hardware per una maggiore protezione. Viene eseguito il provisioning dei firewall hardware su richiesta senza tempo di inattività. Se le regole sono state stabilite correttamente, un firewall può proteggere il tuo server da attività non desiderata. Dopo aver ordinato un firewall, deve essere abilitato e devono essere configurate le regole.

Per ulteriori informazioni, consulta le seguenti informazioni.

* [Firewall hardware (condivisi)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Firewall hardware (dedicati)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)

## Pianifica backup
I backup garantiscono che i tuoi dati vengano archiviati in modo sicuro al di fuori del dispositivo e protetti se persi. I seguenti servizi di backup sono disponibili per archiviare i tuoi dati in un'ubicazione sicura nel caso tu abbia mai bisogno di ricaricare le tue informazioni nel tuo dispositivo:
- {{site.data.keyword.backup_notm}} è un sistema di backup basato sull'agent e automatizzato. Questa è una soluzione “configura e dimentica” popolare per la gestione del tuo dispositivo. È compatibile con il software Microsoft inclusi Exchange e SQL tramite ulteriori plugin. Gli utenti {{site.data.keyword.backup_notm}} interagiscono con questo servizio tramite l'applicazione basata sul web WebCC di {{site.data.keyword.backup_notm}}. Per ulteriori informazioni, vedi [Introduzione ai servizi {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).
- R1Soft Continuous Data Protection (CDP) è un software di backup che può essere installato nel tuo server o nella macchina virtuale autogestita. È raccomandato se vuoi una sola interfaccia per gestire tutti i tuoi backup. Interagisci con CDP R1Soft tramite il tuo sistema di gestione proprietario, che permette l'installazione degli agent sulle macchine virtuali e offre i plugin del database per ulteriori funzioni. Per ulteriori informazioni, vedi [Introduzione ai servizi {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).

## Passi successivi
Dopo aver configurato il tuo server virtuale, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione del tuo server virtuale](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
