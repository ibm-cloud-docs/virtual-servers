---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-25"

keywords: reserved virtual servers, cost savings, guaranteed capacity 
subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Serveurs virtuels réservés
{: #about-reserved-virtual-servers}

L'offre d'instances réservées de serveurs {{site.data.keyword.BluVirtServers}} est une option idéale si vous voulez des ressources garanties pour des déploiements futurs et pour réaliser des économies de coûts. Vous avez le choix entre un contrat d'une durée d'un ou de trois ans pour votre capacité réservée. Dans le cadre de cette capacité réservée, vous pouvez réserver un maximum de 20 instances de serveur virtuel d'une taille spécifique et mettre ces instances à disposition lorsque vous en avez besoin. Cette capacité vous est garantie au sein du POD et du centre de données de votre choix pendant toute la durée du contrat.

Les instances de serveur virtuel réservées offrent de nombreux avantages, notamment :

* **Capacité garantie**

    Lorsque vous réservez une capacité, celle-ci est garantie pendant toute la durée de votre contrat. 
    
* **Disponibilité globale**
    
    L'offre de serveur virtuel réservé est disponible dans les centres de données du monde entier.

* **Mise à disposition fiable**
   
   Vous pouvez à tout moment mettre à disposition et récupérer les instances de serveur virtuel dans vos capacités réservées.

* **Economies de coûts**
    
    Le choix d'un contrat d'un an ou de trois ans permet d'effectuer des paiements mensuels continus et de réduire les coûts par rapport aux cycles de facturation horaires ou mensuels du serveur virtuel.

Les instances de serveur virtuel réservées sont des instances publiques qui utilisent un stockage SAN. Les familles d'instances publiques suivantes sont disponibles pour cette offre. 

| Familles | Description                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Balanced](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Choix recommandé pour les charges de travail de cloud communes nécessitant un équilibre entre les performances et l'évolutivité. Utilise un stockage sur réseau.|
| [Compute](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Choix recommandé pour les charges de travail de trafic Web modéré à élevé.|
| [Memory](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Choix recommandé pour les charges de travail d'analyse en temps réel et de mise en cache de mémoire. |
{: caption="Tableau 1. Sélections de familles de serveurs virtuels publics " caption-side="top"}

## Limitations 

Tenez compte des limitations suivantes avant de réserver de la capacité et de mettre à disposition des instances de serveur virtuel réservées :
  
  * Vous ne pouvez pas mettre à niveau ou rétromigrer vos instances.
  * La capacité réservée ne peut pas être annulée, par contre vous pouvez récupérer les instances de serveur virtuel dans cette capacité.
    
## Notifications

Vous recevrez une notification par e-mail un mois avant la fin du contrat sur la capacité de serveur virtuel réservée.

## Etapes suivantes

Après avoir révisé et choisi les options, vous devez mettre à disposition votre capacité et vos instances réservées. Pour commencer, consultez les rubriques suivantes :

   1. [Mise à disposition de capacité et d'instances réservées](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)
   2. [Foire aux questions : capacité et instances réservées](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances)
