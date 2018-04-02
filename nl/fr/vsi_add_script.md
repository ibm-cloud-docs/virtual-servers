---



copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Ajout d'un script de mise à disposition personnalisé 
{: #adding-post-script}

Les scripts de mise à disposition personnalisés permettent aux utilisateurs d'indiquer une URL d'un script qui s'exécute sur un terminal nouvellement mis à disposition. Vous pouvez publier et gérer des scripts de mise à disposition personnalisés dans le portail {{site.data.keyword.slportal_full}}.
{:shortdesc}

Lors de la commande d'un terminal, vous pouvez sélectionner un script de mise à disposition personnalisé s'il a été publié sur l'écran Scripts de mise à disposition du portail {{site.data.keyword.slportal}}. Si aucun script n'a été ajouté, vous pouvez indiquer une URL. Tout fichier pouvant être exécuté par le système d'exploitation incluant notamment les fichiers binaires combinés ou les langues prises en charge par le système d'exploitation, peut être un script de mise à disposition. Procédez comme suit pour ajouter un script de mise à disposition personnalisé sur le portail {{site.data.keyword.slportal}}.

**Remarque :** Cette fonction est actuellement disponible uniquement pour les systèmes d'exploitation de type Linux et Unix.

## Ajout d'un script de mise à disposition

1. Dans le menu **Unités** du portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window}, sélectionnez **Gérer** > **Scripts de mise à disposition**.
2. Cliquez sur **Ajout de scripts de mise à disposition**.
4. Dans la zone Nom, entrez un nom de script unique.
5. Dans la zone URL, entrez l'URL exacte à associer au script.
6. Cliquez sur **Ajouter**.

## Etapes suivantes
Une fois qu'une commande contenant un script de mise à disposition est soumise, le terminal est mis à disposition. Avant que ce dernier ne devienne disponible, le script spécifié est téléchargé dans le terminal. L'origine du script de mise à disposition détermine le comportement lors de la dernière étape du processus de mise à disposition. Si le script est disponible à partir d'une URL HTTPS, ce dernier est téléchargé et s'exécute sans qu'aucune intervention supplémentaire de l'utilisateur ne soit requise. Si le script est fourni via HTTP, il est téléchargé uniquement. Pour les scripts fournis via HTTP, l'administrateur doit se connecter au terminal et exécuter le script manuellement.
