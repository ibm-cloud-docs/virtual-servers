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
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# Informazioni sui server virtuali dedicati
{: #dedicated-virtual-servers}

L'offerta dell'host dedicato per l'infrastruttura {{site.data.keyword.Bluemix}} è un server dedicato, virtualizzato e a singolo tenant. Fornisce il massimo controllo sul posizionamento del carico di lavoro e opzioni di post provisioning flessibili. Puoi decidere in quale data center {{site.data.keyword.cloud_notm}} predeterminato vengono collocati i tuoi server virtuali e può essere garantita la capacità assegnando gli host direttamente al tuo account.
{:shortdesc}

L'offerta include le seguenti funzioni:

* Affinità e anti-affinità. Puoi specificare le relazioni host-to-virtual server e virtual server-to-virtual server che devono rimanere, che sono conosciute come le regole di affinità e anti-affinità. Queste regole di aiutano ad assicurarti che i tuoi carichi di lavoro siano posizionati appropriatamente in base ai tuoi requisiti del carico di lavoro.
* Gestione post distribuzione. Puoi migrare i server virtuali tra gli host dedicati in base ai tuoi requisiti del carico di lavoro.
* Visibilità carico di lavoro. Puoi visualizzare il consumo delle risorse, ovvero core, RAM e archiviazione locale, per ciascun host, il che ti offre il massimo controllo sulla gestione del tuo carico di lavoro.

Puoi scegliere tra due modelli di distribuzione: host dedicati e istanze dedicate. Gli host dedicati aiutano nel controllo del posizionamento del carico di lavoro e le istanze dedicate offrono l'isolamento a singolo tenant.

Le istanze dedicate non forniscono alcune delle funzioni di controllo offerte dagli host dedicati.  Consulta la seguente tabella per ulteriori dettagli.
{:note}

| Funzione server virtuale dedicato | Istanze host dedicato | Istanze dedicate |
| ------- | ------- | ------- |
| Isolamento a singolo tenant | ![Icona di casella di spunta](../../icons/checkmark-icon.svg) | ![Icona di casella di spunta](../../icons/checkmark-icon.svg) |
| Controllo posizionamento del server virtuale | ![Icona di casella di spunta](../../icons/checkmark-icon.svg) |   |
| Visibilità della risorsa | ![Icona di casella di spunta](../../icons/checkmark-icon.svg) |   |
| Fatturazione istanza |   | ![Icona di casella di spunta](../../icons/checkmark-icon.svg) |
| Fatturazione host<sup>(1)</sup> | ![Icona di casella di spunta](../../icons/checkmark-icon.svg) |   |
| Controllo post distribuzione | ![Icona di casella di spunta](../../icons/checkmark-icon.svg) |   |
| Riserve capacità | ![Icona di casella di spunta](../../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="Tabella 1. Funzioni di controllo" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup>Il prezzo dell'host è comprensivo di core, RAM, SSD locale e velocità di rete. Il prezzo del sistema operativo Premium, l'archiviazione SAN (storage area network) e i componenti aggiuntivi software sarà stabilito per istanza in base al prezzo e alle licenze esistenti in un modello orario o mensile.

Tieni presente quanto segue quando ordini gli host dedicati e le istanze host dedicato:

* La dimensione dei tuoi host viene determinata dai tuoi carichi di lavoro che stai eseguendo su di essi. L'impostazione predefinita è 56 Core X 242 GB RAM X 1.2 TB, ma puoi scegliere tra ulteriori configurazioni.
* Puoi ordinare solo due host alla volta. Ad esempio, se hai bisogno di sei host, devi posizionare tre ordini separati.
* Ogni host avrà bisogno del proprio nome univoco e puoi assegnare automaticamente il tuo POD.

## Passi successivi

Dopo aver controllato e deciso le tue opzioni di distribuzione, è il momento di eseguire il provisioning del tuo server virtuale. Per iniziare, consulta [Provisioning delle istanze e degli host dedicati](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated).
