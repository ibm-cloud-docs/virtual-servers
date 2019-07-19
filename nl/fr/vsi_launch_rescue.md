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
{:table: .aria-labeledby="caption"}


# Lancement de Rescue Kernel
{: #launching-rescue}

Rescue Kernel est un environnement de secours actif conçu pour vous permettre de mettre en ligne un serveur Bare Metal ou un serveur virtuel en vue de résoudre les problèmes système qui seraient normalement résolus uniquement via le rechargement du système d'exploitation. Rescue Kernel doit être lancé dans la console {{site.data.keyword.cloud}}. Procédez comme suit pour lancer Rescue Kernel pour une unité.
{:shortdesc}

## Avant de commencer
Tout d'abord, accédez au menu Unité et assurez-vous de disposer des droits de compte appropriés pour exécuter les tâches.

* Accédez au menu Unité de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des droits de compte et accès aux unités requis. Seul le propriétaire de compte ou un utilisateur disposant de droit d'infrastructure classique **Gérer les utilisateurs** peut modifier les droits.

Pour plus d'informations sur les droits, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux unités](/docs/vsi?topic=virtual-servers-managing-device-access).

## Lancement de Rescue Kernel

1. Dans le menu **Unités**, sélectionnez **Liste des unités**.
2. Dans la **Liste des unités**, cliquez sur le nom de l'unité à récupérer.
3. Dans le menu *Actions*, sélectionnez **Mode récupération**.
4. Cliquez sur **Oui** pour que votre terminal passe en mode Rescue Kernel immédiatement. 

## Lancement de Rescue Kernel pour une instance Windows

1. Dans le menu **Unités**, sélectionnez **Liste des unités**.
2. Dans la **Liste des unités**, cliquez sur le nom de l'unité à récupérer.
3. Dans le menu *Actions*, sélectionnez **Initialiser à partir d'une image**.
4. Sélectionnez **Initialiser à partir de cette image** en regard de l'image publique, *WindowsRescueStandalone.iso*.

## Etapes suivantes
Après le lancement de Rescue Kernel, l'unité est mise hors tension et est réamorcée dans Rescue Kernel pour le système d'exploitation de l'unité. Cette opération peut durer plusieurs minutes.

L'accès distant à l'unité est disponible à partir de l'adresse IP de cette dernière. Vous pouvez accéder à l'unité dans Rescue Kernel en utilisant les données d'identification root ou de l'administrateur pour les unités enregistrées dans la console {{site.data.keyword.cloud_notm}}. Lors de l'utilisation de Rescue Kernel, vous pouvez détecter les problèmes et les résoudre comme vous le feriez sur une unité amorcée normalement. Si nécessaire, vous pouvez monter les unités dans le système d'exploitation de Rescue Kernel. Pour quitter Rescue Kernel et faire en sorte que votre unité fonctionne dans son environnement habituel, réamorcez l'unité dans la console {{site.data.keyword.cloud_notm}} ou à partir du système d'exploitation de Rescue Kernel.

Pour plus d'informations sur le réamorçage d'une unité, voir [Gestion des serveurs virtuels](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
