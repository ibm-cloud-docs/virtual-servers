---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Mise à disposition d'instances dédiées

Vous disposez de deux méthodes pour la mise à disposition de vos instances dédiées. Vous pouvez utiliser, soit le catalogue {{site.data.keyword.Bluemix}}, soit le portail {{site.data.keyword.slportal_full}}. Des ID de connexion uniques sont requis pour le catalogue et le portail {{site.data.keyword.slportal}}. Le nom d'utilisateur et le mot de passe du catalogue ne fonctionnent pas pour la connexion au portail et vice-versa. Pour configurer vos données d'identification permettant d'accéder au catalogue {{site.data.keyword.Bluemix_notm}} ou au portail {{site.data.keyword.slportal}}, voir [Inscription à {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window}
{:shortdesc}

## Connexion au catalogue IBM Cloud
Procédez comme suit pour vous connecter au catalogue {{site.data.keyword.Bluemix_notm}} afin de lancer la mise à disposition de vos instances dédiées. 

1. Ouvrez une fenêtre de navigateur et entrez [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/){: new_window}.
2.	Cliquez sur le lien **Se connecter** (coin supérieur droit). 
3.	Entrez votre adresse électronique ou votre ID IBM puis cliquez sur **Continuer**.
4.	Entrez votre mot de passe puis cliquez sur **Se connecter**.
5.	Sélectionnez **Infrastructure > Calcul**.
6.  Cliquez sur **Serveurs virtuels**.
7.	Sélectionnez l'option **Serveurs virtuels dédiés**.
8.  Cliquez sur **Créer**. 

La page principale du portail {{site.data.keyword.slportal}} s'affiche.

## Connexion au portail client
Procédez comme suit pour vous connecter au portail {{site.data.keyword.slportal}} en vue d'effectuer une commande d'instances dédiées.

1.	Ouvrez une nouvelle fenêtre de navigateur et entrez [https://control.softlayer.com](https://control.softlayer.com){: new_window}. 
2.	Entrez votre nom d'utilisateur et votre mot de passe puis cliquez sur **Se connecter** OU cliquez sur **Connexion par ID IBM**.
3.	Entrez votre adresse électronique ou votre ID IBM puis cliquez sur **Continuer**.
4.	Entrez votre mot de passe puis cliquez sur **Se connecter**.

La page principale du portail {{site.data.keyword.slportal}} s'affiche.

## Mise à disposition de vos instances dédiées
{: #provision-dedicated-instances}
Vous pouvez mettre à disposition vos instances dédiées de deux manières, via l'icône **Unités** ou le menu **Unités**.

### Mise à disposition de vos instances d'hôte dédiées via l'icône Unités
{: #ordering-dedicated-devices-menu}
La première méthode de mise à disposition d'instances d'hôte dédiées consiste à utiliser l'icône **Appareil** sur la page principale du portail {{site.data.keyword.slportal}}. Pour cela, suivez la procédure présentée ci-dessous.

1.	Cliquez sur l'icône **Unités**. La fenêtre **Commander des services et des produits SoftLayer** s'affiche. 
2.  Sélectionnez **Horaire** ou **Mensuel** sous Serveurs virtuels dédiés. La page de configuration de votre serveur Cloud** s'affiche. 

3.	Entrez les informations suivantes :
       
    <table>
    <CAPTION>Tableau 1. Sélection d'instances d'hôte dédiées</CAPTION>
    <THEAD>
    <TR>
    <th>Zone</th>
    <th>Valeur</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantité</td>
    <td>Nombre d'instances dédiées à déployer.</td>
    </tr>
    <tr>
    <td>Emplacement</td>
    <td>
    <ul>
    <li>Affectation automatique – {{site.data.keyword.Bluemix_notm}} affecte automatiquement votre instance à un hôte dans votre centre de données sélectionné.</li>
    <li>Spécification d'hôte – Utilisation avec des instances d'hôte dédiées. Pour plus d'informations sur les hôtes dédiés et les instances d'hôte dédiées, voir [Serveurs virtuels dédiés](../vsi/vsi_dedicated.html).</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Centre de données</td>
    <td>Sélectionnez le centre de données dans lequel les instances doivent être mises à disposition.</td>
    </tr>
    <tr>
    <td>Instance de calcul</td>
    <td> Sélectionnez la mémoire et l'unité centrale pour chaque instance dans une commande de mise à disposition.</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> Sélectionnez la mémoire RAM pour chaque instance dans une commande de mise à disposition.</td>
    </tr>
    <tr>
    <td>Système d'exploitation</td>
    <td>Sélectionnez le système d'exploitation pour l'instance. Un message d'erreur est généré lorsqu'il existe un conflit entre le serveur et le système d'exploitation (sélection de Linux sur un serveur Microsoft SQL, par exemple).</td>
    </tr>
    <tr>
    <td>Premier disque</td>
    <td>Sélectionnez SAN ou Local pour chaque instance dans une commande.</td>
    </tr>
    <tr>
    <td>Disques supplémentaires</td>
    <td>Vous pouvez mettre à disposition jusqu'à quatre disques d'amorçage supplémentaires (SAN ou local) par instance dédiée.</td>
    </tr>
    <td>Options réseau</td>
    <td> Sélectionnez les options appropriées ou utilisez les valeurs par défaut.</td>
    </tr>
    <tr>
    <td>Modules complémentaires</td>
    <td> Sélectionnez les options appropriées ou utilisez les valeurs par défaut.</td>
    </tr>
    <tr>
    </TBODY>
    </table> 

4.	Cliquez sur le bouton **Ajouter à la commande**. La page Réservation s'affiche.
5.  Entrez les informations suivantes sur la page *Réservation* sous *Configuration système avancée*:

<table>
    <CAPTION>Tableau 2. Configuration système avancée pour l'instance dédiée</CAPTION>
    <THEAD>
    <TR>
    <th>Zone</th>
    <th>Valeur</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Sélection VLAN</td>
    <td>Ajoutez le nouveau serveur à un réseau local virtuel (VLAN) sous votre compte si vous avez déjà commandé au moins un serveur.</td>
    </tr>
    <tr>
    <td>Scripts de mise à disposition</td>
    <td>Indiquez un script vous permettant d'automatiser certaines étapes après la mise à disposition.</td>
    </tr>
    <tr>
    <td>Clés SSH</td>
    <td>Indiquez une clé publique de votre clé SSH, qui vous permet de vous connecter à votre serveur après sa mise à disposition.</td>
    </tr>
    <tr>
    <td>Métadonnées utilisateur</td>
    <td>Métadonnées facultatives pour les scripts de mise à disposition personnalisés.</td>
    </tr>
    <tr>
    <td>Nom d'hôte</td>
    <td>Entrez un nom permanent ou temporaire pour votre serveur, par exemple, server1.</td>
    </tr>
    <tr>
    <td>Domaine</td>
    <td>Entrez nom de sous-domaine qui ne présente aucun conflit avec un nom de domaine Internet, par exemple, test.acme.com.</td>
    </tr>
    </TBODY>
    </table>

6.  Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
7. Confirmez ou entrez vos informations de paiement puis cliquez sur le bouton **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

    Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page **Détails de l'unité** après la connexion à {{site.data.keyword.Bluemix_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

### Mise à disposition de vos instances dédiées via le menu Terminaux

La seconde méthode consiste à mettre à disposition vos instances dédiées via le menu **Unités** sur la page principale du portail {{site.data.keyword.slportal}}. Pour cela, suivez la procédure présentée ci-dessous.

1.	Cliquez sur **Unités > Liste des unités**. 
 
    La page *Unités* affiche tous les types d'unités (serveurs virtuels, serveurs Bare Metal, hôtes dédiés et contrôleurs de distribution d'application NetScaler) de votre compte. 

2.	Cliquez sur le lien **Commandes d'unités** sur le côte droit de la page.
    La fenêtre **Commander des services et des produits SoftLayer** s'affiche.
3.	Suivez la procédure [Mise à disposition de vos instances d'hôte dédiées via l'icône Unités](#ordering-dedicated-devices-menu), à partir de l'étape 2.

### Etapes suivantes
Une fois que votre serveur virtuel est mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs virtuels](../vsi/vsi_managing.html).
