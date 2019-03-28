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

# Affichage de la fonction d'interruption de facturation
{: #viewing-suspend-billing-feature}

Vous pouvez voir si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation dans le portail {{site.data.keyword.slportal_full}} ou via l'API {{site.data.keyword.slapi_short}}.

## Affichage de la fonction d'interruption de facturation dans le portail client
Pour voir si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation dans le portail {{site.data.keyword.slportal}}, procédez comme suit :

1. Connectez-vous au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
2. Dans le menu **Unités**, sélectionnez **Liste d'unités**.
3. Dans **Liste des unités**, cliquez sur le nom de votre instance de serveur virtuel.
4. Dans l'onglet **Configuration** de la section **Dispositions générales**, vous pouvez voir si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation. 

| Zone                                 | Valeur                     |
| --------------------------------------| ------------------------- |
| Interrompre la facturation : activée ou mise hors tension | La fonction est prise en charge.     |
| Interrompre la facturation : non disponible          | La fonction n'est pas prise en charge. |
{: caption="Tableau 1. Détails de la fonction d'interruption de facturation" caption-side="top"}

## Affichage de la fonction d'interruption de facturation via l'API SoftLayer

La commande ci-après est un exemple de demande visant à vérifier si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation dans l'API {{site.data.keyword.slapi_short}}.

**Remarque** : la demande et la réponse JSON suivantes représentent un exemple générique.

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

Voici un exemple de réponse JSON à la demande :

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

Pour plus d'informations, voir la [documentation de l'API SLDN![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}.

## Etapes suivantes

Pour en savoir plus sur la fonction d'interruption de facturation, passez en revue les informations suivantes :
1. [A propos de l'interruption de facturation](/docs/vsi?topic=virtual-servers-requirements)
2. [Gestion des serveurs virtuels](/docs/vsi?topic=virtual-servers-managing-virtual-servers)
