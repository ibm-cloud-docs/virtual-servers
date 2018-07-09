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
{:table: .aria-labeledby="caption"}

# Augmentation de la vitesse de port dans Windows

La vitesse de port par défaut pour les serveurs client est de 10 Mbits/s (pour les réseaux publics comme pour les réseaux privés). Si vous souhaitez augmenter vos vitesses de port à 100 Mbits/s ou 1000 Mbits/s, ouvrez un ticket et formulez une demande. Le département des ventes vous demandera d'approuver les frais minimaux et un technicien changera les vitesses de port sur votre réseau.

Une fois la mise à jour effectuée du côté du réseau, codez les interfaces réseau pertinentes sur votre serveur.

Suivez les étapes suivantes pour forcer la vitesse de port sur un serveur Windows. **Remarque :** connectez-vous toujours à votre serveur sur le réseau sur lequel vous ne travaillez PAS afin d'éviter de bloquer votre accès au serveur.

1. Sélectionnez **Démarrer > Panneau de configuration > Connexions réseau**.
2. Cliquez sur la connexion réseau que vous tentez de mettre à niveau/rétromigrer.
  * Pour les mises à niveau de port public, sélectionnez **Connexion au réseau local 2** OU **FrontEnd**.
  * Pour les mises à niveau de port privé, sélectionnez **Connexion au réseau local** OU **BackEnd**.
3. Dans la fenêtre Etat de la connexion, vérifiez que la carte réseau sélectionnée est le port que vous souhaitez mettre à jour.
4. Sélectionnez l'onglet Support (notez l'adresse IP) :
  * En cas de mise à niveau d'un port public, l'adresse IP doit être une adresse IP publique.
  * En cas de mise à niveau d'un port privé, l'adresse IP doit être une adresse au format 10.x.x.x.
5. Si les adresses IP ne correspondent pas, répétez les étapes 1 à 3 pour l'autre connexion réseau.

## Etat du réseau local

Sélectionnez l'onglet **Général** à nouveau, puis sélectionnez **Properties.** Une nouvelle fenêtre s'affiche.

Sur l'onglet **Général** de la fenêtre **Propriétés de connexion**, sélectionnez **Configurer**. La fenêtre Propriétés du pilote s'affiche.

1. Sélectionnez l'onglet **Avancé**.
2. Sélectionnez **Vitesse de liaison&duplex** dans la liste des propriétés.
3. Sélectionnez l'onglet **Valeur** à droite et définissez la vitesse de port que vous augmentez à duplex intégral :
  1. Pour 10 Mbits/s, sélectionnez 10Mbps/Full
  2. Pour 100 Mbits/s, sélectionnez 100Mbps/Full
  3. Pour 1000 Mbits/s, sélectionnez Auto
4. Cliquez sur OK.  

Le serveur démarrera alors immédiatement avec la nouvelle vitesse, et il est possible que vous soyez brièvement déconnecté lors de la renégociation du lien.
