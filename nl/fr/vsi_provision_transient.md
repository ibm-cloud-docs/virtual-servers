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
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Mise à disposition d'instances transitoires
{: #ordering-vs-transient}
Vous pouvez mettre à disposition vos instances de serveur virtuel transitoires via le portail {{site.data.keyword.slportal_full}}.
{:shortdesc}

## Avant de commencer
Avant de commencer, passez en revue les conditions requises présentées ci-dessous.

  1. Vérifiez que vos données d'identification sont configurées sur le portail {{site.data.keyword.slportal}}.

  2. Vérifiez les considérations sur la capacité des instances de serveur virtuel. Pour plus d'informations, voir [Considérations relatives à la capacité](ts_capacity_bp.html).

## Connexion
Vérifiez que vous êtes connecté au portail {{site.data.keyword.slportal}} :

  1. Accédez au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.

La page principale du portail {{site.data.keyword.slportal}} s'affiche.

## Mise à disposition d'une instance de serveur virtuel transitoire
{: #ordering-transient-instance}
Après avoir rempli les conditions préalables, mettez à disposition une instance de serveur virtuel. Vous pouvez mettre à disposition vos instances transitoires de deux manières : via le menu **Unités** ou en cliquant sur l'icône **Unités**.

### Mise à disposition d'une instance de serveur virtuel transitoire via l'icône Unités
Pour mettre à disposition votre instance de serveur virtuel transitoire via l'icône *Unités*, procédez comme suit :

1.  Dans le portail {{site.data.keyword.slportal}}, recherchez la section **Commande**, puis cliquez sur **Unités**.
2.  Sous *Serveur virtuel public* sur la page *Unités*, cliquez sur **Transitoire** pour l'offre Serveur virtuel.
3.  Sur la page de configuration de votre serveur Cloud**, indiquez les informations appropriées.
4.  Cliquez sur **Ajouter à la commande** pour continuer.
5.  Confirmez ou modifiez les informations de domaine pour le serveur.
5.  Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
6.  Confirmez ou entrez vos informations de paiement et cliquez sur **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

 Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page *Détails de l'unité*. 

### Mise à disposition d'une instance de serveur virtuel transitoire via le menu Unités
{: #ordering-transient-devices-menu}

Vous pouvez également mettre à disposition vos instances de serveur virtuel transitoires via le menu *Unités* sur la page principale du portail {{site.data.keyword.slportal}}.

1. Cliquez sur **Unités > Liste des unités**.

   La page Unités affiche tous les types de terminal (hôtes dédiés, serveurs virtuels, serveurs Bare Metal et contrôleurs de distribution d'application NetScaler) de votre compte.
2. Cliquez sur le lien **Commander unités** dans le coin supérieur droit.
3. Sous *Serveur virtuel public* sur la page *Unités*, cliquez sur **Transitoire** pour l'offre Serveur virtuel.
4. Sur la page de configuration de votre serveur Cloud**, indiquez les informations appropriées.
5. Cliquez sur **Ajouter à la commande** pour continuer.
6. Confirmez ou modifiez les informations de domaine pour le serveur.
7. Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
8. Confirmez ou entrez vos informations de paiement et cliquez sur **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page *Détails de l'unité*. 

Vous pouvez aussi mettre à disposition un serveur virtuel transitoire via l'{{site.data.keyword.slapi_short}}. Pour obtenir un exemple, voir [Mise à disposition d'une instance transitoire à l'aide de Create Object](../vsi/vsi_provision_api.html#api-rest-transient).
{:tip}

## Etapes suivantes
Une fois que votre serveur virtuel est mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs virtuels](../vsi/vsi_managing.html).
