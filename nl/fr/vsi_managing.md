---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Gestion des serveurs virtuels
{: #managing-virtual-servers}

Vous pouvez gérer des serveurs virtuels, ainsi que d'autres unités, à partir de la liste des détails de l'unité.
{:shortdesc}


## Avant de commencer
Tout d'abord, accédez au menu Unité et assurez-vous de disposer des droits de compte appropriés pour exécuter les tâches.

* Accédez au menu Unité de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des droits de compte et accès aux unités requis. Seul le propriétaire de compte ou un utilisateur disposant de droit d'infrastructure classique **Gérer les utilisateurs** peut modifier les droits.

Pour plus d'informations sur les droits, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux unités](/docs/vsi?topic=virtual-servers-managing-device-access).

## Types d'unité
La liste des détails d'unité affiche les types d'unité suivants : 

| Unité  | Type d'unité |
| ------  | ------------ | 
| Serveurs virtuels | Virtuel |
| Serveurs Bare Metal | Serveur  |
| Hôtes dédiés | Hôte virtuel dédié  | 
{: caption="Tableau 1. Types d'unité " caption-side="top"}

Les actions que vous voyez dépendent du type d'unité, ainsi que des droits octroyés à votre compte utilisateur.


Procédez comme suit afin d'effectuer les tâches de gestion pour vos serveurs virtuels.

1. Dans le menu **Unités**, sélectionnez **Liste des unités**.
2. Cliquez sur **Actions** pour l'unité à gérer et sélectionnez la tâche souhaitée.

* Vous pouvez interagir avec les serveurs dans la console {{site.data.keyword.cloud_notm}} soit dans la vue d'instantané (récapitulatif de votre unité), soit dans l'écran de détails de l'unité (liste détaillée complète). Pour afficher votre serveur et interagir avec ce dernier dans la vue d'instantané, cliquez sur la flèche en regard du nom de l'unité pour développer la vue. Pour afficher votre serveur et interagir avec ce dernier dans l'écran de détails de l'unité, cliquez sur le nom de l'unité du serveur.

* Vous pouvez ajouter des remarques à une unité à tout moment à partir de l'onglet **Configuration**. Les remarques vous permettent d'identifier des détails sur l'unité, son utilisation et les actions effectuées sur cette dernière.
 {:tip}

## Réamorçage
Le réamorçage est l'une des actions les plus simples réalisées sur une unité. Le réamorçage d'une unité entraîne la mise hors tension immédiate de l'unité, suivie d'une mise sous tension. Il est réalisé pour différentes raisons qui dépendent de l'unité et des besoins professionnels de chaque utilisateur. Les réamorçages d'unités peuvent s'effectuer à partir de la liste des unités ou à partir de l'affichage des unités d'une unité spécifique. Les serveurs virtuels peuvent être réamorcés à tout moment.

Un redémarrage est très utile lorsque vous rencontrez un problème empêchant le serveur de démarrer sur le système d’exploitation en raison d’un problème de configuration. Vous pouvez également effectuer l'amorçage dans Rescue Kernel. Après avoir démarré sur Rescue Kernel, vous pouvez monter le ou les lecteurs de votre serveur, puis résoudre le problème de configuration. Une fois le problème résolu, redémarrez simplement le serveur à partir de la ligne de commande. Le serveur redémarre alors dans le noyau par défaut de votre serveur.
{:tip}

## Sous tension/Hors tension 
Si l'unité a été mise hors tension, elle reste à cet état et doit être mise sous tension manuellement à l'aide de la procédure ci-dessus. Les utilisateurs ne peuvent pas interagir avec une unité lorsque cette dernière est hors tension. Si le serveur virtuel prend en charge la fonction d'interruption de facturation, la facturation est interrompue pour certaines ressources de traitement. Vous ne pouvez pas exécuter toutes les actions de gestion sur une instance tant que la facturation n'a pas repris. Pour plus d'informations, voir [Interruption de facturation](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing). Pour savoir si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation, voir [Affichage de la fonction d'interruption de facturation](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature#viewing-suspend-billing-feature). Si l'unité a été mise sous tension, les utilisateurs peuvent interagir avec elle normalement. Elle reste sous tension jusqu'à ce qu'une action soit effectuée.

## Attribution d'un nouveau nom
Une fois l'unité renommée, le nom est automatiquement mis à jour dans la console {{site.data.keyword.cloud_notm}}. Lorsque vous effectuez une recherche dans la console {{site.data.keyword.cloud_notm}}, utilisez le nouveau nom d'unité pour rechercher le contenu associé. Répétez les étapes précédentes pour renommer l'unité une nouvelle fois.

## Annulation
Si vous annulez une unité, vous mettez fin à son utilisation. Les unités peuvent être annulées immédiatement ou au moment d'un anniversaire de facturation. Une fois l'annulation de votre unité confirmée, l'action ne peut plus être annulée. Aucun remboursement n'est effectué pour les annulations immédiates.

Une fois l'annulation confirmée, le processus d'annulation de l'unité commence. Si une annulation immédiate est demandée, l'unité est annulée immédiatement. Si l'annulation d'une date anniversaire de facturation a été demandée, l'unité reste active jusqu'à la date anniversaire de facturation suivante. Dès son annulation, l'unité disparaît de la liste des unités de la console {{site.data.keyword.cloud_notm}}. Les éléments de facturation sont également retirés des factures lorsque les soldes restants sont payés sur l'unité, le cas échéant. Si vous avez des questions sur la facture d'une unité annulée, ouvrez un ticket et sélectionnez Demande de comptabilité en objet. Aucun remboursement n'est effectué pour les annulations immédiates.

## Etapes suivantes
Si vous avez besoin de configurer à nouveau un serveur virtuel existant, voir [Nouvelle configuration d'un serveur virtuel existant](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).
