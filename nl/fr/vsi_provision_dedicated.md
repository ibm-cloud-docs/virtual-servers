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

# Mise à disposition d'instances et d'hôtes dédiés
{: #ordering-vs-dedicated}

Vous disposez de deux méthodes pour la mise à disposition de vos instances dédiées. Vous pouvez utiliser, soit le catalogue {{site.data.keyword.Bluemix}}, soit le portail {{site.data.keyword.slportal_full}}. Des ID de connexion uniques sont requis pour le catalogue et le portail {{site.data.keyword.slportal}}. Le nom d'utilisateur et le mot de passe du catalogue ne fonctionnent pas pour la connexion au portail et vice-versa. Pour configurer vos données d'identification permettant d'accéder au catalogue {{site.data.keyword.Bluemix_notm}} ou au portail {{site.data.keyword.slportal}}, voir [Inscription à {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window}
{:shortdesc}

## Connexion au catalogue IBM Cloud
Procédez comme suit pour vous connecter au catalogue {{site.data.keyword.Bluemix_notm}} afin de lancer la mise à disposition de vos instances d'hôtes dédiées et de vos hôtes dédiés. 

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
Procédez comme suit pour vous connecter au portail {{site.data.keyword.slportal}} afin de commencer la commande de vos hôtes dédiés et de vos instances d'hôte dédiées.

1.	Ouvrez une nouvelle fenêtre de navigateur et entrez [https://control.softlayer.com](https://control.softlayer.com){: new_window}. 
2.	Entrez votre nom d'utilisateur et votre mot de passe puis cliquez sur **Se connecter** OU cliquez sur **Connexion par ID IBM**.
3.	Entrez votre adresse électronique ou votre ID IBM puis cliquez sur **Continuer**.
4.	Entrez votre mot de passe puis cliquez sur **Se connecter**.

La page principale du portail {{site.data.keyword.slportal}} s'affiche.

## Mise à disposition de votre hôte dédié 
Procédez comme suit pour mettre à disposition vos hôtes dédiés.

1.	Cliquez sur l'icône **Unités**.
2.  Cliquez sur le lien **Serveur virtuel dédié à l'heure** ou **Serveur virtuel dédié au mois**. 

   **Remarque :** Les serveurs dédiés sont des serveurs privés.

La page de configuration du serveur Cloud** s'affiche. Sur cette page, vous pouvez commander une instance dédiée associée ou non à un hôte dédié. Des informations supplémentaires sur la commande d'instances sont disponibles à la section [Mise à disposition d'instances d'hôte dédiées](#provision-dedicated-instances).

4.	Cliquez sur le bouton permettant de créer un hôte**** sur le côté droit du formulaire.
5.	Entrez les informations suivantes :
    
    <table>
    <CAPTION>Tableau 1. Sélections de mise à disposition d'hôte dédié</CAPTION>
    <THEAD>
    <TR>
    <th>Zone</th>
    <th>Valeur</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantité</td>
    <td>Entrez le nombre d'hôtes dédiés à commander. Seuls deux hôtes dédiés peuvent être déployés par commande de mise à disposition.</td>
    </tr>
    <tr>
    <td>Emplacement</td>
    <td>Sélectionnez le centre de données {{site.data.keyword.cloud}} dans lequel placer vos hôtes. Pour obtenir la liste des centres de données applicables, voir A propos de.</td>
    </tr>
    <td>Hôte dédié</td>
    <td>Valeur par défaut : 56 coeurs X 242 RAM X 1,2 To</td>
    </tr>
    </TBODY>
    </table>
    
    Le récapitulatif de la commande s'affiche sur le côté droit de la page *Configuration*. 
    
6.  Cliquez sur le bouton **Ajouter à la commande**.
7.  Confirmez vos sélections sur la page *Réservation* et accédez à *Configuration du système avancé d'hôte dédié*.
8.  Entrez les informations suivantes :

    <table>
    <CAPTION>Tableau 2. Configuration système avancée des hôtes dédiés</CAPTION>
    <THEAD>
    <TR>
    <th>Zone</th>
    <th>Valeur</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Sélection du pod</td>
    <td>Cliquez sur la zone déroulante puis sélectionnez le pod dans lequel placer votre hôte dédié.</td>
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

9.  Cliquez sur la case à cocher **Conditions des services Cloud**.
10. Confirmez ou entrez vos informations de paiement puis cliquez sur le bouton **Soumettre**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

    Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page **Détails de l'unité** après la connexion à {{site.data.keyword.Bluemix_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

## Mise à disposition de vos instances d'hôte dédiées
{: #provision-dedicated-instances}
Vous pouvez mettre à disposition vos instances d'hôte dédiées de deux manières, via l'icône **Unités** ou le menu **Unités**.

### Mise à disposition de vos instances d'hôte dédiées via le menu Unités
{: #ordering-dedicated-devices-menu}

La première méthode consiste à mettre à disposition vos instances d'hôte dédiées via le menu **Unités** sur la page principale du portail {{site.data.keyword.slportal}}. Pour cela, suivez la procédure présentée ci-dessous.

1.	Cliquez sur **Unités > Liste des unités**. 
 
    La page *Unités* affiche tous les types d'unités (hôtes dédiés, serveurs virtuels, serveurs Bare Metal et contrôleurs de distribution d'application NetScaler) de votre compte. 

2.	Sélectionnez l'hôte de vos instances d'hôte dédiées en cliquant sur son lien sous **Nom de l'unité**.
    
    L'onglet **Configuration** de la page *Détails de l'unité* s'affiche alors. L'onglet **Tickets** répertorie vos tickets de support actifs et l'onglet **Allocations** affiche votre utilisation de mémoire pour la période de facturation sélectionnée. Pour plus d'informations sur les onglets, voir la section relative à l'utilisation des détails de l'unité pour la gestion de vos instances et de votre hôte dédiés.

3.	Faites défiler jusqu'au cadre **Instances**.

    La fréquence de facturation de votre hôte dédié (à l'heure ou au mois) détermine la facturation de vos instances d'hôte dédiées. Si vous avez des hôtes facturés mensuellement, vous pouvez mettre à disposition à la fois des instances d'hôte facturées à l'heure ou mensuellement. Deux liens sont disponibles (lien d'ajout à l'heure ou d'ajout au mois********) lors de la mise à disposition de vos instances. Les hôtes dédiés facturés à l'heure peuvent uniquement mettre à disposition des instances d'hôte dédiées facturées à l'heure et seul le lien d'ajout à l'heure**** sera affiché. 

4.	Cliquez sur le lien d'ajout à l'heure**** si votre hôte est facturé à l'heure ou mensuellement. Cliquez sur le lien d'ajout au mois**** si votre hôte est facturé mensuellement. La page de configuration de votre serveur Cloud** s'affiche. 

5.	Entrez les informations suivantes :
       
    <table>
    <CAPTION>Tableau 3. Sélection d'instances d'hôte dédiées</CAPTION>
    <THEAD>
    <TR>
    <th>Zone</th>
    <th>Valeur</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantité</td>
    <td>Nombre d'instances d'hôte dédiées à déployer sur un seul hôte.</td>
    </tr>
    <tr>
    <td>Emplacement</td>
    <td>
    <ul>
    <li>Affectation automatique – {{site.data.keyword.Bluemix_notm}} affecte automatiquement votre instance à un hôte sans que vous n'ayez besoin d'en indiquer un. Votre instance est placée dans un centre de données disposant de capacité. Si vous affectez automatiquement votre instance, vous n'utiliserez pas la capacité de vos hôtes dédiés.</li>
    <li>Spécification de l'hôte – Votre hôte dédié associé à votre compte s'affiche sous Hôte dédié. </li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Hôte dédié</td>
    <td>Sélectionnez l'hôte dédié dans la liste où les instances doivent être mises à disposition.</td>
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
    <td>Vous pouvez mettre à disposition jusqu'à quatre disques d'amorçage supplémentaires (SAN ou local) par instance d'hôte dédiée.</td>
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

6.	Cliquez sur le bouton **Ajouter à la commande**.
7.  Entrez les informations suivantes sur la page *Réservation* sous *Configuration système avancée*:

<table>
    <CAPTION>Tableau 4. Configuration système avancée des instances d'hôte dédiés</CAPTION>
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

8.  Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
9. Confirmez ou entrez vos informations de paiement puis cliquez sur le bouton **Soumettre**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.


Une fois vos instances d'hôte dédiées mises à disposition, vous recevez un message électronique.

### Mise à disposition de vos instances d'hôte dédiées via l'icône Unités
La seconde méthode de mise à disposition d'instances d'hôte dédiées consiste à utiliser l'icône **Appareil** sur la page principale du portail {{site.data.keyword.slportal}}. Pour cela, suivez la procédure présentée ci-dessous.

1.	Cliquez sur l'icône **Unités** et sélectionnez **Horaire** ou **Mensuel** sous Serveurs virtuels dédiés.
2.	Suivez la procédure [Mise à disposition de vos instances d'hôte dédiées via le menu Unités](#ordering-dedicated-devices-menu), à partir de l'étape 5.

### Etapes suivantes
Une fois que votre serveur virtuel est mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs virtuels](../vsi/vsi_managing.html).


