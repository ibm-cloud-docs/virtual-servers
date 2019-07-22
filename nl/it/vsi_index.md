---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-29"

keywords: virtual servers, provisioning process, IBM Cloud Virtual Servers

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Esercitazione introduttiva
{: #getting-started-tutorial}

Puoi distribuire {{site.data.keyword.BluVirtServers}} in pochi minuti. I server virtuali vengono distribuiti dalla tua scelta di immagini del server virtuale e nella regione geografica che abbia senso per i tuoi carichi di lavoro.
{:shortdesc}

Prova i nostri server virtuali su un cloud privato virtuale! Per ulteriori informazioni, consulta [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started).
{:tip}

Quando crei un server virtuale nell'infrastruttura classica, puoi scegliere tra un ambiente (a tenancy multipla) pubblico o un ambiente (a tenancy singola) dedicato. Quindi, a seconda dell'ambiente scelto, devi anche selezionare oraria, mensile o i server virtuali temporanei. Nel caso dei server virtuali pubblici, scegli anche di utilizzare l'archiviazione locale o basata su SAN.

## Informazioni preliminari

Prima di iniziare, controlla i seguenti prerequisiti.

  1. Devi disporre di un account aggiornato per ordinare i server virtuali. Questo processo può richiedere del tempo e devi richiederne l'approvazione prima di continuare. Per ulteriori informazioni sull'upgrade del tuo account, consulta [Passaggio all'ID IBM](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
  2. Controlla e scegli le tue opzioni di distribuzione. Per ulteriori informazioni, consulta i seguenti argomenti:

|              Opzioni di distribuzione                           |  Descrizione                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Server virtuale pubblico](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)            | Gestito da IBM, distribuzioni server virtuale a più tenant|
|[Server virtuale temporaneo](/docs/vsi?topic=virtual-servers-about-vs-transient)| Gestito da IBM, distribuzioni server virtuale a più tenant a un costo ridotto e consigliati per i carichi di lavoro flessibili |
|[Server virtuale riservato](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers)  | Gestito da IBM, distribuzioni server virtuale a più tenant con capacità garantita per un termine del contratto |
|[Server virtuale dedicato](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers)      | Gestito da IBM, distribuzioni server virtuale a singolo tenant            |
{: caption="Tabella 1. Opzioni di distribuzione" caption-side="top"}   

## Provisioning di un server virtuale

Dopo aver deciso un'opzione di distribuzione, avvia il processo di provisioning.

|              Istruzioni di provisioning                                         |  Descrizione                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisioning di istanze pubbliche](/docs/vsi?topic=virtual-servers-ordering-vs-public)                | Provisioning di istanze pubbliche con varie opzioni             |
|[Provisioning di istanze temporanee](/docs/vsi?topic=virtual-servers-ordering-vs-transient)                | Provisioning di istanze temporanee con varie opzioni            |
|[Provisioning della capacità e delle istanze riservate](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances)            | Provisioning di capacità e istanze riservate con varie opzioni |
|[Provisioning di istanze e host dedicati](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)| Provisioning di istanze private o dedicate su host dedicati|
{: caption="Tabella 2. Informazioni di provisioning" caption-side="top"}

## Passi successivi

Dopo aver eseguito il provisioning del tuo server virtuale ed è possibile utilizzarlo, puoi configurare i tuoi server virtuali utilizzando la console
{{site.data.keyword.cloud_notm}} o la {{site.data.keyword.slapi_short}}. Per ulteriori informazioni, vedi [Configurazione di server virtuali](/docs/vsi?topic=virtual-servers-configuring-virtual-servers).
