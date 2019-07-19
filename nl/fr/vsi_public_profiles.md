---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

keywords: public virtual servers, network traffic, virtual server deployment, profile

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Profils
{: #about-virtual-server-profiles}

Lorsque vous mettez à disposition des instances de serveur virtuel {{site.data.keyword.cloud}}, vous pouvez faire votre choix dans des familles de profils pris en charge. Un profil est une combinaison d'UC virtuelle et de RAM pouvant être instanciée rapidement pour démarrer une instance de serveur virtuel. Dans la console {{site.data.keyword.cloud_notm}}, vous pouvez choisir parmi les configurations de profil les plus courantes ou sélectionner dans une liste de profils la mieux adaptée à vos besoins.
{:shortdesc}

Les familles d'instances de serveur virtuel suivantes sont disponibles. 

En fonction de votre type d'instance, certaines familles peuvent ne pas être disponibles.
{:note}

| Familles | Description                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Balanced](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Choix recommandé pour les charges de travail de cloud communes nécessitant un équilibre entre les performances et l'évolutivité. Utilise un stockage sur réseau. |
| [Stockage Balanced Local](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage) | Idéal pour les charges de travail de base de données volumineuses nécessitant des performances d'E-S élevées avec un temps d'attente très faible. |
| [Compute](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Choix recommandé pour les charges de travail de trafic Web modéré à élevé. |
| [Memory](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Choix recommandé pour les charges de travail d'analyse en temps réel et de mise en cache de mémoire. |
| [GPU](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#gpu)  | Choix optimal pour les charges de travail à performances élevées. |
{: caption="Tableau 1. Sélections de familles de serveurs virtuels publics " caption-side="top"}

Certaines de ces familles sont également disponibles pour IBM Cloud Virtual Servers for VPC. Pour plus d'informations, voir [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen).
{:tip}

## Balanced
{: #balanced}

Les profils Balanced (avec stockage réseau) sont idéaux pour les charges de travail cloud courantes qui exigent un équilibre entre performances et évolutivité. Les performances réseau vont de standard à premium.

L'offre est disponible dans les profils suivants :

| Profil   | UC virtuelle    | RAM     | Type de stockage |
| --------- | ------- | ------- | ------------ |
| B1.1x2    | 1       | 2 Go    | SAN          |
| B1.1x4    | 1       | 4 Go    | SAN          |
| B1.2x4    | 2       | 4 Go    | SAN          |
| B1.2x8    | 2       | 8 Go    | SAN          |
| B1.4x8    | 4       | 8 Go    | SAN          |
| B1.4x16   | 4       | 16 Go   | SAN          |
| B1.8x16   | 8       | 16 Go   | SAN          |
| B1.8x32   | 8       | 32 Go   | SAN          |
| B1.16x32  | 16      | 32 Go   | SAN          |
| B1.16x64  | 16      | 64 Go   | SAN          |
| B1.32x64  | 32      | 64 Go   | SAN          |
| B1.32x128 | 32      | 128 Go  | SAN          |
| B1.48x192 | 48      | 192 Go  | SAN          |
{: caption="Tableau 2. Profils Balanced avec stockage en réseau" caption-side="top"}

### Remarques sur le stockage

* Disque d'amorçage principal SAN (25 ou 100 Go) avec des disques supplémentaires disponibles, jusqu'à 2 To chacun (cinq disques autorisés au total).
* La tarification des serveurs virtuels publics utilisant le stockage SAN inclut l'unité centrale virtuelle, la mémoire et un disque d'amorçage principal. Le prix des disques supplémentaires dépend de la taille du disque et de la quantité sélectionnée.  

Les profils Balanced (avec stockage en réseau) sont disponibles dans tous les centres de données.

Tous les systèmes d'exploitation pris en charge (RHEL, CentOS, Windows, Ubuntu et autres), les bases de données prises en charge et les modules logiciels complémentaires sont également disponibles avec cette offre. 

## Stockage Balanced Local
{: #balanced-local-storage}

Les profils de stockage local Balanced sont principalement destinés aux charges de travail de base de données volumineuses nécessitant des performances d'E-S élevées avec un temps d'attente très faible. Les performances réseau vont de standard à premium.

Cette offre est disponible dans différents profils et centres de données, avec les options de stockage local suivantes :

* [Unité de disque dur locale ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#HDD)
* [Unité SSD locale ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#SSD)

### Unité de disque dur locale
{: #HDD}
 
<table>
<CAPTION>Tableau 3. Profils de stockage local Balanced sur des unités de disque dur locales</CAPTION>
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

#### Remarques sur le stockage
* <sup>(*)</sup>Les profils locaux Balanced incluent un disque d'amorçage de stockage local de 100 Go. Vous pouvez ensuite sélectionner un second disque (options présentées dans le tableau 3). Tout disque local supplémentaire est facultatif. Si vous avez besoin de plus de 500 Go, deux disques supplémentaires sont requis (par exemple, 8 coeurs exigent 2 x 250 Go de stockage local).
*	Le stockage local maximal est limité par les coeurs. 
*	Le stockage Balanced Local est disponible dans le monde entier. Le type de stockage (unité SSD locale ou unité de disque dur locale) dépend toutefois de l'emplacement du centre de données. 
*	Vous ne pouvez pas déconnecter les disques principaux ou secondaires.

Les centres de données suivants prennent en charge les serveurs virtuels de stockage Balanced local sur unité de disque dur locale :

| Centres de données disponibles - Unité de disque dur locale |       |
| ---------------------- | ----- |
| Dallas (DAL01)         | Dallas (DAL05)   |
| Dallas (DAL06)         | Houston (HOU02)  |
| Seattle (SEA01)        | San Jose (SJC01) |
| Washington, DC (WDC01) |                  |
{: class="simple-tab-table"}
{: caption="Tableau 4. Centres de données disponibles (unité de disque dur locale) - Amériques " caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd1}
{: tab-title="Americas"}

| Centres de données disponibles - Unité de disque dur locale |
| ---------------------- |
| Amsterdam (AMS01)      |
{: class="simple-tab-table"}
{: caption="Tableau 5. Centres de données disponibles (unité de disque dur locale) - Europe" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd2}
{: tab-title="Europe"}

| Centres de données disponibles - Unité de disque dur locale |
| ---------------------- |
| Hong Kong (HKG02)      | 
| Singapour (SNG01)|
{: class="simple-tab-table"}
{: caption="Tableau 6. Centres de données disponibles (unité de disque dur locale) - Asie-Pacifique " caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd3}
{: tab-title="Asia-Pacific"}

Tous les systèmes d'exploitation pris en charge (RHEL, CentOS, Windows, Ubuntu et autres), les bases de données prises en charge et les modules logiciels complémentaires sont également disponibles avec cette offre.  

### Unité SSD locale 
{: #SSD}

<table>
<CAPTION>Tableau 7. Profils de stockage local Balanced sur des unités SSD locales</CAPTION>
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

#### Remarques sur le stockage
* <sup>(*)</sup>Les profils locaux Balanced incluent un disque d'amorçage de stockage local de 100 Go. Vous pouvez ensuite sélectionner un second disque (options présentées dans le tableau ci-dessus). Tout disque local supplémentaire est facultatif. Si vous avez besoin de plus de 500 Go, deux disques supplémentaires sont requis (par exemple, 8 coeurs exigent 2 x 250 Go de stockage local).
*	Le stockage local maximal est limité par les coeurs. 
*	Le stockage Balanced Local est disponible dans le monde entier. Le type de stockage (unité SSD locale ou unité de disque dur locale) dépend toutefois de l'emplacement du centre de données. 
*	Vous ne pouvez pas déconnecter les disques principaux ou secondaires.

Les centres de données suivants prennent en charge les serveurs virtuels de stockage local Balanced sur unité SSD locale :

| Centres de données disponibles - Unité SSD locale |        |
| ---------------------------------- | ------ |
| Dallas (DAL09)                     | Dallas (DAL10)         |
| Dallas (DAL12)                     | Dallas (DAL13)         |
| Queretaro (MEX01)                  | Montréal (MON01)|
| Sao Paulo (SAO01)                  | San Jose (SJC03)       |
| San Jose (SJC04)                   | Toronto (TOR01)        |
| Washington, DC (WDC04)             | Washington, DC (WDC06) |
| Washington, DC (WDC07)             |                        |
{: class="simple-tab-table"}
{: caption="Tableau 8. Centres de données disponibles (unité SSD locale) - Amériques " caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd1}
{: tab-title="Americas"}

| Centres de données disponibles - Unité SSD locale |       |
| ---------------------------------- | ----- |
| Amsterdam (AMS03)                  | Francfort (FRA02)|
| Londres (LON02)                    | Londres (LON04)    |
| Londres (LON06)                    | Milan (MIL01)     |
| Oslo (OSL01)                       | Paris (PAR01)     |
{: class="simple-tab-table"}
{: caption="Tableau 9. Centres de données disponibles (unité SSD locale) - Europe " caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd2}
{: tab-title="Europe"}

| Centres de données disponibles - Unité SSD locale |       |
| ---------------------------------- | ----- |
| Chennai (CHE01)                    | Melbourne (MEL01) |
| Seoul (SEO01)                      | Sydney (SYD01)    |
| Sydney (SYD04)                     | Tokyo (TOK02)     |
{: class="simple-tab-table"}
{: caption="Tableau 10. Centres de données disponibles (unité SSD locale) - Asie-Pacifique " caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd3}
{: tab-title="Asia-Pacific"}

Tous les systèmes d'exploitation pris en charge (RHEL, CentOS, Windows, Ubuntu et autres), les bases de données prises en charge et les modules logiciels complémentaires sont également disponibles avec cette offre.

## Compute
{: #compute}

Les profils Compute sont recommandés pour les charges de travail avec des demandes d'unité centrale importantes, comme les fortes charges de travail de trafic Web, le traitement de lots de production et les serveurs Web frontaux.

L'offre est disponible dans les profils suivants :

| Profil      | UC virtuelle     | RAM       | Type de stockage |
| ------------ | -------- | --------- | ------------ |
| C1.1x1       | 1        | 1 Go      | SAN          |
| C1.2x2       | 2        | 2 Go      | SAN          |
| C1.4x4       | 4        | 4 Go      | SAN          |
| C1.8x8       | 8        | 8 Go      | SAN          |
| C1.16x16     | 16       | 16 Go     | SAN          |
| C1.32x32     | 32       | 32 Go     | SAN          |
{: caption="Tableau 11. Profils Compute " caption-side="top"}

### Remarques sur le stockage
* Disque d'amorçage principal SAN (25 ou 100 Go) avec des disques supplémentaires disponibles, jusqu'à 2 To chacun (cinq disques autorisés au total).
* La tarification des serveurs virtuels publics utilisant le stockage SAN inclut l'unité centrale virtuelle, la mémoire et un disque d'amorçage principal. Le prix des disques supplémentaires dépend de la taille du disque et de la quantité sélectionnée.  

Les profils Compute sont disponibles dans tous les centres de données.

Tous les systèmes d'exploitation pris en charge (RHEL, CentOS, Windows, Ubuntu et autres), les bases de données prises en charge et les modules logiciels complémentaires sont également disponibles avec cette offre.

## Memory
{: #memory}

Les profils Memory sont recommandés pour les charges de travail intensives de mémoire (mise en cache importantes ou analyse en mémoire, par exemple).

L'offre est disponible dans les profils suivants :

| Profil      | UC virtuelle     | RAM       | Type de stockage |
| ------------ | -------- | --------- | ------------ |
| M1.1x8       | 1        | 8 Go      | SAN          |
| M1.2x16      | 2        | 16 Go     | SAN          |
| M1.4x32      | 4        | 32 Go     | SAN          |
| M1.8x64      | 8        | 64 Go     | SAN          |
| M1.16x128    | 16       | 128 Go    | SAN          |
| M1.30x240    | 30       | 240 Go    | SAN          |
| M1.48x384    | 48       | 384 Go    | SAN          |
| M1.56x448    | 56       | 448 Go    | SAN          |
| M1.64x512    | 64       | 512 Go    | SAN          |
{: caption="Tableau 12. Profils Memory" caption-side="top"}

### Remarques sur le stockage
* Disque d'amorçage principal SAN (25 ou 100 Go) avec des disques supplémentaires disponibles, jusqu'à 2 To chacun (5 disques autorisés au total).
* La tarification des serveurs virtuels publics utilisant le stockage SAN inclut l'unité centrale virtuelle, la mémoire et un disque d'amorçage principal. Le prix des disques supplémentaires dépend de la taille du disque et de la quantité sélectionnée.  

Les profils Memory sont disponibles dans tous les centres de données.

Tous les systèmes d'exploitation pris en charge (RHEL, CentOS, Windows, Ubuntu et autres), les bases de données prises en charge et les modules logiciels complémentaires sont également disponibles avec cette offre.

## Processeurs graphiques (GPU)
{: #gpu}

Les profils de processeur graphique sont particulièrement adaptés aux charges de travail hautes performances qui nécessitent une plus grande densité de calcul pour réduire la gestion des ressources et les coûts ainsi qu'aux processus d'intelligence artificielle, aux applications graphiques et de données intenses, ou au développement de nouvelles applications exigeant des performances rapides.

Alimentés par les processeurs graphiques NVDIA Tesla, les versions {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” et "ac2" offrent toutes deux un stockage SSD en bloc et local. Les profils de processeur graphique suivants sont disponibles :  

<table>
<CAPTION>Tableau 13. Profils de processeur graphique P100</CAPTION>
<THEAD>
<TR>
<th>Profil</th>
<th>Processeurs graphiques (GPU)</th>
<th>RAM GPU (Go)</th>
<th>UC virtuelle</th>
<th>RAM UC virtuelle (Go)</th>
<th>Type de stockage</th>
<th>Disque d'amorçage (Go)</th>
<th>Disques secondaires (2 et 3) (Go)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>En bloc (SAN)</td>
<td>25</td>
<td>Aucun</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD local ou SAN</td>
<td>100</td>
<td>Aucun (SAN)<br>300 (local)</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>En bloc (SAN)</td>
<td>25</td>
<td>Aucun</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD local ou SAN</td>
<td>100</td>
<td>Aucun (SAN)<br>600 (local)</td></tr>

</TBODY>
</table>

Les profils de processeur graphique P100 sont disponibles dans les centres de données _DAL13_, _LON06_ et _WDC07_.
{: note}

<table>
<CAPTION>Tableau 14. Profils de processeur graphique V100</CAPTION>
<THEAD>
<TR>
<th>Profil</th>
<th>Processeurs graphiques (GPU)</th>
<th>RAM GPU (Go)</th>
<th>UC virtuelle</th>
<th>RAM UC virtuelle (Go)</th>
<th>Type de stockage</th>
<th>Disque d'amorçage (Go)</th>
<th>Disques secondaires (2 et 3) (Go)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>En bloc (SAN)</td>
<td>25</td>
<td>Aucun</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD local ou SAN</td>
<td>100</td>
<td>Aucun (SAN)<br>300 (local)</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>En bloc (SAN)</td>
<td>25</td>
<td>Aucun</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD local ou SAN</td>
<td>100</td>
<td>Aucun (SAN)<br>600 (local)</td></tr>

</TBODY>
</table>

Les profils de processeur graphique V100 sont disponibles dans les centres de données _DAL10_, _DAL12_, _LON04_ et _WDC07_.
{: note}

### Conditions requises du GPU 
Vérifiez les conditions requises ci-dessous pour le GPU.

1. Les serveurs virtuels de profil de processeur graphique sont disponibles uniquement sur un système d'exploitation prenant en charge le mode d'amorçage HVM (Hardware Virtual Machine). Consultez la liste suivante pour connaître les systèmes d'exploitation prenant en charge le mode d'amorçage HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Des pilotes NVIDIA et des logiciels appropriés doivent être installés. Pour en savoir plus sur les logiciels et les pilotes NVIDIA, voir [Installation de pilotes de GPU et de progiciels](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages).  

Le logiciel que vous installez peut nécessiter des conditions logicielles particulières ainsi que des configurations spécifiques au système d'exploitation.
{: note}

### Ajout ou suppression d'unités GPU 
Vous pouvez changer le nombre de processeurs graphiques sur votre serveur virtuel après votre commande initiale, mais cela dépend du nombre de processeurs graphiques que vous avez mis à disposition. 

- Si un processeur graphique est mis à disposition, vous pouvez en ajouter un autre, ou
- Si deux processeurs graphiques sont mis à disposition, vous pouvez revenir à un seul processeur graphique.

