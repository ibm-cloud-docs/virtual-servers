---
copyright:
  years: 2014, 2018
lastupdated: "2018-10-18"
---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# Scripts de mise à disposition

Un script de mise à disposition est un script qui peut être téléchargé, ou téléchargé et exécuté, sur une unité durant le processus de mise à disposition. Pour les comptes existants, les scripts de mise à disposition sont gérés dans le portail {{site.data.keyword.slportal_full}}. Durant le processus de commande, vous pouvez entrer manuellement des scripts pour les nouveaux comptes ou des scripts qui ne font pas encore l'objet d'un suivi.

Vous pouvez aussi utiliser une image activée initiée par le cloud et fournir des données utilisateur afin d'effectuer automatiquement des tâches de configuration ou exécuter des scripts. Pour plus d'informations, voir [Mise à disposition d'une image activée initiée par le cloud](/docs/infrastructure/image-templates/image_cloud-init.html#provisioning-with-a-cloud-init-enabled-image).
{: tip}

Lors du processus de mise à disposition, les scripts de mise à disposition qui sont associés à une URL HTTP sont téléchargés sur l'unité. Après la mise à disposition, un administrateur doit exécuter le script manuellement sur l'unité. Les scripts qui sont associés à une URL HTTPS sont téléchargés et s'exécutent automatiquement. Les scripts de mise à disposition sont disponibles actuellement sur les systèmes d'exploitation Linux standard (Cent, RHEL, Fedora, Debian ou Ubuntu), Windows et FreeBSD. Les autres systèmes, comme Vyatta, Netscaler, XenServer ou VMware, ne sont pas pris en charge. Le script de mise à disposition peut être tout type de fichier qui est exécuté par le système d’exploitation, incluant les fichiers binaires combinés ou toute langue prise en charge par le système d'exploitation.

Pour plus d'informations, voir [Gestion d'un script de mise à disposition](add-provisioning-script.html).
