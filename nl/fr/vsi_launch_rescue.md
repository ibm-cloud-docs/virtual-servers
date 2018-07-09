---



copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Lancement d'un noyau de secours 
{: #launching-rescue}

Le noyau de secours est un environnement de secours actif, conçu pour permettre aux clients de mettre en ligne un serveur Bare Metal ou un serveur virtuel en vue de résoudre les problèmes système qui seraient normalement résolus uniquement via le rechargement du système d'exploitation. Le noyau de secours doit être lancé sur le portail {{site.data.keyword.slportal_full}}. Procédez comme suit pour lancer le noyau de secours pour un terminal.
{:shortdesc}

## Lancement du noyau de secours

1. Accédez au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) en utilisant vos données d'identification uniques.
2. Dans la Liste des unités, cliquez sur le nom de l'élément à récupérer.
3. Cliquez sur la liste déroulante *Actions* dans le coin supérieur droit puis sélectionnez **Mode sans échec**. (Sinon, vous pouvez aussi cliquer sur l'onglet *Gestion à distance* et sélectionnez **Mode sans échec**.)
4. Cliquez sur le bouton **Oui** pour que votre terminal passe en mode Noyau de secours immédiatement. Cliquez sur le bouton **Non** pour annuler l'action.

## Sous Windows VSI

1. Accédez au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) en utilisant vos données d'identification uniques.
2. Dans la Liste des unités, cliquez sur le nom de l'élément à récupérer.
3. Cliquez sur la liste déroulante *Actions* dans l'angle supérieur droit et sélectionnez l'option d'**initialisation à partir de l'image**.
4. Sélectionnez **Initialiser À Partir De Cette Image** en regard de l'image publique, *WindowsRescueStandalone.iso*.


## Etapes suivantes
Après le lancement du noyau de secours, le terminal est mis hors tension et est réamorcé dans le noyau de secours pour le système d'exploitation du terminal. Cette opération peut durer plusieurs minutes.

L'accès distant au terminal est disponible à partir de l'adresse IP de ce dernier. Vous pouvez accéder au terminal dans le noyau de secours en utilisant les données d'identification root ou de l'administrateur pour les terminaux enregistrés sur le portail {{site.data.keyword.slportal}}. Lors de l'utilisation du noyau de secours, vous pouvez détecter les problèmes et les résoudre comme vous le feriez sur un terminal normalement amorcé. Si nécessaire, vous pouvez monter les terminaux dans le système d'exploitation du noyau de secours. Pour quitter ce dernier et faire en sorte que votre terminal fonctionne dans son environnement habituel, réamorcez le terminal dans le portail {{site.data.keyword.slportal}} ou à partir du système d'exploitation de noyau de secours.

Pour plus d'informations sur le réamorçage d'un terminal, voir [Gestion des serveurs virtuels](../vsi/vsi_managing.html).

