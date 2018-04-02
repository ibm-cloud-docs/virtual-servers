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


# Gestion de l'accès aux terminaux
{: #managing-device-access}

Pour accéder aux détails d'un terminal spécifique et gérer ces derniers, votre compte utilisateur doit disposer des droits appropriés.  Une fois que l'administrateur de compte accorde à votre compte utilisateur l'accès à un terminal, vous pouvez afficher les détails du terminal en utilisant le portail {{site.data.keyword.slportal_full}} ou l'API.  Les informations ou l'action que vous voyez dépendent du type de terminal, ainsi que des droits octroyés à votre compte utilisateur.
{:shortdesc}

**Remarque :** Si votre compte a des terminaux pour lesquels l'accès ne vous pas a été accordé, un message "Nom d'unité inconnu" s'affiche lorsque vous tentez d'accéder à ces terminaux.

Vous pouvez affecter un accès au terminal pour les utilisateurs de votre compte mais non pour vous même. Seul un administrateur de compte peut accéder à tous les terminaux du compte client et peut définir l'accès pour tous les autres utilisateurs du compte. 

Vous devez disposer des droits suivants pour accéder aux détails du terminal pour les serveurs virtuels publics ou les serveurs virtuels privés.

**Affichage des détails des serveurs virtuels**

Permet d'afficher les adresses IP, le type de système d'exploitation, les mots de passe et d'autres informations pour un serveur virtuel spécifique.  Vous pouvez également mettre à jour les mots de passe de serveur virtuel dans le portail. Un utilisateur doit disposer de ce droit d'accès pour afficher les instances publiques, les instances dédiées et les instances d'hôte dédiées.

**Affichage des détails pour les hôtes dédiés virtuels**

Permet d'afficher les adresses IP, le type de système d'exploitation, les mots de passe et d'autres informations pour un hôte virtuel spécifique.  Vous pouvez également migrer les instances dédiées vers un autre hôte dédié. Un utilisateur doit disposer de ce droit d'accès pour afficher les hôtes dédiés.

## Ajout de droits permettant d'afficher des instances de serveur virtuel
Suivez la procédure présentée ci-dessous pour ajouter des droits d'*affichage des détails de serveur virtuel* pour vos utilisateurs enfant. Seul un administrateur de compte peut accorder des droits à d'autres utilisateurs du compte.  

1. Accédez au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
2. Sélectionnez **Compte > Utilisateurs** dans la barre de navigation pour accéder à l'écran Utilisateurs.
3. Cliquez sur le nom d'utilisateur approprié pour accéder au profil utilisateur.
4. cliquez sur l'icône **Autorisations du portail** pour accéder à l'écran Autorisations du portail.
5. Sur l'onglet *Appareil*, sélectionnez **Afficher les détails du serveur virtuel** pour ajouter ces droits au profil de l'utilisateur.

Pour fournir l'accès à un niveau de terminal spécifique, suivez la procédure décrite ci-dessous.

1. Cliquez sur l'icône **Accès à l'unité** pour accéder à l'écran Accès à l'unité.
2. Cliquez sur l'onglet **Accès rapide**. 
   Remarque : Vous pouvez également sélectionner un terminal individuel à la place.
3. Dans la liste déroulante *Type d'unité*, sélectionnez **Tous les serveurs virtuels**.
4. Sélectionnez la case à cocher **Accorder l'accès automatiquement lors de l'ajout de nouveaux appareils** si l'utilisateur associé doit toujours avoir accès à ce type de terminal.
5. Vérifiez que les terminaux corrects sont sélectionnés.
6. Cliquez sur **Mettre à jour l'accès à l'unité**.

## Ajout de droits permettant d'afficher des hôtes dédiés
Suivez la procédure présentée ci-dessous pour ajouter des droits d'*affichage des détails d'hôte dédié virtuel* pour vos utilisateurs enfant. Seul un administrateur de compte peut accorder des droits à d'autres utilisateurs du compte.

1. Accédez au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
2. Sélectionnez **Compte > Utilisateurs** dans la barre de navigation pour accéder à l'écran Utilisateurs.
3. Cliquez sur le nom d'utilisateur approprié pour accéder au profil utilisateur.
4. cliquez sur l'icône **Autorisations du portail** pour accéder à l'écran Autorisations du portail.
5. Sur l'onglet *Appareil*, sélectionnez **Afficher les détails d'hôte virtuel dédié** pour ajouter ces droits au profil de l'utilisateur.

Pour fournir l'accès à un niveau de terminal spécifique, suivez la procédure décrite ci-dessous.

1. Cliquez sur l'icône **Accès à l'unité** pour accéder à l'écran Accès à l'unité.
2. Cliquez sur l'onglet **Accès rapide**. 
   Remarque : Vous pouvez également sélectionner des terminaux individuels à la place.
3. Dans la liste déroulante *Type d'unité*, sélectionnez **Tous les hôtes dédiés**.
4. Sélectionnez la case à cocher **Accorder l'accès automatiquement lors de l'ajout de nouveaux appareils** si l'utilisateur associé doit toujours avoir accès à ce type de terminal.
5. Vérifiez que les terminaux corrects sont sélectionnés.
6. Cliquez sur **Mettre à jour l'accès à l'unité**.

**Remarque :** Vous pouvez également utiliser le service d'API SoftLayer_User_Customer::addBulkDedicatedHostAccess pour octroyer à un utilisateur l'accès à un ou plusieurs hôtes dédiés. Pour plus d'informations, voir [Adding Bulk Dedicated Host Access ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://sldn.softlayer.com/reference/services/softlayer_user_customer/addbulkdedicatedhostaccess){: new_window}.  

## Etapes suivantes
Les droits d'accès utilisateur sont mis à jour dès que les modifications sont soumises. Si des droits ont été octroyés, l'utilisateur peut afficher les fonctions sélectionnées ou interagir avec ces dernières. Si des droits ont été retirés, l'utilisateur ne peut plus afficher les fonctions sélectionnées ou interagir avec ces dernières. Les droits peuvent être mis à jour à nouveau à tout moment.
