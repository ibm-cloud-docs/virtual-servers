---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-06"

keywords: virtual server, suspend billing feature, virtual server instances, suspend billing

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}

# Interruption de la facturation
{: #requirements}

Lorsque vous mettez hors tension un serveur virtuel prenant en charge la fonction d'interruption de facturation, les coûts relatifs à certaines ressources de traitement ne sont pas décomptés. La facturation s'arrête automatiquement lorsque le serveur est mis hors tension. La fonction d'interruption de facturation vous permet de réduire les coûts et vous évite d'avoir à remettre à disposition un serveur virtuel quand vous avez à nouveau besoin de ses ressources.
{:shortdesc}

La plupart des instances de serveur virtuel créées avant le 1er novembre 2018 ne prennent pas en charge la fonction d'interruption de facturation. Pour savoir si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation, voir [Affichage de la fonction d'interruption de facturation](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature).

Cette fonction est disponible dans les centres de données du monde entier. Pour qu'une instance de serveur virtuel prenant en charge la fonction d'interruption de facturation puisse être mise à disposition, elle doit être configurée avec les paramètres suivants :

* SAN horaire
* Profils publics de l'une des familles suivantes :
  * Balanced
  * Compute
  * Memory

Vous pouvez utiliser la fonction d'interruption de facturation comme une alternative plus rapide à la mise à disposition et à la récupération d'une instance de serveur virtuel.
{:tip}

La facturation est uniquement interrompue lorsque vous mettez hors tension votre instance de serveur virtuel via la console {{site.data.keyword.cloud}}, l'interface de ligne de commande ou {{site.data.keyword.slapi_short}}. Si vous mettez hors tension votre instance de serveur virtuel directement à travers le système d'exploitation, la facturation n'est pas interrompue pour cette instance.
{:note}

## Détails de la mise à disposition

Vous pouvez mettre à disposition une instance de serveur virtuel prenant en charge la fonction d'interruption de facturation via le catalogue {{site.data.keyword.cloud_notm}} (cloud.ibm.com), l'interface de ligne de commande ou l'API {{site.data.keyword.slapi_short}}. Vous ne pouvez pas mettre à disposition d'instance de serveur virtuel prenant en charge la fonction d'interruption de facturation via le portail {{site.data.keyword.slportal}} (control.softlayer.com). Pour plus d'informations sur la mise à disposition d'instances de serveur virtuel publiques, voir [Mise à disposition d'instances publiques](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public).

Pour le catalogue {{site.data.keyword.cloud_notm}}, vous devez posséder un compte mis à niveau afin de commander des serveurs virtuels. Pour plus d'informations sur la mise à niveau de votre compte, voir [Basculement sur IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

### Mise à disposition via l'API Softlayer
Vous pouvez mettre à disposition une instance de serveur virtuel prenant en charge la fonction d'interruption de facturation via l'API {{site.data.keyword.slapi_short}}. Pour obtenir des exemples d'API, voir [Mise à disposition d'une instance publique en utilisant Place Order Object](/docs/vsi?topic=virtual-servers-api-rest-public#provisioning-a-public-instance-using-place-order-object).

Vous devez spécifier l'ID de package d'interruption de facturation spécifique durant le processus de mise à disposition. Vous pouvez effectuer une requête relative à l'ID de package de suspension de facturation dans l'API {{site.data.keyword.slapi_short}} en utilisant le nom de clé keyName `SUSPEND_CLOUD_SERVER`. Pour un exemple de recherche des packages de serveur, voir [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Détails de facturation

Il est important de distinguer/connaître les coûts qui ne sont pas décomptés quand votre instance de serveur virtuel est hors tension et ceux qui continuent à vous être facturés.

| Ressource                      | Arrêt de la facturation   | Poursuite de la facturation |
| ----------------------------- | ----------------- | ---------------- |
| UC virtuelle                          | ![Icône de coche](../../icons/checkmark-icon.svg) |                  |
| RAM                           | ![Icône de coche](../../icons/checkmark-icon.svg) |                  |
| Vitesse de port                    | ![Icône de coche](../../icons/checkmark-icon.svg) |                  |
| Licences de système d'exploitation     | ![Icône de coche](../../icons/checkmark-icon.svg) |                  |
| Surveillance des modules complémentaires            | ![Icône de coche](../../icons/checkmark-icon.svg) |                  |
| Adresse IP publique secondaire |                   | ![Icône de coche](../../icons/checkmark-icon.svg) |
| Stockage                       |                   | ![Icône de coche](../../icons/checkmark-icon.svg) |
{: row-headers}
{: class="comparison-table"}
{: caption="Tableau 1. Détails de facturation des ressources" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the resource. The column headers identify whether billing stops or persists when your instance is powered off. To understand whether billing stops or persists for a resource, navigate to the row in the table, and find the billing information you are interested in."}  

Lorsque vous mettez à disposition une instance de serveur virtuel qui prend en charge la fonction d'interruption de facturation, les durées d'utilisation sont calculées par seconde, aussi bien pour la durée d'utilisation que pour la durée d'interruption de votre instance de serveur virtuel. Même si vous n'avez jamais initié la fonction d'interruption de la facturation en arrêtant votre instance, les coûts sont calculés à la seconde pour le cycle de vie de l'instance.
{:note}

### Charge d'utilisation minimale
Les instances de serveur virtuel qui prennent en charge la fonction d'interruption de facturation ont une charge d'utilisation minimale qui s'applique dans certains cas. Si l'utilisation est supérieure à 25 %, vous êtes facturé pour cette utilisation. Si elle est inférieure à 25 %, vous payez 25 % des heures durant lesquelles l'instance a existé au sein du cycle de facturation actuel.

### Facture et facturation
Quand vous interrompez la facturation sur un serveur virtuel, quelques changements sont apportés sur votre facture. Les charges respectives apparaissent désormais sous forme d'informations avec détails d'utilisation. Vous verrez, par exemple, les ajouts ci-après qui reflètent les heures disponibles, les heures utilisées et le nombre total d'heures facturées :

```
Computing instance usage...
RAM usage...
Operating system usage...
```
{:screen}

## Détails des ressources

### Stockage

Lorsque vous interrompez la facturation sur une instance de serveur virtuel, la facturation du stockage associé continue mais vous ne pouvez pas accéder aux données stockées tant que l'instance de serveur virtuel est hors tension. Lorsque vous reprenez la facturation sur l'instance, vous pouvez de nouveau accéder à vos données.

### Adresses IP

Toutes les adresses IP publiques sont conservées quand la facturation est interrompue pour votre instance de serveur virtuel.

### Limitations

Les instances de serveur virtuel qui sont interrompues continuent d'être prises en compte dans le quota d'unités à l'échelle du compte. Pour en savoir plus sur les limites d'instance, voir la section [Foire aux questions : serveurs virtuels](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#concurrent).

## Etapes suivantes
Après avoir mis à disposition un serveur virtuel prenant en charge l'interruption de facturation, vous pouvez commencer à interrompre et reprendre la facturation sur l'unité.

Lorsque la facturation est interrompue sur une instance de serveur virtuel, vous ne pouvez pas effectuer sur l'instance toutes les actions habituelles tant que la facturation pour l'unité n'a pas repris. Vous pouvez voir si votre unité est arrêtée, ainsi que la date effective à laquelle le statut a changé, via l'API {{site.data.keyword.slapi_short}} ou en accédant à la page Détails de l'unité dans le portail {{site.data.keyword.slportal}}.

Pour interrompre la facturation sur une instance de serveur virtuel, mettez le serveur virtuel hors tension. Pour plus d'informations, voir [Gestion des serveurs virtuels](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
