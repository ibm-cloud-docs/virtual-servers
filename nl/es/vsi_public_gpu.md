---



copyright:
  years: 2017, 2018
lastupdated: "2018-09-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
Los tipos de GPU son adecuados para cargas de trabajo de alto rendimiento que requieren más densidad de cálculo para reducir los costes y la gestión de los recursos. Los tipos de GPU son ideales para procesos de inteligencia artificial, para aplicaciones de gran cantidad de datos y gráficos o para desarrollar nuevas aplicaciones que requieren un rápido rendimiento.

Basados en las GPU NVDIA Tesla, los tipos {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” y "ac2" ofrecen tanto almacenamiento en bloque como SSD local. Puede elegir entre los siguientes tipos de GPU disponibles:  

  <table>
<CAPTION>Tabla 1. Tipos de GPU P100</CAPTION>
<THEAD>
<TR>
<th>Tipo</th>
<th>GPU</th>
<th>RAM de GPU (GB)</th>
<th>vCPU</th>
<th>RAM de GPU (GB)</th>
<th>Tipo de almacenamiento</th>
<th>Disco de arranque (GB)</th>
<th>Discos secundarios (2 y 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Bloque (SAN)</td>
<td>25</td>
<td>Ninguno</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD o SAN local</td>
<td>100</td>
<td>Ninguno (SAN)<br>300 (Local)</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Bloque (SAN)</td>
<td>25</td>
<td>Ninguno</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD o SAN local</td>
<td>100</td>
<td>Ninguno (SAN)<br>600 (Local)</td></tr>

</TBODY>
</table>

**Nota: ** los tipos de GPU P100 están disponibles en los centros de datos _DAL13_, _LON06_ y _WDC07_.

<table>
<CAPTION>Tabla 2. Tipos de GPU V100</CAPTION>
<THEAD>
<TR>
<th>Tipo</th>
<th>GPU</th>
<th>RAM de GPU (GB)</th>
<th>vCPU</th>
<th>RAM de GPU (GB)</th>
<th>Tipo de almacenamiento</th>
<th>Disco de arranque (GB)</th>
<th>Discos secundarios (2 y 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Bloque (SAN)</td>
<td>25</td>
<td>Ninguno</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD o SAN local</td>
<td>100</td>
<td>Ninguno (SAN)<br>300 (Local)</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Bloque (SAN)</td>
<td>25</td>
<td>Ninguno</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD o SAN local</td>
<td>100</td>
<td>Ninguno (SAN)<br>600 (Local)</td></tr>

</TBODY>
</table>

**Nota: ** los tipos de GPU V100 están disponibles en los centros de datos _DAL10_, _DAL12_ y _LON04_<!--WDC07-->.


## Antes de empezar
Revise los siguientes requisitos previos de GPU.

1. Los servidores virtuales del tipo de GPU solo están disponibles en un sistema operativo que soporte la modalidad de arranque de máquina virtual de hardware (HVM). Consulte la siguiente lista para ver los sistemas operativos que dan soporte a la modalidad de arranque HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Deben instalarse el software y los controladores NVIDIA adecuados. Para obtener más información sobre el software y los controladores NVIDIA, consulte [Instalación de paquetes de software y controladores de GPU](../vsi/vsi_gpu_nvidia_drivers.html).  
**Nota:** el software que instale puede tener software de requisito previo y configuraciones específicas del sistema operativo.

## Añadir o eliminar GPU 
Puede cambiar el número de GPU en el servidor virtual después de su pedido inicial. Sin embargo, esto depende del número de GPU que haya suministrado. Puede tener una de las opciones siguientes.

- Si se suministra una GPU, puede añadir otra GPU, o bien
- Si se suministran dos GPU, puede volver a una GPU.
