---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-26"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# A propos de l'interruption de facturation (bêta)
{: #requirements}

Quand vous mettez hors tension un serveur virtuel prenant en charge la fonction d'interruption de facturation, les coûts relatifs à certaines ressources de traitement ne sont pas décomptés. La facturation s'arrête automatiquement quand le serveur est mis hors tension. La fonction d'interruption de facturation vous permet de réduire les coûts et vous évite d'avoir à remettre à disposition un serveur virtuel quand vous avez à nouveau besoin de ses ressources. L'interruption de facturation n'est prise en charge que sur les nouvelles mises à disposition et non pas sur les instances existantes.
{:shortdesc}

Pour avoir accès à la fonction d'interruption de facturation, vous devez mettre à disposition la nouvelle instance de serveur virtuel en utilisant l'API {{site.data.keyword.slapi_short}} pour spécifier le package de suspension de facturation. La nouvelle instance de serveur virtuel doit être configurée avec les paramètres suivants :

* SAN horaire
* L'une des familles suivantes :
  * Balanced
  * Compute
  * Memory
* L'un des centres de données {{site.data.keyword.cloud}} suivants :

| Centres de données |         |
| ------------ | ------- | 
|SEO01         |  WDC01  |
|SAO01         |  WDC04  |
|TOK02         |  WDC06  |
|DAL01         |  WDC07  |
|DAL05         |  LON02  |
|DAL06         |  LON04  |
|DAL09         |  LON06  |
|DAL10         |  FRA02  |
|DAL12         |  FRA04  |
|DAL13         |  FRA05  |
{: caption="Tableau 1. Centres de données pris en charge" caption-side="top"}

Vous pouvez utiliser la fonction d'interruption de facturation comme une alternative plus rapide à la mise à disposition/hors disposition d'une instance de serveur virtuel.
{:tip}

## Mise à disposition

Pour la bêta, pour mettre à disposition une instance de serveur virtuel prenant en charge la fonction d'interruption de facturation, vous devez utiliser l'API {{site.data.keyword.slapi_short}}. Pour des exemples d'API, voir [Mise à disposition d'une instance publique en utilisant Place Order Object](../vsi/vsi_provision_api.html#provisioning-a-public-instance-using-place-order-object). 

Vous devez aussi spécifier l'ID de package de suspension de facturation spécifique durant le processus de mise à disposition. Vous pouvez effectuer une requête relative à l'ID de package de suspension de facturation dans l'API {{site.data.keyword.slapi_short}} en utilisant le nom de clé keyName `SUSPEND_CLOUD_SERVER`. Pour un exemple de recherche des packages de serveur, voir [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Détails de facturation

Il est important de distinguer/connaître les coûts qui ne sont pas décomptés quand votre instance de serveur virtuel est hors tension et ceux qui continuent à vous être facturés.

| Ressource                      | Arrêt de la facturation   | Poursuite de la facturation |
| ----------------------------- | ----------------- | ---------------- |
| UC virtuelle                          |          X        |                  |
| RAM                           |          X        |                  |
| Vitesse de port                    |          X        |                  |
| Licences de système d'exploitation     |          X        |                  |
| Surveillance des modules complémentaires            |          X        |                  |
| Adresse IP publique secondaire |                   |         X        |
| Stockage                       |                   |         X        |
{: caption="Tableau 1. Détails de facturation des ressources" caption-side="top"}   

**Remarque :** quand vous mettez à disposition une instance de serveur virtuel qui prend en charge la fonction d'interruption de facturation, les durées d'utilisation sont calculées par minute, aussi bien pour la durée en utilisation que celle en période d'interruption d'utilisation de votre instance de serveur virtuel. Même si vous n'avez jamais initié la fonction d'interruption de facturation en mettant votre instance hors tension, la facturation est calculée par minute de cycle de vie de l'instance. 

### Charge d'utilisation minimale
Les instances de serveur virtuel qui prennent en charge la fonction d'interruption de facturation ont une charge d'utilisation minimale par mois. Si l'utilisation est supérieure à 25 %, vous êtes facturé pour cette utilisation. Si elle est inférieure à 25 %, vous payez 25 % des heures durant lesquelles l'instance a existé au sein du cycle de facturation actuel. 

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

Quand vous interrompez la facturation sur une instance de serveur virtuel, le stockage associé est conservé mais vous ne pouvez pas accéder aux données tant que l'instance de serveur virtuel est hors tension. Quand vous reprenez la facturation sur l'instance, vous pouvez accéder à vos données et la facturation normale recommence.

### Adresses IP

Toutes les adresses IP publiques sont conservées quand la facturation est interrompue pour votre instance de serveur virtuel.

Vous pouvez voir si votre unité est arrêtée, ainsi que la date effective à laquelle le statut a changé, via l'API {{site.data.keyword.slapi_short}} ou en accédant à la page Détails de l'unité dans le portail {{site.data.keyword.slportal_full}}.

### Limitations

Le nombre d'instances simultanées prises en charge dépend du quota d'unités de votre compte. Pour en savoir plus sur les limites d'instances simultanées, voir la section [Foire aux questions : serveurs virtuels](vsi_faqs_vs.html#concurrent).

## Etapes suivantes
Après avoir mis à disposition un serveur virtuel prenant en charge l'interruption de facturation, vous pouvez commencer à interrompre et reprendre la facturation sur l'unité.
Quand la facturation est interrompue sur une instance de serveur virtuel, vous ne pouvez pas effectuer sur l'instance toutes les actions habituelles tant que vous n'avez pas repris la facturation pour l'unité.

Pour interrompre la facturation sur une instance de serveur virtuel, mettez le serveur virtuel hors tension. Pour plus d'informations, voir [Gestion des serveurs virtuels](vsi_managing.html).
