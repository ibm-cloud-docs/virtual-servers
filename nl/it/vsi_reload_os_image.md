---



copyright:
  years: 2017
lastupdated: "2017-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Ricaricamento SO utilizzando un template dell'immagine
Simile al ricaricamento standard, ricaricare un dispositivo da un template dell'immagine permette all'utente di ripristinare o riconfigurare un dispositivo basato su un modello dell'immagine pre-esistente associato all'account del portale clienti in uso. Durante il processo di ricaricamento SO standard, le opzioni di configurazione per il dispositivo possono essere selezionate individualmente, mentre la funzione di caricamento dall'immagine carica la configurazione esattamente come viene visualizzata nel template dell'immagine. Puoi ancora aggiungere funzioni facoltative per eseguire il ricaricamento.
Utilizza le seguenti istruzioni per eseguire un ricaricamento SO da un template dell'immagine utilizzando la funzione di caricamento dall'immagine nel portale clienti.
{:shortdesc}

## Esecuzione del ricaricamento utilizzando un template dell'immagine
1. Esegui il backup di tutti i dati nel dispositivo.
  
   **Nota:** il ricaricamento SO elimina tutti i dati dal disco rigido. Se non viene eseguito il backup dei dati prima di avviare il ricaricamento SO, non possono venire ripristinati. Bluemix (Softlayer) non esegue il backup di tutti i dati archiviati nei dispositivi dei clienti e non è responsabile per i dati persi associati al processo di ricaricamento SO.
  
2. Dalla pagina dell'elenco dei dispositivi, seleziona **Carica dall'immagine** dal menu **Azioni** del dispositivo desiderato.

3. Seleziona la casella di spunta del template dell'immagine desiderata per selezionare il template dell'immagine che sarà ricaricato nel dispositivo.

   **Nota:** prima di completare il ricaricamento, il template dell'immagine viene copiato nel data center che contiene il dispositivo, se non è già ubicato nello stesso data center. Se il template dell'immagine deve essere copiato nel data center appropriato, potrebbe venire addebitato un ulteriore costo se il template non viene eliminato dall'ubicazione dopo il completamento del ricaricamento SO.
  
4. Decidi se vuoi aggiungere una qualsiasi funzione facoltativa. Tutte le funzioni facoltative che selezioni vengono aggiunte al dispositivo come parte del processo di ricaricamento.
   
   <table>
   <CAPTION>Tabella 1. Funzioni facoltative</CAPTION>
   <THEAD>
   <TR>
   <th>Funzioni facoltative</th>
   <th>Passi</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   </tr>
   <tr>
   <td>Sì, voglio aggiungere funzioni facoltative.</td>
   <td>
   <ol>
   <li>Fai clic su <b>Carica immagine selezionata</b>.</li>
   <li>Controlla la configurazione dell'immagine e procedi o annulla.</li>
   <li>Fai clic su <b>Conferma ricaricamento SO</b> per confermare l'azione e avviare il processo di ricaricamento SO.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>No, non voglio aggiungere funzioni facoltative.</td>
   <td>Fai clic su <b>Visualizza funzioni facoltative</b>.</td>
   </tr>
   </TBODY>
   </table>

5. Configura le opzioni aggiuntive, come rilevanti. Fai riferimento alla seguenti informazioni per ulteriori dettagli.
   
   <dl>
   <dt>Script di post installazione</dt>
   <dd>Aggiunge uno script di post installazione nuovo o esistente.</dd>
   <dt>Chiave SSH</dt>
   <dd>Aggiunge una chiave SSH al dispositivo al momento dell'azione di ricaricamento. </dd>
   <dt>Reimpostazione password IPMI</dt>
   <dd> Questa opzione è disponibile solo per i dispositivi fisici. </dd>
   <dt>Applicare gli aggiornamenti BIOS della scheda madre</dt>
   <dd>Questa opzione è disponibile solo per i dispositivi fisici. </dd>
   <dt>Applicare gli aggiornamenti al firmware per tutti i dischi rigidi</dt>
   <dd>Questa opzione è disponibile solo per i dispositivi fisici.</dd>
   <dt>Aggiungere il pool di riserva dopo il ricaricamento SO</dt>
   <dd>Questa opzione è disponibile solo per i dispositivi fisici e richiede l'approvazione interna prima di essere disponibile su un account.</dd>
   <dt>Cancellare tutti i dischi rigidi</dt>
   <dd> Questa opzione è disponibile solo per i dispositivi fisici e richiede autorizzazioni utente speciali configurate dall'amministratore dell'account.</dd>
   <dt>Ricaricamento SO con protezione del disco</dt>
   <dd>Conserva tutti i dati sul disco primario corrente durante il processo di ricaricamento SO. La protezione del disco primario nell'unità primaria lo converte in un dispositivo di archiviazione portatile. Questa opzione è disponibile solo nei dispositivi virtuali e verranno addebitati ulteriori costi nei modelli di fatturazione (orario o mensile) del dispositivo. Gli addebiti possono venire impediti annullando il dispositivo di archiviazione portatile ogni volta dopo la sua creazione.</dd>
   </dl>

6. Fai clic su **Carica immagine selezionata**.

7. Controlla la configurazione dell'immagine e fai clic su **Avanti** per procedere alla schermata successiva o su **Annulla** per annullare l'azione.

   **Nota:** dopo aver fatto clic su **Avanti**, tutte le porte di rete del dispositivo vengono sistematicamente arrestate e il dispositivo non è disponibile per un massimo di 15 minuti. Durante questo tempo, l'azione può venire annullata in qualsiasi momento facendo clic su **Annulla**. Il passo successivo deve essere completato entro 15 minuti facendo clic su **Avanti** o il passo precedente deve venire completato nuovamente. Questo processo è una misura di sicurezza per garantire che nessun ulteriore dato venga aggiunto al dispositivo tra la conferma della configurazione e l'avvio del ricaricamento SO.

8. Fai clic su **Conferma ricaricamento SO** per confermare l'azione e avviare il processo di ricaricamento SO. Fai clic su **Annulla** per annullare l'azione.

## Operazioni successive
Dopo aver avviato il processo di ricaricamento SO, il dispositivo viene portato offline e viene avviato il processo di ricaricamento SO.
Il periodo di durata del ricaricamento SO varia in base alla configurazione nuova o corrente del dispositivo.
Se il ricaricamento impiega più di 24 ore,
contatta il nostro team di supporto. Quando il dispositivo ritorna online, funziona come specificato nella nuova configurazione del ricaricamento SO. Tutti i dati precedentemente salvati nel dispositivo vanno persi, ma puoi ripristinarli se hai effettuato un backup del dispositivo prima del ricaricamento. Se non è stato eseguito il backup dei dati, non possono venire ripristinati.

 Per registrare nuovamente il tuo dispositivo con eValut, consulta [Re-registering your device with eVault ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
