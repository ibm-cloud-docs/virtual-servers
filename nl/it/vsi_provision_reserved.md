---

copyright:
  years: 2018
lastupdated: "2018-10-05"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning della capacità e delle istanze riservate
{: #provisioning-reserved-capacity-and-instances}

## Informazioni preliminari

Puoi eseguire il provisioning della tua capacità e delle tue istanze tramite il catalogo {{site.data.keyword.cloud}}. Devi eseguire il provisioning della tua capacità riservata prima delle tue istanze del server virtuale.

**Nota**: se non sei l'amministratore dell'account, il tuo account utente deve includere l'autorizzazione **Gestisci capacità riservate**. L'amministratore dell'account può concedere l'autorizzazione dell'utente dalla scheda **Autorizzazioni portale** nella console. Per ulteriori informazioni sull'aggiornamento delle autorizzazioni, consulta [Gestione dell'accesso all'infrastruttura](/docs/iam?topic=iam-mngclassicinfra).

## Accesso al catalogo IBM Cloud

Utilizza la seguente procedura per accedere al catalogo {{site.data.keyword.cloud_notm}} e iniziare il provisioning della tua capacità e delle tue istanze riservate.

  1. Accedi al catalogo [{{site.data.keyword.cloud_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/catalog/){: new_window} utilizzando le tue credenziali univoche.

## Provisioning della capacità riservata

Nel catalogo {{site.data.keyword.cloud_notm}}, completa la seguente procedura per eseguire il provisioning della tua capacità riservata.

  1. Nella sezione **Infrastruttura di calcolo**, fai clic sul tile **Server virtuali**.
  2. Seleziona l'opzione **Server virtuale riservato**.
  3. Fai clic su **Crea**.
  4. Per creare una nuova capacità riservata, seleziona **Nuova capacità +**. Dalla pagina **Capacità Riservata**, immetti o seleziona le seguenti informazioni:

| Campo                   | Valore               |                                                                                                                                                                                                                                                                                                                                 
| ----------------------- | ------------------- |
| Nome                    | È obbligatorio un nome per la tua capacità riservata. |                                                                                                                                                                                                                                                                                                       
| Capacità server virtuale | Seleziona il numero di istanze che vuoi assegnare a questa capacità riservata (limite di 20 istanze). |                                                                                                                                                                                                                                                
| Ubicazione                | Seleziona l'ubicazione specifica richiesta per i tuoi carichi di lavoro. Le ubicazioni sono composte da regioni; ciascuna regione è un'area geografica separata. **Nota:** non puoi selezionare singole ubicazioni per ogni istanza del server virtuale di cui esegui il provisioning all'interno di questa capacità riservata. La tua selezione è l'ubicazione di tutte le istanze del server virtuale di cui esegui il provisioning all'interno di questa capacità riservata. |
| POD                     | Seleziona il POD specifico per la tua ubicazione. |
| Termini del piano              | Scegli tra un termine del contratto di uno o tre anni. |                                                                                                                                                                                                                                                                                            
| Profilo                 | Seleziona dai profili popolari o da tutte le combinazioni vCPU e RAM disponibili di archiviazione di backup SAN (bilanciata, memoria o calcolo). **Nota:** non puoi combinare le diverse dimensioni del profilo all'interno della serie di istanze del server virtuale assegnate a questa capacità o modificarle successivamente. La serie di istanze del server virtuale che riservi deve essere della stessa dimensione. |
{: caption="Tabella 1. Selezioni di provisioning della capacità riservata" caption-side="top"}


## Provisioning delle istanze riservate

Dopo aver eseguito il provisioning della tua capacità riservata, è ora di eseguirlo delle tue istanze del server virtuale riservate. È possibile eseguire il provisioning delle istanze del server virtuale riservate in qualsiasi momento durante i termini del contratto perché la tua capacità è garantita. Completa la seguente procedura per eseguire il provisioning delle tue istanze riservate:

1. Nel catalogo {{site.data.keyword.cloud_notm}}, seleziona il tile **Server virtuali** nella sezione **Infrastruttura di calcolo**.
2. Seleziona l'opzione **Server virtuale riservato**.
3. Fai clic su **Crea**.
4. Per eseguire il provisioning di un'istanza del server virtuale, immetti o seleziona le seguenti informazioni:

| Campo                     | Valore               |                                                                                                                                                                                                                                                                                                                                 
| ------------------------- | ------------------- |
| Nome                      | È obbligatorio un nome per le tue istanze del server virtuale riservate. |                                                                                                                                                                                                                                                                                                       
| Fatturazione                   | Seleziona la fatturazione oraria o mensile. |                                                                                                                                                                                                                                                
| Capacità riservata         | Seleziona la tua capacità riservata o seleziona **Nuova capacità +** per eseguire il provisioning di ulteriore capacità riservata. |                                                                                                                                                                                                     
| Componenti aggiuntivi                   | Scegli ulteriori archiviazione rete o software. |                                                                                                                                                                                                                                                                                            
{: caption="Tabella 1. Selezioni di provisioning della capacità riservata" caption-side="top"}

## Passi successivi

Dopo aver eseguito il provisioning della tua capacità e delle tue istanze del server virtuale riservate, puoi iniziare a gestirle. Per ulteriori informazioni, vedi [Gestione dei server virtuali](/docs/vsi?topic=virtual-servers-managing-virtual-servers). Se hai domande sulla capacità e le istanze riservate, consulta [FAQ: capacità e istanze riservate](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances).
