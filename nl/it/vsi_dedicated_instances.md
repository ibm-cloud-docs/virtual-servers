---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Provisioning delle istanze dedicate
{: #provisioning-dedicated-instances}

Hai due opzioni su come eseguire il provisioning delle tue istanze dedicate. La prima è attraverso il catalogo {{site.data.keyword.Bluemix}} e la seconda tramite il {{site.data.keyword.slportal_full}}. Il catalogo e il {{site.data.keyword.slportal}} richiedono ID di accesso univoci. I tuoi nome utente e password del catalogo non funzionano per accedere al portale e viceversa. Vedi [Registrazione a {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-signup#signup) per configurare le tue credenziali del catalogo {{site.data.keyword.Bluemix_notm}} o del {{site.data.keyword.slportal}}.
{:shortdesc}

## Provisioning di istanze del server virtuale dedicate
{: #provision-dedicated-instances}
Puoi eseguire il provisioning della tua istanza del server virtuale dedicata tramite il catalogo {{site.data.keyword.cloud_notm}} o il {{site.data.keyword.slportal}}.

### Provisioning di un'istanza del server virtuale dedicata tramite il catalogo IBM Cloud
Per eseguire il provisioning di un'istanza del server virtuale dedicata tramite il catalogo {{site.data.keyword.cloud_notm}}, completa la seguente procedura:

  1. Accedi al catalogo [{{site.data.keyword.cloud_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/catalog/){: new_window} utilizzando le tue credenziali univoche.
  2. Nella sezione **Infrastruttura di calcolo**, fai clic sul tile **Server virtuali**.
  3. Seleziona l'opzione **Virtual Server dedicato**.
  4. Fai clic su **Crea**.
  5. Nella sezione **Host dedicato**, seleziona **Assegnazione automatica**. {{site.data.keyword.cloud_notm}} assegna quindi automaticamente la tua istanza a un host nel tuo data center selezionato.

     **Nota**: per gli host dedicati, seleziona **Specifica host** oppure **Crea host**. Per ulteriori informazioni sugli host dedicati e le istanze host dedicato, vedi [Server virtuali dedicati](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers).

  5. Completa tutte le informazioni pertinenti per la tua istanza del server virtuale dedicata.
  6. Dopo aver riesaminato il riepilogo dell'ordine, fai clic sulla casella di spunta **Accordi di servizio di terze parti**.
  7. Fai clic su **Provisioning**.

### Provisioning di un'istanza del server virtuale dedicata tramite il portale del cliente
Per eseguire il provisioning di un'istanza del server virtuale dedicata tramite il {{site.data.keyword.slportal}}, completa la seguente procedura:

1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.
2. Individua la sezione **Order** e fai clic su **Devices**. Viene visualizzata la finestra **Order SoftLayer Product and Services**.
3.  Seleziona **Hourly** o **Monthly** in Dedicated Virtual Servers. Vieni reindirizzato alla pagina *Configure your Cloud Server*.

4.	Immetti le seguenti informazioni:

    <table>
    <CAPTION>Tabella 1. Selezioni di istanze host dedicato</CAPTION>
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
    <li>Specifica host – Utilizzato con le istanze host dedicato. Vedi [Server virtuali dedicati](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers) per ulteriori informazioni sugli host dedicati e sulle istanze host dedicato.</li>
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
    <td>Sistema operativo</td>
    <td>Seleziona il sistema operativo per l'istanza. Tieni presente che viene emesso un messaggio di errore se è presente un conflitto tra il server e il sistema operativo. Ad esempio, selezionando Linux su un server Microsoft SQL.</td>
    </tr>
    <tr>
    <td>Primo disco</td>
    <td>Selezionare SAN o locale per ogni istanza in un ordine.</td>
    </tr>
    <tr>
    <td>Dischi aggiuntivi</td>
    <td>Puoi eseguire il provisioning di un massimo di quattro dischi di avvio aggiuntivi-SAN o locale-per istanza dedicata.</td>
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

5.	Fai clic sul pulsante **Aggiungi all'ordine**. Sarai reindirizzato alla pagina di checkout.
6.  Immetti le seguenti informazioni nella pagina *Checkout* in *Configurazione avanzata del sistema*:

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

7.  Fai clic sulle caselle di spunta **Cloud Service terms** e **Third-Party Services Agreement**.
8. Conferma o immetti le tue informazioni di pagamento e fai clic sul pulsante **Submit Order**. Sarai reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

    Viene inviata una serie di email al tuo amministratore di riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione e il completamento del provisioning. L'email di completamento del provisioning includerà un link che ti porterà direttamente alla pagina **Dettagli del dispositivo** dopo aver eseguito l'accesso a {{site.data.keyword.Bluemix_notm}}. Un'altra opzione potrebbe essere quella di accedere direttamente al {{site.data.keyword.slportal}}.

## Passi successivi
Dopo aver eseguito il provisioning del tuo server virtuale ed è possibile utilizzarlo, puoi configurare i tuoi server virtuali utilizzando il
{{site.data.keyword.slportal_full}} o l'{{site.data.keyword.slapi_full}}. Per ulteriori informazioni, vedi [Configurazione di server virtuali](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
