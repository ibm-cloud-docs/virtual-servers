---



copyright:
  years: 2017, 2018
lastupdated: "2018-6-18"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Processeurs graphiques (GPU)
Les versions de processeurs graphiques (GPU) sont idéales pour les charges de travail haute performance qui nécessitent une densité de calcul supérieure pour réduire la gestion des ressources et les coûts. Les processeurs graphiques sont parfaits pour les applications de données et de graphiques intenses ou pour développer de nouvelles applications nécessitant des performances rapides.

Optimisé par les processeurs graphiques NVDIA Tesla P100 GPUs, {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” offre à la fois un stockage en bloc et un stockage SSD local. Les versions de GPU suivantes sont disponibles :  

  <table>
<CAPTION>Tableau 1. Versions de GPU</CAPTION>
<THEAD>
<TR>
<th>Version</th>
<th>GPU</th>
<th>RAM GPU (Go)</th>
<th>UC virtuelle</th>
<th>RAM UC virtuelle (Go)</th>
<th>Type de stockage</th>
<th>Disque d'amorçage (Go)</th>
<th>Disque secondaire (Go)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>En bloc (SAN)</td>
<td>25 et 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Unité SSD locale</td>
<td>100</td>
<td>2 x 300</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>En bloc (SAN)</td>
<td>25 et 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Unité SSD locale</td>
<td>100</td>
<td>2 x 600</td></tr>

</TBODY>
</table>

**Remarque :** les versions de GPU sont disponibles dans les centres de données _DAL13_, _LON06_,and _WDC07_.

## Avant de commencer
Vérifiez les conditions requises ci-dessous pour le GPU.

1. Les serveurs virtuels de version de GPU sont uniquement disponibles sur un système d'exploitation prenant en charge le mode d'amorçage HVM (Hardware Virtual Machine). Consultez la liste suivante pour connaître les systèmes d'exploitation prenant en charge le mode d'amorçage HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Des pilotes NVIDIA et des logiciels appropriés doivent être installés. Pour en savoir plus sur les logiciels et les pilotes NVIDIA, voir [Installation de pilotes de GPU et de progiciels](../vsi/vsi_gpu_nvidia_drivers.html).  
**Remarque :** le logiciel que vous installez peut nécessiter des conditions logicielles particulières ainsi que des configurations spécifiques au système d'exploitation.

# Ajout ou suppression de processus graphiques
Vous pouvez changer le nombre de processeurs graphiques sur votre serveur virtuel après votre commande initiale, mais cela dépend du nombre de processeurs graphiques que vous avez mis à disposition. Depuis la commande de mise à disposition, vous disposez de l'une des options suivantes :
- Si un processeur graphique est mis à disposition, vous pouvez en ajouter un autre, ou
- Si deux processeurs graphiques sont mis à disposition, vous pouvez revenir à un seul processeur graphique.
