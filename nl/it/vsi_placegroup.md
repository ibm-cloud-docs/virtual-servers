---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Gruppi di posizionamento
{: #placement-groups}

L'alta disponibilità (HA, High Availability) è un aspetto importante di qualsiasi distribuzione cloud. Sia che si tratti del sito web del tuo business di e-commerce o di un database di produzione utilizzato dall'applicazione chiave della tua azienda, deve rimanere attivo. A questo scopo, la messa a punto di un'infrastruttura resiliente è qualcosa che i nostri client di architettura IT si sforzano di implementare per raggiungere percentuali di “tempo di attività” sempre più elevate. Sebbene il tempo di attività sia strettamente monitorato nelle organizzazioni IT, può scendere sotto i livelli chiave o comportare dei tempi di inattività considerevoli, che rappresentano un enorme problema per l'intero business.

La creazione della ridondanza ad ogni livello della tua infrastruttura per eliminare ogni singolo punto di errore (SPOF) è la chiave per una corretta esecuzione di questa metrica. Per i carichi di lavoro in esecuzione sui server virtuali, comporta l'implementazione delle soluzioni di failover con più server virtuali che possono automaticamente sostituirsi tra loro nel caso di un arresto anomalo.

Tuttavia, a meno che il provisioning dei tuoi server virtuali pubblici non venga eseguito in data center diversi, non esiste alcun modo per determinare dove dovrebbero essere posizionati l'uno rispetto all'altro. Questo può essere problematico se stai 1) implementando l'HA e 2) i tuoi server virtuali si trovano sullo stesso host fisico, lasciandoli vulnerabili nel caso di un'interruzione di una singola parte di hardware. Mentre questo potrebbe essere improbabile, i gestori IT non possono disporre di uno SPOF per le applicazioni critiche. La creazione tramite i data center è opzionale, ma può introdurre alcune verifiche di rete che richiedono ulteriori dispositivi o l'aumento della latenza, specialmente nelle regioni con un solo data center.

La progettazione dei gruppi di posizionamento per i server virtuali {{site.data.keyword.cloud}} risolve questo problema. I gruppi di posizionamento ti forniscono un certo controllo sull'host in cui viene posizionato un nuovo server virtuale pubblico. Con questa release è presente una regola di “distribuzione”, ossia tutti i server virtuali all'interno di un gruppo di posizionamento vengono tutti distribuiti su host differenti. Puoi creare un'applicazione altamente disponibile all'interno di un data center che sa che i tuoi server virtuali sono isolati tra loro.

I gruppi di posizionamento con la regola di “distribuzione” sono disponibili per la creazione in data center {{site.data.keyword.cloud_notm}} selezionati. Una volta creato, puoi eseguire il provisioning di un nuovo server virtuale in tale gruppo e garantire che non si trovi sullo stesso host dei tuoi altri server virtuali. Il vantaggio principale? Non c'è assolutamente alcun addebito per l'utilizzo di questa funzione. A seconda della disponibilità, i gruppi di posizionamento {{site.data.keyword.cloud_notm}} per i server virtuali sono una funzione gratuita.

Puoi creare il tuo gruppo di posizionamento e assegnargli fino a cinque nuove istanze del server virtuale. Con la regola di "distribuzione", il provisioning di ciascuno dei server virtuali viene eseguito su host fisici differenti.

## Passi successivi

Per creare e gestire nuovi gruppi di posizionamento, vedi [Gestione dei gruppi di posizionamento](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup#vsi_managing_placegroup).
