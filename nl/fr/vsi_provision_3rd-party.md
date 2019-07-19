---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# Mise à disposition d'une instance de serveur virtuel à partir d'une image tierce 
{: #ordering-3P}

Vous pouvez mettre à disposition une instance de serveur virtuel à partir d'une image créée par un fournisseur tiers. Les images tierces sont disponibles via le lien Cloud Images du catalogue {{site.data.keyword.cloud}}.
{:shortdesc}

## Avant de commencer
Avant de commencer, assurez-vous que les données d'identification du catalogue {{site.data.keyword.cloud_notm}} sont définies.

Pour le catalogue {{site.data.keyword.Bluemix_notm}}, vous devez posséder un compte mis à niveau afin de commander des serveurs virtuels. Pour plus d'informations sur la mise à niveau de votre compte, voir [Basculement sur IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

## Sélection d'une image de serveur virtuel 
1. Connectez-vous au catalogue [{{site.data.keyword.cloud_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/catalog/){: new_window} à l'aide de vos données d'identification uniques.
2. Dans la section **Cloud Images**, localisez et cliquez sur l'image tierce que vous souhaitez déployer.
3. Vérifiez les détails de l'image personnalisée et cliquez sur **Continuer**. La page **Instance de serveur virtuel - image personnalisée** s'affiche avec votre image personnalisée présélectionnée. 

## Révision et sélection des options de déploiement 
Pour plus d'informations, voir les rubriques suivantes :

|              Options de déploiement                           |  Description                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
| [Serveur virtuel public](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)       | Déploiements de serveurs virtuels à service partagé géré par IBM|
| [Serveur virtuel transitoire](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)| Déploiements de serveurs virtuels à service partagé géré par IBM offerts à un coût réduit et idéaux pour les charges de travail flexibles |
| [Serveur virtuel réservé](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | Déploiements de serveurs virtuels à service partagé géré par IBM avec capacité garantie pendant la durée du contrat |
| [Serveur virtuel dédié](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)      | Déploiements de serveurs virtuels à service exclusif géré par IBM            |
{: caption="Tableau 1. Options de déploiement" caption-side="top"}

## Mise à disposition d'un serveur virtuel
Une fois que vous avez choisi une option de déploiement, commencez le processus de mise à disposition. Pour plus d'informations, voir les rubriques suivantes.

Dans la mesure où vous avez démarré le processus de mise à disposition avec une image personnalisée, vous ne pouvez pas modifier le type d'image pendant ce processus.
{:note}

|              Instructions de mise à disposition                                 |  Description                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
| [Mise à disposition d'instances publiques](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                | Mise à disposition d'instances publiques avec plusieurs options             |
| [Mise à disposition d'instances transitoires](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                | Mise à disposition d'instances transitoires avec plusieurs options            |
| [Mise à disposition de capacité et d'instances réservées](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | Mise à disposition de capacité et d'instances réservées avec plusieurs options |
| [Mise à disposition d'instances et d'hôtes dédiés](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)| Mise à disposition d'instances privées ou d'instances dédiées sur des hôtes dédiés.|
{: caption="Tableau 2. Informations de mise à disposition" caption-side="top"}


## Etapes suivantes
Une fois que votre serveur virtuel est mis à disposition et est disponible pour être utilisé, vous pouvez configurer vos serveurs virtuels à l'aide de la console {{site.data.keyword.cloud_notm}} ou de {{site.data.keyword.slapi_short}}. Pour plus d'informations, voir [Configuration des serveurs virtuels](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
