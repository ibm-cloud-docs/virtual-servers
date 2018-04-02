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

#  Ricaricamento del SO
Puoi ricaricare il sistema operativo (SO) su un dispositivo in qualsiasi momento per ripristinarlo al suo ordine di lavoro originale o per riconfiguralo con un software differente. Un ricaricamento SO rimuove tutti i dati dal dispositivo e applica una configurazione "come nuova", come specificato durante il processo di configurazione dell'impostazione del ricaricamento del SO. Poiché i ricaricamenti SO eliminano tutti i dati dal dispositivo, se non ne è stato eseguito il backup prima del ricaricamento, vengono eliminati definitivamente e non possono venire ripristinati.
{:shortdesc}

**Importante:** se desideri conservare i tuoi dati, eseguine il backup prima di eseguire un ricaricamento.

## Esecuzione di un ricaricamento
1. Da **Elenco dispositivi**, fai clic sul server che necessita di un ricaricamento SO.
2. Dal menu **Azioni** nella parte in alto a sinistra della pagina, seleziona **Ricaricamento SO**.
3. Decidi se vuoi ricaricare la configurazione esistente o ricaricare il dispositivo con una nuova configurazione.

   <table>
   <CAPTION>Tabella 1. Opzioni di ricaricamento SO</CAPTION>
   <THEAD>
   <TR>
   <th>Tipo di ricaricamento</th>
   <th>Passi</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Se desideri ricaricare utilizzando una nuova configurazione...</td>
   <td>
   <ol>
   <li>Fai clic su <b>Modifica</b> per la categoria che richiede un aggiornamento.</li>
   <li>Seleziona il nuovo software da applicare al dispositivo dall'elenco a discesa <i>Seleziona software</i>.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Se desideri ricaricare utilizzando una configurazione esistente...</td>
   <td>Procedi con l'operazione successiva.</td>
   </tr>
   </TBODY>
   </table>

4. Decidi se uno script di post installazione deve venire applicato dopo il provisioning del dispositivo.

   Se desideri applicare uno script di post installazione, selezionalo dall'elenco a discesa Script esistenti o immetti un URL qualificato per il nuovo script.  Altrimenti, procedi al passo successivo.

5. Per i dispositivi fisici, decidi se le partizioni installate devono venire aggiunte, rimossa o non essere modificate.
   
   <table>
   <CAPTION>Tabella 2. Opzioni azione di partizione</CAPTION>
   <THEAD>
   <TR>
   <th>Azione di partizione</th>
   <th>Passi</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Per aggiungere le partizioni installate...</td>
   <td>
   <ul>
   <li>Fai clic sul link <b>Aggiungi un'altra partizione</b>.</li>
   <li>Immetti il nome esatto della partizione.</li>
   <li>Immetti la dimensione della partizione (in GB). Se vuoi, puoi selezionare Cresci per far crescere la partizione per riempire lo spazio disco rimanente.
   <p><b>Nota:</b> può essere selezionata solo una partizione per la crescita alla volta. Questa partizione è più grande della dimensione specificata e riempie tutta la capacità disponibile. La capacità della partizione Cresci viene calcolata sottraendo la dimensione combinata di tutte le partizioni dal numero di capacità totale di cui è stato eseguito il provisioning nella sezione delle partizioni installate.</p>
   </li>
   </ul>
   </td>
   </tr>
   <tr>
   <td>Per eliminare le partizioni installate...</td>
   <td>Fai clic sull'icona <b>Elimina</b> per eliminare la partizione.</td>
   </tr>
   <tr>
   <td>Per non modificare...</td>
   <td>Procedi con l'operazione successiva.</td>
   </tr>
   </TBODY>
   </table>
    
6. Decidi se applicare una o più chiavi SSH al dispositivo.

7. Seleziona le caselle di spunta applicabili per le opzioni desiderate che vuoi vengano applicate al dispositivo durante o dopo un ricaricamento SO.

   **Nota:** le opzioni variano in base al dispositivo. Non tutte le opzioni sono disponibili per ogni dispositivo.

8. Fai clic sul pulsante **Ricarica la precedente configurazione** per continuare con la finestra a comparsa Riesamina. Fai clic sul pulsante **Annulla** per annullare le modifiche al dispositivo e uscire dalla schermata.

9. Verifica che tutti i dettagli nella sezione Nuova configurazione siano corretti.  

10. Fai clic sul pulsante **Conferma ricaricamento SO** per confermare e avviare il ricaricamento SO. Fai clic sul pulsante **Annulla** per annullare l'azione.

## Operazioni successive
Dopo aver avviato il processo di ricaricamento SO, il dispositivo viene portato offline e viene avviato il processo di ricaricamento SO.
Il periodo di durata del ricaricamento SO varia in base alla configurazione nuova o corrente del dispositivo.
Durante il processo di configurazione, il tempo minimo del ricaricamento SO viene visualizzato in ogni schermata.
L'intervallo di tempo visualizzato è una stima effettuata dal sistema e viene fornita per cortesia. Se il ricaricamento impiega più di 24 ore,
contatta il nostro team di supporto. Quando il dispositivo ritorna online, funziona come specificato nella nuova configurazione del ricaricamento SO. Tutti i dati precedentemente salvati nel dispositivo vanno persi, ma puoi ripristinarli se hai effettuato un backup del dispositivo prima del ricaricamento.
Se non è stato eseguito il backup dei dati, non possono venire ripristinati.
 
Per registrare nuovamente il tuo dispositivo con eVault, consulta [Re-registering your device with eVault ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
