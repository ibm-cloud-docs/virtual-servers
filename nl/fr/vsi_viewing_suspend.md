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

# Affichage de la fonction d'interruption de facturation
{: #viewing-suspend-billing-feature}

## Avant de commencer
Tout d'abord, accédez au menu Unité et assurez-vous de disposer des droits de compte appropriés pour exécuter la tâche. 

* Accédez au menu Unité de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des droits de compte et accès aux unités requis. Seul le propriétaire de compte ou un utilisateur disposant de droit d'infrastructure classique **Gérer les utilisateurs** peut modifier les droits. 

Pour plus d'informations sur les droits, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux unités](/docs/vsi?topic=virtual-servers-managing-device-access).

## Affichage de la fonction d'interruption de facturation 
Pour voir si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation, procédez comme suit :

1. Dans le menu **Unités**, sélectionnez **Liste des unités**. 
2. Dans **Liste des unités**, cliquez sur le nom de votre instance de serveur virtuel. 
3. Dans la section **Détails de l'instance**, vous pouvez voir si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation.  

| Zone                                 | Valeur                     |
| --------------------------------------| ------------------------- |
| Facturation suspendue : activée à la mise hors tension | La fonction est prise en charge.     |
| Facturation suspendue : non disponible          | La fonction n'est pas prise en charge. |
{: caption="Tableau 1. Détails de la fonction d'interruption de facturation" caption-side="top"}

## Affichage de la fonction d'interruption de facturation via l'API SoftLayer

La commande ci-après est un exemple de demande visant à vérifier si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation dans l'API {{site.data.keyword.slapi_short}}.

La demande et la réponse JSON suivantes représentent un exemple générique.
{:note}

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
1. [Interruption de la facturation ](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [Gestion des serveurs virtuels](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

