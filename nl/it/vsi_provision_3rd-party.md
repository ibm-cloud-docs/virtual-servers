---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# Provisioning di un'istanza del server virtuale da un'immagine di terze parti
{: #ordering-3P}

Puoi eseguire il provisioning di un'istanza del server virtuale da un'immagine creata da un fornitore di terze parti. Le immagini di terze parti sono disponibili tramite il link delle immagini cloud del catalogo {{site.data.keyword.cloud}}.
{:shortdesc}

## Informazioni preliminari
Prima di cominciare, assicurati di aver configurato le tue credenziali del catalogo {{site.data.keyword.cloud_notm}}.

Per il catalogo {{site.data.keyword.Bluemix_notm}}, devi disporre di un account di cui è stato eseguito l'upgrade per ordinare i server virtuali. Per ulteriori informazioni sull'upgrade del tuo account, consulta [Passaggio all'ID IBM](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

## Selezione di un'immagine del server virtuale
1. Accedi al catalogo [{{site.data.keyword.cloud_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/catalog/){: new_window} utilizzando le tue credenziali univoche.
2. Nella sezione **Immagini cloud**, individua e fai clic sull'immagine di terze parti che vuoi distribuire.
3. Controlla i dettagli dell'immagine personalizzata e fai clic su **Continua**. Viene visualizzata la pagina **Istanza server virtuale - Immagine personalizzata** con la tua immagine personalizzata preselezionata.

## Controllo e scelta delle tue opzioni di distribuzione
Per ulteriori informazioni, consulta i seguenti argomenti:

|              Opzioni di distribuzione                           |  Descrizione                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Server virtuale pubblico](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)            | Gestito da IBM, distribuzioni server virtuale a più tenant|
|[Server virtuale temporaneo](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)| Gestito da IBM, distribuzioni server virtuale a più tenant a un costo ridotto e consigliati per i carichi di lavoro flessibili |
|[Server virtuale riservato](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | Gestito da IBM, distribuzioni server virtuale a più tenant con capacità garantita per un termine del contratto |
|[Server virtuale dedicato](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)      | Gestito da IBM, distribuzioni server virtuale a singolo tenant            |
{: caption="Tabella 1. Opzioni di distribuzione" caption-side="top"}

## Provisioning di un server virtuale
Dopo aver deciso un'opzione di distribuzione, avvia il processo di provisioning. Per ulteriori informazioni, fai riferimento ai seguenti argomenti.

Poiché hai avviato il processo di provisioning con un'immagine personalizzata, non puoi modificare il tipo di immagine durante il processo di provisioning.
{:note}

|              Istruzioni di provisioning                                         |  Descrizione                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisioning di istanze pubbliche](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                | Provisioning di istanze pubbliche con varie opzioni             |
|[Provisioning di istanze temporanee](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                | Provisioning di istanze temporanee con varie opzioni            |
|[Provisioning della capacità e delle istanze riservate](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | Provisioning di capacità e istanze riservate con varie opzioni |
|[Provisioning di istanze e host dedicati](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)| Provisioning di istanze private o dedicate su host dedicati.|
{: caption="Tabella 2. Informazioni di provisioning" caption-side="top"}


## Passi successivi
Dopo aver eseguito il provisioning del tuo server virtuale ed è possibile utilizzarlo, puoi configurare i tuoi server virtuali utilizzando la console
{{site.data.keyword.cloud_notm}} o la {{site.data.keyword.slapi_short}}. Per ulteriori informazioni, vedi [Configurazione di server virtuali](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
