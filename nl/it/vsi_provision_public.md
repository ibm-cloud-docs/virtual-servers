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

# Provisioning di istanze pubbliche
{: #ordering-vs-public}

## Informazioni preliminari
Hai due opzioni per eseguire il provisioning delle tue istanze del server virtuale pubbliche. La prima è attraverso il catalogo {{site.data.keyword.Bluemix}} e la seconda tramite il {{site.data.keyword.slportal_full}}. Il catalogo e il {{site.data.keyword.slportal}} richiedono ID di accesso univoci. I tuoi nome utente e password del catalogo non funzionano per accedere al portale e viceversa.
{:shortdesc}

Prima di iniziare, controlla i seguenti prerequisiti.

  1. Assicurati di aver impostato le credenziali del catalogo {{site.data.keyword.Bluemix_notm}} o del {{site.data.keyword.slportal}}. 
  
     **Nota:** per il catalogo {{site.data.keyword.Bluemix_notm}}, devi disporre di un account aggiornato per ordinare i server virtuali. Per ulteriori informazioni sull'aggiornamento del tuo account, consulta [Passaggio all'ID IBM](https://console.bluemix.net/docs/admin/softlayerlink.html).
  
  2. Se non lo hai fatto, rivedi le opzioni di distribuzioni che sono disponibili. Per ulteriori informazioni, consulta [Opzioni di distribuzione: server virtuale pubblico](../vsi/vsi_public.html).

## Accesso 
Assicurati di aver eseguito l'accesso, attraverso il catalogo {{site.data.keyword.Bluemix_notm}} o il {{site.data.keyword.slportal}}: 

  <table>
   <CAPTION>Tabella 1. Scegli un'ubicazione di accesso</CAPTION>
   <THEAD>
   <TR>
   <th>Se desideri accedere con...</th>
   <th>Allora...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Catalogo IBM Cloud</td>
   <td>
   <ol>
   <li>Apri una nuova finestra del browser e immetti <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Fai clic sul link <b>Accedi</b> (angolo in basso a destra). </li>
   <li>Immetti la tua email o il tuo ID IBM e fai clic su <b>Continua.</b></li>
   <li>Immetti la tua password e fai clic su <b>Accedi.</b></li>
   <li>Seleziona <b>Infrastruttura</b> > <b>Calcola</b>.</li>
   <li>Fai clic sul tile <b>Server virtuali</b>.</li>
   <li>Seleziona l'opzione <b>Server virtuali pubblici</b>.</li>
   <li>Fai clic su <b>Crea</b>. Viene aperta la pagina principale del {{site.data.keyword.slportal}}.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Portale clienti</td>
   <td>
   <ol>
   <li>Apri una nuova finestra del browser e immetti <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Immetti i tuoi nome utente e password e fai clic su <b>Accedi</b>. O fai clic su <b>Accedi con ID IBM</b>. Quindi, immetti la tua email o il tuo ID IBM e fai clic su <b>Continua</b>. Immetti la tua password e fai clic su <b>Accedi</b>. Viene aperta la pagina principale del {{site.data.keyword.slportal}}.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Provisioning di un'istanza del server virtuale pubblica
{: #ordering-public-instance}
Dopo aver completato i prerequisiti, puoi iniziare a eseguire il provisioning di un'istanza del server virtuale pubblica. Puoi eseguire il provisioning delle tue istanze pubbliche in due modi -- tramite il menu **Dispositivi** o l'icona **Dispositivi**.

### Provisioning di un'istanza del server virtuale pubblica tramite l'icona Dispositivi
Per eseguire il provisioning della tua istanza del server virtuale pubblica tramite l'icona *Dispositivi*, completa le seguenti istruzioni:

1.  Dal {{site.data.keyword.slportal}}, individua la sezione **Ordine** e fai clic su **Dispositivi**.
2.  Nella pagina Dispositivi, fai clic su **Oraria** o **Mensile** per una delle offerte del Virtual Server.
3.  Nella pagina *Configura il tuo server cloud*, compila tutte le informazioni importanti.
4.  Fai clic sul pulsante **Aggiungi all'ordine** per continuare.
5.  Conferma o modifica le informazioni sul dominio per il server.
5.  Fai clic sulle caselle di spunta **Termini servizio cloud** e sulla casella di spunta **Accordo servizi di terze parti**.
6.  Conferma o immetti le tue informazioni di pagamento e fai clic sul pulsante **Inoltra ordine**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

 Viene inviata una serie di email al tuo amministratore di riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione e il completamento del provisioning. L'email di completamento del provisioning include un link alla pagina *Dettagli del dispositivo*, dopo aver eseguito l'accesso a {{site.data.keyword.Bluemix_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.

### Provisioning di un'istanza del server virtuale pubblica tramite il menu Dispositivi
{: #ordering-public-devices-menu}

Puoi inoltre eseguire il provisioning delle tue istanze del server virtuale pubbliche tramite il menu *Dispositivi* nella pagina principale del {{site.data.keyword.slportal}}. 

1. Fai clic su **Dispositivi > Elenco dispositivi**.

   La pagina Dispositivi visualizza tutti i tipi di dispositivo-server virtuale, i server bare metal, gli host dedicati e i controller di distribuzione dell'applicazione NetScaler nel tuo account.
2. Fai clic sul link **Ordine dispositivi** nell'angolo in alto a destra.
3. Nella pagina Dispositivi, fai clic su **Oraria** o **Mensile** per una delle offerte del Virtual Server.
4. Nella pagina *Configura il tuo server cloud*, compila tutte le informazioni importanti.
5. Fai clic sul pulsante **Aggiungi all'ordine** per continuare.
6. Conferma o modifica le informazioni sul dominio per il server.
7. Fai clic sulle caselle di spunta **Termini servizio cloud** e sulla casella di spunta **Accordo servizi di terze parti**.
8. Conferma o immetti le tue informazioni di pagamento e fai clic sul pulsante **Inoltra ordine**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

Viene inviata una serie di email al tuo amministratore di riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione e il completamento del provisioning. L'email di completamento del provisioning include un link alla pagina *Dettagli del dispositivo*, dopo aver eseguito l'accesso a {{site.data.keyword.Bluemix_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.

### Passi successivi
Dopo che è stato eseguito il provisioning del tuo server virtuale, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione del tuo server virtuale](../vsi/vsi_managing.html).
