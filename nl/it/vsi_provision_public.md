---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning di istanze pubbliche
{: #ordering-vs-public}

## Informazioni preliminari
Hai due opzioni per eseguire il provisioning delle tue istanze del server virtuale pubbliche. La prima è attraverso il catalogo {{site.data.keyword.Bluemix}} e la seconda tramite il {{site.data.keyword.slportal}}. Il catalogo e il {{site.data.keyword.slportal}} richiedono ID di accesso univoci. I tuoi nome utente e password del catalogo non funzionano per accedere al portale e viceversa.
{:shortdesc}

Prima di iniziare, controlla i seguenti prerequisiti.

  1. Assicurati di aver impostato le credenziali del catalogo {{site.data.keyword.Bluemix_notm}} o del {{site.data.keyword.slportal}}.

     **Nota:** per il catalogo {{site.data.keyword.Bluemix_notm}}, devi disporre di un account aggiornato per ordinare i server virtuali. Per ulteriori informazioni sull'aggiornamento del tuo account, consulta [Passaggio all'ID IBM](https://console.bluemix.net/docs/admin/softlayerlink.html).

  2. Se non lo hai fatto, rivedi le opzioni di distribuzioni che sono disponibili. Per ulteriori informazioni, consulta [Opzioni di distribuzione: server virtuale pubblico](../vsi/vsi_public.html).

  3. Controlla le considerazioni sulla capacità dell'istanza del server virtuale.  Per ulteriori informazioni, vedi [Considerazioni sulla capacità](ts_capacity_bp.html).

## Provisioning di un'istanza del server virtuale pubblica
{: #ordering-public-instance}

Dopo aver completato i prerequisiti, puoi iniziare a eseguire il provisioning di un'istanza del server virtuale pubblica. Puoi eseguire il provisioning dell'istanza pubblica attraverso il catalogo {{site.data.keyword.cloud_notm}} o {{site.data.keyword.slportal}}.

### Provisioning di un'istanza del server virtuale pubblica tramite il catalogo IBM Cloud
Per eseguire il provisioning di un'istanza del server virtuale pubblica tramite il catalogo {{site.data.keyword.cloud_notm}}, completa le seguenti istruzioni:

  1. Accedi al catalogo [{{site.data.keyword.cloud_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/catalog/){: new_window} utilizzando le tue credenziali univoche. 
  2. Nella sezione **Infrastruttura di calcolo**, fai clic sul tile **Server virtuali**.
  3. Seleziona l'opzione **Server virtuale pubblico**.
  4. Fai clic su **Crea**.
  5. Completa tutte le informazioni pertinenti per la tua istanza del server virtuale. 
  6. Dopo aver riesaminato il riepilogo dell'ordine, fai clic sulla casella di spunta **Accordi di servizio di terze parti**. 
  7. Fai clic su **Provisioning**.
  
### Provisioning di un'istanza del server virtuale pubblica tramite il portale del cliente
Per eseguire il provisioning della tua istanza del server virtuale pubblica tramite {{site.data.keyword.slportal}}, completa le seguenti istruzioni:

  1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.
  2. Individua la sezione **Order** e fai clic su **Devices**. 
  3. Nella pagina Devices, fai clic su **Hourly SAN**, **Hourly local**, **Monthly** o **Transient** per una delle offerte di Virtual Server.
  4. Nella pagina *Configure your Cloud Server*, compila tutte le informazioni pertinenti.
  5. Fai clic sul pulsante **Add to Order** per continuare.
  6. Conferma o modifica le informazioni sul dominio per il server.
  7. Fai clic sulle caselle di spunta **Cloud Service terms** e **Third-Party Service Agreement**.
  8. Conferma o immetti le tue informazioni di pagamento e fai clic sul pulsante **Submit Order**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

 Viene inviata una serie di email al tuo amministratore di riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione e il completamento del provisioning. L'email di completamento del provisioning include un link alla pagina *Device Details*, dopo aver eseguito l'accesso a {{site.data.keyword.Bluemix_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.

## Passi successivi
Dopo che è stato eseguito il provisioning del tuo server virtuale, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione del tuo server virtuale](../vsi/vsi_managing.html).
