---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-14"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurazione delle autorizzazioni dell'utente per il ridimensionamento automatico 
{: #user-permissions-required-to-use-auto-scale}

L'accesso alle opzioni del ridimensionamento automatico richiede un'autorizzazione utente speciale oltre alla capacità di ordinare e gestire {{site.data.keyword.virtualmachinesshort}}. Per accedere alle funzioni del ridimensionamento automatico, devi avere l'autorizzazione per gestire tutti i server virtuali nell'account in aggiunta a tutti i dispositivi virtuali aggiunti in futuro.

Se sei l'amministratore dell'account e vuoi concedere l'autorizzazione agli utenti per accedere alle opzioni del ridimensionamento automatico, completa la seguente procedura:

1. Accedi alla pagina [Accesso (IAM) ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/iam#/users){: new_window} nella console {{site.data.keyword.cloud}}. 
2. Nella scheda **Utenti**, seleziona **Visualizzato da: Miei utenti dell'infrastruttura classica**.
3. Seleziona un utente e fai quindi clic sulla scheda **Infrastruttura classica**.
4. Espandi la categoria **Dispositivi** nella scheda **Autorizzazioni** e seleziona **Gestisci gruppi di ridimensionamento automatico**.
5. Fai clic su **Applica**.

## Passi successivi

Una volta che disponi dell'autorizzazione per accedere alle opzioni del ridimensionamento automatico, sei pronto ad utilizzare la funzione. Per iniziare, rivedi le seguenti informazioni:

1. [Gestione dei picchi di traffico con il ridimensionamento automatico basato sulle pianificazioni](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling)
2. [Gestione dei picchi di traffico con il ridimensionamento automatico basato sulle risorse](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling)
3. [FAQ: ridimensionamento automatico](/docs/vsi?topic=virtual-servers-faqs-auto-scale)

