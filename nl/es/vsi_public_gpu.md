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

# GPU
Los tipos de GPU son adecuados para cargas de trabajo de alto rendimiento que requieren más densidad de cálculo para reducir los costes y la gestión de los recursos. Las GPU son ideales para aplicaciones de gran cantidad de datos y gráficos, o para desarrollar nuevas aplicaciones que requieren un rápido rendimiento.

Basada en las GPU NVDIA Tesla P100, la familia {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” ofrece almacenamiento SSD local (acl1) y en bloque (ac1). Puede elegir entre los siguientes tipos de GPU disponibles:  

<table>

<caption>Tabla 1. Tipos de GPU</caption>

  
<thead>
<td rowspan="4"></td>
  <th colspan="4">Tipos de GPU</th>
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
  <th><b>RAM de GPU (GB)</b></th>
  <td>16</td>
  <td>16</td>
  <td>32</td>
  <td>32</td>
</tr>

<tr>
  <th><b>vCPU</b></th>
  <td>8</td>
  <td>8</td>
  <td>16</td>
  <td>16</td>
</tr>

<tr>
  <th><b>RAM de vCPU (GB)</b></th>
  <td>60</td>
  <td>60</td>
  <td>120</td>
  <td>120</td>
</tr>

<tr>
  <th><b>Tipo de almacenamiento</b></th>
  <td>Bloque (SAN)</td>
  <td>SSD local</td>
  <td>Bloque (SAN)</td>
  <td>SSD local</td>
</tr>

<tr>
  <th><b>Disco de rearranque (GB)</b></th>
  <td>25 y 100</td>
  <td>100</td>
  <td>25 y 100</td>
  <td>100</td>
</tr>

<tr>
  <th><b>Disco secundario (GB)</b></th>
  <td>4 x 2000</td>
  <td>2 x 300</td>
  <td>4 x 2000</td>
  <td>2 x 300</td>
</tr>

</TBODY>
</table>


**Nota:** los tipos de GPU están disponibles en el centro de datos _DAL13_.

## Antes de empezar
Revise los siguientes requisitos previos de GPU.

1. Los servidores virtuales de la familia GPU solo están disponibles en un sistema operativo que soporte la modalidad de arranque de máquina virtual de hardware (HVM). Consulte la siguiente lista de sistemas operativos con modalidad de arranque HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Windows 2012 R2
  - Windows 2016

2. Deben instalarse el software y los controladores NVIDIA adecuados. Para obtener más información sobre el software y los controladores NVIDIA, consulte [Instalación de paquetes de software y controladores de GPU](../vsi/vsi_gpu_nvidia_drivers.html).

**Nota:** el software que instale puede tener software de requisito previo y configuraciones específicas del sistema operativo.


