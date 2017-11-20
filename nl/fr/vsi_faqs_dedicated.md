---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Foire aux questions : Instances et hôtes dédiés

## Qu'est-ce qu'un hôte dédié ?
Les hôtes dédiés {{site.data.keyword.Bluemix}} sont des serveurs physiques validés pour un groupe d'utilisateurs. Les hôtes dédiés offrent la capacité de mise à disposition de serveur virtuel et un contrôle d'emplacement optimal.

## Quels sont les avantages d'utiliser des hôtes dédiés et non des instances dédiées ?
Une location unique est garantie pour les deux offres. Les hôtes dédiés permettent de définir sur quel hôte mettre à disposition les instances d'hôte dédiés. Vous pouvez également : 
   * Contrôler le centre de données {{site.data.keyword.cloud}} dans lequel le serveur est placé
   * Gérer vos serveurs lors du changement des exigences de charge de travail ; par exemple, la migration de serveurs virtuels entre vos hôtes dédiés sur le même pod

## Puis-je conserver mes instances dédiées existantes ou ai-je besoin de configurer un hôte dédié et des instances d'hôte dédiées ?
Oui, vous pouvez conserver vos instances dédiées existantes. 

## Puis-je échanger la mise à disposition des instances dédiées (autosignées) et des instances d'hôte dédiées ?
Non. Les instances dédiées autosignées existantes ne peuvent pas être mises à disposition à nouveau sur les hôtes dédiés. Si vous avez besoin de serveurs virtuels, vous devez les mettre à disposition sur des hôtes dédiés en tant qu'instances d'hôte dédiées.

## Quel type de serveur (virtuel ou Bare Metal) prend en charge l'offre d'hôte dédié ?
L'offre est prise en charge sur les serveurs virtuels, {{site.data.keyword.Bluemix_notm}} n'a pas d'offre Bare Metal. La durée nécessaire à la mise à disposition et la gestion de la virtualisation sont différentes pour les hôtes virtuels et les serveurs Bare Metal.

## Quel est le cycle de vie de mise à disposition d'un hôte dédié ?
Les hôtes dédiés sont alloués à des utilisateurs lors de la mise à disposition. Ils seront conservés sur le compte jusqu'à ce qu'ils soient réclamés. 
Les hôtes dédiés sont proposés uniquement dans la tarification à la demande, horaire ou mensuelle. Lorsqu'ils sont récupérés, les modèles de facturation procèdent à une facturation horaire ou mensuelle des offres {{site.data.keyword.BluSoftlayer_full}}. 

## Comment l'offre d'hôte dédié est-elle facturée ?
Vous pouvez acheter des hôtes dédiés à la demande avec une facturation horaire ou mensuelle. Les hôtes facturés à l'heure uniquement permettent seulement la mise à disposition d'instances horaires alors que les hôtes facturés au mois uniquement permettent de mettre à disposition des instances mensuelles *et* horaires. La tarification des hôtes dédiés inclut le coeur, la mémoire RAM, le stockage SSD local et les vitesses des ports réseau. Le prix des systèmes d'exploitation Premium, du stockage SAN et des modules complémentaires logiciels ainsi que les licences est facturé en fonction de l'instance déployée (à l'heure ou au mois) sur l'hôte dédié. Le modèle de tarification des instances dédiées et publiques {{site.data.keyword.Bluemix_notm}} est également utilisé pour ces éléments.

## J'exécute un hôte dédié à la demande, comment suis-je facturé ?
Vous êtes facturé à l'heure ou au mois pour les hôtes dédiés. Les instances d'hôte dédiées mises à disposition sur des hôtes dédiés peuvent générer des frais d'instance, comme cela est indiqué dans la réponse à la question **Comment une offre d'hôte dédiée est-elle facturée ?**

## Comment la location est-elle définie lors de la mise à disposition d'hôtes dédiés et d'instances d'hôte dédiées ?
La location par défaut pour les instances dédiées est à service exclusif. Vous pouvez mettre à disposition des instances dédiées sur un hôte dédié (instances d'hôte dédiées) ou sur un hôte auto-affecté (instances dédiées). Les instances dédiées sur les hôtes auto-affectés n'offrent pas le même niveau de gestion que celles sur un hôte dédié.

## Puis-je associer différentes configurations d'instance d'hôte dédiée sur mon hôte dédié ?
Oui. Vous pouvez mettre à disposition différentes tailles de serveur virtuel sur des hôtes dédiés en respectant les allocations de capacité.

## Comment connaître le nombre d'instances d'hôte dédiées pouvant être exécutées sur chaque hôte dédié ?
Chaque hôte dédié a une allocation spécifique de coeur, de mémoire RAM et de stockage SSD local. Vous pouvez consulter les allocations de ressource sur l'onglet correspondant afin de connaître le nombre d'instances d'hôte dédiées mises à disposition, la capacité d'hôte en cours utilisée et les éléments disponibles.

## Quelles images peuvent être mises à disposition sur les hôtes dédiés ?
Vous pouvez mettre à disposition des images de stockage de serveur virtuel {{site.data.keyword.Bluemix_notm}} ou importer vos propres images, comme cela est indiqué dans le contrat de tiers.

## Existe-t-il une limite au nombre d'hôtes dédiés pouvant être alloués à un seul compte ?
Oui, les limitations de ressource sont définies par compte, selon les spécifications en tant que ressources de service pour la totalité de {{site.data.keyword.BluSoftlayer_notm}}. Vous pouvez avoir plusieurs commandes par compte mais uniquement deux hôtes dédiés par commande de mise à disposition.

## Les déploiements d'hôte dédié peuvent-ils être sollicités de manière excessive ?
Non, vous ne pouvez mettre à disposition que la capacité indiquée sur les hôtes dédiés.

