---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-03"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mise à disposition d'instances publiques
{: #ordering-vs-public}

## Avant de commencer
Il existe deux méthodes de mise à disposition de vos instances de serveur virtuel public. Vous pouvez utiliser, soit le catalogue {{site.data.keyword.Bluemix}}, soit le portail {{site.data.keyword.slportal}}. Des ID de connexion uniques sont requis pour le catalogue et le portail {{site.data.keyword.slportal}}. Le nom d'utilisateur et le mot de passe du catalogue ne fonctionnent pas pour la connexion au portail et vice-versa.
{:shortdesc}

Avant de commencer, passez en revue les conditions requises présentées ci-dessous.

  1. Vérifiez que les données d'identification du portail {{site.data.keyword.slportal}} ou du catalogue {{site.data.keyword.Bluemix_notm}} sont définies.

     **Remarque :** Pour le catalogue {{site.data.keyword.Bluemix_notm}}, vous devez disposer d'un compte mis à niveau pour pouvoir commander des serveurs virtuels. Pour plus d'informations sur la mise à niveau de votre compte, voir [Basculement sur IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).

  2. Si vous ne l'avez pas encore fait, consultez les options de déploiement disponibles. Pour plus d'informations, voir [Serveurs virtuels publics](../vsi/vsi_public.html).

  3. Vérifiez les considérations sur la capacité des instances de serveur virtuel.  Pour plus d'informations, voir [Considérations relatives à la capacité](ts_capacity_bp.html).

## Mise à disposition d'une instance de serveur virtuel public
{: #ordering-public-instance}

Après avoir rempli les conditions préalables, vous pouvez commencer à mettre à disposition une instance de serveur virtuel publique. Vous pouvez mettre à disposition votre instance publique via le catalogue {{site.data.keyword.cloud_notm}} ou le portail {{site.data.keyword.slportal}}.

### Mise à disposition d'une instance de serveur virtuel publique via le catalogue IBM Cloud
Pour mettre à disposition une instance de serveur virtuel publique via {{site.data.keyword.cloud_notm}}, procédez comme suit :

  1. Connectez-vous au catalogue [{{site.data.keyword.cloud_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/catalog/){: new_window} à l'aide de vos données d'identification uniques. 
  2. Dans la section **Infrastructure de calcul**, cliquez sur la vignette **Serveurs virtuels**.
  3. Sélectionnez l'option **Serveur virtuel public**.
  4. Cliquez sur **Créer**.
  5. Complétez toutes les informations pertinentes pour votre instance de serveur virtuel. 
  6. Après avoir examiné le récapitulatif de votre commande, cliquez sur la case **Accords de service tiers**. 
  7. Cliquez sur **Mettre à disposition**.
  
### Mise à disposition d'une instance de serveur virtuel publique via le portail client
Pour mettre à disposition votre instance de serveur virtuel publique via le portail {{site.data.keyword.slportal}}, procédez comme suit :

  1. Connectez-vous au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
  2. Localisez la section **Commande** et cliquez sur **Unités**. 
  3. Sur la page Unités, cliquez sur **SAN horaire**, **Local horaire**, **Mensuel** ou **Transitoire** correspondant aux offres de Serveur virtuel.
  4. Sur la page de configuration de votre serveur Cloud**, indiquez les informations pertinentes.
  5. Cliquez sur le bouton **Ajouter à la commande** pour continuer.
  6. Confirmez ou modifiez les informations de domaine pour le serveur.
  7. Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
  8. Confirmez ou entrez vos informations de paiement puis cliquez sur le bouton **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

 Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page *Détails de l'unité* après la connexion à {{site.data.keyword.Bluemix_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

## Etapes suivantes
Une fois que votre serveur virtuel est mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs virtuels](../vsi/vsi_managing.html).
