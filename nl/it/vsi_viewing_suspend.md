---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-28"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Visualizzazione della funzione di sospensione della fatturazione
{: #viewing-suspend-billing-feature}

## Informazioni preliminari
Per prima cosa passa al menu del dispositivo e assicurati di disporre delle autorizzazioni account corrette per completare l'attività. 

* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assicurati di avere tutte le autorizzazioni account necessarie e l'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione dell'infrastruttura classica **Manage Users**, può modificare le autorizzazioni. 

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione accesso dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Visualizzazione della funzione di sospensione della fatturazione 
Per determinare se la tua istanza del server virtuale supporta la funzione di sospensione della fatturazione, attieniti alla seguente procedura:

1. Dal menu **Devices**, seleziona **Device List**. 
2. Da **Device List**, fai clic sul nome della tua istanza del server virtuale. 
3. Nella sezione **Instance details**, puoi visualizzare se la tua istanza del server virtuale supporta la funzione di sospensione della fatturazione. 

| Campo                                 | Valore                     |
| --------------------------------------| ------------------------- |
| Sospensione della fatturazione: Abilitata o Spenta | La funzione è supportata.     |
| Sospensione della fatturazione: Non disponibile          | La funzione non è supportata. |
{: caption="Tabella 1. Dettagli della sospensione della fatturazione" caption-side="top"}

## Visualizzazione della funzione di sospensione della fatturazione tramite l'API SoftLayer

Il seguente comando è una richiesta di esempio di verifica per appurare se la tua istanza del server virtuale supporta la funzione di sospensione della fatturazione tramite la {{site.data.keyword.slapi_short}}.

La richiesta e la risposta JSON di seguito riportate sono un esempio generico.
{:note}

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

La seguente è la risposta JSON di esempio alla richiesta:

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

Per ulteriori informazioni, consulta la [documentazione della API SLDN ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}.

## Passi successivi

Per ulteriori informazioni sulla funzione di sospensione della fatturazione, consulta le seguenti informazioni:
1. [Sospensione della fatturazione ](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [Gestione di server virtuali](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

