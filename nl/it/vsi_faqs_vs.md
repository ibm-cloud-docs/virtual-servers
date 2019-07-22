---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-09"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# FAQ: server virtuali  
{: #faqs-virtual-servers}

## Quali tipi di server virtuali sono disponibili per l'utilizzo?
{: faq}
{{site.data.keyword.BluSoftlayer_full}} offre un paio di tipi di server virtuali all'interno della sua infrastruttura classica. L'offerta standard è un server virtuale su base pubblica, che è un ambiente a più tenant, adatto per diversi bisogni. Se stai cercando un ambiente a singolo tenant, considera l'offerta del Virtual Server dedicato. L'opzione del server virtuale dedicato è ideale per le applicazioni con requisiti della risorsa più severi. Per ulteriori informazioni sulle offerte del server virtuale correnti, consulta [Introduzione ai server virtuali](/docs/vsi?topic=virtual-servers-getting-started-with-virtual-servers#getting-started-with-virtual-servers).

IBM Cloud offre l'infrastruttura VPC (Virtual Private Cloud), ossia la piattaforma cloud di prossima generazione. Puoi creare il tuo spazio in {{site.data.keyword.cloud_notm}} per eseguire un ambiente isolato all'interno del cloud pubblico utilizzando VPC. VPC fornisce la sicurezza di un cloud privato con l'agilità e la facilità di un cloud pubblico. Per ulteriori informazioni, vedi [Informazioni su Virtual Private Cloud](https://cloud.ibm.com/docs/vpc-on-classic?topic=vpc-on-classic-about).

## Dove posso trovare le informazioni sui prezzi per i tipi di istanza pubblica?
{: faq}

Per informazioni sui prezzi, vedi [Crea il tuo server virtuale ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud/virtual-servers){: new_window}.

## Dove posso trovare le informazioni sui prezzi per le istanze pubbliche virtuali?
{: faq}

La stima dei tuoi costi per un server {{site.data.keyword.cloud_notm}} a supporto del tuo carico di lavoro inizia nel [catalogo {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/catalog). Dal catalogo, seleziona **Calcola** e scegli il tipo di server - Bare Metal Server, Virtual Server o Virtual Server per VPC (Virtual Private Cloud). Per le informazioni sui prezzi, vedi [Virtual servers provisioning calculator ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

## Posso aggiungere l'archiviazione disco al mio server virtuale orario o mensile?
{: faq}

Puoi eseguire o annullare l'upgrade dell'archiviazione disco per tutti i server virtuali aggiornando le tue opzioni di archiviazione nei campi *Primo disco* fino a *Quinto disco* nella schermata *Configurazione* del dispositivo che desideri aggiornare. Per ulteriori informazioni, consulta [Riconfigurazione di un server virtuale esistente](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).

## Quanti server virtuali orari posso avviare?
{: #concurrent}
{: faq}

Il numero di istanze che puoi eseguire dipende dal livello di maturità del tuo account. Per impostazione predefinita, un account più vecchio di 45 giorni ha un limite di 20 istanze che possono essere eseguite sui server virtuali pubblici, dedicati e bare metal in qualsiasi momento.  Un account più recente ha un limite più piccolo. Se vuoi incrementare il tuo limite, contatta il supporto per darci più informazioni su cosa stai facendo e di quante istanze contemporanee hai bisogno.

## Sarò addebitato per larghezza di banda per i miei server virtuali orari?
{: faq}

La fatturazione virtuale oraria è suddivisa per il traffico in entrata e in uscita. Tutto il traffico in entrata verso il tuo server virtuale è gratuito. Il traffico in uscita viene misurato e addebitato per GB, con i totali valutati alla fine del tuo periodo di fatturazione.

## In quali casi il mio server virtuale viene migrato su un altro host?
{: faq}

In casi limitati potrebbe essere necessario migrare un server virtuale su un altro host. Se è richiesta una migrazione, il server virtuale viene arrestato, migrato e quindi riavviato. Un server virtuale potrebbe essere migrato nei seguenti casi:

* Un hypervisor deve essere aggiornato, un host viene disattivato o un host non può più caricare nuove istanze. Se un host è contrassegnato per una di queste modifiche, quando viene riavviato uno dei suoi server virtuali dalla console {{site.data.keyword.cloud_notm}}, il riavvio attiva automaticamente il server virtuale da migrare su un altro host.
* Manutenzione dell'infrastruttura. Potresti ricevere un'email che indica che è necessaria la manutenzione su un sistema che ospita il tuo server virtuale. Potrebbe essere necessario migrare il tuo server virtuale come parte della manutenzione dell'infrastruttura.
* Un aggiornamento a un'istanza esistente. Per prestazioni costanti, se aggiorni un'istanza, questa potrebbe essere migrata a un host diverso per garantire che riceva la CPU e la memoria dedicata appropriata.
* Un host dedicato ha un malfunzionamento. Le istanze dedicate vengono migrate a un altro host vuoto senza utilizzare alcuna capacità esistente di cui potresti disporre.

Durante una finestra di manutenzione, potresti vedere un'opzione **Migra host** nel menu **Azioni** del tuo dispositivo nella console {{site.data.keyword.cloud_notm}}. L'opzione **Migra host** ti consente di migrare il server virtuale su un nuovo host a tuo piacimento durante un periodo di manutenzione specificato. Se non avvii la migrazione durante il periodo di manutenzione, il server virtuale viene migrato automaticamente per completare la manutenzione richiesta. L'opzione **Migra host** non persiste ed è disponibile solo durante i periodi di manutenzione che vengono comunicati tramite le notifiche di manutenzione.

Potresti anche visualizzare l'opzione **Migra host** se è richiesto che uno dei tuoi server virtuali abbia un determinato livello di hypervisor che non è disponibile nell'host corrente.

## Cosa succede ai miei dati quando la mia archiviazione portatile viene eliminata?
{: faq}

Quando l'archiviazione viene eliminata, tutti i puntatori ai dati su quel volume vengono rimossi, quindi i dati diventano inaccessibili. Se l'archiviazione fisica viene rifornita in un altro account, viene assegnata una nuova serie di puntatori. Non c'è modo per il nuovo account di accedere ai dati che potevano trovarsi nell'archiviazione fisica. La nuova serie di puntatori mostra tutti 0. Quando vengono scritti i nuovi dati nel volume/LUN, tutti i dati non accessibili che ancora esistono vengono sovrascritti.

## Posso utilizzare una sottoscrizione Red Hat Cloud Access per creare un server virtuale?
{: faq}

Sì. Quando importi un'immagine, puoi specificare che fornirai la licenza del sistema operativo. Per ulteriori informazioni, vedi [Utilizza Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription#using-your-own-os-license-or-subscription). Puoi quindi ordinare un server virtuale da quel template dell'immagine e utilizzare la tua sottoscrizione [Red Hat Cloud Access ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} esistente.

## Quale è la differenza tra un server virtuale e un VPS (virtual private server)?
{: faq}

Un server virtuale è simile alle piattaforme VPS (virtual private server) o VDS (virtual dedicated server) con cui potresti già avere familiarità. Questi ambienti "server virtuale" consento il provisioning di ambienti distinti privatamente e in sicurezza su un solo nodo hardware, ma VDS e VPS sono più limitati nelle loro capacità. Le opzioni VPS e VDS sono generalmente limitate a un'architettura a singolo server. Le uniche risorse che possono essere aggiunte o divise tra ogni server virtuale in una VDS o VPS sono le risorse fisicamente installate su tale server singolo.

Viene eseguito il provisioning dei server virtuali su un'architettura cloud a più server che raggruppa tutte le risorse hardware disponibili per le istanze individuali da utilizzare. I server virtuali possono utilizzare una piattaforma di archiviazione primaria basata su SAN a capacità altamente condivisa o un'archiviazione disco locale dalle elevate prestazioni. Poiché ogni istanza fa parte di un ambiente cloud più grande, la comunicazione tra tutti i server virtuali è istantanea.

## Perché ricevo un errore di capacità quando eseguo il provisioning di un server virtuale?
{: faq}

Quando esegui il provisioning di un server virtuale, potresti riceve un messaggio di errore che indica che la capacità disponibile non è sufficiente per completare la richiesta. Quando il provisioning non riesce, tutte le istanze del server virtuale in questa richiesta particolare non riescono. Un errore di capacità si verifica quando non ci sono risorse disponibili sufficienti nel router o nel data center per soddisfare la richiesta del servizio. Ci sono molti motivi per cui potresti ricevere questo errore. La disponibilità delle risorse cambia frequentemente, per cui puoi attendere e riprovare più tardi. Per ulteriori informazioni sulle strategie per evitare questo errore, vedi [Considerazioni sulle risorse per le istanze del server virtuale](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).

## Come accedo al mio server?
{: faq}

Accedi alla tua console e passa al tuo menu **Dispositivi**. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices). Nella scheda **Elenco dispositivi**, seleziona la tua istanza. Puoi visualizzare e gestire i nomi utente e le password del dispositivo da utilizzare per l'accesso. Per ulteriori informazioni, vedi [Visualizzazione e gestione dei nomi utente e delle password del dispositivo](https://test.cloud.ibm.com/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device). 

## Come utilizzo la VPN per accedere alla rete privata IBM Cloud?
{: faq}

Puoi accedere alla VPN tramite [l'interfaccia web](https://www.softlayer.com/VPN-Access){: external} o utilizzare un [client VPN autonomo](/docs/infrastructure/iaas-vpn?topic=VPN-standalone-vpn-clients) per Linux, macOS o Windows. Per ulteriori informazioni su cosa fare quando sei connesso alla VPN, vedi [Utilizza la VPN SSL](/docs/infrastructure/iaas-vpn?topic=VPN-use-ssl-vpn).

## Come riavvio il mio server virtuale?
{: faq}

I riavvii del dispositivo possono essere fatti dall'**Elenco dispositivi** o dalla vista dell'istantanea di una singola istanza. Passa alla tua istanza del server virtuale nell'**Elenco dispositivi** nella tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices). Seleziona **Azioni** per il dispositivo che vuoi gestire e seleziona **Riavvia**.

## Come utilizzo il kernel di salvataggio?
{: faq}

Il riavvio nel kernel di salvataggio è utile se stai riscontrando un problema con il server. Per avviare il kernel di salvataggio, seleziona il nome del dispositivo dall'**Elenco dispositivi** nella tua console. Nel menu **Azioni**, seleziona **Modo di salvataggio** o **Avvia da immagine** per un'istanza Windows. Per ulteriori informazioni, vedi [Avvio del kernel di salvataggio](/docs/vsi?topic=virtual-servers-launching-rescue).

## Dove trovo lo stato della rete?
{: faq}

Puoi accedere alla pagina dello **Stato** direttamente all'indirizzo [{{site.data.keyword.cloud_notm}} - Status](https://cloud.ibm.com/status){: external} per visualizzare lo stato corrente delle risorse nelle ubicazioni {{site.data.keyword.cloud_notm}}. Puoi filtrare l'elenco selezionando delle ubicazioni e dei componenti specifici (ad esempio, puoi selezionare i server virtuali e visualizzare la connettività di rete).

## Come richiedo un report di conformità?
{: faq}

Per informazioni sulla visualizzazione o la richiesta delle informazioni sulla conformità, inclusi i report SOC, vedi [Come faccio a sapere che i miei dati sono sicuri?](/docs/overview?topic=overview-security)

