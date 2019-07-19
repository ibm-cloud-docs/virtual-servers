---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-09"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# Foire aux questions : serveurs virtuels  
{: #faqs-virtual-servers}

## Quels types de serveurs virtuels sont disponibles pour utilisation ? 
{: faq}
{{site.data.keyword.BluSoftlayer_full}} inclut plusieurs types de serveur virtuel au sein de l'Infrastructure classique. L'offre standard est un serveur virtuel public, qui est un environnement à service partagé, adapté à un grand nombre de besoins. Si vous cherchez un environnement à service exclusif, pensez à l'offre Serveur virtuel dédié. L'option de serveur virtuel dédié est idéale pour les applications ayant des besoins en ressources plus stricts. Pour plus d'informations sur l'offre de serveur virtuel actuelle, voir [Serveurs virtuels - Initiation](/docs/vsi?topic=virtual-servers-getting-started-with-virtual-servers#getting-started-with-virtual-servers).

IBM Cloud propose l'infrastructure VPC (Virtual Private Cloud), plateforme cloud de nouvelle génération. Vous créez votre propre espace dans {{site.data.keyword.cloud_notm}} pour exécuter un environnement isolé dans le cloud public à l'aide de VPC. VPC offre la sécurité d'un cloud privé alliée à l'agilité et à la facilité d'un cloud public. Pour plus d'informations, voir [A propos de Virtual Private Cloud](https://cloud.ibm.com/docs/vpc-on-classic?topic=vpc-on-classic-about). 

## Où puis-je trouver des informations de tarification pour les types d'instance publique ?
{: faq}

Pour obtenir des informations de tarification, voir [Build your virtual server ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/cloud/virtual-servers){: new_window}.

## Où puis-je trouver des informations de tarification pour les instances publiques virtuelles ?
{: faq}

L'estimation du coût de prise en charge de votre charge de travail par un serveur {{site.data.keyword.cloud_notm}} commence dans le [catalogue {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/catalog). Dans le catalogue, sélectionnez **Calcul** et choisissez le type de serveur - Serveur bare metal, Serveur virtuel ou Serveur virtuel pour VPC (Virtual Private Cloud). Pour plus d'informations sur la tarification, voir [Calculateur de mise à disposition de serveurs virtuels ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

## Puis-je ajouter du stockage sur disque à mon serveur virtuel horaire ou mensuel ?
{: faq}

Vous pouvez mettre à niveau ou rétromigrer le stockage sur disque pour tout serveur virtuel en mettant à jour vos options de stockage dans les zones *Premier disque* à *Cinquième disque* de l'écran *Configuration* du terminal que vous mettez à jour. Pour plus d'informations, voir [Nouvelle configuration d'un serveur virtuel existant](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).

## Combien de serveurs virtuels horaires puis-je démarrer ?
{: #concurrent}
{: faq}

Le nombre d'instances que vous pouvez exécuter dépend du niveau de maturité de votre compte. Par défaut, un compte de plus de 45 jours a une limite de 20 instances pouvant s'exécuter à tout moment sur des serveurs virtuels publics, des serveurs virtuels dédiés et des serveurs bare metal. Un compte plus récent a une limite inférieure Si vous souhaitez augmenter la limite, contactez le support pour l'informer de votre activité et indiquer le nombre d'instances simultanées dont vous pourriez avoir besoin.

## Comment suis-je facturé pour la bande passante de mes serveurs virtuels horaires ?
{: faq}

La facturation virtuelle horaire est séparée pour le trafic entrant et sortant. L'ensemble du trafic entrant vers votre serveur virtuel est gratuit. Le trafic sortant est mesuré et facturé par Go et est évalué à la fin de votre période de facturation.

## Dans quels cas mon serveur virtuel est-il migré vers un hôte différent ?
{: faq}

Dans certains cas, il peut s'avérer nécessaire de migrer un serveur virtuel vers un hôte différent. Si une migration est requise, le serveur virtuel est arrêté migré, puis redémarré. Un serveur virtuel peut être migré dans les cas suivants :

* Un hyperviseur doit être mis à jour, un hôte est déclassé ou un hôte n'est pas autorisé à accepter de nouvelles instances. Si un hôte est marqué pour l'un de ces changements et que l'un de ses serveurs virtuels est réamorcé à partir de la console {{site.data.keyword.cloud_notm}}, le réamorçage déclenche automatiquement la migration du serveur virtuel vers un hôte différent.
* Maintenance de l'infrastructure. Vous pouvez recevoir un courrier électronique indiquant qu'une maintenance est requise sur un système qui héberge votre serveur virtuel. Il se peut que votre serveur virtuel doive être migré dans le cadre de la maintenance d'infrastructure.
* Mise à niveau vers une instance existante. A des fins de cohérence des performances, il se peut qu'une instance mise à niveau soit migrée vers un hôte différent pour bénéficier d'une UC et de la quantité de mémoire appropriées.
* Un hôte dédié échoue. Les instances dédiées sont migrées vers un autre hôte vide sans utiliser aucune des capacités existantes que vous pourriez avoir. 

Pendant une fenêtre de maintenance, l'option **Migrer un hôte** est susceptible de s'afficher dans le menu **Actions** de votre terminal dans la console {{site.data.keyword.cloud_notm}}. L'option **Migrer un hôte** vous permet de migrer le serveur virtuel vers un nouvel hôte quand vous le souhaitez pendant une période de maintenance spécifiée. Si vous ne lancez pas la migration pendant la période de maintenance, le serveur virtuel est automatiquement migré afin que la maintenance demandée soit menée à bien. L'option **Migrer un hôte** ne s'affiche pas de manière permanente et est disponible uniquement pendant les périodes de maintenance communiquées via les notifications de maintenance.

Vous pouvez également voir l'option **Migrer un hôte** si l'un des serveurs virtuels doit avoir un certain niveau d'hyperviseur qui n'est pas disponible sur l'hôte en cours.

## Qu'arrive-t-il à mes données lorsque mon dispositif de stockage portable est supprimé ?
{: faq}

Lorsque le dispositif de stockage est supprimé, tous les pointeurs vers les données de ce volume sont supprimés, et les données deviennent par conséquent inaccessibles. Si le dispositif de stockage physique est alloué à un nouveau compte, un nouvel ensemble de pointeurs est affecté. Il n'existe aucune possibilité pour le nouveau compte d'accéder aux données contenues antérieurement sur le dispositif de stockage physique. Le nouvel ensemble de pointeurs affiche tous les 0. Lorsque de nouvelles données sont écrites dans le volume/LUN, toutes les données inaccessibles existantes sont écrasées.

## Puis-je utiliser un abonnement Red Hat Cloud Access pour créer un serveur virtuel ?
{: faq}

Oui. Lorsque vous importez une image, vous pouvez préciser que vous fournirez la licence du système d'exploitation. Pour plus d'informations, voir [Utilisation de Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription#using-your-own-os-license-or-subscription). Vous pouvez ensuite commander un serveur virtuel à partir de ce modèle d'image et utiliser votre abonnement [Red Hat Cloud Access ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} existant.

## Quelle est la différence entre un serveur virtuel et un serveur privé virtuel (VPS) ?
{: faq}

Un serveur virtuel est similaire aux plateformes de serveur privé virtuel (VPS) ou de serveur dédié virtuel (VDS) que vous connaissez peut-être déjà. Ces environnements de "serveur virtuel" permettent de mettre à disposition des environnements distincts en toute sécurité sur un noeud matériel, mais les fonctions des serveurs dédiés virtuels (VDS) et des serveurs privés virtuels (VPS) sont plus limitées. Les options VPS et VDS sont généralement limitées à une architecture à serveur unique. Les seules ressources pouvant être ajoutées ou réparties entre chaque serveur virtuel sur un serveur VDS ou un VPS sont les ressources installées physiquement sur ce serveur unique. 

Les serveurs virtuels sont mis à disposition sur une architecture en cloud à plusieurs serveurs qui regroupe toutes les ressources matérielles disponibles pour les instances individuelles à utiliser. Les serveurs virtuels peuvent utiliser une plateforme de stockage principal de type SAN à haute capacité partagée ou un stockage de disque local à haute performance. Etant donné que chaque instance fait partie d'un environnement de cloud plus étendu, la communication entre tous les serveurs virtuels est instantanée.

## Pour quelle raison une erreur de capacité s'affiche-t-elle lors de la mise à disposition d'un serveur virtuel ?
{: faq}

Lorsque vous mettez à disposition un serveur virtuel, un message d'erreur indiquant que la demande ne peut aboutir en raison d'une capacité insuffisante s'affiche. Lorsque la mise à disposition échoue, toutes les instances de serveur virtuel faisant partie de cette demande spécifique échouent. Une erreur de capacité se produit lorsque le nombre de ressources disponibles est insuffisant dans le routeur ou dans le centre de données pour répondre à la demande de service. Il existe une série de raisons pour lesquelles cette erreur peut se produire. La disponibilité des ressources change fréquemment, et il est donc conseillé d'attendre et de réessayer plus tard. Pour plus d'informations sur les stratégies permettant d'éviter cette erreur, voir [Considérations relatives aux ressources pour les instances de serveur virtuel](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).

## Comment puis-je me connecter à mon serveur ? 
{: faq}

Connectez-vous à votre console et accédez au menu **Unités**. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices). Dans la **Liste des unités**, sélectionnez votre instance. Vous pouvez afficher et gérer les noms d'utilisateur et les mots de passe d'unité à utiliser pour la connexion. Pour plus d'informations, voir [Affichage et gestion des noms d'utilisateur et des mots de passe des unités](https://test.cloud.ibm.com/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device).  

## Comment puis-je utiliser un réseau privé virtuel (VPN) pour accéder au réseau privé IBM Cloud ? 
{: faq}

Vous pouvez vous connecter au VPN via [l'interface Web](https://www.softlayer.com/VPN-Access){: external} ou utiliser un [client VPN autonome](/docs/infrastructure/iaas-vpn?topic=VPN-standalone-vpn-clients) pour Linux, macOS ou Windows. Pour plus d'informations sur les actions à mettre en oeuvre une fois que vous êtes connecté au VPN, consultez [Utilisation d'un VPN SSL](/docs/infrastructure/iaas-vpn?topic=VPN-use-ssl-vpn).

## Comment puis-je redémarrer mon serveur virtuel ?  
{: faq}

Les réamorçages d'unités peuvent s'effectuer à partir de la **Liste des unités** ou de la vue d'instantané d'une instance donnée. Accédez à votre instance de serveur virtuel dans la **Liste des unités** de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices). Sélectionnez **Actions** pour l'unité à gérer et sélectionnez **Réamorcer**.

## Comment puis-je utiliser Rescue Kernel ? 
{: faq}

Effectuer l'amorçage dans Rescue Kernel est utile si vous rencontrez un problème lié au serveur. Pour lancer Rescue Kernel, sélectionnez le nom de l’unité dans la **Liste des unités** de votre console. Dans le menu **Actions**, sélectionnez **Mode récupération** ou sélectionnez **Initialiser à partir d'une image** pour une instance Windows. Pour plus d'informations, voir [Lancement de Rescue Kernel](/docs/vsi?topic=virtual-servers-launching-rescue).

## Où puis-je trouver le statut du réseau ? 
{: faq}

Vous pouvez accéder à la page **Statut** directement sur [{{site.data.keyword.cloud_notm}} - Statut](https://cloud.ibm.com/status){: external} pour afficher le statut actuel des ressources dans tous les emplacements {{site.data.keyword.cloud_notm}}. Vous pouvez filtrer la liste en sélectionnant des composants et des emplacements spécifiques (par exemple, vous pouvez sélectionner Virtual Servers et afficher la connectivité réseau). 

## Comment puis-je demander un rapport de conformité ? 
{: faq}

Pour plus d'informations sur l'affichage ou la demande d'informations de conformité, y compris les rapports SOC, voir [Comment savoir si mes données sont protégées ?](/docs/overview?topic=overview-security)

