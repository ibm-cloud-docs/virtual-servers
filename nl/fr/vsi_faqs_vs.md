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


# Foire aux questions : Serveurs virtuels  

## Quels types de serveur virtuel sont disponibles pour être utilisés ?
{{site.data.keyword.BluSoftlayer_full}} inclut plusieurs types de serveur virtuel. L'offre standard est un serveur virtuel public, qui est un environnement multi-location, adapté à un grand nombre de besoins. Si vous cherchez un environnement à service exclusif, pensez à l'offre Serveur virtuel dédié. L'option de serveur virtuel dédié est idéale pour les applications ayant des besoins en ressources plus stricts. Pour plus d'informations sur l'offre de serveur virtuel actuelle, voir [Serveurs virtuels - Initiation](../vsi/vsi_index.html).

## Où puis-je trouver des informations de tarification pour les types d'instance publique ?
Pour obtenir des informations de tarification, voir [Build your virtual server ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers){: new_window}.

## Puis-je ajouter du stockage sur disque à mon serveur virtuel horaire ou mensuel ?
Vous pouvez mettre à niveau ou rétromigrer le stockage sur disque pour tout serveur virtuel en mettant à jour vos options de stockage dans les zones *Premier disque* à *Cinquième disque* de l'écran *Configuration* du terminal que vous mettez à jour. Pour plus d'informations, voir [Nouvelle configuration d'un serveur virtuel existant](../vsi/vsi_reconfigure.html).

## Combien de serveurs virtuels horaires puis-je démarrer ?

Par défaut, un compte dispose d'une limite de 20 instances pouvant être exécutées sur des serveurs virtuels publics, des serveurs virtuels dédiés et des serveurs Bare Metal.  Si vous souhaitez augmenter cette limite, contactez le support pour l'informer de votre activité et indiquer le nombre d'instances simultanées dont vous pourriez avoir besoin.

## Comment suis-je facturé pour la bande passante de mes serveurs virtuels horaires ?

La facturation virtuelle horaire est séparée pour le trafic entrant et sortant. L'ensemble du trafic entrant vers votre serveur virtuel est gratuit. Le trafic sortant est mesuré et facturé par Go et est évalué à la fin de votre période de facturation.

## Dans quels cas mon serveur virtuel est-il migré vers un hôte différent ? 

Dans certains cas, il peut s'avérer nécessaire de migrer un serveur virtuel vers un hôte différent. Si une migration est requise, le serveur virtuel est arrêté migré, puis redémarré. Un serveur virtuel peut être migré dans les cas suivants :

* Un hyperviseur doit être mis à jour, un hôte est déclassé ou un hôte n'est pas autorisé à accepter de nouvelles instances. Si un hôte est marqué pour l'un de ces changements et que l'un de ses serveurs virtuels est réamorcé à partir du portail {{site.data.keyword.slportal_full}}, le réamorçage déclenche automatiquement la migration du serveur virtuel vers un hôte différent. 
* Maintenance de l'infrastructure. Vous pouvez recevoir un courrier électronique indiquant qu'une maintenance est requise sur un système qui héberge votre serveur virtuel. Il se peut que votre serveur virtuel doive être migré dans le cadre de la maintenance d'infrastructure.
* Mise à niveau vers une instance existante. A des fins de cohérence des performances, il se peut qu'une instance mise à niveau soit migrée vers un hôte différent pour bénéficier d'une UC et de la quantité de mémoire appropriées. 

Pendant une fenêtre de maintenance, l'option **Migrer un hôte** est susceptible de s'afficher dans le menu **Actions** de votre terminal dans le portail {{site.data.keyword.slportal}}. L'option **Migrer un hôte** vous permet de migrer le serveur virtuel vers un nouvel hôte quand vous le souhaitez pendant une période de maintenance spécifiée. Si vous ne lancez pas la migration pendant la période de maintenance, le serveur virtuel est automatiquement migré afin que la maintenance demandée soit menée à bien. L'option **Migrer un hôte** ne s'affiche pas de manière permanente et est disponible uniquement pendant les périodes de maintenance communiquées via les notifications de maintenance.

Vous pouvez également voir l'option **Migrer un hôte** si l'un des serveurs virtuels doit avoir un certain niveau d'hyperviseur qui n'est pas disponible sur l'hôte en cours.

## Puis-je utiliser un abonnement Red Hat Cloud Access pour créer un serveur virtuel ? 

Oui. Lorsque vous importez une image, vous pouvez préciser que vous fournirez la licence du système d'exploitation. Pour plus d'informations, voir [Utilisation de Red Hat Cloud Access](../infrastructure/image-templates/use-red-hat-cloud-access.html). Vous pouvez ensuite commander un serveur virtuel à partir de ce modèle d'image et utiliser votre abonnement [Red Hat Cloud Access ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} existant.

## Quelle est la différence entre un serveur virtuel et un serveur privé virtuel (VPS) ?

Un serveur virtuel est similaire aux plateformes de serveur privé virtuel (VPS) ou de serveur dédié virtuel (VDS) que vous connaissez peut-être déjà. Ces environnements de "serveur virtuel" permettent de mettre à disposition des environnements distincts en toute sécurité sur un noeud matériel, mais les fonctions des serveurs dédiés virtuels (VDS) et des serveurs privés virtuels (VPS) sont plus limitées. Les options VPS et VDS sont généralement restreintes à une architecture de serveur unique, ainsi seules les ressources installées physiquement sur ce serveur peuvent être ajoutées/réparties entre chaque serveur virtuel sur un serveur VDS ou VPS.

Les serveurs virtuels sont mis à disposition sur une architecture en cloud à plusieurs serveurs qui regroupe toutes les ressources matérielles disponibles pour les instances individuelles à utiliser. Les serveurs virtuels peuvent optimiser une plateforme de stockage principal de type SAN à haute capacité partagée ou un stockage de disque local à haute performances. Etant donné que chaque instance fait partie d'un environnement de cloud plus étendu, la communication entre tous les serveurs virtuels est instantanée.

## Je n'arrive pas à me connecter à l'API de virtualisation. Comment puis-je résoudre ce problème ?

Cette erreur survient généralement lorsqu'un mot de passe est obsolète. Pour résoudre ce problème, mettez à jour le mot de passe root ou de l'administrateur pour le système d'exploitation du serveur virtuel dans le portail {{site.data.keyword.slportal_full}}.
