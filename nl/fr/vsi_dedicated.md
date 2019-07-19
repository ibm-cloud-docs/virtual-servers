---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# A propos des serveurs virtuels dédiés  
{: #dedicated-virtual-servers}

L'offre d'hôte dédié de l'infrastructure {{site.data.keyword.Bluemix}} est un serveur dédié, à service exclusif et virtualisé. Ainsi, vous pouvez contrôler de manière optimale le placement de la charge de travail et vous disposez d'options flexibles à appliquer après la mise à disposition. Vous pouvez définir dans quel centre de données {{site.data.keyword.cloud_notm}} vos serveur virtuels sont placés et vous assurer qu'ils disposent de capacité en allouant vos hôtes directement à votre compte.
{:shortdesc}

L'offre inclut les fonctions suivantes :

* Affinité et anti-affinité. Vous pouvez définir des relations hôte/serveur virtuel et serveur virtuel/serveur virtuel, également appelées règles d'affinité et d'anti-affinité. Ces règles permettent de garantir que vos charges de travail sont correctement placées en fonction des exigences de votre charge de travail.
* Gestion après le déploiement. Vous pouvez migrer des serveurs virtuels entre des hôtes dédiés en fonction des exigences de votre charge de travail.
* Visibilité de la charge de travail. Vous pouvez afficher la consommation des ressources (coeur, mémoire RAM et stockage local) pour chaque hôte, ce qui permet un contrôle optimal de la gestion de votre charge de travail.

Vous pouvez choisir un des deux modèles de déploiement suivants : hôtes dédiés et instances dédiées. Les hôtes dédiés permettent de contrôler le placement de la charge de travail et les instances dédiées permettent un isolement à service exclusif.

Les instances dédiées ne fournissent pas toutes les fonctions de contrôle proposées par les hôtes dédiés. Pour plus de détails, voir le tableau suivant.
{:note}

| Fonction de serveur virtuel dédié | Instances des hôtes dédiés | Instances dédiées |
| ------- | ------- | ------- |
| Isolement à service exclusif | ![Icône de coche](../../icons/checkmark-icon.svg) | ![Icône de coche](../../icons/checkmark-icon.svg) |
| Contrôle du placement de serveur virtuel | ![Icône de coche](../../icons/checkmark-icon.svg) |   |
| Visibilité des ressources | ![Icône de coche](../../icons/checkmark-icon.svg) |   |
| Facturation d'instance |   | ![Icône de coche](../../icons/checkmark-icon.svg) |
| Facturation d'hôte<sup>(1)</sup> | ![Icône de coche](../../icons/checkmark-icon.svg) |   |
| Contrôle ultérieur au déploiement | ![Icône de coche](../../icons/checkmark-icon.svg) |   |
| Réservations de capacité | ![Icône de coche](../../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="Tableau 1. Fonctions de contrôle" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup>La tarification de l'hôte inclut le coeur, la mémoire RAM, l'unité SSD locale et les vitesses réseau. La tarification du système d'exploitation Premium, du stockage SAN et des modules complémentaires logiciels s'effectue par instance. La tarification et l'octroi de licence sont établis de manière horaire ou mensuelle.

Prenez en compte les éléments suivants lorsque vous commandez un ou plusieurs hôtes dédiés et instances d'hôte dédiées :

* La taille de vos hôtes est déterminée par les charges de travail exécutées. La configuration par défaut est 56 coeurs X 242 Go de RAM X 1,2 To, mais vous pouvez choisir parmi des configurations supplémentaires. 
* Vous pouvez commander deux hôtes à la fois uniquement. Par exemple, si vous avez besoin de six hôtes, vous devez effectuer trois commandes.
* Chaque hôte doit avoir son propre nom unique et vous pouvez affecter automatiquement votre pod.

## Etapes suivantes

Une fois que vous avez défini vos options de déploiement, mettez à disposition votre serveur virtuel. Pour commencer, voir [Mise à disposition d'instances et d'hôtes dédiés](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated).
