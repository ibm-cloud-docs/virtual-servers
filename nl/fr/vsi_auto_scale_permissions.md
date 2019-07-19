---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-14"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration des droits utilisateur pour la mise à l'échelle automatique 
{: #user-permissions-required-to-use-auto-scale}

L'accès aux options de mise à l'échelle automatique requiert un droit utilisateur spécial outre la possibilité de commander et de gérer {{site.data.keyword.virtualmachinesshort}}. Pour accéder aux fonctions de mise à l'échelle automatique, vous devez être habilité à gérer tous les serveurs virtuels du compte, ainsi que les éventuels périphériques virtuels ajoutés à l'avenir.

Si vous êtes l'administrateur du compte et que vous souhaitez autoriser les utilisateurs à accéder aux options de mise à l'échelle automatique, procédez comme suit : 

1. Connectez-vous à la page [Accès (IAM) ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/iam#/users){: new_window} dans la console {{site.data.keyword.cloud}}. 
2. Dans l'onglet **Utilisateurs**, sélectionnez **Afficher par : Mes utilisateurs d'infrastructure classique**.
3. Sélectionnez un utilisateur, puis cliquez sur l'onglet **Infrastructure classique**. 
4. Développez la catégorie **Unités** dans l'onglet **Droits**, puis sélectionnez **Gérer les groupes de mise à l'échelle auto**.
5. Cliquez sur **Appliquer**.

## Etapes suivantes

Une fois que vous avez l'autorisation d'accéder aux options de mise à l'échelle automatique et de les utiliser, vous êtes prêt à utiliser la fonctionnalité Auto Scale. Pour commencer, consultez les rubriques suivantes :

1. [Gestion des pics de trafic avec mise à l'échelle automatique basée planning](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling)
2. [Gestion des pics de trafic avec mise à l'échelle automatique basée ressources](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling)
3. [Foire aux questions : Auto Scale](/docs/vsi?topic=virtual-servers-faqs-auto-scale)

