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


# Riconfigurazione di un server virtuale esistente
{: #reconfiguring-virtual-servers}

Dopo aver eseguito il provisioning del tuo server virtuale, puoi eseguire l'upgrade o il downgrade della sua configurazione in qualsiasi momento.  

**Nota importante:** esistono molti server virtuali pubblici disponibili nelle caratteristiche preconfigurate. Per un tempo limitato, puoi modificare tutti i server virtuali disponibili prima delle caratteristiche preconfigurate. Dopodiché, ti verrà richiesto di migrare o annullare le istanze esistenti e riordinarle. 

Non puoi modificare dimensione disco, RAM e core individuali di un server virtuale che utilizza le caratteristiche. Devi prendere una differente caratteristica con core, RAM e dimensione disco preconfigurati secondo i tuoi bisogni. La caratteristica del server virtuale che selezioni determina i core, la RAM e le dimensioni del disco validi.  

I server virtuali dedicati sono più personalizzabili; pertanto, puoi modificare i core, la RAM e le dimensioni disco individuali.

Utilizza le seguenti istruzioni per riconfigurare un server virtuale esistente.
{:shortdesc}

## Modifica di un server virtuale esistente (che utilizza caratteristiche preconfigurate)
1. Accedi al [{{site.data.keyword.slportal_full}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) utilizzando le tue credenziali univoche. 
2. Dall'elenco dei dispositivi, fai clic sul nome del server virtuale che desideri riconfigurare.
3. Nella scheda **Configurazione**, puoi fare clic su **Modifica** o **Modifica configurazione dispositivo** per aggiornare i seguenti elementi. 
  <dl>
  <dt>Dimensione</dt>
  <dd>Seleziona una nuova dimensione.</dd>
  <p><note>Nota: quando modifichi una caratteristica che utilizza la memoria locale, non puoi passare a una caratteristica che utilizza memoria non locale. Allo stesso modo, quando modifichi una caratteristica che utilizza la memoria non locale non puoi passare a una caratteristica che utilizza memoria locale.
  </note></p>
  </dl>
4. Dopo aver specificato le modifiche del server virtuale, completa l'aggiornamento della configurazione.
  <dl>
  
  <dt>Data di aggiornamento</dt>
  <dd>Puoi fare clic sulla casella di spunta Immediatamente per un aggiornamento immediato o pianificare un'ora di attivazione dell'aggiornamento.</dd>

  <dt>Ora di aggiornamento</dt>
  <dd>Immetti la data (YYYY-MM-DD) per l'attivazione dell'aggiornamento.</dd>

  <dt>Note</dt>
  <dd>Immetti tutte le note applicabili al tuo dispositivo. </dd>
  </dl>

5. Fai clic su **Continua**.
6. Controlla la tua conferma di ordine per accuratezza.  Fai clic su **Modifica** per modificare il tuo aggiornamento.
7. Fai clic su **Conferma** per confermare il tuo ordine e applicare le modifiche al tuo dispositivo.

## Modifica di un server virtuale esistente (prima delle caratteristiche preconfigurate) o di un server virtuale dedicato
1. Dall'elenco dei dispositivi, fai clic sul nome del server virtuale che desideri riconfigurare.
2. Nella scheda **Configurazione**, puoi fare clic sul link **Aggiornamento core o RAM** per aggiornare i seguenti elementi. 
  
|   Opzioni di aggiornamento       |  Descrizione                                                                                                |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| Data di aggiornamento            | Immetti la data (YYYY-MM-DD) per l'attivazione dell'aggiornamento.                                                |
| Ora di aggiornamento            | Seleziona l'ora dalle caselle a discesa per l'ora del giorno in cui l'aggiornamento diventa attivo o fai clic sulla casella di spunta **Immediato** per un aggiornamento immediato.                                                                                        |
| Core                   | Seleziona il numero di core per l'aggiornamento, se applicabile. |
| RAM                     | Seleziona la quantità di RAM da applicare al tuo dispositivo per l'aggiornamento, se applicabile.   |
| Velocità porta di uplink      | Seleziona le nuove velocità di porta di uplink per il tuo dispositivo, se applicabile. |
| Larghezza di banda pubblica        | Seleziona la quantità (in GB) della larghezza di banda pubblica per il tuo dispositivo, se applicabile.   |
| Primo disco – Quinto disco | Seleziona l'opzione di spazio/archiviazione del disco per il tuo primo disco, se applicabile. Vedi **Note sul disco** qui di seguito per ulteriori informazioni.                                                                                                                               |
| Note                   | Immetti tutte le note applicabili al tuo dispositivo.                                                                 |
{: caption="Tabella 1. Opzioni di distribuzione" caption-side="top"}   
  
  **Note sul disco:**
  * È disponibile sia l'archiviazione locale che SAN.  Ricontrolla la selezione per assicurarti che l'opzione di archiviazione sia corretta.
  * Per i server virtuali pubblici, se stai aggiornando l'archiviazione locale e hai bisogno di più core o RAM, potresti perdere il tuo disco secondario. Quando modifichi una caratteristica del server virtuale che utilizza l'archiviazione locale, la caratteristica è preimpostata e le caratteristiche non confrontabili non possono essere selezionate.
3. Fai clic su **Continua**.
4. Controlla la tua conferma di ordine per accuratezza.  Fai clic su **Modifica** per modificare il tuo aggiornamento.
5. Fai clic su **Conferma** per confermare il tuo ordine e applicare le modifiche al tuo dispositivo.
