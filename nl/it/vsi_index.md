---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Introduzione ai server virtuali
Puoi distribuire {{site.data.keyword.BluVirtServers}} in pochi minuti. I server virtuali vengono distribuiti dalla tua scelta di immagini del server virtuale e nella regione geografica che abbia senso per i tuoi carichi di lavoro.
{:shortdesc}

Quando crei un server virtuale, puoi scegliere tra un ambiente (a tenancy multipla) pubblico o un ambiente (a tenancy singola) dedicato. Quindi, a seconda dell'ambiente scelto, devi anche selezionare oraria, mensile o i server virtuali temporanei. Nel caso dei server virtuali pubblici, scegli anche di utilizzare l'archiviazione locale o basata su SAN.

## Informazioni preliminari

Prima di iniziare, controlla i seguenti prerequisiti.

  1. Devi disporre di un account aggiornato per ordinare i server virtuali. Questo processo può richiedere del tempo e devi richiederne l'approvazione prima di continuare. Per ulteriori informazioni sull'aggiornamento del tuo account, consulta [Passaggio all'ID IBM](https://console.bluemix.net/docs/admin/softlayerlink.html).
  2. Controlla e scegli le tue opzioni di distribuzione. Per ulteriori informazioni, consulta i seguenti argomenti:

|              Opzioni di distribuzione                           |  Descrizione                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Server virtuale pubblico](../vsi/vsi_public.html)            | Gestito da IBM, distribuzioni server virtuale a più tenant|
|[Server virtuale temporaneo](../vsi/vsi_about_transient.html)| Gestito da IBM, distribuzioni server virtuale a più tenant a un costo ridotto e consigliati per i carichi di lavoro flessibili |
|[Server virtuale dedicato](../vsi/vsi_dedicated.html)      | Gestito da IBM, distribuzioni server virtuale a singolo tenant            |
{: caption="Tabella 1. Opzioni di distribuzione" caption-side="top"}   

## Provisioning di un server virtuale

Dopo aver deciso un'opzione di distribuzione, avvia il processo di provisioning.

|              Istruzioni provisioning                                         |  Descrizione                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisioning di istanze pubbliche](../vsi/vsi_provision_public.html)                | Provisioning di istanze pubbliche con varie opzioni             |
|[Provisioning di istanze temporanee](../vsi/vsi_provision_transient.html)                | Provisioning di istanze temporanee con varie opzioni            |
|[Provisioning di istanze e host dedicati](../vsi/vsi_provision_dedicated.html)| Provisioning di istanze private o dedicate su host dedicati|
{: caption="Tabella 2. Informazioni di provisioning" caption-side="top"}

## Passi successivi

Dopo aver eseguito il provisioning del tuo server virtuale ed è possibile utilizzarlo, puoi configurare i tuoi server virtuali utilizzando il
{{site.data.keyword.slportal_full}} o l'{{site.data.keyword.slapi_full}}. Per ulteriori informazioni, vedi [Configurazione di server virtuali](../vsi/vsi_configuring.html).
