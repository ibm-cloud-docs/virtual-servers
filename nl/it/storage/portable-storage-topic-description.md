---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informazioni sui volumi di archiviazione portatile

I volumi di archiviazione portatile sono soluzioni di archiviazione ausiliarie disponibili esclusivamente su {{site.data.keyword.BluVirtServers_short}}. Possono essere connessi a un solo server virtuale alla volta. Costituiscono inoltre una soluzione ideale se desideri trasferire dati tra i server virtuali presenti in qualsiasi data center sulla rete di {{site.data.keyword.cloud}}. I volumi di archiviazione portatile sono utili per le applicazioni di database che richiedono l'accesso all'archiviazione a livello di blocco non formattata e non elaborata e per lo spostamento di dataset di grandi dimensioni tra i {{site.data.keyword.BluVirtServers_short}}.

Quando un volume di archiviazione portatile è collegato a un server virtuale in un data center diverso rispetto al server virtuale originale, il sistema interno di {{site.data.keyword.cloud}} copia il volume nella SAN del nuovo data center. Il sistema verifica quindi l'integrità del volume copiato e rimuove il volume portatile originale dalla SAN del data center originale.

## Passi successivi
Per ulteriori informazioni su come utilizzare i volumi di archiviazione portatile, vedi le seguenti attività:
* [Accesso all'archiviazione portatile](/docs/vsi/storage?topic=virtual-servers-accessing-portable-storage)
* [Modifica della descrizione dell'archiviazione portatile](/docs/vsi/storage?topic=virtual-servers-editing-a-portable-storage-description)
