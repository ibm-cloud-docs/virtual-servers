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

# GPU
Los tipos de GPU son adecuados para cargas de trabajo de alto rendimiento que requieren más densidad de cálculo para reducir los costes y la gestión de los recursos. Los tipos de GPU son ideales para aplicaciones de gran cantidad de datos y gráficos, o para desarrollar nuevas aplicaciones que requieren un rápido rendimiento.

Basada en las GPU NVDIA Tesla P100, el tipo {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” ofrece tanto almacenamiento en bloque como SSD local. Puede elegir entre los siguientes tipos de GPU disponibles:  

  <table>
<CAPTION>Tabla 1. Tipos de GPU</CAPTION>
<THEAD>
<TR>
<th>Tipo</th>
<th>GPU</th>
<th>RAM de GPU (GB)</th>
<th>vCPU</th>
<th>RAM de GPU (GB)</th>
<th>Tipo de almacenamiento</th>
<th>Disco de arranque (GB)</th>
<th>Disco secundario (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Bloque (SAN)</td>
<td>25 y 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD local</td>
<td>100</td>
<td>2 x 300</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Bloque (SAN)</td>
<td>25 y 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD local</td>
<td>100</td>
<td>2 x 600</td></tr>

</TBODY>
</table>

**Nota: ** los tipos de GPU están disponibles en los centros de datos _ DAL13 _, _LON06_ y _WDC07_.

## Antes de empezar
Revise los siguientes requisitos previos de GPU.

1. Los servidores virtuales del tipo de GPU solo están disponibles en un sistema operativo que soporte la modalidad de arranque de máquina virtual de hardware (HVM). Consulte la siguiente lista de sistemas operativos con modalidad de arranque HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Deben instalarse el software y los controladores NVIDIA adecuados. Para obtener más información sobre el software y los controladores NVIDIA, consulte [Instalación de paquetes de software y controladores de GPU](../vsi/vsi_gpu_nvidia_drivers.html).  
**Nota:** el software que instale puede tener software de requisito previo y configuraciones específicas del sistema operativo.

# Añadir o eliminar GPU
Puede cambiar el número de GPU en el servidor virtual después de su pedido inicial. Sin embargo, esto depende del número de GPU que haya suministrado. Puede tener una de las opciones siguientes. Desde la pantalla de pedidos de suministro, tiene una de las opciones siguientes:
- Si se suministra una GPU, puede añadir otra GPU, o bien
- Si se suministran dos GPU, puede volver a una GPU.
