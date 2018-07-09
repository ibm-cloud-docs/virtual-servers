---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Provisioning delle istanze temporanee
{: #ordering-vs-transient}
Puoi eseguire il provisioning delle tue istanze del server virtuale temporanee tramite {{site.data.keyword.slportal_full}}.
{:shortdesc}

## Informazioni preliminari
Prima di iniziare, controlla i seguenti prerequisiti.

  1. Assicurati di aver impostato le tue credenziali di {{site.data.keyword.slportal}}.

  2. Controlla le considerazioni sulla capacità dell'istanza del server virtuale.  Per ulteriori informazioni, vedi [Considerazioni sulla capacità](ts_capacity_bp.html).

## Accesso
Assicurati di aver eseguito l'accesso a {{site.data.keyword.slportal}}:

  1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.

Viene aperta la pagina principale del {{site.data.keyword.slportal}}.

## Provisioning di un'istanza del server virtuale temporanea
{: #ordering-transient-instance}
Dopo aver completato i prerequisiti, esegui il provisioning di un'istanza del server virtuale temporanea. Puoi eseguire il provisioning delle tue istanze temporanee in due modi: tramite il menu **Dispositivi** o l'icona **Dispositivi**.

### Provisioning di un'istanza del server virtuale temporanea tramite l'icona Dispositivi
Per eseguire il provisioning della tua istanza del server virtuale temporanea tramite l'icona *Dispositivi*, completa le seguenti istruzioni:

1.  Dal {{site.data.keyword.slportal}}, individua la sezione **Ordine** e fai clic su **Dispositivi**.
2.  In *Virtual Server pubblico* nella pagina *Dispositivi*, fai clic su **Temporaneo** per l'offerta del Virtual Server.
3.  Nella pagina *Configura il tuo server cloud*, compila tutte le informazioni importanti.
4.  Fai clic su **Aggiungi all'ordine** per continuare.
5.  Conferma o modifica le informazioni sul dominio per il server.
5.  Fai clic sulle caselle di spunta **Termini servizio cloud** e sulla casella di spunta **Accordo servizi di terze parti**.
6.  Conferma o immetti le tue informazioni di pagamento e fai clic su **Inoltra ordine**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

 Viene inviata una serie di email al tuo amministratore di riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione e il completamento del provisioning. L'email di completamento del provisioning include un link alla pagina *Dettagli del dispositivo*.

### Provisioning di un'istanza del server virtuale temporanea tramite il menu Dispositivi
{: #ordering-transient-devices-menu}

Puoi inoltre eseguire il provisioning delle tue istanze del server virtuale temporanee tramite il menu *Dispositivi* nella pagina principale del {{site.data.keyword.slportal}}.

1. Fai clic su **Dispositivi > Elenco dispositivi**.

   La pagina Dispositivi visualizza tutti i tipi di dispositivo-server virtuale, i server bare metal, gli host dedicati e i controller di distribuzione dell'applicazione NetScaler nel tuo account.
2. Fai clic sul link **Ordine dispositivi** nell'angolo in alto a destra.
3. In *Virtual Server pubblico* nella pagina *Dispositivi*, fai clic su **Temporaneo** per l'offerta del Virtual Server.
4. Nella pagina *Configura il tuo server cloud*, compila tutte le informazioni importanti.
5. Fai clic su **Aggiungi all'ordine** per continuare.
6. Conferma o modifica le informazioni sul dominio per il server.
7. Fai clic sulle caselle di spunta **Termini servizio cloud** e sulla casella di spunta **Accordo servizi di terze parti**.
8. Conferma o immetti le tue informazioni di pagamento e fai clic su **Inoltra ordine**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

Viene inviata una serie di email al tuo amministratore di riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione e il completamento del provisioning. L'email di completamento del provisioning include un link alla pagina *Dettagli del dispositivo*.

Puoi anche eseguire il provisioning di un server virtuale temporaneo utilizzando {{site.data.keyword.slapi_short}}. Per un esempio, consulta [Provisioning di un'istanza temporanea utilizzando Crea oggetto](../vsi/vsi_provision_api.html#api-rest-transient).
{:tip}

## Passi successivi
Dopo che è stato eseguito il provisioning del tuo server virtuale, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione del tuo server virtuale](../vsi/vsi_managing.html).
