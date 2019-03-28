---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-30"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:faq: data-hd-content-type='faq'}


# Foire aux questions : Serveurs virtuels  
{: #faqs-virtual-servers}

## Quels types de serveur virtuel sont disponibles pour être utilisés ?
{:faq}

{{site.data.keyword.BluSoftlayer_full}} inclut plusieurs types de serveur virtuel. L'offre standard est un serveur virtuel public, qui est un environnement multilocataire, adapté à un grand nombre de besoins. Si vous cherchez un environnement à service exclusif, pensez à l'offre Serveur virtuel dédié. L'option de serveur virtuel dédié est idéale pour les applications ayant des besoins en ressources plus stricts. Pour plus d'informations sur l'offre de serveur virtuel actuelle, voir [Serveurs virtuels - Initiation](/docs/vsi?topic=virtual-servers-getting-started-tutorial).

## Où puis-je trouver des informations de tarification pour les types d'instance publique ?
{:faq}

Pour obtenir des informations de tarification, voir [Build your virtual server ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers){: new_window}.

## Où puis-je trouver des informations de tarification pour les instances publiques virtuelles ?
{:faq}

Pour obtenir des informations sur la tarification, voir [Virtual servers provisioning calculator](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator).

## Puis-je ajouter du stockage sur disque à mon serveur virtuel horaire ou mensuel ?
{:faq}

Vous pouvez mettre à niveau ou rétromigrer le stockage sur disque pour tout serveur virtuel en mettant à jour vos options de stockage dans les zones *Premier disque* à *Cinquième disque* de l'écran *Configuration* du terminal que vous mettez à jour. Pour plus d'informations, voir [Nouvelle configuration d'un serveur virtuel existant](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers).

## Combien de serveurs virtuels horaires puis-je démarrer ?
{:faq}

Par défaut, un compte dispose d'une limite de 20 instances pouvant être exécutées sur des serveurs virtuels publics, des serveurs virtuels dédiés et des serveurs Bare Metal.  Si vous souhaitez augmenter cette limite, contactez le support pour l'informer de votre activité et indiquer le nombre d'instances simultanées dont vous pourriez avoir besoin.

## Comment suis-je facturé pour la bande passante de mes serveurs virtuels horaires ?
{:faq}

La facturation virtuelle horaire est séparée pour le trafic entrant et sortant. L'ensemble du trafic entrant vers votre serveur virtuel est gratuit. Le trafic sortant est mesuré et facturé par Go et est évalué à la fin de votre période de facturation.

## Dans quels cas mon serveur virtuel est-il migré vers un hôte différent ?
{:faq}
Dans certains cas, il peut s'avérer nécessaire de migrer un serveur virtuel vers un hôte différent. Si une migration est requise, le serveur virtuel est arrêté migré, puis redémarré. Un serveur virtuel peut être migré dans les cas suivants :

* Un hyperviseur doit être mis à jour, un hôte est déclassé ou un hôte n'est pas autorisé à accepter de nouvelles instances. Si un hôte est marqué pour l'un de ces changements et que l'un de ses serveurs virtuels est réamorcé à partir du portail {{site.data.keyword.slportal_full}}, le réamorçage déclenche automatiquement la migration du serveur virtuel vers un hôte différent.
* Maintenance de l'infrastructure. Vous pouvez recevoir un courrier électronique indiquant qu'une maintenance est requise sur un système qui héberge votre serveur virtuel. Il se peut que votre serveur virtuel doive être migré dans le cadre de la maintenance d'infrastructure.
* Mise à niveau vers une instance existante. A des fins de cohérence des performances, il se peut qu'une instance mise à niveau soit migrée vers un hôte différent pour bénéficier d'une UC et de la quantité de mémoire appropriées.

Pendant une fenêtre de maintenance, l'option **Migrer un hôte** est susceptible de s'afficher dans le menu **Actions** de votre terminal dans le portail {{site.data.keyword.slportal}}. L'option **Migrer un hôte** vous permet de migrer le serveur virtuel vers un nouvel hôte quand vous le souhaitez pendant une période de maintenance spécifiée. Si vous ne lancez pas la migration pendant la période de maintenance, le serveur virtuel est automatiquement migré afin que la maintenance demandée soit menée à bien. L'option **Migrer un hôte** ne s'affiche pas de manière permanente et est disponible uniquement pendant les périodes de maintenance communiquées via les notifications de maintenance.

Vous pouvez également voir l'option **Migrer un hôte** si l'un des serveurs virtuels doit avoir un certain niveau d'hyperviseur qui n'est pas disponible sur l'hôte en cours.

## Qu'arrive-t-il à mes données lorsque mon dispositif de stockage portable est supprimé ?
{:faq}

Lorsque le dispositif de stockage est supprimé, tous les pointeurs vers les données de ce volume sont supprimés, et les données deviennent par conséquent totalement inaccessibles. Si le dispositif de stockage physique est alloué à un nouveau compte, un nouvel ensemble de pointeurs sont affectés. Il n'existe aucune possibilité pour le nouveau compte d'accéder aux données contenues antérieurement sur le dispositif de stockage physique. Le nouvel ensemble de pointeurs affiche tous les 0. Lorsque de nouvelles données sont écrites dans le volume/LUN, toutes les données inaccessibles existantes sont écrasées.

## Puis-je utiliser un abonnement Red Hat Cloud Access pour créer un serveur virtuel ?
{:faq}

Oui. Lorsque vous importez une image, vous pouvez préciser que vous fournirez la licence du système d'exploitation. Pour plus d'informations, voir [Utilisation de Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription). Vous pouvez ensuite commander un serveur virtuel à partir de ce modèle d'image et utiliser votre abonnement [Red Hat Cloud Access ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} existant.

## Quelle est la différence entre un serveur virtuel et un serveur privé virtuel (VPS) ?
{:faq}
Un serveur virtuel est similaire aux plateformes de serveur privé virtuel (VPS) ou de serveur dédié virtuel (VDS) que vous connaissez peut-être déjà. Ces environnements de "serveur virtuel" permettent de mettre à disposition des environnements distincts en toute sécurité sur un noeud matériel, mais les fonctions des serveurs dédiés virtuels (VDS) et des serveurs privés virtuels (VPS) sont plus limitées. Les options VPS et VDS sont généralement restreintes à une architecture de serveur unique, ainsi seules les ressources installées physiquement sur ce serveur peuvent être ajoutées ou réparties entre chaque serveur virtuel sur un serveur VDS ou VPS.

Les serveurs virtuels sont mis à disposition sur une architecture en cloud à plusieurs serveurs qui regroupe toutes les ressources matérielles disponibles pour les instances individuelles à utiliser. Les serveurs virtuels peuvent optimiser une plateforme de stockage principal de type SAN à haute capacité partagée ou un stockage de disque local à haute performances. Etant donné que chaque instance fait partie d'un environnement de cloud plus étendu, la communication entre tous les serveurs virtuels est instantanée.

<!--## I'm unable to connect to the virtualization API. How can I fix this?-->

<!--This error generally occurs because a password is outdated. To fix this, update the root or Administrator password for the virtual server's operating system in the {{site.data.keyword.slportal_full}}.-->

## Pour quelle raison une erreur de capacité s'affiche-t-elle lors de la mise à disposition d'un serveur virtuel ?
{:faq}

Lorsque vous mettez à disposition un serveur virtuel, un message d'erreur indiquant que la demande ne peut aboutir en raison d'une capacité insuffisante s'affiche. Lorsque la mise à disposition échoue, toutes les instances de serveur virtuel faisant partie de cette demande spécifique échouent. Une erreur de capacité se produit lorsque le nombre de ressources disponibles est insuffisant dans le routeur ou dans le centre de données pour répondre à la demande de service. Il existe une série de raisons pour lesquelles cette erreur peut se produire. La disponibilité des ressources change fréquemment, et il est donc conseillé d'attendre et de réessayer plus tard. Pour plus d'informations sur les stratégies permettant d'éviter cette erreur, voir [Capacity considerations](/docs/vsi?topic=virtual-servers-capacity-considerations).
