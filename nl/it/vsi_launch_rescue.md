---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Avvio di un kernel di salvataggio
{: #launching-rescue}

Il kernel di salvataggio è un ambiente di salvataggio live, progettato per fornire ai clienti la possibilità di portare un server bare metal o virtuale online, per poter risolvere i problemi del sistema che normalmente possono venire risolti tramite un ricaricamento SO. Il kernel di salvataggio deve essere avviato nel {{site.data.keyword.slportal_full}}. Utilizza le seguenti istruzioni per avviare il kernel di salvataggio di un dispositivo.
{:shortdesc}

## Avvia il kernel di salvataggio

1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) utilizzando le tue credenziali univoche.
2. Dall'elenco dei dispositivi, fai clic sul nome del dispositivo che desideri salvare.
3. Fai clic sull'elenco a discesa *Azioni* nell'angolo in alto a destra e seleziona **Salvataggio**. (In alternativa, puoi fare clic sulla scheda *Gestione remota* e selezionare **Salvataggio**.)
4. Fai clic sul pulsante **Sì** per passare immediatamente il tuo dispositivo al kernel di salvataggio. Fai clic sul pulsante **No** per annullare l'azione.

## In VSI di Microsoft

1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) utilizzando le tue credenziali univoche.
2. Dall'elenco dei dispositivi, fai clic sul nome del dispositivo che desideri salvare.
3. Fai clic sull'elenco a discesa *Azioni* nell'angolo in alto a destra e seleziona **Avvio da immagine**.
4. Seleziona **Avvio da immagine** accanto all'immagine pubblica, *WindowsRescueStandalone.iso*.


## Passi successivi
Dopo aver avviato il kernel di salvataggio, il dispositivo viene spento e riavviato nel kernel di salvataggio per il sistema operativo del dispositivo. Questa operazione potrebbe richiedere alcuni minuti.

L'accesso remoto al dispositivo è disponibile dall'indirizzo IP del dispositivo. Puoi accedere al dispositivo nel kernel di salvataggio utilizzando le credenziali amministratore o root per i dispositivi che sono registrati nel {{site.data.keyword.slportal}}. Quando utilizzi il kernel di salvataggio, puoi risolvere e rilevare problemi come se fossi su un dispositivo avviato regolarmente. Se necessario, puoi montare le unità nel SO del kernel di salvataggio. Per uscire dal kernel di salvataggio e riportare il dispositivo nel suo ambiente regolare, riavvia il dispositivo nel {{site.data.keyword.slportal}} o dal SO del kernel di salvataggio.

Per ulteriori informazioni sul riavvio di un dispositivo, vedi [Gestione dei server virtuali](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
