---

copyright:
  years: 2014, 2018
lastupdated: "2018-04-27"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestion d'un script de mise à disposition
{: #managing-a-provisioning-script}

Utilisez des scripts de mise à disposition pour spécifier une URL dans un script à exécuter sur une unité nouvellement mise à disposition. Il n'y a pas de restrictions pour le nom de script ; toutefois, l'utilisation d'une convention de dénomination similaire pour chaque script facilite l'identification. Les scripts de mise à disposition doivent être associés à un nom de domaine complet et accessibles en utilisant les protocoles HTTP ou HTTPS. Le type de protocole qui est utilisé a un impact sur la réponse automatisée du système quand le script de mise à disposition est téléchargé sur le périphérique.

* L'utilisation d'un **protocole HTTP** nécessite qu'un administrateur exécute le script manuellement après son téléchargement.
* En utilisant des téléchargements de **protocoles HTTPS**, exécutez le script automatiquement, si possible. Si l'URL n'est pas associée à un script exécutable, le script est téléchargé et aucune action supplémentaire n'a besoin d'être effectuée.

## Accès à l'écran des scripts de mise à disposition
1. Entrez dans le portail [{{site.data.keyword.slportal_full}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} avec vos données d'identification unique.
2. Sélectionnez **Unités > Gérer > Scripts de mise à disposition** dans la navigation pour accéder à l'écran des scripts de mise à disposition.


## Ajout d'un script de mise à disposition
{: #add-provisioning-script}

1. Dans l'écran **Scripts de mise à disposition** du portail {{site.data.keyword.slportal}}, cliquez sur **Ajout de scripts de mise à disposition** en haut de l'écran.
* Entrez un **nom d'identification** pour le script de mise à disposition dans la zone **Nom**.
* Entrez le **nom de domaine complet** qui est associé au script dans la zone **URL**.
* Cliquez sur **Ajouter** pour ajouter le script de mise à disposition au compte. Cliquez sur **Annuler** pour annuler l'action.

## Edition des détails des scripts de mise à disposition

1. Dans l'écran **Scripts de mise à disposition** du portail {{site.data.keyword.slportal}}, cliquez dans la colonne **Nom** ou **URL** du script de mise à disposition pour ouvrir le script pour éditions.
3. Mettez à jour le nom ou l'URL.
  * **Remarque :** quand vous mettez à jour une URL, vous devez utiliser un nom de domaine complet ou le changement n'est pas sauvegardé.
4. Cliquez sur l'écran pour sauvegarder la modification.

## Etapes suivantes

Les scripts de mise à disposition qui sont associés à un compte peuvent être modifiés ou retirés à tout moment. Ils sont sauvegardés dans le portail {{site.data.keyword.slportal}} jusqu'à ce qu'ils soient retirés et peuvent être associés à toute nouvelle unité commandée via le portail {{site.data.keyword.slportal}}. Si le script est associé à une URL HTTP, il est téléchargé sur la nouvelle unité durant la mise à disposition. Les scripts qui sont associés avec des URL HTTPS sont téléchargés et, le cas échéant, s'exécutent sur la nouvelle unité.

Une fois que vous avez édité un script, les mises à jour valides s'affichent immédiatement sur l'écran. Les changements effectués dans des scripts de mise à disposition existants n'ont aucun impact sur les sur les unités déjà mises à disposition.
