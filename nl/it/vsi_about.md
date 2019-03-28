---

copyright:
  years: 2017
lastupdated: "2017-11-15"

keywords: scalable virtual servers, virtual servers, key features

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Informazioni sui server virtuali
{: #about-virtual-servers}

{{site.data.keyword.BluVirtServers}} sono server virtuali scalabili che vengono acquistati con i core dedicati e le allocazioni di memoria. Sono una grande opzione se stai cercando risorse di calcolo, che possono essere aggiunti in minuti, con l'accesso alle funzioni come i template dell'immagine. L'hypervisor è totalmente gestito da {{site.data.keyword.BluSoftlayer_full}} e puoi eseguire le attività di gestione e configurazione utilizzando sia il {{site.data.keyword.slportal_full}} che l'{{site.data.keyword.slapi_short}}. I server virtuali vengono distribuiti alle stesse VLAN dei server fisici, consentendoti di estendere i carichi di lavoro tra più server virtuali e bare metal, mentre conservi l'interoperabilità. I server virtuali sono completamente personalizzabili quando li ordini, con opzioni per il ridimensionamento quando il tuo calcolo deve crescere.
{:shortdesc}

Quando crei un server virtuale, puoi scegliere tra la fatturazione oraria e mensile. Puoi inoltre scegliere tra un ambiente (a tenancy multipla) pubblico o un ambiente (a tenancy singola) dedicato. Successivamente, puoi scegliere i dischi locali ad alte prestazioni o l'archiviazione SAN aziendale per il tuo server virtuale.

## Funzioni chiave

Le seguenti informazioni elencano le funzioni chiave incluse con i server virtuali.
### Integrazione senza problemi

{{site.data.keyword.BluVirtServers_short}} sono distribuiti nello stesso pod e rete dei server bare metal e delle applicazioni di rete. Questo ti fornisce la flessibilità di utilizzare la migliore tecnologia per ogni carico di lavoro. Più server virtuali vengono normalmente distribuiti dietro un programma di bilanciamento del carico per utilizzare il traffico web. Questi server possono avere l'accesso diretto alla rete privata di secondo livello ai server del database bare metal e ad altri carichi di lavoro con uso intensivo.
### Completamente personalizzabile

Puoi aggiungere a ogni server virtuale diverse opzioni. Non esistono requisiti del pacchetto predefiniti, per cui puoi ottimizzare ogni server per il carico di lavoro che supporta.

### Provisioning rapido

Viene eseguito il provisioning dei server virtuali ogni 5 minuti, dandoti un tempo di attesa minimo tra l'ordine e il provisioning.
### Gestione remota

Come per tutti i servizi e soluzioni, hai la possibilità di gestire i tuoi server virtuali in remoto. Visualizza e gestisci tutti i dettagli del tuo dispositivo utilizzando il {{site.data.keyword.slportal}} o l'{{site.data.keyword.slapi_short}}. Puoi anche interagire con il server tramite le funzioni KVM o accedere al server con il controllo di gestione completo tramite le interfacce private o pubbliche.
### Facilmente scalabile

Dopo aver eseguito il provisioning del tuo server virtuale, puoi velocemente e facilmente ridimensionare la tua istanza e aggiungere o rimuovere le istanze aggiuntive su richiesta. Puoi prendere un template dell'immagine del server una volta terminata la configurazione e l'ottimizzazione e puoi quindi creare ulteriori server virtuali basati su tale immagine originale.
