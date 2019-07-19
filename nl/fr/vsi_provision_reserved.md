---

copyright:
  years: 2018
lastupdated: "2018-10-05"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mise à disposition de la capacité et des instances réservées
{: #provisioning-reserved-capacity-and-instances}

## Avant de commencer

Vous pouvez mettre à disposition votre capacité et vos instances réservées via le catalogue {{site.data.keyword.cloud}}. Vous devez mettre à disposition votre capacité réservée avant vos instances de serveur virtuel.

**Remarque **: si vous ne disposez pas d'un compte administrateur, votre compte utilisateur doit inclure le droit **Gérer les capacités réservées**. L'administrateur du compte peut accorder le droit d'utilisateur à partir de l'onglet **Autorisations du portail** dans la console. Pour en savoir plus sur la mise à jour des droits, voir [Gestion de l'accès à l'infrastructure](/docs/iam?topic=iam-mngclassicinfra).

## Connexion au catalogue IBM Cloud

Suivez les étapes décrites ci-dessous pour vous connecter au catalogue {{site.data.keyword.cloud_notm}} pour commencer à mettre à disposition votre capacité et vos instances réservées.

  1. Connectez-vous au catalogue [{{site.data.keyword.cloud_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/catalog/){: new_window} à l'aide de vos données d'identification uniques.

## Mise à disposition de la capacité réservée

Dans le catalogue {{site.data.keyword.cloud_notm}}, procédez comme suit pour mettre à disposition votre capacité réservée.

  1. Dans la section **Infrastructure de calcul**, cliquez sur la vignette **Serveurs virtuels**.
  2. Sélectionnez l'option **Serveur virtuel réservé**.
  3. Cliquez sur **Créer**.
  4. Pour créer une nouvelle capacité réservée, sélectionnez **Nouvelle capacité +**. Sur la page **Capacité réservée**, entrez ou sélectionnez les informations suivantes :

| Zone                   | Valeur               |                                                                                                                                                                                                                                                                                                                                 
| ----------------------- | ------------------- |
| Nom                    | Entrez un nom pour votre capacité réservée. |                                                                                                                                                                                                                                                                                                       
| Capacité de serveur virtuel | Sélectionnez le nombre d'instances que vous souhaitez assigner à cette capacité réservée (20 instances max). |                                                                                                                                                                                                                                                
| Emplacement                | Sélectionnez l'emplacement spécifique requis pour vos flux de travaux. Les emplacements sont composés de régions ; chaque région est une zone géographique séparée. **Remarque :** vous ne pouvez pas sélectionner d'emplacements individuels pour chaque instance de serveur virtuel que vous mettez à disposition dans cette capacité réservée. Votre sélection est l'emplacement de toutes les instances de serveur virtuel que vous mettez à disposition dans cette capacité réservée. |
| POD                     | Sélectionnez le point de livraison spécifique à votre emplacement. |
| Durées de plan              | Choisissez entre une durée de contrat de un ou trois ans. |                                                                                                                                                                                                                                                                                            
| Profil                 | Sélectionnez des profils populaires ou toutes les combinaisons de vCPU et RAM disponibles du stockage SAN (balanced, memory ou compute). **Remarque :** vous ne pouvez pas combiner différentes tailles de profil dans l'ensemble d'instances de serveur virtuel assignées à cette capacité, ni les changer ultérieurement. L'ensemble d'instances de serveur virtuel que vous réservez doit avoir la même taille. |
{: caption="Tableau 1. Sélections de mise à disposition de capacité réservée" caption-side="top"}


## Mise à disposition d'instances réservées

Après avoir mis à disposition votre capacité réservée, vous devez mettre à disposition vos instances de serveur virtuel réservées. Les instances de serveur virtuel réservées peuvent être mises à disposition à tout moment durant la durée du contrat car votre capacité est garantie. Effectuez les étapes suivantes pour mettre à disposition vos instances réservées :

1. Dans le catalogue {{site.data.keyword.cloud_notm}}, sélectionnez la vignette **Serveurs virtuels** dans la section **Infrastructure de calcul**.
2. Sélectionnez l'option **Serveur virtuel réservé**.
3. Cliquez sur **Créer**.
4. Pour mettre à disposition une instance de serveur virtuel réservée, entrez ou sélectionnez les informations suivantes :

| Zone                     | Valeur               |                                                                                                                                                                                                                                                                                                                                 
| ------------------------- | ------------------- |
| Nom                      | Entrez un nom pour votre instance de serveur virtuel réservée. |                                                                                                                                                                                                                                                                                                       
| Facturation                   | Sélectionnez la facturation horaire ou mensuelle. |                                                                                                                                                                                                                                                
| Capacité réservée         | Sélectionnez votre capacité réservée ou sélectionnez **Nouvelle capacité +** pour mettre à disposition une capacité réservée supplémentaire. |                                                                                                                                                                                                     
| Modules complémentaires                   | Sélectionnez un stockage, un réseau ou un logiciel additionnel. |                                                                                                                                                                                                                                                                                            
{: caption="Tableau 1. Sélections de mise à disposition de capacité réservée" caption-side="top"}

## Etapes suivantes

Une fois que votre serveur virtuel est mis à disposition et est disponible pour être utilisé, vous pouvez configurer vos serveurs virtuels à l'aide de la console {{site.data.keyword.cloud_notm}} ou de {{site.data.keyword.slapi_short}}. Pour plus d'informations, voir [Configuration des serveurs virtuels](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).

En cas de questions concernant la capacité et les instances réservées, veuillez vous reporter à [Foire aux questions : capacité et instances réservées](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances). 
