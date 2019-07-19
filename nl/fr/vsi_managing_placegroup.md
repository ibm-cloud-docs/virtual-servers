---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:note: .note}
{:new_window: target="_blank"}

# Gestion des groupes de placement
{: #vsi_managing_placegroup}

Vous pouvez gérer des groupes de placement à partir de la page de groupes de placement ou de détails de l'unité dans la console {{site.data.keyword.cloud}}.
{:shortdesc}

## Ajout de groupes de placement

Pour ajouter des groupes de placement à partir de la page de groupes de placement, procédez comme suit :
{:shortdesc}

1. Ouvrez la page [Groupes de placement ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. Sur la page de groupes de placement, cliquez sur **Nouveau groupe**.
3. Entrez un nom, un emplacement, un pod et une règle pour le groupe de placement, puis cliquez sur **Créer**.

Des instances existantes ne peuvent pas être ajoutées à un groupe de placement. Vous pouvez uniquement ajouter une instance de serveur virtuel à un groupe de placement lors de la mise à disposition. 
{:note}

## Gestion des groupes de placement

Pour gérer des groupes de placement à partir de la page de groupes de placement, procédez comme suit :
{:shortdesc}

1. Ouvrez la page [Groupes de placement ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. Sous la section de groupe de placement, vous pouvez exécuter plusieurs tâches de gestion :
     * Afficher une liste de groupes de placement et d'un certain nombre d'instances affectées
     * Ajouter un groupe
     * Renommer un groupe
     * Mettre une instance à disposition
     * Supprimer un groupe
     
Vous devez retirer les serveurs affectés du groupe de placement pour que celui-ci puisse être supprimé.
Pour retirer une instance d'un groupe de placement, vous devez la supprimer ou la récupérer.
{:note}
