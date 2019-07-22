---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Gestione di server virtuali
{: #managing-virtual-servers}

Puoi gestire i server virtuali, insieme ad altri dispositivi, dall'elenco dei dettagli del dispositivo.
{:shortdesc}


## Informazioni preliminari
Per prima cosa passa al menu del dispositivo e assicurati di disporre delle autorizzazioni account corrette per completare le attività.

* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assicurati di avere tutte le autorizzazioni account necessarie e l'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione dell'infrastruttura classica **Manage Users**, può modificare le autorizzazioni.

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione accesso dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Tipi di dispositivo
L'elenco dei dettagli del dispositivo ti mostra i seguenti tipi di dispositivo:

|Dispositivo|Tipo di dispositivo|
| ------  | ------------ | 
|Server virtuali|Virtuale|
|Server bare metal| Server |
| Host dedicati | Host virtuale dedicato | 
{: caption="Tabella 1. Tipi di dispositivo" caption-side="top"}

Le azioni che puoi visualizzare dipendono dal tipo di dispositivo, così come le autorizzazioni concesse al tuo account utente.

Completa le seguenti istruzioni per eseguire le attività di gestione per i tuoi server virtuali.

1. Dal menu **Dispositivi**, seleziona **Elenco dispositivi**.
2. Fai clic su **Azioni** per il dispositivo che vuoi gestire e seleziona l'attività pertinente.

* Puoi interagire con i server nella console {{site.data.keyword.cloud_notm}} sia nella vista dell'istantanea (un riepilogo del tuo dispositivo) che nella pagina dei dettagli del dispositivo (un elenco completamente dettagliato). Per visualizzare e interagire con il tuo server nella vista dell'istantanea, fai clic sulla freccia accanto al nome del dispositivo per espandere la vista. Per visualizzare e interagire con il tuo server nella pagina dei dettagli del dispositivo, fai clic sul nome del dispositivo del server.

* Puoi aggiungere note a un dispositivo in qualsiasi momento dalla scheda **Configurazione**. Le note possono aiutare a identificare i dettagli del dispositivo, il suo uso e le azioni che sono state intraprese sul dispositivo.
 {:tip}

## Riavviare
Un riavvio è una delle azioni dispositivo più elementari. Il riavvio di un dispositivo comporta un immediato spegnimento e riavvio del tuo dispositivo e viene effettuato per vari motivi, spesso specifico per il dispositivo o per i bisogni di business di un utente individuale. I riavvii del dispositivo possono essere fatti dall'elenco dei dispositivi e dalla vista del dispositivo di un dispositivo individuale. I server virtuali possono essere riavviati in qualsiasi momento.

Un riavvio è molto utile quando riscontri un problema in cui il server non può avviare il sistema operativo a causa di un problema di configurazione.  Puoi anche eseguire l'avvio nel kernel di salvataggio. Dopo l'avvio nel kernel di salvataggio, puoi montare le unità del tuo server e poi correggere il problema di configurazione. Dopo aver risolto il problema, riavvia semplicemente il server dalla riga di comando ed esso verrà riavviato nel kernel predefinito del tuo server.
{:tip}

## Accensione/Spegnimento
Se il dispositivo è stato spento, questo rimane nello stato spento e deve essere acceso manualmente ripetendo i passi precedenti. Gli utenti non possono interagire con un dispositivo quando è spento. Se il server virtuale supporta la funzione di sospensione della fatturazione, la fatturazione viene sospesa per alcune risorse di calcolo. Non puoi completare tutte le attività di gestione in un'istanza finché non viene ripresa la fatturazione. Per ulteriori informazioni, vedi [Sospensione della fatturazione](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing). Per appurare se la tua istanza del server virtuale supporta la funzione di sospensione della fatturazione, vedi [Visualizzazione della funzione di sospensione della fatturazione](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature#viewing-suspend-billing-feature). Se il dispositivo è stato acceso, può avvenire la normale interazione. Rimarrà acceso finché non vengono effettuate ulteriori azioni.

## Ridenominare
Dopo aver ridenominato il dispositivo, il nome viene automaticamente aggiornato nella console {{site.data.keyword.cloud_notm}}. Se effettui una ricerca nella console {{site.data.keyword.cloud_notm}}, utilizza il nuovo nome del dispositivo quando tenti di individuare il contenuto ad esso associato. Ripeti i passi precedenti per ridenominare il dispositivo in qualsiasi momento.

## Annullare
Se annulli un dispositivo, interrompi l'utilizzo di tale dispositivo. I dispositivi possono essere annullati immediatamente o alla ricorrenza della fatturazione. Dopo aver confermato l'annullamento del dispositivo, l'azione non può essere annullata. Non possono venire forniti rimborsi per le cancellazioni immediate.

Dopo aver confermato l'annullamento, inizierà il processo di annullamento del dispositivo. Se è stato richiesto un annullamento immediato, il dispositivo verrà annullato immediatamente. Se è stato richiesto un annullamento della ricorrenza di fatturazione, il dispositivo rimarrà attivo fino alla prossima ricorrenza di fatturazione. Dopo l'annullamento, il dispositivo non verrà più visualizzato nell'elenco di dispositivi nella console {{site.data.keyword.cloud_notm}}. Le voci di fatturazione verranno inoltre rimosse dalle fatture quando tutti i saldi in sospeso saranno stati pagati sul dispositivo, se presenti. Per domande su una fattura per un dispositivo annullato, apri un ticket e seleziona Richiesta di account come oggetto del ticket. Non possono venire forniti rimborsi per le cancellazioni immediate.

## Passi successivi
Se devi riconfigurare un server virtuale esistente, consulta [Riconfigurazione di un server virtuale esistente](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).
