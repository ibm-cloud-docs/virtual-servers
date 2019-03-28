---

copyright:
  years: 2018, 2019
lastupdated: "2019-03-01"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Visualizzazione della funzione di sospensione della fatturazione
{: #viewing-suspend-billing-feature}

Puoi visualizzare se la tua istanza del server virtuale supporta la funzione di sospensione della fatturazione nel {{site.data.keyword.slportal_full}} o tramite la {{site.data.keyword.slapi_short}}.

## Visualizzazione della funzione di sospensione della fatturazione nel portale del cliente
Per determinare se la tua istanza del server virtuale supporta la funzione di sospensione della fatturazione nel {{site.data.keyword.slportal}}, attieniti alla seguente procedura:

1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.
2. Dal menu **Devices**, seleziona **Device List**.
3. Da **Device List**, fai clic sul nome della tua istanza del server virtuale.
4. Sulla scheda **Configuration** nella sezione **General**, puoi visualizzare se la tua istanza del server virtuale supporta la funzione di sospensione della fatturazione.

| Campo                                 | Valore                     |
| --------------------------------------| ------------------------- |
| Sospensione della fatturazione: Abilitata o Spenta | La funzione è supportata.     |
| Sospensione della fatturazione: Non disponibile          | La funzione non è supportata. |
{: caption="Tabella 1. Dettagli della sospensione della fatturazione" caption-side="top"}

## Visualizzazione della funzione di sospensione della fatturazione tramite la API Softlayer

Il seguente comando è una richiesta di esempio di verifica per appurare se la tua istanza del server virtuale supporta la funzione di sospensione della fatturazione nella {{site.data.keyword.slapi_short}}.

**Nota**: la richiesta e la risposta JSON di seguito riportate sono un esempio generico.

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
1. [Informazioni sulla sospensione della fatturazione](/docs/vsi?topic=virtual-servers-requirements)
2. [Gestione di server virtuali](/docs/vsi?topic=virtual-servers-managing-virtual-servers)
