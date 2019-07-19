---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestion de scripts de mise à disposition
{: #managing-a-provisioning-script}

Vous pouvez utiliser des scripts de mise à disposition pour spécifier une URL dans un script qui s'exécute sur une unité nouvellement mise à disposition. Tout fichier pouvant être exécuté par le système d'exploitation incluant notamment les fichiers binaires combinés ou les langues prises en charge par le système d'exploitation, peut être un script de mise à disposition. Il n'y a pas de restrictions pour le nom de script ; toutefois, l'utilisation d'une convention de dénomination similaire pour chaque script facilite l'identification. Les scripts de mise à disposition doivent être associés à un nom de domaine complet et accessibles en utilisant les protocoles HTTP ou HTTPS. Le type de protocole qui est utilisé a un impact sur la réponse automatisée du système quand le script de mise à disposition est téléchargé sur le périphérique.  
{:shortdesc}

* L'utilisation d'un **protocole HTTP** nécessite qu'un administrateur exécute le script manuellement après son téléchargement.
* En utilisant des téléchargements de **protocoles HTTPS**, exécutez le script automatiquement, si possible. Si l'URL n'est pas associée à un script valide, le script est téléchargé et aucune action supplémentaire n'a besoin d'être effectuée.

## Avant de commencer
Tout d'abord, accédez au menu Unité et assurez-vous de disposer des droits de compte appropriés pour exécuter les tâches. 

* Accédez au menu Unité de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des droits de compte et accès aux unités requis. Seul le propriétaire de compte ou un utilisateur disposant de droit d'infrastructure classique **Gérer les utilisateurs** peut modifier les droits. 

Pour plus d'informations sur les droits, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux unités](/docs/vsi?topic=virtual-servers-managing-device-access).

## Ajout d'un script de mise à disposition
{: #add-provisioning-script}

1. Dans le menu **Unités**, sélectionnez **Gérer > Scripts de mise à disposition**.
2. Sélectionnez **Ajout de scripts de mise à disposition**. 
3. Entrez un nom d'identification pour le script de mise à disposition dans la zone **Nom**.
4. Entrez le nom de domaine complet qui est associé au script dans la zone **URL**.
5. Cliquez sur **Ajouter** pour ajouter le script de mise à disposition au compte. 

## Edition des détails des scripts de mise à disposition
{: #edit-provisioning-script-details}

1. Dans le menu **Unités**, sélectionnez **Gérer > Scripts de mise à disposition**.
2. Cliquez dans la colonne **Nom** ou **URL** du script de mise à disposition pour ouvrir le script pour éditions.
3. Mettez à jour le nom ou l'URL.
   Quand vous mettez à jour une URL, vous devez utiliser un nom de domaine complet ou le changement n'est pas sauvegardé.
{:note}
4. Cliquez sur l'écran pour sauvegarder la modification.

## Etapes suivantes

Les scripts de mise à disposition qui sont associés à un compte peuvent être modifiés ou retirés à tout moment. Ils sont sauvegardés dans la console {{site.data.keyword.cloud_notm}} jusqu'à ce qu'ils soient retirés et peuvent être associés à toute nouvelle unité commandée via la console {{site.data.keyword.cloud_notm}}. Si le script est associé à une URL HTTP, il est téléchargé sur la nouvelle unité durant la mise à disposition et l'administrateur doit se connecter à l'unité et exécuter le script manuellement. Les scripts qui sont associés à des URL HTTPS sont téléchargés et, le cas échéant, s'exécutent sur la nouvelle unité sans interaction supplémentaire requise. 

Si vous éditez un script, les mises à jour valides s'affichent immédiatement sur l'écran. Les changements effectués dans des scripts de mise à disposition existants n'ont aucun impact sur les sur les unités déjà mises à disposition.

