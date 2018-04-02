---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Gestione di istanze e host dedicati
{: #managing-virtual-servers}

La pagina Dettagli del dispositivo ti consente di gestire l'host e le istanze dedicate, tenere traccia dei tuoi ticket di supporto e monitorare la disponibilità dell'host. Puoi accedere e visualizzare le tue istanze host dedicate in due modi dall'elenco dei dispositivi-come parte del loro host o come un'istanza individuale.
{:shortdesc}

## Scheda di configurazione host
Puoi effettuare diverse attività dalla scheda **Configurazione** per l'host dedicato, inclusa la gestione delle tue istanze host dedicate. Nel menu a discesa delle azioni, puoi ridenominare l'host o annullarlo. Tutte le istanze dell'host dedicato assegnate devono essere annullate o migrate prima di poter annullare un host, altrimenti si riceverà un messaggio di errore.

Le note possono essere conservate sull'host e sulle sue istanze; ad esempio, la migrazione da myDallasHost a myTorHost è pianificata per il XX/XX/XXXX. I frame Generale, Sistema e Rete della pagina ti forniscono dettagli immediati sull'host. Tieni presente che il frame archiviazione fa riferimento alla capacità di archiviazione locale.

Il frame istanze contiene le istanze assegnate a un host specifico, così come la capacità di aggiungere le istanze all'host. Fai clic sul menu Azioni di un'istanza per:

* Riavviare
* Accendere e spegnere
* Ridenominare
*	Visualizzare log di controllo
*	Aggiornare o annullare l'aggiornamento
*	Annullare
*	Migrare

## Scheda dei ticket host
Utilizza la scheda Ticket per aprire i ticket di supporto per l'host e per ognuna delle sue istanze facendo clic sul link Aggiungi un ticket per questo dispositivo.

## Scheda assegnazioni host
La scheda Assegnazione ti consente di visualizzare i core, la RAM e l'archiviazione locale disponibili per il tuo host dedicato. La sezione blu della "torta" rappresenta cosa viene utilizzato mentre la sezione bianca cosa è disponibile.

## Scheda istanza host dedicata
La pagina dei dettagli del dispositivo dell'istanza host dedicata, può essere raggiunta tramite la pagina dei dettagli del dispositivo dell'host o direttamente dall'elenco dei dispositivi. Sono presenti ulteriori schede al livello dell'istanza host dedicata; Configurazione e Ticket sono simili alle schede trovate al livello dell'host. Il link Modifica configurazione dispositivo, nella scheda Configurazione, ti consente di apportare modifiche alle impostazioni del tuo sistema (core, RAM e archiviazione locale) e della rete (velocità porta di uplink e larghezza di banda).

L'utilizzo visualizza un grafico tracciato per tempo basato sull'utilizzo della CPU per data. Puoi scorrere sul grafico per visualizzare l'utilizzo di CPU per una data e ora specifica, il che è utile quando tenti di determinare se hai bisogno di aggiungere capacità di elaborazione.

La larghezza di banda è un altro grafico tracciato per tempo che ti consente di immettere i parametri per visualizzare quanta larghezza di banda sta venendo utilizzata nel tempo. La scheda Archiviazione visualizza tutti i i blocchi aggiuntivi o l'archiviazione file nell'istanza.

# Annulla un host dedicato
Puoi annullare un host dedicato in qualsiasi momento. Un prerequisito per l'annullamento di un host è di aver migrato le istanze dedicate assegnate ad esso in un altro host dedicato o aver annullato le istanze. 
## Annulla un host dedicato dall'elenco dei dispositivi
Utilizza le seguenti istruzioni per annullare un host dedicato dall'elenco dei dispositivi.

1. Selezione **Dispositivo** > **Elenco dispositivi**.
2. Trova l'host dedicato da annullare e fai clic sul menu a discesa **Azioni**.
3. Seleziona **Annulla host**. 
4. Viene visualizzata una finestra a comparsa che contiene un elenco di istanze dedicate assegnate all'host. Dovrai migrare o annullare le istanze, se non lo hai già fatto, prima di annullare l'host. Fai clic su **OK**.

Riceverai un messaggio che conferma che l'host è stato annullato. Ci sarà un link al ticket di supporto per annullare l'host dedicato.
## Annulla un host dedicato dalla pagina dei dettagli del dispositivo
Utilizza le seguenti istruzioni per annullare l'host dedicato dalla pagina dei dettagli del dispositivo.

1. Selezione **Dispositivo** > **Elenco dispositivi**.
2. Trova l'host dedicato da annullare e fai doppio clic su di esso.
3. Verifica che tutte le istanze dedicate assegnate all'host dedicato siano state migrate o annullate.
4. Fai clic sul menu a discesa **Azioni** e seleziona **Annulla host**.

Riceverai un messaggio che conferma che l'host è stato annullato. Ci sarà un link al ticket di supporto per annullare l'host dedicato.

### Annulla un'istanza dedicata

Prima di poter annullare un host dedicato, devono essere annullate le istanze dedicate associate ad esso. Le istanze dedicate possono essere annullate direttamente dall'Elenco dispositivi, dalla pagina Dettagli del dispositivo del loro host assegnato o dalla loro pagina Dettagli del dispositivo. 

1. Seleziona l'istanza dedicata da annullare e fai clic sul menu a discesa **Azioni**.
2. Seleziona **Annulla dispositivo**.
3. Viene visualizzato un messaggio di avvertenza. Fai clic sul menu a discesa **Motivo** e seleziona il motivo per cui stai annullando l'istanza e fai clic su **Continua**.

Riceverai un messaggio che conferma che l'istanza è stata annullata. Ci sarà un link al ticket di supporto per annullare l'istanza dedicata.

