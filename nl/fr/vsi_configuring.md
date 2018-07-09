---



copyright:
  years: 2017, 2018
lastupdated: "2018-03-19"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Configuration des serveurs virtuels
{: #configuring-virtual-servers}

Une fois que vous avez accès à votre serveur virtuel, vérifiez que vous l'avez configuré en prenant en compte les besoins de votre environnement.
{:shortdesc}

## Connexion 
Connectez-vous au portail [{{site.data.keyword.slportal_full}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant les données d'identification que vous avez reçues dans un message électronique lors de la création de votre compte.

## Recherche de votre serveur virtuel
Recherchez votre serveur virtuel dans la liste de terminaux du portail {{site.data.keyword.slportal}}. A partir de cette liste, vous pouvez gérer et mettre à niveau des terminaux ou générer des graphiques d'utilisation de bande passante. Pour plus d'informations, voir [Gestion des serveurs virtuels](../vsi/vsi_managing.html).

## Enregistrement des adresses IP et des données d'identification
Conservez un journal des adresses IP et des données d'identification du serveur à un emplacement sûr afin que vous puissiez accéder rapidement à ces données sans vous connecter au portail {{site.data.keyword.slportal}}. 
- Les adresses IP des terminaux sont disponibles dans la liste des terminaux.
- Les mots de passe des terminaux sont disponibles dans la vue d'instantané du terminal. Cliquez sur la flèche en regard du nom du terminal pour développer la vue.
- Vous pouvez afficher les adresses IP des terminaux en sélectionnant l'option Télécharger CSV dans la Liste des unités. Sélectionnez cette option à partir de Paramètres pour télécharger une liste complète des terminaux ainsi que des informations détaillées au format tableur.

## Mise à jour des données d'identification des logiciels
Des données d'identification temporaires sont affectées à tous les logiciels chargés sur le terminal lors du processus de mise à disposition. Vous pouvez consulter et gérer ces données d'identification sur l'onglet Mots de passe de chaque terminal dans le portail {{site.data.keyword.slportal}}. Utilisez ces données d'identification temporaires lors du premier accès au logiciel. Il est recommandé ensuite de changer le mot de passe. Utilisez un mot de passe fiable composé de lettres, de chiffres et de symboles.

Vous pouvez, si vous le souhaitez, stocker les mises à jour de mot de passe sur l'onglet Mots de passe de chaque terminal. Toutefois, gardez à l'esprit que lorsque vous stockez des mots de passe dans le portail, {{site.data.keyword.slportal}}, toutes les personnes ayant accès au compte et disposant des droits appropriés peuvent voir les mots de passe stockés sur l'écran Mots de passe.

Pour obtenir des informations supplémentaires sur l'affichage et la gestion des données d'identification de vos logiciels, voir [Managing infrastructure access](../iam/mnginfra.html).

## Accès à votre serveur sur le réseau privé
Le réseau privé constitue le point d'entrée pour l'interaction avec vos terminaux via le bureau distant (RDP) utilisant SSH et KVM over IP. L'outil d'accès au VPN permet une connexion de réseau privé au noeud final VPN SSL le plus proche ou au noeud final de votre choix. L'accès VPN est également requis pour l'interaction avec plusieurs services. Pour plus d'informations, voir [Getting started with Virtual Private Networking (VPN)](../infrastructure/iaas-vpn/getting-started.html).

## Configuration de la surveillance
La surveillance permet principalement de vérifier la disponibilité de votre serveur mais elle vous permet également de savoir quand effectuer la mise à l'échelle. Les services de surveillance standard et de surveillance Nimsoft permettent de répondre aux différents besoins de surveillance. La surveillance standard, également appelée “Surveillance de base”, est généralement utilisée avec la méthode ping-et-réponse via une commande ping de service ou ping lente lancée à partir du portail {{site.data.keyword.slportal}}. La surveillance Nimsoft est également appelée “Surveillance avancée” et comporte trois niveaux : De base, Avancé et Premium. Ce service est également accessible via le portail {{site.data.keyword.slportal}}. Pour plus d'informations, voir [Surveillance](../infrastructure/SLmonitoring/monitoring_index.html).

## Sécurisation de votre système
Des pare-feu matériels permettant de sécuriser votre terminal sont disponibles. Ils sont mis à disposition à la demande sans aucune interruption du fonctionnement. Si les règles sont établies correctement, un pare-feu permet de protéger votre serveur d'activités non souhaitées. Une fois que vous avez commandé un pare-feu, il doit être activé et les règles doivent être définies.

Pour plus d'informations, veuillez consulter les rubriques suivantes relatives à la sécurité.

* [Pare-feu matériels (partagés)](../infrastructure/hardware-firewall-shared/getting-started.html)
* [Pare-feu matériels (dédiés)](../infrastructure/hardware-firewall-dedicated/getting-started.html)

Les groupes de sécurité permettent également de limiter le trafic réseau sur vos serveurs virtuels. Vous pouvez utiliser des groupes de sécurité pour promulguer un ensemble de règles de filtre d'adresse IP qui définissent comment gérer le trafic entrant et sortant entre les interfaces publiques et privées d'une instance de serveur virtuel. Pour plus d'informations, voir [Initiation aux groupes de sécurité](/docs/infrastructure/security-groups/sg_index.html).

## Planification des sauvegardes 
Grâce aux sauvegardes, vous disposez d'une copie de vos données stockée en toute sécurité hors de votre terminal. Les services de sauvegarde suivants sont disponibles, ils vous permettent de stocker vos données à un emplacement sûr. Ainsi, vous pouvez recharger vos information sur le terminal :
- La sauvegarde EVault est un système de sauvegarde automatisé utilisant les agents. Il s'agit d'une solution simple et transparente de gestion de votre terminal. Elle est compatible avec les logiciels Microsoft, tels Exchange et SQL, via des plug-in supplémentaires. Les utilisateurs EVault interagissent avec ce service via l'application Web WebCC d'EVault. Pour plus d'informations, voir [Getting Started with Backup Services](../infrastructure/Backup/index.html).
- R1Soft Continuous Data Protection est un logiciel de sauvegarde qui peut être installé sur votre serveur ou sur une machine virtuelle auto-gérée. Il est recommandé d'utiliser ce logiciel si vous souhaitez avoir une seule interface pour gérer toutes vos sauvegardes. Vous interagissez avec R1Soft CDP via votre système de gestion propriétaire, qui permet l'installation des agents sur des machines virtuelles et inclut des plug-in de base de données pour des fonctions supplémentaires. Pour plus d'informations, voir [Getting Started with Backup Services](../infrastructure/Backup/index.html).

## Etapes suivantes
Une fois que votre serveur virtuel est configuré, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs virtuels](../vsi/vsi_managing.html).



