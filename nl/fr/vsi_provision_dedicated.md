---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-16"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mise à disposition d'instances et d'hôtes dédiés
{: #ordering-vs-dedicated}

Vous disposez de deux méthodes pour la mise à disposition de vos instances dédiées. Vous pouvez utiliser, soit le catalogue {{site.data.keyword.Bluemix}}, soit le portail {{site.data.keyword.slportal_full}}. Des ID de connexion uniques sont requis pour le catalogue et le portail {{site.data.keyword.slportal}}. Le nom d'utilisateur et le mot de passe du catalogue ne fonctionnent pas pour la connexion au portail et vice-versa. Pour configurer vos données d'identification permettant d'accéder au catalogue {{site.data.keyword.Bluemix_notm}} ou au portail {{site.data.keyword.slportal}}, voir [Inscription à {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-signup#signup)
{:shortdesc}

## Mise à disposition d'instances et d'hôtes dédiés
Vous pouvez mettre à disposition vos instances et hôtes dédiés via {{site.data.keyword.cloud_notm}} ou le portail {{site.data.keyword.slportal}}.

### Mise à disposition d'instances et d'hôtes dédiés via le catalogue IBM Cloud
Pour mettre à disposition vos instances et vos hôtes dédiés via le catalogue {{site.data.keyword.cloud_notm}}, procédez comme suit :

1. Connectez-vous au catalogue [{{site.data.keyword.cloud_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/catalog/){: new_window} à l'aide de vos données d'identification uniques.
2. Dans la section **Infrastructure de calcul**, cliquez sur la vignette **Serveurs virtuels**.
3. Sélectionnez l'option **Serveur virtuel dédié**.
4. Cliquez sur **Créer**.
5. Dans la section **Hôte dédié**, vous pouvez sélectionner **Créer un hôte** afin de créer un nouvel hôte dédié, ou **Spécifier l'hôte** afin d'effectuer une sélection dans votre liste d'hôtes dédiés existants.
6. Complétez toutes les informations pertinentes pour votre hôte dédié et votre instance de serveur virtuel dédiée.
7. Après avoir examiné le récapitulatif de votre commande, cliquez sur la case **Accords de service tiers**.
8. Cliquez sur **Mettre à disposition**.

### Mise à disposition d'instances et d'hôtes dédiés via le portail client
Pour mettre à disposition vos hôtes dédiés et vos instances d'hôte dédiées via le portail {{site.data.keyword.slportal}}, procédez comme suit :

1. Connectez-vous au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.

#### Mise à disposition de votre hôte dédié
Procédez comme suit pour mettre à disposition vos hôtes dédiés :

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
    <td>La configuration par défaut est 56 coeur X 242 RAM X 1,2 To, mais vous pouvez choisir parmi d'autres configurations. </td>
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

#### Mise à disposition de vos instances d'hôte dédiées
{: #provision-dedicated-instances}

Pour mettre à disposition vos instances d'hôte dédiées via le portail {{site.data.keyword.slportal}}, procédez comme suit :

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
    <td>Placement</td>
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

## Etapes suivantes
Une fois que votre serveur virtuel est mis à disposition et est disponible pour être utilisé, vous pouvez configurer vos serveurs virtuels en utilisant le portail {{site.data.keyword.slportal_full}} ou l'API {{site.data.keyword.slapi_full}}. Pour plus d'informations, voir [Configuration des serveurs virtuels](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
