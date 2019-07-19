---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Stockage Balanced Local
{: #balanced-local-storage}

Les profils de stockage local Balanced sont conçus pour les clusters de base de données de grande taille exigeant des performances d'E-S élevées à faible temps d'attente. Les performances sont plus élevées car les ressources ne sont pas trop sollicitées. Les performances réseau vont de standard à premium.

Cette offre est disponible dans différents profils et centres de données, avec les options de stockage local suivantes :

* [Unité de disque dur locale](/docs/vsi?topic=virtual-servers-HDD#HDD)
* [Unité SSD locale](/docs/vsi?topic=virtual-servers-SSD#SSD)

## Unité de disque dur locale {: #HDD}

<table>
<CAPTION>Tableau 1. Profils de stockage local Balanced sur des unités de disque dur locales</CAPTION>
<THEAD>
<TR>
<th>Profil</th>
<th>UC virtuelle</th>
<th>RAM</th>
<th>Disques secondaires<sup>(*)</sup></th>
<th>Type de stockage</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2 Go</td>
<td>25, 100 Go</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4 Go</td>
<td>25, 100 Go</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4 Go</td>
<td>100, 200 Go</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8 Go</td>
<td>100, 200 Go</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8 Go</td>
<td>150, 300 Go</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16 Go</td>
<td>150, 300 Go</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16 Go</td>
<td>250 Go, (2 x 250 Go)</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32 Go</td>
<td>250 Go, (2 x 250 Go)</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32 Go</td>
<td>300 Go, (2 x 300 Go)</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64 Go</td>
<td>300 Go, (2 x 300 Go)</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64 Go</td>
<td>400 Go, (2 x 400 Go)</td>
<td>Unité de disque dur locale</td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128 Go</td>
<td>400 Go, (2 x 400 Go)</td>
<td>Unité de disque dur locale</td>
</tr>
</TBODY>
</table>

**Remarques sur le stockage :**
* <sup>(*)</sup>Les profils locaux Balanced incluent un disque d'amorçage de stockage local de 100 Go. Vous pouvez ensuite sélectionner un second disque (options présentées dans le tableau ci-dessus). Tout disque local supplémentaire est facultatif. Si vous avez besoin de plus de 500 Go, deux disques supplémentaires sont requis (par exemple, 8 coeurs exigent 2 x 250 Go de stockage local).
*	Le stockage local maximal est limité par les coeurs.
*	Le stockage Balanced Local est disponible dans le monde entier. Le type de stockage (unité SSD locale ou unité de disque dur locale) dépend toutefois de l'emplacement du centre de données.
*	Vous ne pouvez pas déconnecter les disques principaux ou secondaires.

Les centres de données suivants prennent en charge les serveurs virtuels de stockage Balanced Local sur unité de disque dur locale :

|Centres de données (unité de disque dur locale) |        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   |
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02        |        |  
{: caption="Tableau 1. Centres de données pris en charge (unité de disque dur locale)" caption-side="top"}

Tous les systèmes d'exploitation pris en charge (RHEL, CentOS, Windows, Ubuntu et autres), les bases de données prises en charge et les modules logiciels complémentaires sont également disponibles avec cette offre.  

## Unité SSD locale {: #SSD}
<table>
<CAPTION>Tableau 1. Profils de stockage local Balanced sur des unités SSD locales</CAPTION>
<THEAD>
<TR>
<th>Profil</th>
<th>UC virtuelle</th>
<th>RAM</th>
<th>Disques secondaires<sup>(*)</sup></th>
<th>Type de stockage</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2 Go</td>
<td>25, 100 Go</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4 Go</td>
<td>25, 100 Go</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4 Go</td>
<td>100, 200 Go</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8 Go</td>
<td>100, 200 Go</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8 Go</td>
<td>150, 300 Go</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16 Go</td>
<td>150, 300 Go</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16 Go</td>
<td>250 Go, (2 x 250 Go)</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32 Go</td>
<td>250 Go, (2 x 250 Go)</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32 Go</td>
<td>300 Go, (2 x 300 Go)</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64 Go</td>
<td>300 Go, (2 x 300 Go)</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64 Go</td>
<td>400 Go, (2 x 400 Go)</td>
<td>Unité SSD locale</td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128 Go</td>
<td>400 Go, (2 x 400 Go)</td>
<td>Unité SSD locale</td>
</tr>
</TBODY>
</table>

**Remarques sur le stockage :**
* <sup>(*)</sup>Les profils locaux Balanced incluent un disque d'amorçage de stockage local de 100 Go. Vous pouvez ensuite sélectionner un second disque (options présentées dans le tableau ci-dessus). Tout disque local supplémentaire est facultatif. Si vous avez besoin de plus de 500 Go, deux disques supplémentaires sont requis (par exemple, 8 coeurs exigent 2 x 250 Go de stockage local).
*	Le stockage local maximal est limité par les coeurs.
*	Le stockage Balanced Local est disponible dans le monde entier. Le type de stockage (unité SSD locale ou unité de disque dur locale) dépend toutefois de l'emplacement du centre de données.
*	Vous ne pouvez pas déconnecter les disques principaux ou secondaires.

Les centres de données suivants prennent en charge les serveurs virtuels de stockage local Balanced sur unité SSD locale :

|Centres de données (unité SSD locale) |        |         |
|------- |------  |------ |
|AMS03   |LON06   |SJC03  |
|CHE01   |MEL01   |SJC04  |
|DAL09   |MEX01   |SYD01  |
|DAL10   |MIL01   |SYD04  |
|DAL12   |MON01   |TOK02  |       
|DAL13   |OSL01   |TOR01  |
|FRA02   |PAR01   |WDC04  |
|LON02   |SAO01   |WDC06  |
|LON04   |SEO01   | WDC07 |
{: caption="Tableau 2. Centres de données pris en charge (unité SSD locale)" caption-side="top"}

Tous les systèmes d'exploitation pris en charge (RHEL, CentOS, Windows, Ubuntu et autres), les bases de données prises en charge et les modules logiciels complémentaires sont également disponibles avec cette offre.  
