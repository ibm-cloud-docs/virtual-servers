---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Migration d'une instance d'hôte dédiée vers un autre hôte
{: #migrating-dedicated-host}

Vous pouvez migrer vos instances d'hôte dédiées d'un hôte à un autre dans le même pod. Sélectionnez l'instance à migrer à partir de la page des détails de l'unité de l'hôte ou de l'instance. Seules deux instances peuvent être migrées en même temps et la durée de la migration dépend du disque. La migration des disques SAN est plus rapide car une copie du disque est requise pour les disques locaux. Les instances sont hors ligne lors de leur migration. L'hôte reste actif pour n'importe laquelle de ses instances d'hôte dédiées.
{:shortdesc}

## Avant de commencer
Tout d'abord, accédez au menu Unité et assurez-vous de disposer des droits de compte appropriés pour exécuter les tâches.

* Accédez au menu Unité de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des droits de compte et accès aux unités requis. Seul le propriétaire de compte ou un utilisateur disposant de droit d'infrastructure classique **Gérer les utilisateurs** peut modifier les droits.

Pour plus d'informations sur les droits, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux unités](/docs/vsi?topic=virtual-servers-managing-device-access).

## Migration à partir de l'hôte dédié 
Procédez comme suit pour migrer les instances d'hôte dédiées vers un autre hôte dédié dans le même pod à partir de la page de détails de l'unité de l'*hôte dédié d'origine*. 

1. Dans le menu **Unités**, sélectionnez **Liste des unités**.
2. Dans la liste, sélectionnez soit l'hôte, soit l'instance hébergée.
3. Cliquez sur la liste déroulante **Actions** en regard de l'instance dédiée à migrer.
4. Sélectionnez **Migrer** et indiquez l'hôte vers lequel l'instance doit être migrée. N'oubliez pas que l'hôte cible doit se trouver dans le même pod que l'hôte d'origine.
5. Cliquez sur **Migrer** pour lancer la migration. 

La migration commence immédiatement. Lors de la migration, l'instance dédiée est hors ligne tant qu'elle n'est pas sur le nouvel hôte. Vous pouvez afficher la page Détails de l'unité de l'hôte cible afin de vous assurer que la migration de l'instance s'est effectuée correctement.

## Migration à partir de l'instance dédié 
Procédez comme suit pour migrer les instances d'hôte dédiées vers un autre hôte dédié dans le même pod à partir de la page de détails de l'*instance d'hôte dédiée*.

1. Dans le menu **Unités**, sélectionnez **Liste des unités**.
2. Dans la liste, sélectionnez l'instance hébergée à migrer.
3. Cliquez sur **Migrer**.
4. Sélectionnez l'hôte cible vers lequel migrer l'instance. N'oubliez pas que l'hôte cible doit se trouver dans le même pod que l'hôte d'origine.
5. Cliquez sur **Migrer** pour lancer la migration.

La migration commence immédiatement. Lors de la migration, l'instance dédiée est hors ligne tant qu'elle n'est pas sur le nouvel hôte. Vous pouvez afficher la page de détails de l'unité de l'hôte cible afin de vous assurer que la migration de l'instance s'est effectuée correctement.

## Etapes suivantes
Une fois que vous avez migré une instance d'hôte dédiée, assurez-vous que la migration a abouti en vérifiant que son statut est vert sur la page de détails de l'unité du nouvel hôte dédié.

