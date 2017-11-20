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

# Mise à disposition de sélections
Vous devez effectuer les sélections suivantes lorsque vous mettez à disposition un serveur virtuel public.

## Emplacement
Vous pouvez sélectionner le centre de données spécifique dans lequel effectuer le déploiement. Pour les nouveaux déploiement, {{site.data.keyword.Bluemix}} identifie automatiquement le meilleur pod (en fonction de la disponibilité) et crée les réseaux locaux virtuels (VLAN) publics et privés. Outre les environnements existants, vous pouvez sélectionner le pod spécifique, le réseau local virtuel et le sous-réseau dont vous avez besoin.

## Processeurs / Mémoire RAM
Lors de la commande, vous pouvez effectuer une sélection parmi des options de processeur de coeur. Ces options suivent les normes s'appliquant aux déploiements de serveur virtuel. Chaque coeur physique du serveur comporte plusieurs unités d'exécution et se présente sous la forme de deux unités virtuelles (vCPU) ou coeurs. L'offre de serveur virtuel propose au moins 2,0 GHz par coeur et jusqu'à 56 coeurs disponibles sur un serveur virtuel.

L'utilisation de la mémoire RAM est extrêmement directe. L'offre dédie entièrement la quantité de mémoire RAM sélectionnée à votre serveur virtuel (jusqu'à 242 Go sur un seul serveur virtuel).

**Remarque :** Les instances publiques et dédiées ont des valeurs de configuration maximales légèrement différentes. Des allocations très élevées de coeur ou de mémoire limitent les options disponibles.

## Système d'exploitation

Vous sélectionnez également le système d'exploitation à déployer sur le serveur. Vous pouvez sélectionner certaines options gratuites, telles CentOS et Ubuntu. Certains systèmes payants, tels Windows Server et Red Hat Enterprise Linux (RHEL), sont également disponibles. Gardez à l'esprit que vous devez disposer d'un disque principal de 100 Go pour les systèmes Windows.

Pour les clients existants, vous pouvez également effectuer le déploiement à partir d'un modèle d'image via le portail {{site.data.keyword.slportal_full}} en sélectionnant **Equipements -> Gérer -> Images**, puis **Commander un serveur virtuel**  dans le menu *Actions*.  Le système d'exploitation approprié est alors automatiquement sélectionné pour la commande.  Vous pouvez également effectuer une commande d'après une image standard puis effectuer un rechargement dans un modèle d'image à tout moment.

## Stockage

Vous pouvez choisir le réseau SAN ou le stockage local pour chaque serveur virtuel. Vous pouvez ensuite utiliser d'autres produits de stockage en complément, si nécessaire. SAN et le stockage local sont exposés sur le serveur virtuel en tant que disques locaux. Toute modification apportée aux disques, telle la connexion, la déconnexion, la migration, exige une réinitialisation du serveur virtuel. Pour plus d'informations, voir [Options de stockage](../vsi/storage/vsi_about_storage.html).

## Facturation horaire et mensuelle

Vous pouvez sélectionner la facturation horaire ou mensuelle pour un serveur virtuel. La principale différence (outre le coût) réside dans le fait qu'aucune allocation de bande passante n'est incluse pour les serveurs facturés à l'heure. A la fin d'une période de facturation, l'utilisation de la bande passante et le nombre d'heures pendant lesquelles chaque serveur a été actif sur le compte sont calculés. Le nombre total d'éléments en cours d'exécution est disponible dans le portail {{site.data.keyword.slportal}} sous la page Affichage de serveur de virtuel avec un lien vers une page Détails, présentant les lignes d'article, le nombre d'heures et les frais appliqués par élément.

## Bande passante

L'offre inclut 250 Go avec des serveurs virtuels mensuels ayant une liaison montante publique. Vous pouvez acheter des allocations plus importantes à un coût réduit.

## Vitesse de port

Vous pouvez sélectionner la vitesse de liaison montante pour le serveur virtuel, jusqu'à 1 Go/s. Ces liaisons montantes virtuelles dépendent de liaisons montantes physiques redondantes vers les réseaux dédiés et publics IBM. La vitesse dédiée et publique est toujours identique lors de la commande, avec la possibilité de mettre à niveau ou de rétrograder une liaison, si nécessaire.

## Logiciel

Vous pouvez sélectionner le logiciel à installer par {{site.data.keyword.Bluemix_notm}} lors du processus de mise à disposition. {{site.data.keyword.Bluemix_notm}} prend en charge tout logiciel déployé lors de la mise à disposition. Vous pouvez également installer votre propre logiciel une fois le serveur déployé.

## Sécurité

Avant le déploiement, définissez vos options de sécurité. Dans le cadre du processus de commande, vous pouvez sélectionner un pare-feu matériel ou logiciel spécifique au terminal afin d'assurer votre protection. Vous pouvez également déployer des dispositifs de pare-feu dédiés et déployer le serveur virtuel sur un réseau VLAN protégé. 

**Remarque :** Un serveur virtuel ne peut pas être protégé par deux dispositifs de pare-feu sur la même interface. 

Vous pouvez également utiliser des groupes de sécurité pour promulguer un ensemble de règles de filtre d'adresse IP qui définissent comment gérer le trafic entrant et sortant entre les interfaces publiques et privées d'une instance de serveur virtuel.

Pour plus d'informations, voir [Pare-feu](vsi_security_options.html) et [Initiation aux groupes de sécurité](/docs/infrastructure/security-groups/sg_index.html).

## Surveillance

Pour le serveur virtuel, vous pouvez effectuer une sélection parmi différentes options de surveillance. Les options incluent la surveillance standard, qui utilise la fonction ping ainsi que la réponse de service TCP et comporte des réponses facultatives pour les défaillances. Vous pouvez également ajouter la surveillance avancée qui utilise l'agent logiciel Nimsoft offrant un ensemble de fonctions étendues pour la surveillance du serveur virtuel et du logiciel installé.

Pour plus d'informations, voir [Affichage et gestion des moniteurs](vsi_viewing_monitors.html).

## Sauvegarde

Lors de la commande, vous pouvez ajouter des sauvegardes Evault. Vous pouvez également choisir d'acheter une licence R1soft pour votre environnement de sauvegarde R1soft existant ou utiliser une solution de sauvegarde tierce.

Pour plus d'informations, voir [Re-registering your device with eVault ![External link icon](../icons/launch-glyph.svg "External link icon")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.

## Scripts postérieurs à la mise à disposition

Les scripts postérieurs à la mise à disposition peuvent être associés à toute commande de serveur virtuel. Un script développé par un client s'exécute après les autres tâches de mise à disposition. Les scripts sont généralement utilisés pour appliquer à un serveur une configuration spécifique à un client et pour faciliter l'automatisation de la mise à l'échelle.

Pour plus d'informations, voir [Ajout d'un script de mise à disposition personnalisé](vsi_add_script.html).

## Etape suivante
Lorsque vous êtes prêt à mettre à disposition votre serveur virtuel public, voir [Mise à disposition d'instances publiques](vsi_provision_public.html).
