---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

keywords: transient virtual servers, transient instances, transient offering, cost savings

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Server virtuali temporanei
{: #about-vs-transient}
L'offerta temporanea di {{site.data.keyword.BluVirtServers}} è una buona opzione se hai carichi di lavoro flessibili e vuoi contenere i costi. Risparmierai del denaro eseguendo il tuo carico di lavoro in un server virtuale temporaneo. Le istanze temporanee vengono fornite quando è presente della capacità disponibile non utilizzata. Pertanto, quando occorrono le risorse del data center per gli account on-demand completi, potresti anche perdere tali risorse. Il provisioning delle istanze temporanee viene annullato su una base FOFO (First-On First Off) quando è necessario recuperare tali risorse.   

I server virtuali temporanei offrono la seguente flessibilità:

* **Disponibilità globale**

    L'offerta server virtuale temporaneo è disponibile nei data center di tutto il mondo.

* **Risparmio sui costi**

    I server virtuali temporanei sono ideali per i carichi di lavoro di non produzione. Ad esempio, potresti utilizzare un'istanza temporanea per verificare e sviluppare le applicazioni o per verificare la scalabilità negli ambienti che non richiedono tempi di attività costanti.

Le istanze temporanee sono istanze pubbliche che utilizzano l'archiviazione con supporto SAN. Le seguenti famiglie di istanze pubbliche sono disponibili per questa offerta.

| Famiglie  | Descrizione                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Bilanciato](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Migliore per i carichi di lavoro cloud comuni che richiedono un bilanciamento di prestazioni e scalabilità. Utilizza l'archiviazione assegnata di rete.|
| [Calcolo](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Migliore per i carichi di lavoro con traffico web da moderato a elevato.|
| [Memoria](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Migliore per la memorizzazione nella cache e i carichi di lavoro di analisi in tempo reale. |
{: caption="Tabella 1. Selezioni di famiglie del server virtuale pubblico" caption-side="top"}

## Notifiche
Puoi utilizzare {{site.data.keyword.slapi_short}} per ricevere le notifiche quando le risorse sono disponibili per un'istanza temporanea. Puoi anche utilizzare la API per fornire programmaticamente un server virtuale temporaneo quando le risorse diventano disponibili. Allo stesso modo, puoi utilizzare la API per arrestare programmaticamente il provisioning delle istanze quando le risorse diventano indisponibili. Per ulteriori informazioni, vedi [Configurazione delle notifiche di recupero automatizzate](/docs/vsi?topic=virtual-servers-configuring-notifications-for-reclaims-of-transient-virtual-servers#configuring-notifications-for-reclaims-of-transient-virtual-servers).  

## Limitazioni
Tieni presenti le seguenti limitazioni prima di eseguire il provisioning di un server virtuale temporaneo.

* Il numero di istanze contemporanee supportato fa parte della tua quota di dispositivi al livello dell'account. Per ulteriori informazioni sui limiti di istanze contemporanee, consulta [FAQ: server virtuali](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#faqs-virtual-servers).
* Non è possibile eseguire l'upgrade o il downgrade delle istanze temporanee.
* Le risorse possono essere recuperate in qualsiasi momento, senza notifica.
* Le istanze temporanee non possono utilizzare l'archiviazione locale.
* Le istanze temporanee non possono utilizzare i profili basati su GPU.


## Passi successivi

Dopo aver controllato e selezionato il tuo profilo di server virtuale, è il momento di eseguire il provisioning del tuo server virtuale temporaneo. Per iniziare, consulta [Provisioning delle istanze temporanee](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient).

