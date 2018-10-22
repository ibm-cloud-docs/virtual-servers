---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-10"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Istanze e host dedicati 

Gli host dedicati sono server virtuali che ti consentono di specificare il data center e il POD in cui desideri sia posizionato l'host. In seguito assegna le istanze o le macchine virtuali a un host specifico per il massimo controllo sul posizionamento del carico di lavoro e sulle opzioni di provisioning del costo flessibile.
{:shortdesc}

## Capacità garantita
Disponi di capacità garantita nel data center e POD in cui hai posizionato il tuo host. Ad esempio, se il POD che contiene i tuoi host e istanze dedicati raggiunge la capacità, puoi continuare ad assegnare le istanze dedicate al tuo host se dispone di spazio appropriato.

## Carichi di lavoro visibili
Puoi visualizzare il consumo delle risorse globale per tutte le istanze dedicate assegnate a un host dedicato in una pagina. Visualizza l'utilizzo di core, RAM e archiviazione locale, che ti aiuta a determinare se è necessario migrare le istanze dedicate in un altro host dedicato. Questo livello di granularità ti fornisce la possibilità di gestire i tuoi carichi di lavoro con il massimo controllo. 

## Gestione post distribuzione
In aggiunta alla visibilità e alla capacità garantita dei tuoi carichi di lavoro, puoi migrare le tue istanze dedicate tra gli host dedicati per il massimo controllo sul posizionamento del carico di lavoro.

## Manutenzione
Alcune volte, la manutenzione dell'infrastruttura richiede che un host dedicato venga riavviato. Ad esempio, l'hypervisor Xen potrebbe aver bisogno di un aggiornamento. Se hai più host dedicati, disponi delle seguenti opzioni per ridurre il tempo di inattività. 
* La manutenzione viene effettuata dai POD all'interno di un data center. Puoi distribuire i tuoi host dedicati per separare i POD ed estendere la manutenzione richiesta. 
* Puoi creare un ticket di supporto per un host dedicato per richiedere che una manutenzione pianificata venga ritardata. Durante questo periodo, puoi migrare le istanze dedicate (offline) tra gli host dedicati nello stesso POD.

## Alta disponibilità
Se un host dedicato ha un malfunzionamento, i carichi di lavoro sull'host dedicato vengono automaticamente migrati a un nuovo host dedicato. Le istanze dedicate rimangono dedicate per tutto il ciclo di vita del server virtuale.

Per gli scenari di alta disponibilità, potresti voler prendere in considerazione di avere un ulteriore host dedicato designato. Ad esempio, l'host dedicato aggiuntivo ti fornisce la flessibilità di migrare i carichi di lavoro per le finestre di manutenzione.
