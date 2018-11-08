---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Serveurs virtuels transitoires
L'offre de serveurs {{site.data.keyword.BluVirtServers}} transitoires est une bonne option si vos charges de travail sont flexibles et si vous souhaitez réaliser des économies. Vous économiserez de l'argent en exécutant votre charge de travail sur un serveur virtuel transitoire. Des instances transitoires sont fournies lorsque des capacités inutilisées sont disponibles. Par conséquent, lorsque des ressources du centre de données sont requises pour des comptes à la demande qui sont complets, vous pouvez également perdre ces ressources. Les instances transitoires sont retirées (sur la base du premier activé, premier désactivé) lorsque ces ressources ont besoin d'être récupérées.   

Les serveurs virtuels transitoires offrent la flexibilité suivante :

* **Disponibilité globale** 

    L'offre de serveur virtuel transitoire est disponible dans les centres de données du monde entier.
    
* **Economies de coûts** 

    Les serveurs virtuels transitoires sont idéaux pour les charges de travail non associées à un environnement de production. Par exemple, vous pouvez utiliser une instance transitoire pour tester et développer des applications ou pour tester la mise à l'échelle dans des environnements qui ne nécessitent pas une disponibilité constante.

Les instances transitoires sont des instances publiques qui utilisent un stockage SAN.

## Notifications
Vous pouvez utiliser l'{{site.data.keyword.slapi_short}} pour recevoir des notifications lorsque des ressources sont disponibles pour une instance transitoire. Vous pouvez également utiliser l'API pour mettre à disposition un serveur virtuel transitoire à l'aide d'un programme lorsque des ressources deviennent disponibles. De même, vous pouvez utiliser l'API pour arrêter de mettre à disposition des instances à l'aide d'un programme lorsque des ressources deviennent indisponibles. Pour plus d'informations, voir [Configuration des notifications pour la récupération des serveurs virtuels transitoires](configuring-automated-reclaim-notifications.html).

## Limitations
Tenez compte des limitations suivantes avant de mettre à disposition un serveur virtuel transitoire.

* Le nombre d'instances simultanées prises en charge dépend du quota d'unités de votre compte. Pour en savoir plus sur les limites d'instances simultanées, voir la section [Foire aux questions : serveurs virtuels](../vsi/vsi_faqs_vs.html#concurrent).
* Les instances transitoires ne peuvent pas être mises à niveau ni rétromigrées.
* Les ressources peuvent être récupérées à tout moment, sans notification.
* Les instances transitoires ne peuvent pas utiliser la mémoire locale.
* Les instances transitoires peuvent uniquement utiliser le stockage SAN (balanced, compute, memory).
* Les instances transitoires ne peuvent pas utiliser les versions basées sur le GPU.


## Etapes suivantes

Après avoir vérifié et sélectionné votre version de serveur virtuel, mettez à disposition votre serveur virtuel transitoire. Pour commencer, consultez les rubriques suivantes :
1. [Mise à disposition de sélections](../vsi/vsi_public_selections.html)
2. [Mise à disposition d'instances transitoires](../vsi/vsi_provision_transient.html)
