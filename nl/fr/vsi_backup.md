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

# Services de sauvegarde

## Sauvegarde EVault

La sauvegarde EVault est un système de sauvegarde s'appuyant sur les agents et géré via l'utilitaire de gestion sur navigateur WebCC d'EVault permettant aux utilisateurs de sauvegarder des données entre différents serveurs dans un ou plusieurs centres de données sur le réseau {{site.data.keyword.BluSoftlayer_full}}.  Les administrateurs peuvent faire en sorte que des sauvegardes soient effectuées toutes les heures, tous les jours, toutes les semaines ou définir des sauvegardes personnalisées qui ciblent des systèmes complets, des répertoires spécifiques ou même des fichiers individuels.  Des plug-in supplémentaires permettent la compatibilité avec des logiciels, tels Microsoft Exchange et Microsoft SQL, ainsi qu'avec d'autres types de logiciels tiers. Ils permettent également aux utilisateurs d'effectuer une restauration physique ou Bare Metal, lorsque cela est nécessaire.

Pour plus d'informations sur les services de sauvegarde eVault, voir [Initiation aux services de sauvegarde](../infrastructure/Backup/index.html){: new_window}.

## R1Soft CDP

CDP (protection des données en continu) est un logiciel de sauvegarde aux performances élevées créé par R1Soft qui permet la sauvegarde des terminaux physiques et des terminaux virtuels. Idera CDP se compose de trois composants principaux : serveur CDP, agent et plug-in de base de données pouvant être achetés séparément dans les deux premiers composants.  Etant donné que le service R1Soft CDP est une solution de sauvegarde tierce, les interactions avec CDP ont lieu intégralement hors des interfaces propriétaires {{site.data.keyword.Bluemix_short}}. Il est toutefois nécessaire d'effectuer un suivi des mots de passe R1Soft CDP et de stocker ces derniers dans le portail {{site.data.keyword.slportal_full}}.  Toutes les autres interactions avec R1Soft CDP sont présentées sur le site Web R1Soft.

Pour plus d'informations sur les services de sauvegarde R1Soft, voir [Initiation aux services de sauvegarde](../infrastructure/Backup/index.html){: new_window}.
