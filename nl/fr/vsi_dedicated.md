---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Serveurs virtuels dédiés
L'offre d'hôte dédié de l'infrastructure {{site.data.keyword.Bluemix}} est un serveur dédié, à service exclusif et virtualisé. Ainsi, vous pouvez contrôler de manière optimale le placement de la charge de travail et vous disposez d'options flexibles à appliquer après la mise à disposition. Vous pouvez définir dans quel centre de données {{site.data.keyword.cloud}} vos serveur virtuels sont placés et vous assurer qu'ils disposent de capacité en allouant vos hôtes directement à votre compte.
{:shortdesc}

L'offre inclut les fonctions suivantes : 

* Affinité et anti-affinité. Vous pouvez définir des relations hôte/serveur virtuel et serveur virtuel/serveur virtuel, également appelées règles d'affinité et d'anti-affinité. Ces règles permettent de garantir que vos charges de travail sont correctement placées en fonction des exigences de votre charge de travail.
* Gestion après le déploiement. Vous pouvez migrer des serveurs virtuels entre des hôtes dédiés en fonction des exigences de votre charge de travail.
* Visibilité de la charge de travail. Vous pouvez afficher la consommation des ressources (coeur, mémoire RAM et stockage local) pour chaque hôte, ce qui permet un contrôle optimal de la gestion de votre charge de travail.

Vous pouvez choisir un des deux modèles de déploiement suivants : hôtes dédiés et instances dédiées. Les hôtes dédiés permettent de contrôler le placement de la charge de travail et les instances dédiées permettent un isolement à service exclusif. 

**Remarque :** Les instances dédiées ne fournissent pas toutes les fonctions de contrôle proposées par les hôtes dédiés.  Pour plus de détails, voir le tableau suivant. 
<table>
<CAPTION>Tableau 1. Fonctions de contrôle</CAPTION>
<THEAD>
<TR>
<th>Fonction de serveur virtuel dédié</th>
<th>Instances des hôtes dédiés</th>
<th>Instances dédiées</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>Isolement à service exclusif</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td>Contrôle du placement de serveur virtuel</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Visibilité des ressources</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Facturation d'instance</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td>Facturation d'hôte<sup>(1)</sup></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Contrôle ultérieur au déploiement</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Réservations de capacité</td>
<td>X</td>
<td></td>
</tr>
</TBODY>
</table>


<sup>(1)</sup>La tarification de l'hôte inclut le coeur, la mémoire RAM, l'unité SSD locale et les vitesses réseau. La tarification du système d'exploitation Premium, du stockage SAN et des modules complémentaires logiciels s'effectue par instance. La tarification et l'octroi de licence sont établis de manière horaire ou mensuelle.

Prenez en compte les éléments suivants lorsque vous commandez un ou plusieurs hôtes dédiés et instances d'hôte dédiées :

* Emplacement de votre hôte. Vous pouvez effectuer une sélection parmi les centres de données {{site.data.keyword.cloud_notm}} suivants :
      
| Centres de données          ||
| ------------ | ------- | 
|AMS01         |  MON01  |
|AMS03         |  OSL01  |
|CHE01         |  PAR01  |
|DAL05         |  SAO01  |
|DAL06         |  SEO01  |
|DAL09         |  SJC01  |
|DAL10         |  SJC03  |
|DAL12         |  SJC04  |
|DAL13         |  SNG01  | 
|FRA02         |  SYD01  |
|HKG02         |  SYD04  |
|HOU02         |  TOK02  |
|LON02         |  TOR01  |
|LON04         |  WDC01  |
|MEL01         |  WDC04  |
|MEX01         |  WDC06  |
|MIL01         |  WDC07  |
{: caption="Tableau 2. Centres de données pris en charge" caption-side="top"}

* La taille de vos hôtes est déterminée par les charges de travail exécutées. 56 coeurs X 242 Go RAM X 1,2 To constitue la valeur par défaut. 
* Vous pouvez commander deux hôtes à la fois uniquement. Par exemple, si vous avez besoin de six hôtes, vous devez effectuer trois commandes.
* Chaque hôte doit avoir son propre nom unique et vous pouvez affecter automatiquement votre pod.

## Etapes suivantes

Une fois que vous avez défini vos options de déploiement, mettez à disposition votre serveur virtuel. Pour commencer, voir [Mise à disposition d'instances et d'hôtes dédiés](../vsi/vsi_provision_dedicated.html).



  
