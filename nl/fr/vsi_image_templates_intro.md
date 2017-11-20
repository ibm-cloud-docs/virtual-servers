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

# Modèles d'image
Avec les modèles d'image des serveurs {{site.data.keyword.BluVirtServers}}, vous pouvez capturer une image du terminal afin de répliquer rapidement sa configuration avec un nombre retreint de modifications dans le processus de commande. 
{:shortdesc}

Les modèles d'image standard fournissent une option d'image pour tous les serveurs {{site.data.keyword.BluVirtServers_short}}, quel que soit le système d'exploitation. Les modèles d'image standard permettent de capturer une image d'un serveur virtuel existant et d'en créer une nouvelle en fonction de l'image capturée. Les modèles d'image standard ne sont pas compatibles avec les serveurs Bare  Metal.

## Mode de fonctionnement des modèles d'image
Les deux principales actions des modèles d'image sont la création et le déploiement. Lorsque vous demandez la création d'une image, le système automatisé de {{site.data.keyword.BluSoftlayer_full}} fait passer votre serveur hors ligne. Lorsque le serveur est hors ligne, une sauvegarde compressée de vos données est créée, les informations de configuration sont enregistrées et le modèle d'image est stocké dans le réseau SAN de {{site.data.keyword.BluSoftlayer_notm}}. Lors du déploiement du modèle d'image, le système automatisé crée un nouveau serveur en fonction des données rassemblées à partir de l'image sélectionné. Le processus de déploiement effectue des réglages de volume, restaure les données copiées puis réalise des modifications de configuration finales (configurations réseau, par exemple) pour le nouvel hôte. 

## Images privées

Les images privées sont des images créées par un utilisateur sur le compte, ou des images créées sur un autre compte et partagées. Par défaut, toutes les images créées sont privées. 

## Images publiques

Les images publiques sont des machines préconfigurées publiées par {{site.data.keyword.BluSoftlayer_notm}} ou rendues publiques par des clients et disponibles pour une utilisation par tous les clients de {{site.data.keyword.BluSoftlayer_notm}}. Les serveurs virtuels mis à disposition via des modèles d'image publique sont généralement configurés pour des performances optimales, avec des combinaisons spécifiques de plusieurs spécifications de configuration.

Pour plus d'informations sur les modèles d'image, voir [Initiation aux modèles d'image](/docs/infrastructure/image-templates/image_index.html).
