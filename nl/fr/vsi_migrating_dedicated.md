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


# Migration d'une instance d'hôte dédiée vers un autre hôte
{: #migrating-dedicated-host}

Vous pouvez migrer vos instances d'hôte dédiées d'un hôte à un autre dans le même pod. Sélectionnez l'instance à migrer à partir de la page Détails de l'unité de l'hôte ou de l'instance. Seules deux instances peuvent être migrées en même temps et la durée de la migration dépend du disque. La migration des disques SAN est plus rapide car une copie du disque est requise pour les disques locaux. Les instances sont hors ligne lors de leur migration. L'hôte reste actif pour n'importe laquelle de ses instances d'hôte dédiées.
{:shortdesc}

Procédez comme suit pour migrer les instances d'hôte dédiées vers un autre hôte dédié dans le même pod à partir de la page Détails de l'unité de l'*hôte dédié d'origine*.

1. Accédez au portail [{{site.data.keyword.slportal_full}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) en utilisant vos données d'identification uniques.
2. Cliquez sur **Appareil >Liste des unités** puis dans la liste, sélectionnez soit l'hôte, soit l'instance hébergée.
3. Cliquez sur la liste déroulante **Actions** en regard de l'instance dédiée à migrer.
4. Sélectionnez **Migrer** et indiquez l'hôte vers lequel l'instance doit être migrée. N'oubliez pas que l'hôte cible doit se trouver dans le même pod que l'hôte d'origine.
5. Cliquez sur le bouton **Migrer**.

La migration commence immédiatement. Lors de la migration, l'instance dédiée est hors ligne tant qu'elle n'est pas sur le nouvel hôte. Vous pouvez afficher la page Détails de l'unité de l'hôte cible afin de vous assurer que la migration de l'instance s'est effectuée correctement.

Procédez comme suit pour migrer les instances d'hôte dédiées vers un autre hôte dédié dans le même pod à partir de la page Détails de l'*instance d'hôte dédiée*.

1. Accédez au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) en utilisant vos données d'identification uniques.
2. Cliquez sur **Appareil >Liste des unités** puis dans la liste, sélectionnez l'instance hébergée à migrer.
3. Cliquez sur le lien **Migrer** sur le côté droit de la page.
4. Sélectionnez l'hôte cible vers lequel migrer l'instance. N'oubliez pas que l'hôte cible doit se trouver dans le même pod que l'hôte d'origine.
5. Cliquez sur le bouton **Migrer**.

La migration commence immédiatement. Lors de la migration, l'instance dédiée est hors ligne tant qu'elle n'est pas sur le nouvel hôte. Vous pouvez afficher la page Détails de l'unité de l'hôte cible afin de vous assurer que la migration de l'instance s'est effectuée correctement.

## Etapes suivantes
Une fois que vous avez migré une instance d'hôte dédiée, assurez-vous que la migration a abouti en vérifiant que son statut est vert sur la page Détails de l'unité du nouvel hôte dédié.
