---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-03"

subcollection: virtual-servers

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
Vous pouvez mettre à disposition vos instances de serveur virtuel transitoires via le catalogue {{site.data.keyword.cloud}} ou le portail {{site.data.keyword.slportal}}.
{:shortdesc}

## Avant de commencer
Avant de commencer, passez en revue les conditions requises présentées ci-dessous.

  1. Vérifiez que vos données d'identification sont définies pour le catalogue {{site.data.keyword.cloud_notm}} ou le portail {{site.data.keyword.slportal}}.

  **Remarque :** Pour le catalogue {{site.data.keyword.Bluemix_notm}}, vous devez disposer d'un compte mis à niveau pour pouvoir commander des serveurs virtuels. Pour plus d'informations sur la mise à niveau de votre compte, voir [Basculement sur IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).

  2. Vérifiez les considérations sur la capacité des instances de serveur virtuel. Pour plus d'informations, voir [Considérations relatives à la capacité](/docs/vsi?topic=virtual-servers-capacity-considerations).

## Mise à disposition d'une instance de serveur virtuel transitoire
Après avoir rempli les conditions préalables, vous pouvez commencer à mettre à disposition votre instance de serveur virtuel transitoire. Vous pouvez mettre à disposition votre instance via le catalogue {{site.data.keyword.cloud_notm}} ou le portail {{site.data.keyword.slportal}}.

### Mise à disposition d'instances de serveur virtuel transitoires via le catalogue IBM Cloud
Pour mettre à disposition une instance de serveur virtuel transitoire via le catalogue {{site.data.keyword.cloud_notm}}, procédez comme suit :

  1. Connectez-vous au catalogue [{{site.data.keyword.cloud_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/catalog/){: new_window} à l'aide de vos données d'identification uniques.  
  2. Dans la section **Infrastructure de calcul**, cliquez sur la vignette **Serveurs virtuels**.
  3. Sélectionnez l'option **Serveur virtuel transitoire**.
  4. Cliquez sur **Créer**.
  5. Complétez toutes les informations pertinentes pour votre instance de serveur virtuel.
  6. Après avoir examiné le récapitulatif de votre commande, cliquez sur la case **Accords de service tiers**.
  7. Cliquez sur **Mettre à disposition**.

### Mise à disposition d'instances de serveur virtuel transitoires via le portail client
Pour mettre à disposition une instance de serveur virtuel transitoire via le portail {{site.data.keyword.slportal}}, procédez comme suit :

  1. Connectez-vous au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
  2. Localisez la section **Commande** et cliquez sur **Unités**.
  3. Sous *Serveur virtuel public* sur la page *Unités*, cliquez sur **Transitoire** pour l'offre Serveur virtuel.
  4. Sur la page de configuration de votre serveur Cloud**, indiquez les informations pertinentes.
  5. Cliquez sur **Ajouter à la commande** pour continuer.
  6. Confirmez ou modifiez les informations de domaine pour le serveur.
  7. Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
  8. Confirmez ou entrez vos informations de paiement et cliquez sur **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

 Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page *Détails de l'unité*.

Vous pouvez aussi mettre à disposition un serveur virtuel transitoire via l'{{site.data.keyword.slapi_short}}. Pour obtenir un exemple, voir [Mise à disposition d'une instance transitoire à l'aide de Create Object](/docs/vsi?topic=virtual-servers-api-rest-public#api-rest-transient).
{:tip}

## Etapes suivantes
Une fois que votre serveur virtuel est mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs virtuels](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
