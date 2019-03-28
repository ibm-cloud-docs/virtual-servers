---
copyright:
  years: 2014, 2018
lastupdated: "2018-10-23"
---

{:new_window: target="_blank"}

# Opzioni di archiviazione
{: #storage-options}

Puoi scegliere tra SAN (SAN portatile) o archiviazione locale per ciascun server virtuale. Puoi integrare l'archiviazione locale o SAN con altri prodotti se necessario.

## Archiviazione locale

L'archiviazione locale viene creata su dischi che sono locali nell'host del server virtuale. L'archiviazione locale fornisce prestazioni di lettura/scrittura disco migliorate. I dischi sono creati in una configurazione RAID (redundant array of independent disks) per la ridondanza, il posizionamento sul disco e il monitoraggio dell'integrità che sono completamente gestiti da {{site.data.keyword.cloud}}. Nei data center più recenti, questa archiviazione è tutta su SSD (solid state drive) per fornire le migliori prestazioni.

## Archiviazione SAN portatile

I volumi di archiviazione portatile sono soluzioni di archiviazione ausiliarie disponibili esclusivamente su {{site.data.keyword.BluVirtServers_short}}.  La SAN portatile è sviluppata sui cluster di archiviazione all flash di {{site.data.keyword.cloud_notm}} invece che sull'archiviazione host locale. Questa infrastruttura fornisce una maggiore resilienza nel caso di un malfunzionamento host e può anche supportare volumi molto più grandi. Nel caso di un malfunzionamento host, le istanze del server virtuale che utilizzano l'archiviazione basata su SAN vengono automaticamente migrate ad altri host e riavviate.

L'archiviazione portatile è una soluzione ideale se desideri trasferire dati tra i server virtuali presenti in qualsiasi data center sulla rete di {{site.data.keyword.cloud_notm}}. I volumi di archiviazione portatile sono utili per le applicazioni di database che richiedono l'accesso all'archiviazione a livello di blocco non formattata e non elaborata e per lo spostamento di dataset di grandi dimensioni tra i {{site.data.keyword.BluVirtServers_short}}.

Tutti i dischi secondari sono allegati come archiviazione portatile. Nella maggior parte dei casi, questi dischi secondari possono essere scollegati in qualsiasi momento per consentirne lo spostamento su altri server virtuali.

**Eccezione:** con i server virtuali pubblici che utilizzano l'archiviazione locale bilanciata, non puoi scollegare i dischi primari o secondari.

I dischi possono essere ricollegati a un altro server, fintanto che la modifica non superi la quota del disco o il limite massimo della dimensione del volume del server virtuale di destinazione.

**Nota:** i dischi spostati vengono convertiti nel tipo di archiviazione del server di destinazione.

Quando un volume di archiviazione portatile è collegato a un server virtuale in un data center diverso rispetto al server virtuale originale, il sistema interno di {{site.data.keyword.cloud_notm}} copia il volume nella SAN del nuovo data center. Il sistema verifica quindi l'integrità del volume copiato e rimuove il volume portatile originale dalla SAN del data center originale.

## Limitazioni LVM

LVM (Logical volume management) non è supportato come uno schema di partizionamento avviabile. Con configurazione e supporto corretti del sistema operativo, i dischi del server virtuale secondari possono venire utilizzati per le partizioni LVM. Tuttavia, LVM non è un file system supportato per i template dell'immagine o le immagini flex.

## Archiviazione supplementare

I server virtuali sono completamente compatibili con {{site.data.keyword.filestorage_short}}, {{site.data.keyword.blockstorageshort}}, e {{site.data.keyword.cos_full}}. Questi tipi di archiviazione sono raccomandati per le unità cluster, l'archiviazione file condivisa, l'archiviazione dell'archivio, i requisiti di grande archiviazione o requisiti delle prestazioni specifici.

Per ulteriori informazioni sulle opzioni di archiviazione supplementare, consulta le seguenti risorse:

* [Introduzione all'archiviazione a blocchi](/docs/infrastructure/BlockStorage?topic=BlockStorage-GettingStarted)
* [Introduzione all'archiviazione file](/docs/infrastructure/FileStorage?topic=FileStorage-GettingStarted)
* [Introduzione all'archiviazione oggetti](/docs/services/cloud-object-storage?topic=cloud-object-storage-about-ibm-cloud-object-storage#about-ibm-cloud-object-storage)

## Passi successivi
Per ulteriori informazioni su come utilizzare i volumi di archiviazione portatile, vedi le seguenti attività:
* [Accesso all'archiviazione portatile](/docs/vsi/storage?topic=virtual-servers-accessing-portable-storage)
* [Modifica della descrizione dell'archiviazione portatile](/docs/vsi/storage?topic=virtual-servers-editing-a-portable-storage-description)
