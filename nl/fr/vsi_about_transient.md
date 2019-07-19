---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

keywords: transient virtual servers, transient instances, transient offering, cost savings

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Serveurs virtuels transitoires
{: #about-vs-transient}
L'offre de serveurs {{site.data.keyword.BluVirtServers}} transitoires est une bonne option si vos charges de travail sont flexibles et si vous souhaitez réaliser des économies. Vous économiserez de l'argent en exécutant votre charge de travail sur un serveur virtuel transitoire. Des instances transitoires sont fournies lorsque des capacités inutilisées sont disponibles. Par conséquent, lorsque des ressources du centre de données sont requises pour des comptes à la demande qui sont complets, vous pouvez également perdre ces ressources. Les instances transitoires sont retirées (sur la base du premier activé, premier désactivé) lorsque ces ressources ont besoin d'être récupérées.   

Les serveurs virtuels transitoires offrent la flexibilité suivante :

* **Disponibilité globale**

    L'offre de serveur virtuel transitoire est disponible dans les centres de données du monde entier.

* **Economies de coûts**

    Les serveurs virtuels transitoires sont idéaux pour les charges de travail non associées à un environnement de production. Par exemple, vous pouvez utiliser une instance transitoire pour tester et développer des applications ou pour tester la mise à l'échelle dans des environnements qui ne nécessitent pas une disponibilité constante.

Les instances transitoires sont des instances publiques qui utilisent un stockage SAN. Les familles d'instances publiques suivantes sont disponibles pour cette offre. 

| Familles | Description                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Balanced](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Choix recommandé pour les charges de travail de cloud communes nécessitant un équilibre entre les performances et l'évolutivité. Utilise un stockage sur réseau.|
| [Compute](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Choix recommandé pour les charges de travail de trafic Web modéré à élevé.|
| [Memory](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Choix recommandé pour les charges de travail d'analyse en temps réel et de mise en cache de mémoire. |
{: caption="Tableau 1. Sélections de familles de serveurs virtuels publics " caption-side="top"}

## Notifications
Vous pouvez utiliser l'{{site.data.keyword.slapi_short}} pour recevoir des notifications lorsque des ressources sont disponibles pour une instance transitoire. Vous pouvez également utiliser l'API pour mettre à disposition un serveur virtuel transitoire à l'aide d'un programme lorsque des ressources deviennent disponibles. De même, vous pouvez utiliser l'API pour arrêter de mettre à disposition des instances à l'aide d'un programme lorsque des ressources deviennent indisponibles. Pour plus d'informations, voir [Configuration des notifications pour la récupération des serveurs virtuels transitoires](/docs/vsi?topic=virtual-servers-configuring-notifications-for-reclaims-of-transient-virtual-servers#configuring-notifications-for-reclaims-of-transient-virtual-servers).  

## Limitations
Tenez compte des limitations suivantes avant de mettre à disposition un serveur virtuel transitoire.

* Le nombre d'instances simultanées prises en charge dépend du quota d'unités de votre compte. Pour en savoir plus sur les limites d'instances simultanées, voir la section [Foire aux questions : serveurs virtuels](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#faqs-virtual-servers).
* Les instances transitoires ne peuvent pas être mises à niveau ni rétromigrées.
* Les ressources peuvent être récupérées à tout moment, sans notification.
* Les instances transitoires ne peuvent pas utiliser la mémoire locale.
* Les instances transitoires ne peuvent pas utiliser les profils basés sur le GPU.


## Etapes suivantes

Après avoir vérifié et sélectionné votre profil de serveur virtuel, mettez à disposition votre serveur virtuel transitoire. Pour commencer, voir [Mise à disposition d'instances transitoires](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient).

