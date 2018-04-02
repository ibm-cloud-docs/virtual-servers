---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-12"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Provisioning di selezioni
Devi effettuare le seguenti selezioni quando esegui il provisioning di un server virtuale pubblico.

## Ubicazione
Puoi selezionare il data center specifico in cui desideri effettuare la distribuzione. Per le nuove distribuzioni, {{site.data.keyword.Bluemix}} identifica automaticamente il data center migliore (in base alla disponibilità) e crea le VLAN pubbliche e private appropriate. Per aggiunte agli ambienti esistenti, puoi selezionare la sottorete, la VLAN e il data center specifici richiesti dalla tua progettazione. Per ulteriori informazioni sulle VLAN e sulle sottoreti, vedi [Introduzione alle VLAN](/docs/infrastructure/vlans/getting-started.html).

La selezione di una sottorete è facoltativa e deve essere utilizzata solo quando hai bisogno che il tuo dispositivo utilizzi un indirizzo IP da una sottorete. Se selezioni una sottorete, verifica di avere abbastanza indirizzi IP per completare la richiesta. Se non hai abbastanza indirizzi IP per la tua sottorete, il tuo ordine può essere ritardato o annullato.
{:tip}

## Processori / RAM
Quando effettui l'ordine, devi selezionare un opzione processore core. Le opzioni processore core seguono gli standard delle distribuzioni del server virtuale. Ogni core fisico sul server è con hyperthreading e presentato come due CPU virtuali (vCPU) o core. L'offerta del server virtuale fornisce 2.0GHz o meglio per core con un massimo di 56 core disponibili per un solo server virtuale.

La RAM è estremamente diretta. L'offerta dedica completamente la quantità di RAM che selezioni al tuo server virtuale, con un massimo di 242GB per un solo server virtuale.

**Nota:** le istanze dedicate e pubbliche hanno valori massimi di configurazione lievemente differenti. Assegnazioni molto grandi di core o memoria limitano le opzioni disponibili.

## Sistema operativo

Puoi anche selezionare il sistema operativo che deve venire distribuito al server. Puoi selezionare alcune opzioni gratuite come CentOS e Ubuntu. Sono anche disponibili opzioni a pagamento come Windows Server e Red Hat Enterprise Linux (RHEL). È importante tenere presente che Windows richiede un disco primario da 100GB.

Per i clienti esistenti, puoi anche eseguire la distribuzione in base a un template dell'immagine attraverso il {{site.data.keyword.slportal_full}} passando a **Dispositivi -> Gestisci -> Immagini** e selezionando **Ordina server virtuale** dal menu *Azioni*.  Questo seleziona automaticamente il sistema operativo appropriato per l'ordine.  In alternativa, puoi eseguire l'ordine basato su un'immagine standard e quindi ricaricare un template dell'immagine in qualsiasi momento.

## Archiviazione

Hai l'opzione tra archiviazione locale o SAN per ogni server virtuale. Puoi integrare l'archiviazione locale o SAN con altri prodotti se necessario. Sia l'archiviazione locale che SAN sono esposti sul server virtuale come dischi locali. Tutte le modifiche ai dischi, come collegare, scollegare, migrare e così via, richiedono un riavvio del server virtuale. Per ulteriori informazioni, vedi [Opzioni di archiviazione](../vsi/storage/vsi_about_storage.html).

## Fatturazione mensile e oraria

Puoi selezionare la fatturazione mensile o oraria per un server virtuale. La differenza principale, è che i server a fatturazione oraria non dispongono di assegnazione di larghezza di banda inclusa. Al termine di un periodo di fatturazione vengono calcolati l'utilizzo della larghezza di banda e il numero di ore in cui ogni server è stato attivo nell'account. Un totale parziale è disponibile nel {{site.data.keyword.slportal}} nella pagina Vista server virtuale con un link a una pagina Dettagli, che mostra ogni elemento di riga, numero di ore e addebiti di esecuzione per ogni elemento.

## Larghezza di banda

L'offerta include 250GB con i server virtuali a fatturazione mensile che dispongono di un uplink pubblico. Puoi acquistare assegnazioni più grandi a un costo ridotto rispetto alla tariffa generale.

## Velocità porta

Puoi selezionare la velocità uplink per il server virtuale, fino a 1GB/s. Viene eseguito il backup di questi uplink virtuali da uplink fisici ridondanti nelle reti dedicata e pubblica di IBM. La velocità dedicata e pubblica è sempre la stessa del momento dell'ordine, con l'opzione di eseguire l'upgrade o il downgrade di un uplink se necessario.

## Software

Puoi selezionare il software che deve essere installato da {{site.data.keyword.Bluemix_notm}} durante il processo di provisioning. {{site.data.keyword.Bluemix_notm}} fornisce supporto per tutto il software distribuito durante il processo di provisioning. Puoi anche installare il tuo proprio software dopo la distribuzione del server.

## Sicurezza

Prima di distribuire, considera le seguenti opzioni di sicurezza. Come parte del processo di ordine, puoi selezionare un firewall software o hardware specifico per il dispositivo per fornire protezione. In alternativa, puoi distribuire le applicazioni firewall dedicate all'ambiente e distribuire il server virtuale a una VLAN protetta. 

**Nota:** un server virtuale non può essere protetto da due applicazioni firewall nella stessa interfaccia. 

Puoi anche utilizzare i gruppi di sicurezza per attivare una serie di regole di filtro IP che definiscono come gestire il traffico in entrata e in uscita per le interfacce pubbliche e private di un'istanza del server virtuale.

Per ulteriori informazioni, consulta le seguenti raccolte di argomenti di sicurezza.

* [Firewall hardware (condivisi)](../infrastructure/hardware-firewall-shared/getting-started.html)
* [Firewall hardware (dedicati)](../infrastructure/hardware-firewall-dedicated/getting-started.html)
* [Introduzione ai gruppi di sicurezza](/docs/infrastructure/security-groups/sg_index.html)

## Monitoraggio

Puoi selezionare molte opzioni di monitoraggio per il server virtuale. Le opzioni includono il monitoraggio standard, che monitora tramite la risposta del servizio TCP (transmission control protocol) e Ping, e dispone di risposte facoltative nel caso di errori. Puoi anche aggiungere il monitoraggio avanzato che utilizza l'agent software Nimsoft per fornire una vasta serie di funzioni per il monitoraggio del server virtuale e del software installato.

Per ulteriori informazioni, vedi [Monitoraggio](../infrastructure/SLmonitoring/monitoring_index.html).

## Backup

Durante il processo di ordine, puoi aggiungere i backup Evault. Puoi anche scegliere di acquistare una licenza R1soft per il tuo ambiente di backup R1soft esistente o utilizzare una soluzione di backup di terze parti.

Per ulteriori informazioni, consulta [Nuova registrazione del tuo dispositivo con eVault](../infrastructure/Backup/how-do-i-re-register-evault.html).

## Script di post provisioning

Gli script di post provisioning possono essere associati a un qualsiasi ordine del server virtuale. Questo esegue uno script sviluppato dal cliente dopo il completamento di ogni attività di provisioning. Gli script sono comunemente utilizzati per applicare la configurazione specifica del cliente a un server e per agevolare l'automazione della tua strategia di ridimensionamento.

Per ulteriori informazioni, consulta [Aggiunta di un script di provisioning personalizzato](vsi_add_script.html).

## Operazioni successive
Quando sei pronto ad eseguire il provisioning del tuo server virtuale pubblico, consulta [Provisioning di istanze pubbliche](vsi_provision_public.html).
