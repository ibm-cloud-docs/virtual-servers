---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Mise à disposition d'instances dédiées
{: #provisioning-dedicated-instances}

Vous disposez de deux méthodes pour la mise à disposition de vos instances dédiées. Vous pouvez utiliser, soit le catalogue {{site.data.keyword.Bluemix}}, soit le portail {{site.data.keyword.slportal_full}}. Des ID de connexion uniques sont requis pour le catalogue et le portail {{site.data.keyword.slportal}}. Le nom d'utilisateur et le mot de passe du catalogue ne fonctionnent pas pour la connexion au portail et vice-versa. Pour configurer vos données d'identification permettant d'accéder au catalogue {{site.data.keyword.Bluemix_notm}} ou au portail {{site.data.keyword.slportal}}, voir [Inscription à {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-signup#signup)
{:shortdesc}

## Mise à disposition d'instances de serveur virtuel dédiées
{: #provision-dedicated-instances}
Vous pouvez mettre à disposition votre instance de serveur virtuel dédiée via le catalogue {{site.data.keyword.cloud_notm}} ou le portail {{site.data.keyword.slportal}}.

### Mise à disposition d'une instance de serveur virtuel dédiée via le catalogue IBM Cloud
Pour mettre à disposition une instance de serveur virtuel dédiée via le catalogue {{site.data.keyword.cloud_notm}}, procédez comme suit :

  1. Connectez-vous au catalogue [{{site.data.keyword.cloud_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/catalog/){: new_window} à l'aide de vos données d'identification uniques.
  2. Dans la section **Infrastructure de calcul**, cliquez sur la vignette **Serveurs virtuels**.
  3. Sélectionnez l'option **Serveur virtuel dédié**.
  4. Cliquez sur **Créer**.
  5. Dans la section **Hôte dédié**, sélectionnez **Affectation automatique**. {{site.data.keyword.cloud_notm}} affecte automatiquement votre instance à un hôte dans votre centre de données sélectionné.

     **Remarque** : pour les hôtes dédiés, sélectionnez **Spécifier l'hôte** ou **Créer un hôte**. Pour plus d'informations sur les hôtes dédiés et les instances d'hôte dédiées, voir [Serveurs virtuels dédiés](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers).

  5. Complétez toutes les informations pertinentes pour votre instance de serveur virtuel dédiée.
  6. Après avoir examiné le récapitulatif de votre commande, cliquez sur la case **Accords de service tiers**.
  7. Cliquez sur **Mettre à disposition**.

### Mise à disposition d'une instance de serveur virtuel dédiée via le portail client
Pour mettre à disposition une instance de serveur virtuel dédiée via le portail {{site.data.keyword.slportal}}, procédez comme suit :

1. Connectez-vous au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
2. Localisez la section **Commande** et cliquez sur **Unités**. La fenêtre **Commander des services et des produits SoftLayer** s'affiche.
3.  Sélectionnez **Horaire** ou **Mensuel** sous Serveurs virtuels dédiés. La page de configuration de votre serveur Cloud** s'affiche.

4.	Entrez les informations suivantes :

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
    <td>Placement</td>
    <td>
    <ul>
    <li>Affectation automatique – {{site.data.keyword.Bluemix_notm}} affecte automatiquement votre instance à un hôte dans votre centre de données sélectionné.</li>
    <li>Spécification d'hôte – Utilisation avec des instances d'hôte dédiées. Pour plus d'informations sur les hôtes dédiés et les instances d'hôte dédiées, voir [Serveurs virtuels dédiés](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers).</li>
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

5.	Cliquez sur le bouton **Ajouter à la commande**. La page Réservation s'affiche.
6.  Entrez les informations suivantes sur la page *Réservation* sous *Configuration système avancée*:

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

7.  Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
8. Confirmez ou entrez vos informations de paiement puis cliquez sur le bouton **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

    Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page **Détails de l'unité** après la connexion à {{site.data.keyword.Bluemix_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

## Etapes suivantes
Une fois que votre serveur virtuel est mis à disposition et est disponible pour être utilisé, vous pouvez configurer vos serveurs virtuels en utilisant le portail {{site.data.keyword.slportal_full}} ou l'API {{site.data.keyword.slapi_full}}. Pour plus d'informations, voir [Configuration des serveurs virtuels](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
