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


# Gestione di server virtuali
{: #managing-virtual-servers}

Dall'elenco dei dispositivi, puoi gestire i server virtuali e altri dispositivi come i server bare metal e i firewall VLAN.
{:shortdesc}

Nell'elenco dei dispositivi, i server virtuali hanno un tipo di dispositivo di *Virtuale*. I server bare metal sono indicati con il tipo di dispositivo *Server*. Gli host dedicati hanno un tipo di dispositivo di *Host virtuale dedicato*. Molte interazioni disponibili per i dispositivi sono simili, ma ogni tipo di dispositivo dispone inoltre di interazioni specifiche per dispositivo.

Le seguenti attività di gestione del server virtuale sono disponibili dall'elenco dei dispositivi:
* Riavvio -  spegnimento immediato di un dispositivo e riavvio.
* Accensione / Spegnimento - accendere o spegnere un dispositivo in remoto.
* Ridenominazione - modifica o aggiornamento di un nome dispositivo.
* Annullamento - terminare l'utilizzo di un dispositivo. I dispositivi possono essere annullati immediatamente o alla ricorrenza della fatturazione. Dopo aver confermato l'annullamento del dispositivo, l'azione non può essere annullata. Non possono venire forniti rimborsi per le cancellazioni immediate.

Completa le seguenti istruzioni per eseguire le attività di gestione per i tuoi server virtuali dall'elenco dei dispositivi nel portale clienti.  
1. Accedi al [{{site.data.keyword.slportal_full}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche. 
2. Dal menu **Dispositivi**, seleziona **Elenco dispositivi**.
3. Fai clic su **Azioni** per il dispositivo che vuoi gestire e seleziona l'attività di gestione desiderata.

**Suggerimenti:** 
* Puoi interagire con i server nel {{site.data.keyword.slportal}} sia nella vista Istantanea (un riepilogo del tuo dispositivo) che nella schermata Dettagli del dispositivo (un elenco completamente dettagliato). Per visualizzare e interagire con il tuo server nella vista Istantanea, fai clic sulla freccia accanto al nome del dispositivo per espandere la vista. Per visualizzare e interagire con il tuo server nella schermata Dettagli del dispositivo, fai clic sul nome del dispositivo del server.
* Puoi aggiungere note a un dispositivo in qualsiasi momento dalla scheda **Configurazione**. Le note possono aiutare a identificare i dettagli del dispositivo, il suo uso e le azioni che sono state intraprese sul dispositivo.

## Operazioni successive
* **Riavviare**

    Un riavvio è una delle azioni dispositivo più elementari. Il riavvio di un dispositivo comporta un immediato spegnimento e riavvio del tuo dispositivo e viene effettuato per vari motivi, spesso specifico per il dispositivo o per i bisogni di business di un utente individuale. I riavvii del dispositivo possono essere fatti dall'elenco dei dispositivi e dalla vista del dispositivo di un dispositivo individuale. I server virtuali possono essere riavviati in qualsiasi momento.  

* **Accensione/Spegnimento**

    Se il dispositivo è stato spento, questo rimane nello stato spento e deve essere acceso manualmente ripetendo i passi precedenti. Gli utenti non possono interagire con un dispositivo quando è spento. Se il dispositivo è stato acceso, può avvenire la normale interazione. Rimarrà acceso finché non vengono effettuate ulteriori azioni.

* **Ridenominare**

  Dopo aver ridenominato il dispositivo, il nome verrà automaticamente aggiornato nel {{site.data.keyword.slportal}}. Se effettui una ricerca nel {{site.data.keyword.slportal}}, utilizza il nuovo nome del dispositivo quando tenti di individuare il contenuto ad esso associato. Ripeti i passi precedenti per ridenominare il dispositivo in qualsiasi momento.

* **Annullare**

  Dopo aver confermato l'annullamento, inizierà il processo di annullamento del dispositivo. Se è stato richiesto un annullamento immediato, il dispositivo verrà annullato immediatamente. Se è stato richiesto un annullamento della ricorrenza di fatturazione, il dispositivo rimarrà attivo fino alla prossima ricorrenza di fatturazione. Dopo l'annullamento, il dispositivo non verrà più visualizzato nell'elenco di dispositivi nel {{site.data.keyword.slportal}}. Le voci di fatturazione verranno inoltre rimosse dalle fatture quando tutti i saldi in sospeso saranno stati pagati sul dispositivo, se presenti. Per domande su una fattura per un dispositivo annullato, apri un ticket e seleziona Richiesta di account come oggetto del ticket. Non possono venire forniti rimborsi per le cancellazioni immediate.
  
## Passi successivi
Se devi riconfigurare un server virtuale esistente, consulta [Riconfigurazione di un server virtuale esistente](../vsi/vsi_reconfigure.html).

