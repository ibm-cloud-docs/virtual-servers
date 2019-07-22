---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQ: ridimensionamento automatico 
{: #faqs-auto-scale}

## Il ridimensionamento automatico supporta le istanze di ridimensionamento automatico Bare Metal? 
{: faq}

Al momento, il ridimensionamento automatico non supporta le istanze di ridimensionamento automatico Bare Metal.

## Il ridimensionamento automatico funziona con i programmi di bilanciamento del carico?
{: faq}

Sì, il ridimensionamento automatico attualmente funziona per i programmi di bilanciamento del carico locali e utilizza una parte della API del programma di bilanciamento del carico. Per ulteriori informazioni, vedi [Programmi di bilanciamento del carico di ridimensionamento](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Quali sono le diverse politiche di terminazione del ridimensionamento automatico?
{: faq}

Ci sono tre politiche di terminazione del ridimensionamento automatico: newest (più recente), oldest (meno recente) e closest to next charge (più prossimo al successivo addebito). Descrivono in che modo il gruppo sceglie quale membro togliere quando si esegue una riduzione. Per ulteriori informazioni, vedi [Politica di terminazione](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Quali sono le politiche di ridimensionamento automatico?
{: faq}

Una politica contiene una serie di azioni e una serie di trigger. Le politiche di norma sono costituite da questi elementi: nome, periodo di raffreddamento, azione e trigger. Per ulteriori informazioni, vedi [Politiche](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Cosa sono i trigger del ridimensionamento automatico?
{: faq}

I trigger sono delle condizioni che possono essere soddisfatte (solo quando il gruppo è attivo). Ci sono tre tipi di trigger: una tantum (one-time), che si ripete (repeating) e utilizzo delle risorse (resource-use). Per ulteriori informazioni, vedi [Trigger](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Cos'è il conteggio del numero massimo di membri VSI?
{: faq}

È il numero massimo di membri di cui un gruppo consente la presenza. Per ulteriori informazioni, vedi [Conteggio del numero massimo di membri VSI](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Cos'è il conteggio del numero minimo di membri VSI?
{: faq}

È il numero minimo di membri di cui un gruppo consente la presenza. Per ulteriori informazioni, vedi [Conteggio del numero minimo di membri VSI](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Cos'è un asset di ridimensionamento automatico?
{: faq}

Un asset è un membro fisso in un gruppo che non contribuisce al conteggio dei membri e non viene controllato automaticamente in alcun modo. L'asset è presente per fornire ulteriori informazioni ai trigger della politica. Ad esempio, un asset può contribuire alla percentuale CPU dell'intero gruppo se si sta utilizzando la percentuale CPU come un trigger. Attualmente, un gruppo può avere solo degli asset guest virtuali e non esiste alcun limite al loro numero. Inoltre, un gruppo non è richiesto. 

## Cos'è un gruppo di ridimensionamento automatico?
{: faq}

Un gruppo (gruppo di ridimensionamento) è una raccolta specifica del gruppo di asset, membri, programmi di bilanciamento del carico del ridimensionamento, VLAN e politiche. Un gruppo ha tutti i parametri per il ridimensionamento, compresi i limiti di conteggio dei membri e i template di membri dell'istanza del server virtuale ridimensionati. 

## Cos'è un membro di ridimensionamento automatico?
{: faq}

Un membro è un'unità ridimensionata in un gruppo. I membri vengono reclamati oppure ne viene eseguito il provisioning in base alle azioni della politica. Attualmente, tutti i membri sono istanze del server virtuale. Su un gruppo attivo, non c'è mai un numero di membri inferiore al minimo o superiore al massimo consentiti. Anche se sono di norma aggiunti dalle azioni di una politica, i membri possono anche essere aggiunti manualmente da un utente.
