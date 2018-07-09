---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# FAQ: server virtuali  

## Quali tipi di server virtuali sono disponibili per l'utilizzo?
{{site.data.keyword.BluSoftlayer_full}} offre un paio di tipi di server virtuali. L'offerta standard è un server virtuale su base pubblica, che è un ambiente a più tenant, adatto per diversi bisogni. Se stai cercando un ambiente a singolo tenant, considera l'offerta del Virtual Server dedicato. L'opzione del server virtuale dedicato è ideale per le applicazioni con requisiti della risorsa più severi. Per ulteriori informazioni sulle offerte del server virtuale correnti, consulta [Introduzione ai server virtuali](../vsi/vsi_index.html).

## Dove posso trovare le informazioni sui prezzi per i tipi di istanza pubblica?
Per informazioni sui prezzi, vedi [Crea il tuo server virtuale ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers){: new_window}.

## Posso aggiungere l'archiviazione disco al mio Virtual Server orario o mensile?
Puoi eseguire o annullare l'aggiornamento dell'archiviazione disco per tutti i server virtuali aggiornando le tue opzioni di archiviazione nei campi *Primo disco* fino a *Quinto disco* nella schermata *Configurazione* del dispositivo che desideri aggiornare. Per ulteriori informazioni, consulta [Riconfigurazione di un server virtuale esistente](../vsi/vsi_reconfigure.html).

## Quanti server virtuali orari posso avviare?

Per impostazione predefinita, un account ha un limite di 20 istanze che possono essere eseguite sui server virtuali pubblici, dedicati e bare metal in un determinato momento.  Se vuoi incrementare questo limite, contatta il supporto per farci sapere qualcosa di più su cosa stai facendo e di quante istanze contemporanee hai bisogno.

## Sarò addebitato per larghezza di banda per i miei server virtuali orari?

La fatturazione virtuale oraria è suddivisa per il traffico in entrata e in uscita. Tutto il traffico in entrata verso il tuo server virtuale è gratuito. Il traffico in uscita viene misurato e addebitato per GB, con i totali valutati alla fine del tuo periodo di fatturazione.

## In quali casi il mio server virtuale viene migrato su un altro host?

In casi limitati potrebbe essere necessario migrare un server virtuale su un altro host. Se è richiesta una migrazione, il server virtuale viene arrestato, migrato e quindi riavviato. Un server virtuale potrebbe essere migrato nei seguenti casi:

* Un hypervisor deve essere aggiornato, un host viene disattivato o un host non può più caricare nuove istanze. Se un host è contrassegnato per una di queste modifiche, quando viene riavviato uno dei suoi server virtuali dal {{site.data.keyword.slportal_full}}, il riavvio attiva automaticamente il server virtuale da migrare su un altro host.
* Manutenzione dell'infrastruttura. Potresti ricevere un'email che indica che è necessaria la manutenzione su un sistema che ospita il tuo server virtuale. Potrebbe essere necessario migrare il tuo server virtuale come parte della manutenzione dell'infrastruttura.
* Un aggiornamento a un'istanza esistente. Per prestazioni costanti, se aggiorni un'istanza, questa potrebbe essere migrata a un host diverso per garantire che riceva la CPU e la memoria dedicata appropriata.

Durante una finestra di manutenzione potresti vedere un'opzione **Migra host** nel menu **Azioni** del tuo dispositivo nel {{site.data.keyword.slportal}}. L'opzione **Migra host** ti consente di migrare il server virtuale su un nuovo host a tuo piacimento durante un periodo di manutenzione specificato. Se non avvii la migrazione durante il periodo di manutenzione, il server virtuale viene migrato automaticamente per completare la manutenzione richiesta. L'opzione **Migra host** non persiste ed è disponibile solo durante i periodi di manutenzione che vengono comunicati tramite le notifiche di manutenzione.

Potresti anche visualizzare l'opzione **Migra host** se è richiesto che uno dei tuoi server virtuali abbia un determinato livello di hypervisor che non è disponibile nell'host corrente.

## Cosa succede ai miei dati quando la mia archiviazione portatile viene eliminata?

Quando l'archiviazione viene eliminata, tutti i puntatori ai dati su quel volume vengono rimossi, quindi i dati diventano completamente inaccessibili. Se l'archiviazione fisica viene rifornita in un altro account, viene assegnata una nuova serie di puntatori. Non c'è modo per il nuovo account di accedere ai dati che potevano trovarsi nell'archiviazione fisica. La nuova serie di puntatori mostra tutti 0. Quando vengono scritti i nuovi dati nel volume/LUN, tutti i dati non accessibili che ancora esistono vengono sovrascritti.

## Posso utilizzare una sottoscrizione Red Hat Cloud Access per creare un server virtuale?

Sì. Quando importi un'immagine, puoi specificare che fornirai la licenza del sistema operativo. Per ulteriori informazioni, vedi [Utilizza Red Hat Cloud Access](../infrastructure/image-templates/use-red-hat-cloud-access.html). Puoi quindi ordinare un server virtuale da quel template dell'immagine e utilizzare la tua sottoscrizione [Red Hat Cloud Access ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} esistente.

## Quale è la differenza tra un server virtuale e un VPS (virtual private server)?

Un server virtuale è simile alle piattaforme VPS (virtual private server) o VDS (virtual dedicated server) con cui potresti già avere familiarità. Questi ambienti "server virtuale" consento il provisioning di ambienti distinti privatamente e in sicurezza su un solo nodo hardware, ma VDS e VPS sono più limitati nelle loro capacità. Le opzioni VPS e VDS sono generalmente circoscritte a un'architettura a singolo server, per cui solo le risorse che possono essere aggiunte o divise tra ogni server virtuale in una VDS o VPS sono le risorse fisicamente installate su tale server singolo.

Viene eseguito il provisioning dei server virtuali su un'architettura cloud a più server che raggruppa tutte le risorse hardware disponibili per le istanze individuali da utilizzare. I server virtuali possono utilizzare una piattaforma di archiviazione primaria basata su SAN a capacità altamente condivisa o un'archiviazione disco locale dalle elevate prestazioni. Poiché ogni istanza fa parte di un ambiente cloud più grande, la comunicazione tra tutti i server virtuali è istantanea.

## Non posso collegarmi all'API di virtualizzazione. In che modo posso correggere l'errore?

Questo errore generalmente si verifica perché una password è obsoleta. Per correggerlo, aggiorna la password root o di amministratore per il sistema operativo del server virtuale nel {{site.data.keyword.slportal_full}}.
