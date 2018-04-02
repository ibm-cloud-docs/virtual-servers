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

# Provisioning di istanze e host dedicati
{: #ordering-vs-dedicated}

Hai due opzioni su come eseguire il provisioning delle tue istanze dedicate. La prima è attraverso il catalogo {{site.data.keyword.Bluemix}} e la seconda tramite il {{site.data.keyword.slportal_full}}. Il catalogo e il {{site.data.keyword.slportal}} richiedono ID di accesso univoci. I tuoi nome utente e password del catalogo non funzionano per accedere al portale e viceversa. Vedi [Registrazione a {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} per configurare le tue credenziali del catalogo {{site.data.keyword.Bluemix_notm}} o del {{site.data.keyword.slportal}}.
{:shortdesc}

## Accedi al catalogo IBM Cloud
Utilizza la seguente procedura per accedere al catalogo {{site.data.keyword.Bluemix_notm}} e iniziare il provisioning degli host dedicati e delle istanze host dedicate. 

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
Utilizza la seguente procedura per accedere al {{site.data.keyword.slportal}} e iniziare ad ordinare gli host dedicati e le istanze host dedicate.

1.	Apri una nuova finestra del browser e immetti [https://control.softlayer.com](https://control.softlayer.com){: new_window}. 
2.	Immetti i tuoi nome utente e password e fai clic su **Accedi** O su **Accedi con ID IBM**.
3.	Immetti la tua email o il tuo ID IBM e fai clic su **Continua**.
4.	Immetti la tua password e fai clic su **Accedi**.

Sarai reindirizzato alla pagina principale del {{site.data.keyword.slportal}}.

## Esegui il provisioning dell'host dedicato 
Utilizza le seguenti istruzioni per eseguire il provisioning dei tuoi host dedicati.

1.	Fai clic sull'icona **Dispositivi**.
2.  Fai clic sul link **Server virtuale dedicato orario** o **Server virtuale dedicato mensile**. 

   **Nota:** i server dedicati sono server privati.

Vieni reindirizzato alla pagina *Configura il tuo server cloud*. È da questa pagina che puoi ordinare un'istanza dedicata che è associata o meno a un host dedicato. Ulteriori informazioni sull'ordine delle istanze possono essere trovate in [Esegui provisioning delle tue istanze host dedicate](#provision-dedicated-instances).

4.	Fai clic sul pulsante **Crea host** nel lato destro del modulo.
5.	Immetti le seguenti informazioni:
    
    <table>
    <CAPTION>Tabella 1. Selezioni provisioning host dedicati</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valore</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantità</td>
    <td>Immetti il numero di host dedicati da ordinare. Tieni presente che possono venire distribuiti solo due host per ordine di provisioning.</td>
    </tr>
    <tr>
    <td>Ubicazione</td>
    <td>Seleziona il data center {{site.data.keyword.cloud}} in cui vuoi posizionare i tuoi host. Consulta le informazioni dall'elenco di data center disponibili.</td>
    </tr>
    <td>Host dedicato</td>
    <td>Il valore predefinito è 56 Core X 242 RAM X 1.2 TB</td>
    </tr>
    </TBODY>
    </table>
    
    Il tuo riepilogo dell'ordine viene visualizzato al lato destro della pagina *Configurazione*. 
    
6.  Fai clic sul pulsante **Aggiungi all'ordine**.
7.  Conferma le tue selezioni nella pagina *Checkout* e scorri fino a *Configurazione avanzata del sistema host dedicato*.
8.  Immetti le seguenti informazioni:

    <table>
    <CAPTION>Tabella 2. Configurazione avanzata del sistema dell'host dedicato</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valore</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Selezione POD</td>
    <td>Fai clic sulla casella a discesa e seleziona il POD in cui desideri posizionare l'host dedicato.</td>
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

9.  Fai clic sulla casella di spunta **Termini servizio cloud**.
10. Conferma o immetti le tue informazioni di pagamento e fai clic sul pulsante **Inoltra**. Sarai reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

    Viene inviata una serie di email al tuo amministratore di riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione e il completamento del provisioning. L'email di completamento del provisioning includerà un link che ti porterà direttamente alla pagina **Dettagli del dispositivo** dopo aver eseguito l'accesso a {{site.data.keyword.Bluemix_notm}}. Un'altra opzione potrebbe essere quella di accedere direttamente al {{site.data.keyword.slportal}}.

## Esegui il provisioning delle istanze host dedicate
{: #provision-dedicated-instances}
Puoi eseguire il provisioning delle tue istanze host dedicate in due modi tramite il menu **Dispositivi** o l'icona **Dispositivi**.

### Provisioning delle tue istanze host dedicate tramite il menu Dispositivi
{: #ordering-dedicated-devices-menu}

La tua prima opzione è quella di eseguire il provisioning delle tue istanze host dedicate tramite il menu **Dispositivi** dalla pagina principale del {{site.data.keyword.slportal}}. Le seguenti istruzioni ti guidano attraverso questo processo.

1.	Fai clic su **Dispositivi > Elenco dispositivi**. 
 
    La pagina *Dispositivi* visualizza tutti i tipi di dispositivi —host dedicati, server virtuali, server bare metal e controller di distribuzione dell'applicazione NetScaler— presenti nel tuo account. 

2.	Seleziona l'host per le tue istanze host dedicate facendo clic sul suo link in **Nome dispositivo**.
    
    Sei nella scheda **Configurazione** della pagina *Dettagli del dispositivo*. La scheda **Ticket** elenca i tuoi ticket di supporto attivi e la scheda **Assegnazioni** visualizza il tuo utilizzo di memoria per il tuo periodo di fatturazione selezionato. Consulta Utilizzo dei dettagli del dispositivo per gestire le istanze e gli host dedicati per ulteriori informazioni sulle schede.

3.	Scorri al frame **Istanze**.

    Come il tuo host dedicato viene fatturato (mensile o orario) determina la fatturazione delle tue istanze host dedicate. Tieni presente che se hai host fatturati mensilmente, puoi eseguire il provisioning di istanze host dedicate fatturate mensili e orarie. Sono presenti due link-**Aggiungi orario** e **Aggiungi mensile**—disponibili quando esegui il provisioning delle tue istanze. Gli host a fatturazione oraria possono soltanto eseguire il provisioning di istanze host dedicate a fatturazione oraria e verrà visualizzato solo il link **Aggiungi orario**. 

4.	Fai clic sul link **Aggiungi orario** se il tuo host ha fatturazione oraria o mensile; fai clic sul link **Aggiungi mensile** se il tuo host viene fatturato mensilmente. Vieni reindirizzato alla pagina *Configura il tuo server cloud*. 

5.	Immetti le seguenti informazioni:
       
    <table>
    <CAPTION>Tabella 3. Selezioni istanze host dedicate</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valore</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantità</td>
    <td>Il numero di istanze host dedicate da distribuire a un solo host.</td>
    </tr>
    <tr>
    <td>Posizionamento</td>
    <td>
    <ul>
    <li>Assegnazione automatica – {{site.data.keyword.Bluemix_notm}} assegna automaticamente la tua istanza a un host rispetto a quello che hai specificato. La tua istanza sarà posizionata in un data center che dispone di capacità. Se assegni automaticamente la tua istanza, non potrai utilizzare alcuna capacità del tuo host dedicato.</li>
    <li>Specificare host - Il tuo host dedicato associato al tuo account verrà visualizzato in Host dedicato. </li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Host dedicato</td>
    <td>Seleziona l'host dedicato dall'elenco in cui si deve eseguire il provisioning delle istanze.</td>
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
    <td>Puoi eseguire il provisioning fino a quattro dischi di avvio aggiuntivi-SAN o locale-per istanza host dedicata.</td>
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

6.	Fai clic sul pulsante **Aggiungi all'ordine**.
7.  Immetti le seguenti informazioni nella pagina *Checkout* in *Configurazione avanzata del sistema*:

<table>
    <CAPTION>Tabella 4. Configurazione avanzata del sistema dell'istanza host dedicata</CAPTION>
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

8.  Fai clic sulle caselle di spunta **Termini servizio cloud** e **Accordo servizi di terze parti**.
9. Conferma o immetti le tue informazioni di pagamento e fai clic sul pulsante **Inoltra**. Sarai reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.


Riceverai un'email dopo il provisioning delle tue istanze host dedicate.

### Esegui il provisioning delle tue istanze host dedicate tramite l'icona Dispositivi
La seconda opzione per eseguire il provisioning delle istanze host dedicate è quella di utilizzare l'icona **Dispositivo** nella home page del {{site.data.keyword.slportal}}. Le seguenti istruzioni ti guidano attraverso questo processo.

1.	Fai clic sull'icona **Dispositivi** e seleziona **Orario** o **Mensile** in Server virtuali dedicati.
2.	Segui la procedura indicata in [Provisioning delle tue istanze host dedicate tramite il menu Dispositivi](#ordering-dedicated-devices-menu), partendo dal passo 5.

### Passi successivi
Dopo che è stato eseguito il provisioning del tuo server virtuale, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione dei server virtuali](../vsi/vsi_managing.html).


