---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:table: .aria-labeledby="caption"}

# Informazioni sulla sospensione della fatturazione
{: #requirements}

Quando spegni un server virtuale che supporta la funzione di sospensione della fatturazione, non accumuli costi per alcune risorse di calcolo. La fatturazione si arresta automaticamente quando il server viene spento. La funzione di sospensione della fatturazione ti aiuta a ridurre i costi e a prevenire un reprovisioning di un server virtuale quando ti servono nuovamente le risorse.
{:shortdesc}

La maggior parte delle istanze del server virtuale creata prima del 1° novembre 2018 non supporta la funzione di sospensione della fatturazione. Per appurare se la tua istanza del server virtuale supporta la funzione di sospensione della fatturazione, vedi [Visualizzazione della funzione di sospensione della fatturazione](vsi_viewing_suspend.html). 

Questa funzione è disponibile nei data center di tutto il mondo. Per eseguire il provisioning di un'istanza del server virtuale che supporta la funzione di sospensione della fatturazione, l'istanza del server virtuale deve essere configurata con le seguenti impostazioni:

* SAN orario
* Caratteristiche pubbliche di una delle seguenti famiglie:
  * Bilanciato
  * Calcolo
  * Memoria

Puoi utilizzare la funzione di sospensione della fatturazione come un'alternativa più rapida al provisioning e al recupero di un'istanza del server virtuale.
{:tip}

La fatturazione viene sospesa solo quando disattivi la tua istanza del server virtuale tramite {{site.data.keyword.slportal_full}}, la CLI o {{site.data.keyword.slapi_short}}. Se disattivi l'istanza del server virtuale direttamente attraverso il SO, la fatturazione non viene sospesa per quella istanza.
{:note}

## Dettagli del provisioning

Puoi eseguire il provisioning di un'istanza del server virtuale che supporta la funzione di sospensione della fatturazione tramite la CLI, il catalogo {{site.data.keyword.cloud_notm}} o la {{site.data.keyword.slapi_short}}. Per ulteriori informazioni sul provisioning delle istanze del server virtuale pubbliche, vedi [Provisioning di istanze pubbliche](../vsi/vsi_provision_public.html).

Per il catalogo {{site.data.keyword.cloud_notm}}, devi disporre di un account di cui è stato eseguito l'upgrade per ordinare i server virtuali. Per ulteriori informazioni sull'aggiornamento del tuo account, consulta [Passaggio all'ID IBM](https://console.bluemix.net/docs/admin/softlayerlink.html).
{:note}

### Provisioning tramite la API Softlayer
Puoi eseguire il provisioning di un'istanza del server virtuale che supporta la funzione di sospensione della fatturazione tramite la {{site.data.keyword.slapi_short}}. Per gli esempi di API, consulta [Provisioning di un'istanza pubblica utilizzando Effettua ordine oggetto](../vsi/vsi_provision_api.html#provisioning-a-public-instance-using-place-order-object). 

Devi specificare l'ID del pacchetto di sospensione della fatturazione specifico durante il processo di provisioning. Puoi eseguire una query di {{site.data.keyword.slapi_short}} per trovare l'ID del pacchetto di sospensione della fatturazione utilizzando il keyName `SUSPEND_CLOUD_SERVER`. Per un esempio di ricerca dei pacchetti del server, consulta [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Dettagli di fatturazione

È importante comprendere quali costi si arrestano e quali rimangono quando viene spenta la tua istanza del server virtuale.

| Risorsa                      | Fatturazione arrestata   | Fatturazione non arrestata |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          |          X        |                  |
| RAM                           |          X        |                  |
| Velocità porta                    |          X        |                  |
| Licenze sistema operativo     |          X        |                  |
| Monitoraggio componenti aggiuntivi          |          X        |                  |
| Indirizzi IP pubblici secondari |                   |         X        |
| Archiviazione                       |                   |         X        |
{: caption="Tabella 1. Dettagli sulla fatturazione della risorsa" caption-side="top"}   

Quando esegui il provisioning di un'istanza del server virtuale che supporta la funzione di sospensione della fatturazione, i tempi di utilizzo vengono calcolati per minuto, sia per il tempo in uso che per quello in sospensione della tua istanza del server virtuale. Anche se non avvii mai la funzione di sospensione della fatturazione spegnendo la tua istanza, la fatturazione viene calcolata per minuto del ciclo di vita dell'istanza.
{:note}

### Addebito di utilizzo minimo
Le istanze del server virtuale che supportano la funzione di sospensione della fatturazione possono prevedere un addebito di utilizzo minimo che viene applicato in alcuni casi. Se l'utilizzo è maggiore del 25%, vieni addebitato per tale utilizzo. Se l'utilizzo è inferiore al 25%, vieni addebitato per il 25% per le ore in cui l'istanza era presente nel ciclo di fatturazione corrente. 

### Ricevuta della fatturazione
Quando sospendi la fatturazione su un server virtuale, vedrai alcune modifiche nella tua fattura. Gli addebiti importanti ora vengono visualizzati come dettagli in base all'utilizzo. Ad esempio, potresti vedere le seguenti aggiunte che riflettono le ore disponibili, le utilizzate e il numero totale di ore addebitate:

```
Computing instance usage...
RAM usage...
Operating system usage...
```
{:screen}

## Dettagli risorsa

### Archiviazione

Quando sospendi la fatturazione su un'istanza del server virtuale, la fatturazione per l'archiviazione associata persiste, ma non puoi accedere ai dati archiviati mentre l'istanza del server virtuale è spenta. Quando riprendi la fatturazione sull'istanza, puoi accedere nuovamente ai tuoi dati.

### Indirizzi IP

Tutti gli indirizzi IP pubblici vengono conservati quando la fatturazione della tua istanza del server virtuale viene sospesa.

### Limitazioni

Le istanze del server virtuale sospese continuano a essere conteggiate ai fini della tua quota di dispositivi a livello di account. Per ulteriori informazioni sui limiti di istanze, consulta [FAQ: server virtuali](vsi_faqs_vs.html#concurrent).

## Passi successivi
Dopo aver eseguito il provisioning di un server virtuale che supporta la sospensione della fatturazione, puoi iniziare a sospendere e a riprendere la fatturazione sul dispositivo.

Quando la fatturazione viene sospesa su un'istanza del server virtuale, non puoi completare tutte le stesse azioni sull'istanza finché non riprendi la fatturazione sul dispositivo. Puoi vedere se il tuo dispositivo è arrestato, nonché la data rilevante in cui è stato modificato lo stato, tramite la {{site.data.keyword.slapi_short}} o accedendo alla pagina dei dettagli del dispositivo in {{site.data.keyword.slportal}}.

Per sospendere la fatturazione su un'istanza del server virtuale, spegni il server virtuale. Per ulteriori informazioni, vedi [Gestione dei server virtuali](vsi_managing.html).
