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
{:table: .aria-labeledby="caption"}


# Avvio del kernel di salvataggio
{: #launching-rescue}

Il kernel di salvataggio è un ambiente di salvataggio live, progettato per fornirti la possibilità di portare un server bare metal o virtuale online, per poter risolvere i problemi del sistema che normalmente possono venire risolti tramite un ricaricamento SO. Il kernel di salvataggio deve essere avviato nella console {{site.data.keyword.cloud}}. Utilizza le seguenti istruzioni per avviare il kernel di salvataggio di un dispositivo.
{:shortdesc}

## Informazioni preliminari
Per prima cosa passa al menu del dispositivo e assicurati di disporre delle autorizzazioni account corrette per completare le attività.

* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assicurati di avere tutte le autorizzazioni account necessarie e l'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione dell'infrastruttura classica **Manage Users**, può modificare le autorizzazioni.

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione accesso dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Avvio del kernel di salvataggio

1. Dal menu **Dispositivi**, seleziona **Elenco dispositivi**.
2. Dall'**Elenco dispositivi**, fai clic sul nome del dispositivo che desideri salvare.
3. Nel menu *Azioni*, seleziona **Modo di salvataggio**.
4. Fai clic su **Sì** per passare immediatamente il tuo dispositivo al kernel di salvataggio. 

## Avvio del kernel di salvataggio per un'istanza Windows

1. Dal menu **Dispositivi**, seleziona **Elenco dispositivi**.
2. Dall'**Elenco dispositivi**, fai clic sul nome del dispositivo che desideri salvare.
3. Nel menu *Azioni*, seleziona **Avvia da immagine**.
4. Seleziona **Avvio da questa immagine** accanto all'immagine pubblica, *WindowsRescueStandalone.iso*.

## Passi successivi
Dopo aver avviato il kernel di salvataggio, il dispositivo viene spento e riavviato nel kernel di salvataggio per il sistema operativo del dispositivo. Questa operazione potrebbe richiedere alcuni minuti.

L'accesso remoto al dispositivo è disponibile dall'indirizzo IP del dispositivo. Puoi accedere al dispositivo nel kernel di salvataggio utilizzando le credenziali amministratore o root per i dispositivi che sono registrati nella console {{site.data.keyword.cloud_notm}}. Quando utilizzi il kernel di salvataggio, puoi risolvere e rilevare problemi come se fossi su un dispositivo avviato regolarmente. Se necessario, puoi montare le unità nel SO del kernel di salvataggio. Per uscire dal kernel di salvataggio e riportare il dispositivo nel suo ambiente regolare, riavvia il dispositivo nella console {{site.data.keyword.cloud_notm}} o dal SO del kernel di salvataggio.

Per ulteriori informazioni sul riavvio di un dispositivo, vedi [Gestione dei server virtuali](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
