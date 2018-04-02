---



copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Template dell'immagine
Con i template dell'immagine {{site.data.keyword.BluVirtServers}}, puoi acquisire un'immagine del dispositivo per replicarne velocemente la configurazione con piccole modifiche per l'elaborazione. 
{:shortdesc}

I template dell'immagine standard forniscono un'opzione di creazione dell'immagine per tutti i {{site.data.keyword.BluVirtServers_short}}, indipendentemente dal sistema operativo. I template dell'immagine standard ti consentono di acquisire un'immagine di un server virtuale esistente e crearne una nuova che si basa sull'immagine acquisita. Questi template non sono compatibili con i server bare metal.

## Come utilizzare i template dell'immagine
Le due azioni principali di ogni template dell'immagine sono creazione e distribuzione. Quando richiedi di creare un'immagine, il sistema automatizzato di {{site.data.keyword.BluSoftlayer_full}} porta il tuo server offline. Mentre il server è offline, viene creato un backup compresso dei tuoi dati, vengono registrate le informazioni di configurazione e il template dell'immagine viene memorizzato nella SAN di {{site.data.keyword.BluSoftlayer_notm}}. Durante la fase di distribuzione del template dell'immagine, il sistema automatizzato crea un nuovo server basato sui dati raccolti dall'immagine selezionata. Il processo di distribuzione effettua regolazioni per il volume, ripristina i dati copiati e quindi apporta le modifiche finali di configurazione (ad esempio, le configurazioni di rete) per il nuovo host.

## Immagini private

Le immagini private sono immagini create da un utente sull'account o immagini create su un altro account e condivise. Per impostazione predefinita, tutte le immagini che vengono create sono private. 

## Immagini pubbliche

Le immagini pubbliche sono macchine preconfigurate che vengono pubblicate da {{site.data.keyword.BluSoftlayer_notm}} o rese pubbliche dai clienti e sono disponibili per l'uso da parte di tutti i clienti {{site.data.keyword.BluSoftlayer_notm}}. I server virtuali forniti tramite i template dell'immagine pubblica sono generalmente configurati per ottenere prestazioni ottimali, con precise combinazioni di una serie di specifiche di configurazione.

Per ulteriori informazioni sui template dell'immagine, vedi [Introduzione ai template dell'immagine](/docs/infrastructure/image-templates/image_index.html).
