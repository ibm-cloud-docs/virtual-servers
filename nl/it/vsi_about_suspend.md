---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-26"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Informazioni sulla sospensione della fatturazione (Beta)
{: #requirements}

Quando spegni un server virtuale che supporta la funzione di sospensione della fatturazione, non accumuli costi per alcune risorse di calcolo. La fatturazione si arresta automaticamente quando il server viene spento. La funzione di sospensione della fatturazione ti aiuta a ridurre i costi e a prevenire un reprovisioning di un server virtuale quando ti servono nuovamente le risorse. La sospensione della fatturazione è supportata solo per i nuovi provisioning delle istanze, non per le esistenti.
{:shortdesc}

Per accedere alla funzione di sospensione della fatturazione, devi eseguire il provisioning di una nuova istanza del server virtuale utilizzando {{site.data.keyword.slapi_short}} per specificare il pacchetto di sospensione della fatturazione. La nuova istanza del server virtuale deve essere configurata con le seguenti impostazioni:

* SAN orario
* Una delle seguenti famiglie:
  * Bilanciato
  * Calcolo
  * Memoria
* Uno dei seguenti data center {{site.data.keyword.cloud}}:

| Data Center |         |
| ------------ | ------- | 
|SEO01         |  WDC01  |
|SAO01         |  WDC04  |
|TOK02         |  WDC06  |
|DAL01         |  WDC07  |
|DAL05         |  LON02  |
|DAL06         |  LON04  |
|DAL09         |  LON06  |
|DAL10         |  FRA02  |
|DAL12         |  FRA04  |
|DAL13         |  FRA05  |
{: caption="Tabella 1. Data center supportati" caption-side="top"}

Puoi utilizzare la funzione di sospensione della fatturazione come un'alternativa più veloce al provisioning e all'annullamento del provisioning di un'istanza del server virtuale.
{:tip}

## Provisioning

Per la beta, per eseguire il provisioning di un'istanza del server virtuale che supporta la funzione di sospensione della fatturazione, devi utilizzare {{site.data.keyword.slapi_short}}. Per gli esempi di API, consulta [Provisioning di un'istanza pubblica utilizzando Effettua ordine oggetto](../vsi/vsi_provision_api.html#provisioning-a-public-instance-using-place-order-object). 

Devi inoltre specificare l'ID del pacchetto di sospensione della fatturazione specifico durante il processo di provisioning. Puoi eseguire una query di {{site.data.keyword.slapi_short}} per trovare l'ID del pacchetto di sospensione della fatturazione utilizzando il keyName `SUSPEND_CLOUD_SERVER`. Per un esempio di ricerca dei pacchetti del server, consulta [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

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

**Nota:** quando esegui il provisioning di un'istanza del server virtuale che supporta la funzione di sospensione della fatturazione, i tempi di utilizzo vengono calcolati per minuto, sia per i tempo di utilizzi che di sospensione della tua istanza del server virtuale. Anche se non avvii mai la funzione di sospensione della fatturazione spegnendo la tua istanza, la fatturazione viene calcolata per minuto di ciclo di vita dell'istanza. 

### Addebito di utilizzo minimo
Le istanze del server virtuale che supportano la funzione di sospensione della fatturazione hanno un addebito di utilizzo minimo mensile. Se l'utilizzo è maggiore del 25%, vieni addebitato per tale utilizzo. Se l'utilizzo è inferiore al 25%, vieni addebitato per il 25% per le ore in cui l'istanza era presente nel ciclo di fatturazione corrente. 

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

Quando sospendi la fatturazione su un'istanza del server virtuale, l'archiviazione associata rimane, ma non puoi accedere ai dati mentre l'istanza del server virtuale è spenta. Quando riprendi la fatturazione sull'istanza, puoi accedere ai tuoi dati e riinizia la normale fatturazione.

### Indirizzi IP

Tutti gli indirizzi IP pubblici vengono conservati quando la fatturazione della tua istanza del server virtuale viene sospesa.

Puoi vedere se il tuo dispositivo è arrestato, nonché la data rilevante in cui è stato modificato lo stato, tramite {{site.data.keyword.slapi_short}} o accedendo alla pagina dei dettagli del dispositivo in {{site.data.keyword.slportal_full}}.

### Limitazioni

Il numero di istanze contemporanee supportato fa parte della tua quota di dispositivi al livello dell'account. Per ulteriori informazioni sui limiti di istanze contemporanee, consulta [FAQ: server virtuali](vsi_faqs_vs.html#concurrent).

## Passi successivi
Dopo aver eseguito il provisioning di un server virtuale che supporta la sospensione della fatturazione, puoi iniziare a sospendere e a riprendere la fatturazione sul dispositivo.
Quando la fatturazione viene sospesa su un'istanza del server virtuale, non puoi completare tutte le stesse azioni sull'istanza finché non riprendi la fatturazione sul dispositivo.

Per sospendere la fatturazione su un'istanza del server virtuale, spegni il server virtuale. Per ulteriori informazioni, vedi [Gestione dei server virtuali](vsi_managing.html).
