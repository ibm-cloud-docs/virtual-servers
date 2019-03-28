---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Gestion des instances et des hôtes dédiés
{: #managing-dedicated-hosts-instances}

Sur la page Détails de l'unité, vous pouvez gérer vos instances et vos hôtes dédiés, suivre vos tickets de support et surveiller la disponibilité de votre hôte. Vous pouvez accéder à vos instances d'hôte dédiées et les consulter de deux manières dans la liste des unités, soit comme partie de l'hôte, soit en tant qu'instance individuelle.
{:shortdesc}

## Onglet de configuration de l'hôte
Vous pouvez effectuer plusieurs tâches à partir de l'onglet **Configuration** pour l'hôte dédié, notamment la gestion de vos instances d'hôte dédiées. Sous le menu déroulant Actions, vous pouvez renommer l'hôte ou l'annuler. Toutes les instances d'hôte dédiées affectées doivent être annulées ou migrées pour qu'un hôte puisse être annulé. Sinon, un message d'erreur s'affiche.

Il est possible de conserver des remarques sur l'hôte et ses instances, par exemple, la migration entre myDallasHost et myTorHost est planifiée le XX/XX/XXXX. Les cadres Général, Système et Réseau de la page permettent d'avoir en un seul coup d'oeil accès aux détails de l'hôte. Le cadre Stockage inclut des informations sur la capacité de stockage local.

Le cadre Instances contient les instances affectées à un hôte spécifique. Vous pouvez également y ajouter des instances à l'hôte. Cliquez sur le menu Actions pour effectuer une des actions suivantes pour une instance :

* Réamorçage
* Mise sous tension et hors tension
* Attribution d'un nouveau nom
*	Affichage des journaux d'audit
*	Mise à niveau ou rétromigration
*	Annulation
*	Migration

## Onglet des tickets de l'hôte
L'onglet Tickets permet d'ouvrir des tickets pour l'hôte et ses instances. Pour cela, cliquez sur le lien Ajouter un ticket pour cette unité.

## Onglet des allocations de l'hôte
L'onglet Allocations inclut les coeurs, la mémoire RAM et le stockage local disponibles pour votre hôte dédié. La tranche bleue du graphique circulaire représente les éléments utilisés et la tranche blanche les éléments disponibles.

## Onglet de l'instance d'hôte dédiée
La page Détails de l'unité de l'instance d'hôte dédiée est disponible via la page Détails de l'unité de son hôte ou directement à partir de la liste des unités. Des onglets supplémentaires sont disponibles au niveau de l'instance d'hôte dédiée. Configuration et Tickets sont similaires aux onglets disponibles au niveau de l'hôte. Le lien Modifier la configuration de l'unité sur l'onglet Configuration vous permet de modifier la configuration du système (coeur, mémoire RAM et stockage local) ainsi que du réseau (bande passante et vitesses de port de liaison montante).

Le graphique temporel Utilisation présente l'utilisation de l'unité centrale par date. Vous pouvez parcourir le graphique pour voir l'utilisation de l'unité centrale pour une date et heure spécifique, ce qui est utile lorsque vous tentez de déterminer si vous avez besoin d'ajouter de la capacité de traitement.

Le graphique temporel Bande passante, quant à lui, vous permet d'entrer des paramètres pour voir la quantité de bande passante utilisée au fil du temps. L'onglet Stockage affiche tout stockage de fichier ou de bloc supplémentaire sur l'instance.

## Annulation d'un hôte dédié
Vous pouvez annuler un hôte dédié à tout moment. Avant d'annuler un hôte, vous devez avoir migré les instances dédiées qui lui sont affectées vers un autre hôte dédié ou avoir annulé ces instances.
### Annulation d'un hôte dédié à partir de la liste des unités
Procédez comme suit pour annuler un hôte dédié à partir de la liste des unités.

1. Sélectionnez **Appareil** > **Liste des unités**.
2. Recherchez l'hôte dédié à annuler puis cliquez sur le menu déroulant **Actions**.
3. Sélectionnez **Annuler l'hôte**.
4. Une fenêtre en incrustation contenant la liste des instances dédiées affectées à l'hôte s'affiche. Vous devez alors migrer ou annuler les instances avant d'annuler l'hôte. Cliquez sur **OK**.

Un message s'affiche indiquant que l'hôte dédié est annulé. Il contient un lien vers le ticket de support permettant d'effectuer cette opération.
### Annulez un hôte dédié sur la page Détails de l'unité.
Procédez comme suit pour annuler l'hôte dédié à partir de la page Détails de l'unité.

1. Sélectionnez **Appareil** > **Liste des unités**.
2. Recherchez l'hôte dédié à annuler puis cliquez deux fois dessus.
3. Vérifiez que toutes les instances dédiées affectées à l'hôte migré ont été migrées ou annulées.
4. Cliquez sur le menu déroulant **Actions** puis sélectionnez **Annuler l'hôte**.

Un message s'affiche indiquant que l'hôte dédié est annulé. Il contient un lien vers le ticket de support permettant d'effectuer cette opération.

### Annulation d'une instance dédiée

Avant de pouvoir annuler un hôte dédié, les instances dédiées associées à ce dernier doivent être annulées. Les instances dédiées peuvent être annulées directement à partir de la liste des unités, sur la page Détails de l'unité sur un terminal de l'hôte affecté ou sur leurs propres pages Détails de l'unité.

1. Sélectionnez l'instance dédiée à annuler puis cliquez sur le menu déroulant **Actions**.
2. Sélectionnez **Annuler unité**.
3. Un message d'avertissement s'affiche. Cliquez sur le menu déroulant **Raison**, sélectionnez la raison pour laquelle vous annulez l'instance dédiée puis cliquez sur **Continuer**.

Un message s'affiche vous indiquant que l'instance dédiée est annulée. Il contient un lien vers le ticket de support permettant d'effectuer cette opération.
