---



copyright:
  years: 1994, 2017
lastupdated: "2017-12-12"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:screen: .screen}
{:tip .tip}
{:table: .aria-labeledby="caption"}

# Augmenter la vitesse de port dans Linux

Les vitesses de port par défaut des serveurs client est de 10 Mbits/s pour les réseaux publics comme pour les réseaux privés. Si vous souhaitez augmenter vos vitesses de port à 100 Mbits/s ou à 1000 Mbits/s, ouvrez un ticket auprès de notre département des ventes. Celui-ci vous demandera d'approuver les frais mensuels et un technicien changera les limites de la vitesse de port sur le réseau.

Ces commandes affectent la connectivité de votre serveur. Gérez toujours les connexions réseau en vous connectant d'abord à l'adresse IP sur laquelle vous ne travaillez pas.
{:tip}

Vous pouvez vérifier la vitesse actuelle de votre connexion à l'aide des commandes suivantes :

    ```
    # ethtool eth#   (eth1 pour public, eth0 pour privé)
    ```
    {: pre}

La sortie affichera les configurations en cours de cette connexion :

    ```
    root@noc-training-linux [~]# ethtool eth1
    ```
    {: screen}

Paramètres pour eth1 :

        Supported ports: [ MII ]
        Supported link modes:   10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        Supports auto-negotiation: Yes
        Advertised link modes:  10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        Advertised auto-negotiation: Yes
        Speed: 100Mb/s
        Duplex: Full
        Port: MII
        PHYAD: 3
        Transceiver: external
        Auto-negotiation: on
        Supports Wake-on: g
        Wake-on: d
        Link detected: yes
        root@noc-training-linux [~]#

Pour modifier la vitesse, éditez le fichier suivant à l'aide de l'éditeur de texte de votre choix :

    /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 pour public, ifcfg-eth0 pour privé)

Vous trouverez la ligne suivante :

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

Cela permet de forcer la négociation automatique, la vitesse et le mode duplex à l'armorçage et de garder ainsi une configuration cohérente lors d'un redémarrage.
La vitesse peut être modifiée pour correspondre à la vitesse de votre nouveau port. Un redémarrage du réseau est nécessaire pour que la nouvelle vitesse soit utilisée.

Toutes les connexions forcées à 1000 Mbits/s doivent avoir la fonction autoneg activée dans le fichier ifcfg-eth#.
{: tip}
