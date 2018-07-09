---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-10"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Hôtes dédiés et instances dédiées 

Les hôtes dédiés sont des serveurs virtuels qui vous permettent de spécifier le centre de données et le pod dans lesquels placer l'hôte. Affectez ensuite des instances, ou des machines virtuelles, à un hôte spécifique pour disposer d'un contrôle maximal sur le placement de la charge de travail et d'options de mise à disposition à différents coûts.
{:shortdesc}

## Capacité garantie
Vous disposez de capacité dans le centre de données et dans le pod dans lesquels votre hôte est placé. Par exemple, si le pod contenant votre hôte dédié et vos instances dédiées atteint sa capacité maximale, vous pouvez continuer à affecter des instances dédiées à votre hôte si ce dernier dispose de l'espace approprié.

## Charges de travail visibles
Vous pouvez afficher la consommation générale des ressources pour toutes les instances dédiées affectées à un hôte dédié sur une page. Consultez l'utilisation du coeur, de la mémoire RAM et du stockage local afin de déterminer si vous avez besoin de migrer les instances dédiées vers un autre hôte dédié. Ce niveau de granularité vous permet de gérer vos charges de travail avec un contrôle maximal. 

## Gestion ultérieure au déploiement
Outre une capacité garantie et une visibilité de vos charges de travail, vous pouvez migrer vos instances dédiées entre des hôtes dédiés pour un contrôle optimal du placement de la charge de travail.

## Maintenance
La maintenance de l'infrastructure nécessite parfois un hôte dédié pour redémarrer. L'hyperviseur Xen, par exemple, peut avoir besoin d'une mise à jour. Si vous disposez d'hôtes dédiés multiples, les options suivantes vous permettent de réduire le temps d'indisponibilité dû à la maintenance. 
* La maintenance est effectuée par des pods d'un centre de données. Vous pouvez déployer vos hôtes dédiés dans des pods séparés pour répartir la maintenance requise. 
* Vous pouvez créer un ticket de support pour un hôte dédié afin de demander qu'une maintenance planifiée soit retardée. Durant cette période, vous pouvez migrer les instances dédiées (hors ligne) entre les hôtes dédiés du même pod.

## Haute disponibilité
Si un hôte dédié échoue, les charges de travail sur l'hôte dédié sont automatiquement migrées vers un nouvel hôte dédié. Les instances dédiées restent dédiées tout le long du cycle de vie du serveur virtuel.

Pour les scénarios de haute disponibilité, vous pouvez envisager de désigner un hôte dédié supplémentaire, afin qu'il vous fournisse la flexibilité requise pour migrer les charges de travail pour les fenêtres de maintenance.
