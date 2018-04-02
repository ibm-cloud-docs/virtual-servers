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

# Mise à disposition d'instances publiques
{: #ordering-vs-public}

## Avant de commencer
Il existe deux méthodes de mise à disposition de vos instances de serveur virtuel public. Vous pouvez utiliser, soit le catalogue {{site.data.keyword.Bluemix}}, soit le portail {{site.data.keyword.slportal_full}}. Des ID de connexion uniques sont requis pour le catalogue et le portail {{site.data.keyword.slportal}}. Le nom d'utilisateur et le mot de passe du catalogue ne fonctionnent pas pour la connexion au portail et vice-versa.
{:shortdesc}

Avant de commencer, passez en revue les conditions requises présentées ci-dessous.

  1. Vérifiez que les données d'identification du portail {{site.data.keyword.slportal}} ou du catalogue {{site.data.keyword.Bluemix_notm}} sont définies. 
  
     **Remarque :** Pour le catalogue {{site.data.keyword.Bluemix_notm}}, vous devez disposer d'un compte mis à niveau pour pouvoir commander des serveurs virtuels. Pour plus d'informations sur la mise à niveau de votre compte, voir [Basculement sur IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).
  
  2. Si vous ne l'avez pas encore fait, consultez les options de déploiement disponibles. Pour plus d'informations, voir [Serveurs virtuels publics](../vsi/vsi_public.html).

## Connexion 
Vérifiez que vous êtes connecté, soit via le catalogue {{site.data.keyword.Bluemix_notm}}, soit via le portail {{site.data.keyword.slportal}} : 

  <table>
   <CAPTION>Tableau 1. Choix d'un emplacement de connexion</CAPTION>
   <THEAD>
   <TR>
   <th>Connexion à</th>
   <th>Procédure</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Catalogue IBM Cloud</td>
   <td>
   <ol>
   <li>Ouvrez une fenêtre de navigateur et entrez <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Cliquez sur le lien <b>Se connecter</b> (coin inférieur droit). </li>
   <li>Entrez votre adresse électronique ou votre ID IBM puis cliquez sur <b>Continuer</b>.</li>
   <li>Entrez votre mot de passe puis cliquez sur <b>Se connecter.</b></li>
   <li>Sélectionnez <b>Infrastructure</b> > <b>Calcul</b>.</li>
   <li>Cliquez sur <b>Serveurs virtuels</b>.</li>
   <li>Sélectionnez l'option <b>Serveurs virtuels publics</b>.</li>
   <li>Cliquez sur <b>Créer</b>. La page principale du portail {{site.data.keyword.slportal}} s'affiche.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Portail client</td>
   <td>
   <ol>
   <li>Ouvrez une nouvelle fenêtre de navigateur et entrez <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Entrez votre nom d'utilisateur et votre mot de passe puis cliquez sur <b>Se connecter</b>. Ou, cliquez sur <b>Connexion par ID IBM</b>. Entrez ensuite votre adresse électronique ou votre ID IBM puis cliquez sur <b>Continuer</b>. Entrez votre mot de passe puis cliquez sur <b>Se connecter</b>. La page principale du portail {{site.data.keyword.slportal}} s'affiche.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Mise à disposition d'une instance de serveur virtuel public
{: #ordering-public-instance}
Une fois la configuration requise appliquée, vous pouvez commencer à mettre à disposition une instance de serveur virtuel public. Vous pouvez mettre à disposition vos instances publiques de deux manières, via l'icône **Terminaux** ou le menu **Terminaux**.

### Mise à disposition d'une instance de serveur virtuel public via l'icône Terminal
Pour mettre à disposition votre instance de serveur virtuel public via l'icône *Terminaux*, procédez comme suit :

1.  Dans le portail {{site.data.keyword.slportal}}, recherchez la section **Commande**, puis cliquez sur **Unités**.
2.  Sur la page Unités, cliquez sur **Horaire** ou **Mensuel** pour une des offres de serveur virtuel.
3.  Sur la page de configuration de votre serveur Cloud**, indiquez les informations appropriées.
4.  Cliquez sur le bouton **Ajouter à la commande** pour continuer.
5.  Confirmez ou modifiez les informations de domaine pour le serveur.
5.  Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
6.  Confirmez ou entrez vos informations de paiement puis cliquez sur le bouton **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

 Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page *Détails de l'unité* après la connexion à {{site.data.keyword.Bluemix_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

### Mise à disposition d'une instance de serveur virtuel public via le menu Unités
{: #ordering-public-devices-menu}

Vous pouvez également mettre à disposition vos instances de serveur virtuel public via le menu *Unités* sur la page principale du portail {{site.data.keyword.slportal}}. 

1. Cliquez sur **Unités > Liste des unités**.

   La page Unités affiche tous les types de terminal (hôtes dédiés, serveurs virtuels, serveurs Bare Metal et contrôleurs de distribution d'application NetScaler) de votre compte.
2. Cliquez sur le lien **Commander unités** dans le coin supérieur droit.
3. Sur la page Unités, cliquez sur **Horaire** ou **Mensuel** pour une des offres de serveur virtuel.
4. Sur la page de configuration de votre serveur Cloud**, indiquez les informations appropriées.
5. Cliquez sur le bouton **Ajouter à la commande** pour continuer.
6. Confirmez ou modifiez les informations de domaine pour le serveur.
7. Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
8. Confirmez ou entrez vos informations de paiement puis cliquez sur le bouton **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page *Détails de l'unité* après la connexion à {{site.data.keyword.Bluemix_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

### Etapes suivantes
Une fois que votre serveur virtuel est mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs virtuels](../vsi/vsi_managing.html).
