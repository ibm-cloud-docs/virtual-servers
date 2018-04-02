---
copyright:
  years: 2014, 2018
lastupdated: "2018-02-26"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Options de stockage

Vous pouvez choisir le réseau SAN ou le stockage local pour chaque serveur virtuel. Vous pouvez ensuite utiliser d'autres produits de stockage en complément, si nécessaire. 

## Stockage local

Le stockage local est placé sur les disques locaux de l'hôte du serveur virtuel. Le stockage local offre de meilleures performances de lecture/écriture sur disque. Les disques sont créés dans une configuration RAID afin de garantir une redondance, un remplacement des disques et une surveillance de l'état de santé, entièrement gérés par {{site.data.keyword.cloud}}. Dans les centres de données plus récents, le stockage s'effectue uniquement sur unité SSD pour de meilleures performances. 

## Stockage SAN
 
Le stockage SAN repose sur l'infrastructure SAN de {{site.data.keyword.cloud_notm}} et non sur le stockage d'hôte local. Ainsi, la résilience est améliorée lorsqu'une défaillance d'hôte survient. De plus, les volumes de taille plus élevée sont pris en charge. En cas de défaillance d'un hôte, les instances de serveur virtuel utilisant le stockage SAN sont automatiquement migrées vers d'autres hôtes et redémarrées. 

Tous les disques secondaires sont connectés en tant que stockage portable. Dans la plupart des cas, les disques peuvent être déconnectés à tout moment pour être déplacés vers d'autres serveurs virtuels. 

**Exception :** Si vous employez des serveurs virtuels qui utilisent le stockage Balanced Local, vous ne pouvez pas déconnecter les disques principaux ou secondaires.

Les disques peuvent être reconnectés à un autre serveur, tant que les modifications restent dans les limites de taille de volume maximales ou dans les quotas de disque du serveur virtuel cible.

**Remarque :** Le disque déplacé est converti en type de stockage du serveur cible.

## Volumes de stockage portables

Les volumes de stockage portable sont des solutions de stockage auxiliaires exclusivement disponibles sur les serveurs {{site.data.keyword.BluVirtServers_short}}. Il est possible de les connecter à un serveur virtuel à tout moment. Ils constituent également une solution idéale si vous souhaitez transférer des données entre des serveurs virtuels qui existent dans n'importe quel centre de données du réseau {{site.data.keyword.cloud_notm}}. Les volumes de stockage portable sont utiles pour les applications de base de données qui nécessitent un accès à un stockage par blocs, brut non formaté et pour le déplacement de jeux de données volumineux entre des serveurs {{site.data.keyword.BluVirtServers_short}}.

Lorsqu'un volume de stockage portable est connecté à un serveur virtuel d'un centre de données autre que celui du serveur virtuel d'origine, le système interne de {{site.data.keyword.cloud_notm}} copie le volume vers le réseau de stockage SAN du nouveau centre de données. Le système vérifie ensuite l'intégrité du volume copié et retire le volume portable d'origine du réseau de stockage SAN du centre de données d'origine.

## Limitations de gestion de volume logique (LVM)

La gestion LVM n'est pas prise en charge en tant que schéma de partitionnement amorçable. Avec la configuration et le support de système d'exploitation appropriés, les disques du serveur virtuel secondaire peuvent être utilisés pour les partitions LVM. Toutefois, LVM n'est pas un système de fichiers pris en charge pour les modèles d'image ou les images flexibles.

## Stockage supplémentaire

Les serveurs virtuels sont totalement compatibles avec le stockage SAN de fichier et de bloc, ainsi qu'avec le stockage d'objet. Ces types de stockage sont recommandés pour les unités de cluster, le stockage de fichier partagé, le stockage d'archives, les exigences de stockage important ou les exigences de performances spécifiques.

Pour plus d'informations sur les autres options de stockage, reportez-vous aux ressources suivantes :

* [Initiation à Block Storage](/docs/infrastructure/BlockStorage/index.html)
* [Initiation à File Storage](/docs/infrastructure/FileStorage/index.html)
* [Initiation à Object Storage](/docs/services/ObjectStorage/index.html)

## Etapes suivantes
Pour plus d'informations sur l'utilisation des volumes de stockage portable, reportez-vous aux tâches suivantes :
* [Accès au stockage portable](../storage/access-portable-storage-screen.html)
* [Edition de la description d'un stockage portable](../storage/edit-description-portable-storage-volume-psv.html)


