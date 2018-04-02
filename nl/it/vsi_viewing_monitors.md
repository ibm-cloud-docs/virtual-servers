---



copyright:
  years: 2017
lastupdated: "2017-10-23"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Visualizzazione e gestione dei monitoraggi

Il monitoraggio di un dispositivo consente all'utente di avviare i ping lenti e del servizio per assicurarsi che il dispositivo sia online e reattivo.
{:shortdesc}

Se non viene ricevuto un echo nell'intervallo di tempo assegnato (1 secondo per i ping del servizio, 5 secondi per i ping lenti) viene inviato un avviso
all'indirizzo email nell'account. Un stato di **Attivo** nel campo **Stato** indica che è stato ricevuto un echo, mentre **Non attivo**
indica che non è stato ricevuto. Se hai già configurato un monitoraggio di base, puoi seguire le seguenti istruzioni per visualizzare e gestire il monitoraggio del dispositivo.

   <table>
   <CAPTION>Tabella 1. Visualizzare e gestire il monitoraggio del dispositivo</CAPTION>
   <THEAD>
   <TR>
   <th>Se l'azione da effettuare è...</th>
   <th>Allora...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Visualizza monitoraggi</td>
   <td>
   <ol>
   <li>Dall'elenco dei dispositivi, fai clic su <b>Nome dispositivo</b> per accedere al dispositivo.</li>
   <li>Fai clic sulla scheda <b>Monitoraggio</b>. Tutti i ping correnti sono visualizzati nella pagina di destinazione. (La scheda <b>Monitoraggio</b> è visibile solo se è stato configurato almeno un monitoraggio.)</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Aggiungi un monitoraggio</td>
   <td>
   <ol>
   <li>Dalla scheda <b>Monitoraggio</b> della pagina dei dettagli del dispositivo, fai clic su <b>Gestisci monitoraggi</b> nel lato destro della pagina per gestire i monitoraggi associati con questo dispositivo.</li>
   <li>Nella pagina dei monitoraggi, fai clic sulla scheda <b>Aggiungi monitoraggio</b>.</li>
   <li>Seleziona l'indirizzo IP da monitorare dall'elenco a discesa <b>Indirizzo IP</b>.</li>
   <li>Seleziona il tipo di monitoraggio dall'elenco a discesa <b>Tipo di monitoraggio</b>.</li>
   <li>Configura le opzioni di notifica. Dall'elenco a discesa <b>Notifica?</b>, seleziona <b>Utenti di notifica</b> per inviare una notifica agli utenti dei problemi o <b>Non fare nulla</b> per tralasciare la notifica utente.</li>
   <li>Seleziona l'intervallo di tempo per una notifica utente con l'utilizzo dell'elenco a discesa <b>Attesa notifica</b>.</li>
   <li>Fai clic sul pulsante <b>Aggiungi monitoraggio</b> per aggiungere il monitoraggio al dispositivo. Il nuovo monitoraggio viene visualizzato nella sezione <b>Modifica monitoraggi esistenti</b> della schermata.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Modifica un monitoraggio esistente</td>
   <td>
   <ol>
   <li>Nella pagina dei monitoraggi nell'intestazione <b>Modifica monitoraggi esistenti</b>, fai clic sui dettagli di un monitoraggio per aprirlo per la modifica.</li>
   <li>Aggiorna uno qualsiasi dei seguenti campi; Tipo di monitoraggio, Notifica, Attesa notifica.</li>
   <li>Fai clic sul pulsante <b>Aggiorna</b> per aggiornare i dettagli. Fai clic sul pulsante <b>Annulla</b> per annullare la modifica.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Rimuovi un monitoraggio</td>
   <td>
   <ol>
   <li>Nella pagina dei monitoraggi nell'intestazione <b>Modifica monitoraggi esistenti</b>, fai clic sull'icona Rimuovi accanto ai dettagli del monitoraggio.</li>
   <li>Fai clic sul pulsante <b>Sì</b> per rimuovere il monitoraggio. Fai clic sul pulsante <b>No</b> per annullare l'azione.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>
   
## Passi successivi
   
- Se è stato aggiunto un nuovo monitoraggio, verrà visualizzato nella scheda **Monitoraggio**. Il monitoraggio invierà un ping al dispositivo ogni cinque minuti, attendendo una risposta in base al tipo di ping selezionato. Se la risposta prevista non viene ricevuta, viene inviata un'email all'indirizzo email di notifica per l'account nell'intervallo di tempo specificato, se l'invio della notifica è stato selezionato.
- Se un monitoraggio è stato modificato, continuerà a funzionare come specificato nei dettagli del monitoraggio. Se viene modificato il tipo, la quantità di tempo per ricevere il ping sarà differente. Se le opzioni di notifica sono state modificate, il modo in cui gli utenti verranno avvisati dei tentativi non riusciti verrà modificato in base alle nuove selezioni. Il monitoraggio rimarrà accessibile dalla scheda **Monitoraggio**.
- Se un monitoraggio è stato rimosso, non funzionerà più per il dispositivo. Tutto il monitoraggio associato con il monitoraggio rimosso sarà interrotto e non verrà più visualizzato nella scheda **Monitoraggio**.
