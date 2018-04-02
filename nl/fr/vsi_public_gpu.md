---



copyright:
  years: 2017, 2018
lastupdated: "2018-2-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Processeurs graphiques (GPU)
Les versions de processeurs graphiques (GPU) sont idéales pour les charges de travail haute performance qui nécessitent une densité de calcul supérieure pour réduire la gestion des ressources et les coûts. Les GPU sont parfaites pour les applications de données et de graphique intenses ou pour développer de nouvelles applications nécessitant des performances rapides.

Alimenté par les GPU NVDIA Tesla P100, la famille Accelerated Compute “ac1” de {{site.data.keyword.cloud_notm}} offre à la fois un stockage en bloc (ac1) et un stockage SSD local (acl1). Les versions de GPU suivantes sont disponibles :  

<table>

<caption>Tableau 1. Versions de GPU</caption>

  
<thead>
<td rowspan="4"></td>
  <th colspan="4">Versions de GPU</th>
<tr>
  <th>ac1.8x60</th>
  <th>acl1.8x60</th>
  <th>ac1.16x120</th>
  <th>acl1.16x120</th>
</tr>
</thead>
<TBODY>
<tr>
  <th><b>GPU</b></th>
  <td>1 x P100</td>
  <td>1 x P100</td>
  <td>2 x P100</td>
  <td>2 x P100</td>
</tr>
<tr>
  <th><b>Mémoire RAM du GPU (Go)</b></th>
  <td>16</td>
  <td>16</td>
  <td>32</td>
  <td>32</td>
</tr>

<tr>
  <th><b>UC virtuelle</b></th>
  <td>8</td>
  <td>8</td>
  <td>16</td>
  <td>16</td>
</tr>

<tr>
  <th><b>Mémoire RAM du vCPU (Go)</b></th>
  <td>60</td>
  <td>60</td>
  <td>120</td>
  <td>120</td>
</tr>

<tr>
  <th><b>Type de stockage</b></th>
  <td>En bloc (SAN)</td>
  <td>Unité SSD locale</td>
  <td>En bloc (SAN)</td>
  <td>Unité SSD locale</td>
</tr>

<tr>
  <th><b>Disque d'amorçage (Go)</b></th>
  <td>25 et 100</td>
  <td>100</td>
  <td>25 et 100</td>
  <td>100</td>
</tr>

<tr>
  <th><b>Disque secondaire (Go)</b></th>
  <td>4 x 2000</td>
  <td>2 x 300</td>
  <td>4 x 2000</td>
  <td>2 x 300</td>
</tr>

</TBODY>
</table>


**Remarque :** les versions de GPU sont disponibles dans le centre de données _DAL13_.

## Avant de commencer
Vérifiez les conditions requises ci-dessous pour le GPU.

1. Les serveurs virtuels de la famille de GPU sont uniquement disponibles sur un système d'exploitation prenant en charge le mode d'amorçage des machines virtuelles matérielles (HVM). Consultez la liste suivante pour connaître les systèmes d'exploitation prenant en charge le mode d'amorçage HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Windows 2012 R2
  - Windows 2016

2. Des  pilotes NVIDIA et des logiciels appropriés doivent être installés. Pour en savoir plus sur les logiciels et les pilotes NVIDIA, voir [Installation de pilotes de GPU et de progiciels](../vsi/vsi_gpu_nvidia_drivers.html).

**Remarque :** le logiciel que vous installez peut nécessiter des conditions logicielles particulières ainsi que des configurations spécifiques au système d'exploitation.


