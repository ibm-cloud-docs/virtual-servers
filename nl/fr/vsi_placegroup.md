---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Groupes de placement
{: #placement-groups}

La haute disponibilité est un aspect important de tout déploiement dans le cloud. Qu'il s'agisse du site Web de votre entreprise de commerce électronique ou d'une base de données de production utilisée par l’application clé de votre entreprise, elle doit rester opérationnelle. Pour ce faire, nos clients architectes informatiques travaillent sans relâche à mettre en place une infrastructure résiliente pour obtenir des pourcentages toujours plus élevés de temps de disponibilité. Si le temps de disponibilité est surveillé de près par les services informatiques, il peut tomber en dessous des niveaux clés ou provoquer des pannes importantes, ce qui pose d’énormes problèmes pour l’ensemble de l’entreprise. 

Une construction redondante à chaque niveau de votre infrastructure pour éliminer tout point de défaillance unique
(SPOF) est essentielle pour obtenir de bons résultats avec cette métrique. Pour les charges de travail s'exécutant sur des serveurs virtuels, cela signifie implémenter des solutions de basculement avec plusieurs serveurs virtuels pouvant se compléter mutuellement en cas de blocage.

Cependant, à moins que vos serveurs virtuels publics ne soient mis à disposition dans différents centres de données, il n’y a vraiment aucun moyen de déterminer où ils seront placés les uns par rapport aux autres. Cela peut poser un problème si 1) vous envisagez d'utiliser la HA et 2) vos serveurs virtuels arrivent sur le même hôte physique, ce qui les rend vulnérables à une panne dans un matériel unique. Bien que cela soit peu probable, les directeurs informatiques n'ont pas la possibilité d'effectuer un SPOF pour les applications critiques. La construction au sein de centres de données est une possibilité, mais elle peut présenter des problèmes de réseau et nécessiter des dispositifs supplémentaires ou des temps d'attente plus longs, en particulier dans les régions ne disposant que d’un seul centre de données. 

La conception des groupes de placement pour les serveurs virtuels {{site.data.keyword.cloud}} résout ce problème. Les groupes de placement vous permettent de contrôler l'hôte sur lequel un nouveau serveur virtuel public est placé. Dans cette version, il existe une règle de "propagation" qui signifie que les serveurs virtuels d'un groupe de placement sont tous répartis sur des hôtes différents. Vous pouvez créer une application haute disponibilité dans un centre de données en sachant que vos serveurs virtuels sont isolés les uns des autres. 

Les groupes de placement dotés de la règle de "propagation" peuvent être créés dans certains centres de données {{site.data.keyword.cloud_notm}}. Une fois créé, vous pouvez mettre à disposition un nouveau serveur virtuel dans ce groupe et garantir qu'il ne se trouve pas sur le même hôte que l'un de vos autres serveurs virtuels. Cerise sur le gâteau : l’utilisation de cette fonctionnalité est totalement gratuite. Sous réserve de disponibilité, les groupes de placement {{site.data.keyword.cloud_notm}} pour les serveurs virtuels sont une fonctionnalité gratuite 

Vous pouvez créer votre groupe de placement, puis affecter jusqu'à cinq nouvelles instances de serveur virtuel. Avec la règle de "propagation", chacun de vos serveurs virtuels est mis à disposition sur différents hôtes physiques.

## Etapes suivantes

Pour créer et gérer de nouveaux groupes de placement, voir [Gestion des groupes de placement](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup#vsi_managing_placegroup).
