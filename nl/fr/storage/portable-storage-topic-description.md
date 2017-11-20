---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# A propos des volumes de stockage portable

Les volumes de stockage portable sont des solutions de stockage auxiliaires exclusivement disponibles sur les serveurs {{site.data.keyword.BluVirtServers_short}}. Il est possible de les connecter à un serveur virtuel à tout moment. Ils constituent également une solution idéale si vous souhaitez transférer des données entre des serveurs virtuels qui existent dans n'importe quel centre de données du réseau {{site.data.keyword.cloud}}. Les volumes de stockage portable sont utiles pour les applications de base de données qui nécessitent un accès à un stockage par blocs, brut non formaté et pour le déplacement de jeux de données volumineux entre des serveurs {{site.data.keyword.BluVirtServers_short}}.

Lorsqu'un volume de stockage portable est connecté à un serveur virtuel d'un centre de données autre que celui du serveur virtuel d'origine, le système interne d'{{site.data.keyword.cloud}} copie le volume vers le réseau de stockage SAN du nouveau centre de données. Le système vérifie ensuite l'intégrité du volume copié et retire le volume portable d'origine du réseau de stockage SAN du centre de données d'origine.

## Etapes suivantes
Pour plus d'informations sur l'utilisation des volumes de stockage portable, reportez-vous aux tâches suivantes : 
* [Accès au stockage portable](../storage/access-portable-storage-screen.html)
* [Edition de la description d'un stockage portable](../storage/edit-description-portable-storage-volume-psv.html)
