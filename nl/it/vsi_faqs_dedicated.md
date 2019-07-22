---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# FAQ: Istanze e host dedicati
{: #faqs-dedicated-hosts-and-instances}

## Cos'è un host dedicato?
{: faq}

Gli host dedicati di {{site.data.keyword.Bluemix}} sono server fisici assegnati a un gruppo di utenti. Gli host dedicati offrono la capacità di provisioning del server virtuale e il massimo controllo di posizionamento.

## Quali sono i vantaggi di utilizzare gli host dedicati nelle istanze dedicate?
{: faq}

Entrambe le offerte garantiscono la tenancy singola. Gli host dedicati forniscono la flessibilità per specificare su quale host eseguire il provisioning delle istanze host dedicato, così come:
   * Controllo su quale data center {{site.data.keyword.cloud}} è posizionato il server
   * Capacità di gestire i server man mano che cambiano i requisiti del carico di lavoro; ad esempio, migrare i server virtuali tra i tuoi host dedicati sullo stesso POD

## Posso conservare le mie istanze dedicate esistenti o devo configurare un host dedicato e le istanze dell'host dedicato?
{: faq}

Sì, puoi conservare le tue istanze dedicate esistenti.

## Posso scambiare il provisioning delle istanze dedicate (assegnato automaticamente) e le istanze dell'host dedicato?
{: faq}

No. Non può essere rieseguito il provisioning delle istanze dedicate assegnate automaticamente sugli host dedicati. Se necessiti di posizionare il server virtuale, dovrai eseguire il provisioning sugli host dedicati come istanze dell'host dedicato.

## Quale tipo di server, virtuale o bare metal, supporta l'offerta dell'host dedicato?
{: faq}

L'offerta è supportata sui server virtuali; {{site.data.keyword.Bluemix_notm}} ha un'offerta bare metal. Le differenze tra gli host virtuali e i server bare metal sono il tempo di provisioning e la gestione della virtualizzazione.

## Cos'è il ciclo di vita di provisioning di un host dedicato?
{: faq}

Gli host dedicati vengono assegnati agli utenti dopo il provisioning. Saranno conservati nell'account finché non vengono recuperati. Gli host dedicati vengono offerti solo in base al prezzo su richiesta, orario o mensile, pertanto, una volta reclamati, i modelli di fatturazione verranno addebitati come offerte {{site.data.keyword.BluSoftlayer_full}} orarie o mensili.

## Come viene addebitata l'offerta dell'host dedicato?
{: faq}

Puoi acquistare gli host dedicati su richiesta con fatturazione mensile o oraria. Gli host solo orari consentono il provisioning di soltanto istanze orarie; gli host solo mensili ti consentono di eseguire il provisioning di istanze mensili *e* orarie. Il prezzo per gli host dedicati include core, RAM, archiviazione SSD locale e velocità della porta di rete. I prezzi e le licenze dei sistemi operativi premium, dell'archiviazione SAN (storage area network) e dei componenti aggiuntivi software vengono addebitati in base all'istanza distribuita —oraria o mensile— sull'host dedicato. Per questi elementi viene seguito lo stesso modello di prezzi delle istanze pubbliche e dedicate di {{site.data.keyword.Bluemix_notm}}.

## Sto eseguendo un host dedicato su richiesta, come mi verrà fatturato?
{: faq}

Ti verrà fatturato per frequenza su richiesta mensile o oraria per gli host dedicati. Le istanze host dedicato di cui è stato eseguito il provisioning sugli host dedicati possono avere degli addebiti sulle istanze come indicato nella risposta a **Come viene addebitata l'offerta dell'host dedicato**.

## Quale è la tenancy specificata durante il provisioning degli host dedicati e delle istanze dell'host dedicato?
{: faq}

La tenancy predefinita per le istanze dedicate è la tenancy singola. Avrai l'opzione di eseguire il provisioning delle istanze dedicate su un host dedicato (istanze host dedicato) o su un host assegnato automaticamente (istanze dedicate). Le istanze dedicate sugli host assegnati automaticamente non offrono lo stesso livello di gestione degli host dedicati.

## Posso combinare e associare diverse configurazioni dell'istanza dell'host dedicato nel mio host dedicato?
{: faq}

Sì. Puoi eseguire il provisioning di dimensioni del server virtuale diverse sugli host dedicati nella relative assegnazioni di capacità.

## Come possono sapere quante istanze dell'host dedicato posso eseguire per ogni host dedicato?
{: faq}

Ogni host dedicato ha una specifica assegnazione di core, RAM e archiviazione SSD locale. Sarai in grado di visualizzare le assegnazioni delle risorse nella scheda Assegnazioni dell'host per sapere di quante istanze host dedicato viene eseguito il provisioning, la capacità attuale dell'host utilizzata e ciò che è disponibile.

## Di quali immagini può essere eseguito il provisioning sugli host dedicati?
{: faq}

Puoi eseguire il provisioning delle immagini stock del server virtuale {{site.data.keyword.Bluemix_notm}} o importare le tue proprie immagini come indicato nel contratto di terze parti.

## Esiste un limite di quanti host dedicati possono essere assegnati a un singolo account?
{: faq}

Sì, esiste un limite di risorse per ogni account, come definito per tutte le risorse di {{site.data.keyword.BluSoftlayer_notm}} as a Service. Puoi avere più ordini per account ma solo due host dedicati per ordine di provisioning.

## Le distribuzioni dell'host dedicato possono essere sovrascritte?
{: faq}

No; puoi soltanto eseguire il provisioning della capacità elencata negli host dedicati.
