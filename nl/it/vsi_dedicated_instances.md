---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Provisioning delle istanze dedicate

Hai due opzioni su come eseguire il provisioning delle tue istanze dedicate. La prima è attraverso il catalogo {{site.data.keyword.Bluemix}} e la seconda tramite il {{site.data.keyword.slportal_full}}. Il catalogo e il {{site.data.keyword.slportal}} richiedono ID di accesso univoci. I tuoi nome utente e password del catalogo non funzionano per accedere al portale e viceversa. Vedi [Registrazione a {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} per configurare le tue credenziali del catalogo {{site.data.keyword.Bluemix_notm}} o del {{site.data.keyword.slportal}}.
{:shortdesc}

## Accedi al catalogo IBM Cloud
Utilizza la seguente procedura per accedere al {{site.data.keyword.Bluemix_notm}} ed iniziare il provisioning delle tue istanze dedicate. 

1. Apri una nuova finestra del browser e immetti [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/){: new_window}.
2.	Fai clic sul link **Accedi** (angolo in alto a destra). 
3.	Immetti la tua email o il tuo ID IBM e fai clic su **Continua**.
4.	Immetti la tua password e fai clic su **Accedi**.
5.	Seleziona **Infrastruttura > Calcola**.
6.  Fai clic sul tile **Server virtuali**.
7.	Seleziona l'opzione **Server virtuali dedicati**.
8.  Fai clic su **Crea**. 

Sarai reindirizzato alla pagina principale del {{site.data.keyword.slportal}}.

## Accedi al portale clienti
Utilizza la seguente procedura per accedere al {{site.data.keyword.slportal}} e iniziare a ordinare le tue istanze dedicate.

1.	Apri una nuova finestra del browser e immetti [https://control.softlayer.com](https://control.softlayer.com){: new_window}. 
2.	Immetti i tuoi nome utente e password e fai clic su **Accedi** O su **Accedi con ID IBM**.
3.	Immetti la tua email o il tuo ID IBM e fai clic su **Continua**.
4.	Immetti la tua password e fai clic su **Accedi**.

Sarai reindirizzato alla pagina principale del {{site.data.keyword.slportal}}.

## Esegui il provisioning delle tue istanze dedicate
{: #provision-dedicated-instances}
Puoi eseguire il provisioning delle tue istanze dedicate in due modi tramite l'icona **Dispositivi** o il menu **Dispositivi**.

### Esegui il provisioning delle tue istanze host dedicate tramite l'icona Dispositivi
{: #ordering-dedicated-devices-menu}
La prima opzione per eseguire il provisioning delle istanze host dedicate è quella di utilizzare l'icona **Dispositivo** nella home page del {{site.data.keyword.slportal}}. Le seguenti istruzioni ti guidano attraverso questo processo.

1.	Fai clic sull'icona **Dispositivi**. Viene visualizzata la finestra **Ordina servizi e prodotti SoftLayer**. 
2.  Seleziona **Orario** o **Mensile** in Server virtuali dedicati. Vieni reindirizzato alla pagina *Configura il tuo server cloud*. 

3.	Immetti le seguenti informazioni:
       
    <table>
    <CAPTION>Tabella 1. Selezioni di istanze host dedicate</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valore</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantità</td>
    <td>Il numero di istanze dedicate da distribuire.</td>
    </tr>
    <tr>
    <td>Posizionamento</td>
    <td>
    <ul>
    <li>Assegnazione automatica – {{site.data.keyword.Bluemix_notm}} assegna automaticamente la tua istanza a un host nel data center che hai selezionato.</li>
    <li>Specifica host – Utilizzato con le istanze host dedicate. Consulta [Server virtuali dedicati](../vsi/vsi_dedicated.html) per ulteriori informazioni sugli host dedicati e sulle istanze host dedicate.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Data Center</td>
    <td>Seleziona il data center in cui si deve eseguire il provisioning delle istanze.</td>
    </tr>
    <tr>
    <td>Calcolo dell'istanza</td>
    <td> Seleziona la memoria e la CPU per ogni istanza in un ordine di provisioning.</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> Seleziona la RAM per ogni istanza in un ordine di provisioning.</td>
    </tr>
    <tr>
    <td>Sistema Operativo</td>
    <td>Seleziona il sistema operativo per l'istanza. Tieni presente che viene emesso un messaggio di errore se è presente un conflitto tra il server e il sistema operativo. Ad esempio, selezionando Linux su un server Microsoft SQL.</td>
    </tr>
    <tr>
    <td>Primo disco</td>
    <td>Selezionare SAN o locale per ogni istanza in un ordine.</td>
    </tr>
    <tr>
    <td>Dischi aggiuntivi</td>
    <td>Puoi eseguire il provisioning fino a quattro dischi di avvio aggiuntivi-SAN o locale-per istanza dedicata.</td>
    </tr>
    <td>Opzioni di rete</td>
    <td> Seleziona le opzioni appropriate o utilizza i valori predefiniti.</td>
    </tr>
    <tr>
    <td>Componenti aggiuntivi</td>
    <td> Seleziona le opzioni appropriate o utilizza i valori predefiniti.</td>
    </tr>
    <tr>
    </TBODY>
    </table> 

4.	Fai clic sul pulsante **Aggiungi all'ordine**. Sarai reindirizzato alla pagina di checkout.
5.  Immetti le seguenti informazioni nella pagina *Checkout* in *Configurazione avanzata del sistema*:

<table>
    <CAPTION>Tabella 2. Configurazione avanzata del sistema dell'istanza dedicata</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valore</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Selezione VLAN</td>
    <td>Aggiungi il nuovo server a una VLAN nel tuo account se hai già ordinato almeno un server.</td>
    </tr>
    <tr>
    <td>Script di provisioning</td>
    <td>Fornisci uno script che ti consente di automatizzare alcune fasi dopo il provisioning.</td>
    </tr>
    <tr>
    <td>Chiavi SSH</td>
    <td>Fornisci una chiave pubblica o la tua chiave SSH, che ti consentirà di accedere al tuo server dopo averne effettuato il provisioning.</td>
    </tr>
    <tr>
    <td>Metadati utenti</td>
    <td>Metadati facoltativi per gli script di provisioning personalizzati.</td>
    </tr>
    <tr>
    <td>Nome host</td>
    <td>Immetti un nome permanente o temporaneo per il tuo server, ad esempio, server1.</td>
    </tr>
    <tr>
    <td>Dominio</td>
    <td>Immetti un dominio secondario che non sia in conflitto con un nome dominio internet, ad esempio, test.acme.com.</td>
    </tr>
    </TBODY>
    </table>

6.  Fai clic sulle caselle di spunta **Termini servizio cloud** e **Accordo servizi di terze parti**.
7. Conferma o immetti le tue informazioni di pagamento e fai clic sul pulsante **Inoltra ordine**. Sarai reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

    Viene inviata una serie di email al tuo amministratore di riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione e il completamento del provisioning. L'email di completamento del provisioning includerà un link che ti porterà direttamente alla pagina **Dettagli del dispositivo** dopo aver eseguito l'accesso a {{site.data.keyword.Bluemix_notm}}. Un'altra opzione potrebbe essere quella di accedere direttamente al {{site.data.keyword.slportal}}.

### Provisioning delle tue istanze dedicate tramite il menu Dispositivi

La tua seconda opzione è quella di eseguire il provisioning delle tue istanze dedicate tramite il menu **Dispositivi** dalla pagina principale del {{site.data.keyword.slportal}}. Le seguenti istruzioni ti guidano attraverso questo processo.

1.	Fai clic su **Dispositivi > Elenco dispositivi**. 
 
    La pagina *Dispositivi* visualizza tutti i tipi di dispositivi —server virtuali, server bare metal, host dedicati e controller di distribuzione dell'applicazione NetScaler— presenti nel tuo account. 

2.	Fai clic sul link **Ordine di dispositivi** nel lato destro della pagina.
    Viene visualizzata la finestra **Ordina servizi e prodotti SoftLayer**.
3.	Segui le istruzioni nel menu [Provisioning delle tue istanze dedicate tramite il menu Dispositivi](#ordering-dedicated-devices-menu), partendo dal passo 2.

### Passi successivi
Dopo che è stato eseguito il provisioning del tuo server virtuale, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione dei server virtuali](../vsi/vsi_managing.html).
