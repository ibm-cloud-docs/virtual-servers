---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Services de sauvegarde
{: #back-up-services}

## IBM Cloud Backup

{{site.data.keyword.backup_full}} est un système de sauvegarde automatisé s'appuyant sur les agents et géré via l'utilitaire de gestion sur navigateur WebCC d'{{site.data.keyword.backup_notm}} permettant aux utilisateurs de sauvegarder des données entre différents serveurs dans un ou plusieurs centres de données sur le réseau {{site.data.keyword.BluSoftlayer}}. Les administrateurs peuvent faire en sorte que des sauvegardes soient effectuées toutes les heures, tous les jours, toutes les semaines ou définir des sauvegardes personnalisées qui ciblent des systèmes complets, des répertoires spécifiques ou même des fichiers individuels. Des plug-in supplémentaires permettent la compatibilité avec des logiciels, tels Microsoft Exchange et Microsoft SQL, ainsi qu'avec d'autres types de logiciels tiers. Ils permettent également aux utilisateurs d'effectuer une restauration physique ou Bare Metal, lorsque cela est nécessaire.

Pour plus d'informations sur les services {{site.data.keyword.backup_notm}}, voir [Initiation aux services {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-gettingstarted#gettingstarted).

## R1Soft CDP

CDP (protection des données en continu) est un logiciel de sauvegarde aux performances élevées créé par R1Soft qui permet la sauvegarde des terminaux physiques et des terminaux virtuels. Idera CDP se compose de trois composants principaux : serveur CDP, agent et plug-in de base de données pouvant être achetés séparément dans les deux premiers composants. Etant donné que le service R1Soft CDP est une solution de sauvegarde tierce, les interactions avec CDP ont lieu intégralement hors des interfaces propriétaires {{site.data.keyword.Bluemix_short}}. Il est toutefois nécessaire d'effectuer un suivi des mots de passe R1Soft CDP et de stocker ces derniers dans le portail {{site.data.keyword.slportal}}. Toutes les autres interactions avec R1Soft CDP sont présentées sur le site Web R1Soft.

Pour plus d'informations sur les services de sauvegarde R1Soft, voir la [documentation R1Soft![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://wiki.r1soft.com/display/ServerBackupManager/Home){: new_window}.
