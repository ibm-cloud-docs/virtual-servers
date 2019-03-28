---

copyright:
  years: 2014, 2017
lastupdated: "2017-12-12"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Upgrade della velocità della porta in Windows
{: #upgrading-port-speed-in-windows}

La velocità della porta predefinita per i server del cliente (sia per le reti private che pubbliche) è 10 Mbps. Se vuoi aggiornare una delle tue velocità della porta a 100 Mbps o 1000 Mbps, apri un ticket con la richiesta. Il dipartimento delle vendite ti chiede di approvare l'addebito minimo e un tecnico modifica le velocità della porta sulla rete.

Dopo aver completato l'upgrade nel lato della rete, imposta come hardcoded le interfacce di rete appropriate nel tuo server.

Segui queste istruzioni per forzare la velocità della porta in un sistema Windows. **Nota:** collegati sempre al tuo server sulla rete che NON stai utilizzando per evitare di bloccarti all'esterno del server.

1. Seleziona **Avvia > Seleziona pannello di controllo > Seleziona connessioni di rete**.
2. Fai clic sulla connessione di rete per cui stai tentando l'upgrade/downgrade.
  * Per gli upgrade della porta pubblica seleziona **Connessione area locale 2** OR **FrontEnd**.
  * Per gli upgrade della porta privata seleziona **Connessione area locale** OR **BackEnd**.
3. Dalla finestra dello stato della connessione, verifica che la scheda di rete che hai selezionato sia la porta che vuoi aggiornare.
4. Seleziona la scheda di supporto (prendi nota dell'indirizzo IP):
  * Per un upgrade della porta pubblica l'IP dovrebbe essere un indirizzo IP pubblico.
  * Per un upgrade della porta privata l'IP dovrebbe essere un indirizzo 10.x.x.x.
5. Se gli indirizzi IP non corrispondono, ripeti i passi da 1 a 3 per l'altra configurazione di rete.

## Stato LAN

Seleziona nuovamente la **Scheda generale** e poi seleziona **Proprietà.** Viene visualizzata una nuova finestra.

Dalla scheda **Generale** della finestra **Proprietà della connessione**, seleziona **Configura**. Viene visualizzata la finestra delle proprietà del driver.

1. Selezionare la scheda **Avanzate**.
2. Seleziona **Velocità di collegamento e duplex** dall'elenco delle proprietà.
3. Seleziona la scheda **Valore** a destra e imposta la velocità della porta che stai aggiornando con il duplex completo:
  1. Per 10 MBS seleziona: 10Mbps/Full
  2. Per 100 MBS seleziona: 100Mbps/Full
  3. Per 1000 MBS seleziona: Auto
4. Fai clic su OK.  

Questo comporta che il server inizia immediatamente ad utilizzare la nuova velocità, per cui potresti venire brevemente scollegato mentre viene rinegoziato il link.
