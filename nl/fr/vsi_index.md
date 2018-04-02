---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Serveurs virtuels - Initiation
Vous pouvez déployer les serveurs {{site.data.keyword.BluVirtServers}} en quelques minutes seulement. Les serveurs virtuels sont déployés à partir des images de serveur virtuel de votre choix et dans la zone géographique adaptée à vos charges de travail.
{:shortdesc}

Lorsque vous créez un serveur virtuel, vous pouvez choisir entre un environnement public (à service partagé) ou un environnement dédié (à service exclusif). Ensuite, suivant l'environnement choisi, vous devez également sélectionner des serveurs virtuels horaires, mensuels ou transitoires. Dans le cas des serveurs virtuels publics, vous choisissez également d'utiliser un dispositif de stockage SAN ou une mémoire locale.

## Avant de commencer

Avant de commencer, passez en revue les conditions requises présentées ci-dessous.

  1. Vous devez disposer d'un compte mis à niveau pour commander des serveurs virtuels. Ce processus peut être assez long et nécessite que votre demande soit approuvée. Pour plus d'informations sur la mise à niveau de votre compte, voir [Basculement sur IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).
  2. Consultez et choisissez vos options de déploiement. Pour plus d'informations, voir les rubriques suivantes :

|              Options de déploiement                           |  Description                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Serveur virtuel public](../vsi/vsi_public.html)            | Déploiements de serveurs virtuels à service partagé géré par IBM|
|[Serveur virtuel transitoire](../vsi/vsi_about_transient.html)| Déploiements de serveurs virtuels à service partagé géré par IBM offerts à un coût réduit et idéaux pour les charges de travail flexibles |
|[Serveur virtuel dédié](../vsi/vsi_dedicated.html)      | Déploiements de serveurs virtuels à service exclusif géré par IBM            |
{: caption="Tableau 1. Options de déploiement" caption-side="top"}   

## Mise à disposition d'un serveur virtuel

Une fois que vous avez choisi une option de déploiement, commencez le processus de mise à disposition.

|              Instructions de mise à disposition                                         |  Description                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Mise à disposition d'instances publiques](../vsi/vsi_provision_public.html)                | Mise à disposition d'instances publiques avec plusieurs options             |
|[Mise à disposition d'instances transitoires](../vsi/vsi_provision_transient.html)                | Mise à disposition d'instances transitoires avec plusieurs options            |
|[Mise à disposition d'instances et d'hôtes dédiés](../vsi/vsi_provision_dedicated.html)| Mise à disposition d'instances privées ou d'instances dédiées sur des hôtes dédiés.|
{: caption="Tableau 2. Informations de mise à disposition" caption-side="top"}

## Etapes suivantes

Une fois que votre serveur virtuel est mis à disposition et est disponible pour être utilisé, vous pouvez configurer vos serveurs virtuels en utilisant le portail {{site.data.keyword.slportal_full}} ou l'API {{site.data.keyword.slapi_full}}. Pour plus d'informations, voir [Configuration des serveurs virtuels](../vsi/vsi_configuring.html).
