---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Gestion de l'accès aux unités
{: #managing-device-access}

Pour accéder aux détails d'une unité spécifique et gérer ces derniers, votre compte utilisateur doit disposer des droits appropriés. Une fois que l'administrateur de compte accorde à votre compte utilisateur l'accès à une unité, vous pouvez afficher les détails de l'unité à l'aide de la console {{site.data.keyword.cloud}} ou de {{site.data.keyword.slapi_short}}. Les informations ou les actions que vous voyez dépendent du type d'unité, ainsi que des droits octroyés à votre compte utilisateur.
{:shortdesc}

Si votre compte dispose d'unités pour lesquelles l'accès ne vous pas a été accordé, un message "Nom d'unité inconnu" s'affiche lorsque vous tentez d'accéder à ces unités.
{:note}

Vous pouvez affecter un accès à l'unité pour les utilisateurs de votre compte mais non pour vous même. Seul un administrateur de compte peut accéder à toutes les unités du compte client et peut définir l'accès pour tous les autres utilisateurs du compte. 

Vous devez disposer des droits suivants pour accéder aux détails de l'unité pour les serveurs virtuels publics ou les serveurs virtuels privés.

* **Afficher les détails du serveur virtuel** - Permet d'afficher les adresses IP, le type de système d'exploitation, les mots de passe et d'autres informations pour un serveur virtuel spécifique. Vous pouvez également mettre à jour les mots de passe de serveur virtuel dans le portail. Vous devez disposer de ce droit d'accès pour afficher les instances publiques, les instances dédiées et les instances d'hôte dédiées.

* **Afficher les détails d'hôte dédié virtuel** - Permet d'afficher les adresses IP, le type de système d'exploitation, les mots de passe et d'autres informations pour un hôte virtuel spécifique. Vous pouvez également migrer les instances dédiées vers un autre hôte dédié. Vous devez disposer de ce droit d'accès pour afficher les hôtes dédiés.


## Ajout de droits d'accès pour les utilisateurs
Si vous êtes l'administrateur du compte et que vous souhaitez autoriser les utilisateurs à afficher les détails des serveurs virtuels et des hôtes dédiés, procédez comme suit. 

1. Connectez-vous à la page [Accès (IAM) ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/iam#/users){: new_window} dans la console {{site.data.keyword.cloud}}. 
2. Dans l'onglet **Utilisateurs**, sélectionnez **Afficher par : Mes utilisateurs d'infrastructure classique**.
3. Sélectionnez un utilisateur, puis cliquez sur l'onglet **Infrastructure classique**. 
4. Développez la catégorie **Unités** dans l'onglet **Droits**, puis sélectionnez **Afficher les détails du serveur virtuel** et **Afficher les détails d'hôte dédié virtuel**.
5. Cliquez sur **Appliquer**.

### Ajout de droits d'accès spécifiques de niveau unité 
Si vous souhaitez octroyer aux utilisateurs un accès à un niveau d'unité spécifique, procédez comme suit. 

1. Dans l'onglet **Utilisateurs**, sélectionnez **Afficher par : Mes utilisateurs d'infrastructure classique**.  
2. Sélectionnez un utilisateur, puis cliquez sur l'onglet **Infrastructure classique**. 
3. Dans la section **Sélectionner un type** de l'onglet **Unités**, sélectionnez le droit approprié : **Tous les serveurs bare metal**, **Tous les hôtes dédiés** ou **Tous les serveurs virtuels**. 
4. Dans la section **Activer un accès ultérieur** de l'onglet **Unités**, sélectionnez le droit approprié : **Accès automatique au serveur bare metal**, **Accès automatique à l'hôte dédié** ou **Accès automatique au serveur virtuel**. Ce droit permet à vos utilisateurs d'avoir toujours accès au type d'unité lors de l'ajout de nouvelles unités. 
5. Cliquez sur **Définir** pour appliquer les nouveaux droits d'accès.

## Ajout de droits d'accès pour les utilisateurs dans le portail client
Si vous êtes l'administrateur du compte et que vous souhaitez autoriser les utilisateurs à afficher les détails des serveurs virtuels et des hôtes dédiés, procédez comme suit. 

1. Accédez au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
2. Sélectionnez **Compte > Utilisateurs** dans la barre de navigation pour accéder à l'écran Utilisateurs.
3. Cliquez sur le nom d'utilisateur approprié pour accéder au profil utilisateur.
4. cliquez sur l'icône **Autorisations du portail** pour accéder à l'écran Autorisations du portail.
5. Sur l'onglet **Unités**, sélectionnez **Afficher les détails du serveur virtuel** et **Afficher les détails d'hôte dédié virtuel** pour ajouter ces droits au profil de l'utilisateur.

### Ajout de droits d'accès spécifiques de niveau unité dans le portail client 
Pour fournir l'accès à un niveau d'unité spécifique, suivez la procédure décrite ci-dessous.

1. Cliquez sur l'icône **Accès à l'unité** pour accéder à l'écran Accès à l'unité.
2. Cliquez sur l'onglet **Accès rapide**. 
3. Dans la liste déroulante **Type d'unité**, sélectionnez **Tous les serveurs virtuels** et **Tous les hôtes dédiés**.
4. Sélectionnez la case à cocher **Accorder l'accès automatiquement lors de l'ajout de nouveaux appareils** si l'utilisateur associé doit toujours avoir accès à ce type d'unité.
5. Vérifiez que les unités correctes sont sélectionnées.
6. Cliquez sur **Mettre à jour l'accès à l'unité**.

Vous pouvez également utiliser le service d'API SoftLayer_User_Customer::addBulkDedicatedHostAccess pour octroyer à un utilisateur l'accès à un ou plusieurs hôtes dédiés. Pour plus d'informations, voir [Adding Bulk Dedicated Host Access ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/reference/services/SoftLayer_User_Customer/addBulkDedicatedHostAccess/){: new_window}.  
{:note}

## Etapes suivantes
Les droits d'accès utilisateur sont mis à jour dès que les modifications sont soumises. Si des droits ont été octroyés, l'utilisateur peut afficher les fonctions sélectionnées ou interagir avec ces dernières. Si des droits ont été retirés, l'utilisateur ne peut plus afficher les fonctions sélectionnées ou interagir avec ces dernières. Les droits peuvent être mis à jour à nouveau à tout moment.

