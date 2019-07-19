---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Configuration des serveurs virtuels
{: #configuring-virtual-servers}

Lorsque vous avez accès à votre serveur virtuel, veillez à modifier votre mot de passe et à envisager de configurer SSH pour une solution d’authentification plus sécurisée. Il existe de nombreuses autres options pour configurer votre serveur virtuel pour répondre aux besoins de votre environnement.
{:shortdesc}

## Connexion
Connectez-vous à la [console {{site.data.keyword.cloud}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/classic?){: new_window} à l'aide des données d'identification que vous avez reçues dans un message électronique lors de la création de votre compte. Sinon, vous pouvez vous connecter à [{{site.data.keyword.slportal}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){:new_window}.

## Recherche de votre serveur virtuel
Recherchez votre serveur virtuel dans la liste des unités, dans la console {{site.data.keyword.cloud_notm}}. A partir de cette liste, vous pouvez gérer et mettre à niveau des terminaux ou générer des graphiques d'utilisation de bande passante. Pour plus d'informations, voir [Gestion des serveurs virtuels](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).

## Changement de votre mot de passe
Changez votre mot de passe en utilisant des directives de mot de passe fort. Voir [Affichage et gestion des noms d'utilisateur et des mots de passe des unités](/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device#view-update-user-name-password-for-device). 

## Configuration de SSH
SSH offre une meilleure solution de sécurité que l’authentification par mot de passe. Voir [Initiation aux clés SSH](/docs/infrastructure/ssh-keys?topic=ssh-keys-getting-started-tutorial#getting-started-tutorial).

## Enregistrement des adresses IP et des données d'identification
Conservez un journal des adresses IP et des données d'identification du serveur à un emplacement sûr afin que vous puissiez accéder rapidement à ces données sans vous connecter à la console {{site.data.keyword.cloud_notm}}.
- Les adresses IP des terminaux sont disponibles dans la liste des terminaux.
- Les mots de passe des terminaux sont disponibles dans la vue d'instantané du terminal. Cliquez sur la flèche en regard du nom du terminal pour développer la vue.
- Vous pouvez afficher les adresses IP des terminaux en sélectionnant l'option Télécharger CSV dans la Liste des unités. Sélectionnez cette option à partir de Paramètres pour télécharger une liste complète des terminaux ainsi que des informations détaillées au format tableur.

## Mise à jour des données d'identification des logiciels
Des données d'identification temporaires sont affectées à tous les logiciels chargés sur l'unité lors du processus de mise à disposition. Vous pouvez consulter et gérer ces données d'identification sur l'onglet Mots de passe de chaque unité dans la console {{site.data.keyword.cloud_notm}}. Utilisez ces données d'identification temporaires lors du premier accès au logiciel. Il est recommandé ensuite de changer le mot de passe. Utilisez un mot de passe fiable composé de lettres, de chiffres et de symboles.

Vous pouvez, si vous le souhaitez, stocker les mises à jour de mot de passe sur l'onglet Mots de passe de chaque terminal. Toutefois, gardez à l'esprit que lorsque vous stockez des mots de passe dans la console {{site.data.keyword.cloud_notm}}, toutes les personnes ayant accès au compte et disposant des droits appropriés peuvent voir les mots de passe stockés sur l'écran Mots de passe.

Pour obtenir des informations supplémentaires sur l'affichage et la gestion des données d'identification de vos logiciels, voir [Gestion de l'accès à l'infrastructure classique](/docs/vsi?topic=iam-mngclassicinfra).

## Accès à votre serveur sur le réseau privé
Le réseau privé constitue le point d'entrée pour l'interaction avec vos unités via le bureau distant (RDP) utilisant SSH et KVM over IP. L'outil d'accès au VPN permet une connexion de réseau privé au noeud final VPN SSL le plus proche ou au noeud final de votre choix. L'accès VPN est également requis pour l'interaction avec plusieurs services. Pour plus d'informations, voir [Getting started with Virtual Private Networking (VPN)](/docs/infrastructure/iaas-vpn?topic=VPN-gettingstarted-with-virtual-private-networking).

## Configuration de la surveillance
La surveillance permet principalement de vérifier la disponibilité de votre serveur mais elle vous permet également de savoir quand effectuer la mise à l'échelle. Les services de surveillance standard et de surveillance Nimsoft permettent de répondre aux différents besoins de surveillance. La surveillance standard, également appelée “Surveillance de base”, est généralement utilisée avec la méthode ping-et-réponse via une commande ping de service ou ping lente lancée à partir de la console {{site.data.keyword.cloud_notm}}. La surveillance Nimsoft est également appelée “Surveillance avancée” et comporte trois niveaux : De base, Avancé et Premium. Ce service est également accessible via la console {{site.data.keyword.cloud_notm}}. Pour plus d'informations, voir [Surveillance](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring#monitoring).

## Configuration des groupes de sécurité
Vous pouvez utiliser des groupes de sécurité pour limiter le trafic réseau sur vos serveurs virtuels. Utilisez des groupes de sécurité pour définir un ensemble de règles de filtrage IP qui définissent la gestion du trafic entrant et sortant vers les interfaces publique et privée d'une instance de serveur virtuel. Pour plus d'informations, voir [Initiation aux groupes de sécurité](/docs/infrastructure/security-groups?topic=security-groups-getting-started).

## Configuration des pare-feux
Des pare-feux matériels sont également disponibles pour garantir une protection renforcée. Ils sont mis à disposition à la demande sans aucune interruption du fonctionnement. Si les règles sont établies correctement, un pare-feu permet de protéger votre serveur d'activités non souhaitées. Une fois que vous avez commandé un pare-feu, il doit être activé et les règles doivent être définies.

Pour plus d'informations, voir les rubriques suivantes.

* [Pare-feux matériels (partagés)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Pare-feux matériels (dédiés)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)

## Planification des sauvegardes
Grâce aux sauvegardes, vous disposez d'une copie de vos données stockée en toute sécurité hors de votre terminal. Les services de sauvegarde suivants sont disponibles, ils vous permettent de stocker vos données à un emplacement sûr. Ainsi, vous pouvez recharger vos information sur le terminal :
- {{site.data.keyword.backup_notm}} est un système de sauvegarde automatisé s'appuyant sur les agents. Il s'agit d'une solution simple et transparente de gestion de votre terminal. Elle est compatible avec les logiciels Microsoft, tels Exchange et SQL, via des plug-in supplémentaires. Les utilisateurs {{site.data.keyword.backup_notm}} interagissent avec ce service via l'application Web WebCC d'{{site.data.keyword.backup_notm}}. Pour plus d'informations, voir [Initiation aux services {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).
- R1Soft Continuous Data Protection est un logiciel de sauvegarde qui peut être installé sur votre serveur ou sur une machine virtuelle auto-gérée. Il est recommandé d'utiliser ce logiciel si vous souhaitez avoir une seule interface pour gérer toutes vos sauvegardes. Vous interagissez avec R1Soft CDP via votre système de gestion propriétaire, qui permet l'installation des agents sur des machines virtuelles et inclut des plug-in de base de données pour des fonctions supplémentaires. Pour plus d'informations, voir [Initiation aux services {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).

## Etapes suivantes
Une fois que votre serveur virtuel est configuré, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs virtuels](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
