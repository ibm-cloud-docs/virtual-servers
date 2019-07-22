---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

keywords: public virtual servers, network traffic, virtual server deployment

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Server virtuali pubblici
{: #about-public-virtual-servers}

Le offerte {{site.data.keyword.BluVirtServers}} pubbliche sono gestite da IBM, con distribuzioni del server virtuali a più tenant. Ti forniscono scalabilità veloce e prezzi più adeguati con dimensioni predefinite che soddisfano tutti i requisiti di business per operativi velocemente.
{:shortdesc}

I server virtuali pubblici hanno molti vantaggi, inclusi i seguenti:

* **Disponibilità globale** 

    L'offerta server virtuale pubblico è disponibile nei data center di tutto il mondo.

* **Scelte di configurazione, distribuzione rapida e scalabilità** 

    L'offerta server virtuale pubblico ti fornisce opzioni di server virtuali piccoli o grandi per soddisfare vari requisiti del carico di lavoro.

Il traffico di rete per i server virtuali pubblici, che include la SAN VSI e altre archiviazioni collegate alla rete, non ha alcuna garanzia. Se il traffico di rete di un'istanza del server virtuale inizia ad avere un impatto significativo e negativo su altri server virtuali, tale istanza potrebbe venire riavviata su un nuovo host, o in casi estremi, completamente disabilitata. Questo impatto negativo viene spesso rilevato quando i livelli di traffico si avvicinano a 20.000-30.000 pacchetti al secondo (PPS).  Per garantire la rete, si consiglia l'utilizzo dell'offerta Virtual Server dedicato. Per ulteriori informazioni, consulta l'ambiente a singolo tenant, l'offerta [Server virtuale dedicato](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers).

Le seguenti famiglie di istanze pubbliche sono disponibili per questa offerta. 

| Famiglie  | Descrizione                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Bilanciato](/docs/vsi?topic=virtual-servers-balanced#balanced) | Migliore per i carichi di lavoro cloud comuni che richiedono un bilanciamento di prestazioni e scalabilità. Utilizza l'archiviazione assegnata di rete. |
| [Archiviazione locale bilanciata](/docs/vsi?topic=virtual-servers-balanced-local-storage#balanced-local-storage) | Migliore per grandi carichi di lavoro di database che richiedono prestazioni I/O elevate e latenza molto bassa. |
| [Calcolo](/docs/vsi?topic=virtual-servers-compute#compute) | Migliore per i carichi di lavoro con traffico web da moderato a elevato.|
| [Memoria](/docs/vsi?topic=virtual-servers-memory#memory)  | Migliore per la memorizzazione nella cache e i carichi di lavoro di analisi in tempo reale. |
| [GPU](/docs/vsi?topic=virtual-servers-gpu#gpu)  | Migliore per i carichi di lavoro ad elevate prestazioni.
{: caption="Tabella 1. Selezioni di famiglie del server virtuale pubblico" caption-side="top"}

Alcune di queste famiglie sono anche disponibili per IBM Cloud Virtual Servers for VPC. Per ulteriori informazioni, consulta [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started).
{:tip}

## Passi successivi

Dopo aver esaminato e deciso il tuo profilo del server virtuale, è il momento di eseguire il provisioning del tuo server virtuale pubblico. Per iniziare, consulta [Provisioning delle istanze pubbliche](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public).
