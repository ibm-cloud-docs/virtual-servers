---



copyright:
  years: 2018
lastupdated: "2018-10-31"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Groupes de placement

Grâce aux groupes de placement pour les serveurs {{site.data.keyword.BluVirtServers}}, vous pouvez utiliser des instances publiques afin de générer la haute disponibilité dans un centre de données ou vous pouvez fournir un niveau supplémentaire de tolérance aux pannes dans un déploiement plus grand.
{:shortdesc}

Créez votre groupe de placement, puis affectez jusqu'à 5 nouvelles instances de serveur virtuel. Avec la règle de propagation, chacun de vos serveurs virtuels est mis à disposition sur différents hôtes physiques. 

Pour commencer, procédez comme suit :
 
1. A partir de votre navigateur, ouvrez [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){:new_window} et connectez-vous à votre compte. 
2. Sur la page Groupes de placement, cliquez sur **Ajouter un groupe de placement**.
3. Entrez un nom, une description et un centre de données pour le groupe de placement, puis cliquez sur **Ajouter**.
4. Localisez la section **Commande** et cliquez sur **Unités**.
5. Sur la page Unités, cliquez sur **Horaire** ou **Mensuel** pour l'une des offres de serveur virtuel.
6. Indiquez les autres informations requises et cliquez sur l'option **Ajouter à la commande**. La page de réservation s'ouvre.
7. Vous pouvez sélectionner n'importe quel groupe de placement existant. L'option **Propager** signifie que les instances figureront sur différents matériels physiques. 
8. Pour terminer, cliquez sur **Soumettre une commande**.

##Limitations
Des instances existantes ne peuvent pas être ajoutées à un groupe de placement. Vous pouvez uniquement ajouter une instance de serveur virtuel à un groupe de placement lors de la mise à disposition.  

Pour retirer une instance d'un groupe de placement, vous devez la supprimer ou la récupérer. 
     
## Etapes suivantes

Pour créer et gérer de nouveaux groupes de placement, voir [Gestion des groupes de placement](vsi_managing_placegroup.html).
