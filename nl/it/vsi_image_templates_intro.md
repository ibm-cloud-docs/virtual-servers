---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Template dell'immagine
{: #image-templates}

Con i template dell'immagine {{site.data.keyword.BluVirtServers}}, puoi acquisire un'immagine del dispositivo per replicarne velocemente la configurazione con piccole modifiche per l'elaborazione.
{:shortdesc}

I template dell'immagine forniscono un'opzione di creazione dell'immagine per tutti i {{site.data.keyword.BluVirtServers_short}}, indipendentemente dal sistema operativo. I template dell'immagine ti consentono di acquisire un'immagine di un server virtuale esistente e crearne una nuova che si basa sull'immagine acquisita. I template dell'immagine non sono compatibili con i server bare metal.

## Come utilizzare i template dell'immagine
Le due azioni principali di ogni template dell'immagine sono creazione e distribuzione. Quando richiedi di creare un'immagine, il sistema automatizzato di {{site.data.keyword.BluSoftlayer_full}} porta il tuo server offline. Mentre il server è offline, viene creato un backup compresso dei tuoi dati, vengono registrate le informazioni di configurazione e il template dell'immagine viene memorizzato nella SAN di {{site.data.keyword.BluSoftlayer_notm}}. Durante la fase di distribuzione del template dell'immagine, il sistema automatizzato crea un nuovo server basato sui dati raccolti dall'immagine selezionata. Il processo di distribuzione effettua regolazioni per il volume, ripristina i dati copiati e quindi apporta le modifiche finali di configurazione (ad esempio, le configurazioni di rete) per il nuovo host.

Per ulteriori informazioni sui template dell'immagine, vedi [Introduzione ai template dell'immagine](/docs/infrastructure/image-templates?topic=image-templates-getting-started-with-image-templates).
