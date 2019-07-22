---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:note: .note}
{:new_window: target="_blank"}

# Gestione dei gruppi di posizionamento
{: #vsi_managing_placegroup}

Puoi gestire i gruppi di posizionamento utilizzando la pagina dei gruppi di posizionamento oppure la pagina dei dettagli del dispositivo nella console {{site.data.keyword.cloud}}.
{:shortdesc}

## Aggiunta di gruppi di posizionamento

Per aggiungere dei gruppi di posizionamento dalla pagina dei gruppi di posizionamento, completa la seguente procedura:
{:shortdesc}

1. Apri la pagina [Gruppi di posizionamento ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. Nella pagina dei gruppi di posizionamento, fai clic su **Nuovo gruppo**.
3. Immetti un nome, un'ubicazione, un pod e una regola per il gruppo di posizionamento e fai clic su **Crea**.

Le istanze esistenti non possono essere aggiunte a un gruppo di posizionamento; puoi aggiungere un'istanza del server virtuale a un gruppo di posizionamento solo in fase di provisioning. 
{:note}

## Gestione dei gruppi di posizionamento

Per gestire i gruppi di posizionamento dalla pagina dei gruppi di posizionamento, completa la seguente procedura:
{:shortdesc}

1. Apri la pagina [Gruppi di posizionamento ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. Nella sezione del gruppo di posizionamento, puoi completare diverse attività di gestione.
     * Visualizzare un elenco di gruppi di posizionamento e il numero di istanze assegnate
     * Aggiungere un gruppo
     * Ridenominare un gruppo
     * Eseguire il provisioning di un'istanza
     * Eliminare un gruppo
     
Devi rimuovere i server assegnati dal gruppo di posizionamento prima che il gruppo di posizionamento possa essere eliminato. Per rimuovere un'istanza da un gruppo di posizionamento, devi eliminare o recuperare l'istanza.
{:note}
