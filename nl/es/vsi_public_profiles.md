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

# Perfiles
{: #about-virtual-server-profiles}

Al suministrar instancias de servidor virtual de {{site.data.keyword.cloud}}, puede seleccionar entre las familias de perfiles con soporte. Un perfil es una combinación de vCPU y RAM que se puede instanciar rápidamente para iniciar una instancia de servidor virtual. En la consola de {{site.data.keyword.cloud_notm}}, puede elegir una de las configuraciones de perfil más populares o seleccionar en una lista los perfiles que mejor se adapten a sus necesidades.
{:shortdesc}

Están disponibles las familias de instancias de servidor virtual siguientes.

En función de su tipo de instancia, es posible que algunas familias no estén disponibles.
{:note}

| Familias  | Descripción                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Equilibrado](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Adecuado para cargas de trabajo comunes de la nube que requieren un equilibrio entre rendimiento y escalabilidad. Utiliza almacenamiento conectado a red. |
| [Almacenamiento local equilibrado](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage) | Mejor para cargas de trabajo de base de datos grandes que requieran un rendimiento de E/S alto con muy poca latencia. |
| [Cálculo](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Adecuado para cargas de trabajo con un tráfico en la web entre moderado y alto. |
| [Memoria](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Adecuado para cargas de trabajo con colocación en memoria caché y análisis en tiempo real. |
| [GPU](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#gpu)  | Adecuado para cargas de trabajo de alto rendimiento. |
{: caption="Tabla 1. Selecciones de familias de servidores virtuales públicos" caption-side="top"}

Algunas de estas familias también están disponibles para IBM Cloud Virtual Servers for VPC. Para obtener más información, consulte [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen).
{:tip}

## Equilibrado
{: #balanced}

Los perfiles equilibrados (con almacenamiento conectado en red) son ideales para las cargas de trabajo en la nube común que requieren un equilibrio de rendimiento y escalado. El rendimiento de la red está comprendido entre estándar y premium.

Están disponibles los siguientes perfiles de esta oferta:

| Perfil   | vCPU    | RAM     | Tipo de almacenamiento |
| --------- | ------- | ------- | ------------ |
| B1.1x2    | 1       | 2 GB    | SAN          |
| B1.1x4    | 1       | 4 GB    | SAN          |
| B1.2x4    | 2       | 4 GB    | SAN          |
| B1.2x8    | 2       | 8 GB    | SAN          |
| B1.4x8    | 4       | 8 GB    | SAN          |
| B1.4x16   | 4       | 16 GB   | SAN          |
| B1.8x16   | 8       | 16 GB   | SAN          |
| B1.8x32   | 8       | 32 GB   | SAN          |
| B1.16x32  | 16      | 32 GB   | SAN          |
| B1.16x64  | 16      | 64 GB   | SAN          |
| B1.32x64  | 32      | 64 GB   | SAN          |
| B1.32x128 | 32      | 128 GB  | SAN          |
| B1.48x192 | 48      | 192 GB  | SAN          |
{: caption="Tabla 2. Perfiles equilibrados con almacenamiento conectado en red" caption-side="top"}

### Notas de almacenamiento

* Disco de arranque primario SAN (25 o 100 GB) con discos adicionales disponibles, hasta 2 TB cada uno (se permiten un total de cinco discos).
* Los precios de los servidores virtuales públicos que utilizan almacenamiento SAN incluyen CPU virtual, memoria y disco de arranque primario mínimo. Los precios de los discos adicionales dependen del tamaño del disco y de la cantidad seleccionada.  

Los perfiles equilibrados (con almacenamiento conectado a red) están disponibles en todos los centros de datos.

Todos los sistemas operativos admitidos (como por ejemplo RHEL, CentOS, Windows, Ubuntu y otros), bases de datos admitidas y complementos de software también están disponibles con esta oferta. 

## Almacenamiento local equilibrado
{: #balanced-local-storage}

Los perfiles de almacenamiento local equilibrado son principalmente para cargas de trabajo de base de datos grandes que requieran un rendimiento de E/S alto con muy poca latencia. El rendimiento de la red está comprendido entre estándar y premium.

La oferta está disponible en distintos perfiles y centros de datos, con las siguientes opciones de almacenamiento local:

* [HDD local](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#HDD)
* [SSD local](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#SSD)

### HDD local
{: #HDD}
 
<table>
<CAPTION>Tabla 3. Perfiles de almacenamiento local equilibrado utilizando la unidad de disco duro local</CAPTION>
<THEAD>
<TR>
<th>Perfil</th>
<th>vCPU</th>
<th>RAM</th>
<th>Discos secundarios<sup>(*)</sup></th>
<th>Tipo de almacenamiento</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>HDD local</td>
</tr>
</TBODY>
</table>

#### Notas de almacenamiento
* <sup>(*)</sup>Los perfiles locales equilibrados se suministran automáticamente con un disco de arranque de almacenamiento local de 100 GB. A continuación, puede seleccionar un segundo disco (las opciones se muestran en la tabla 3). Los discos locales adicionales son opcionales. Si necesita más de 500 GB, se necesitarán dos discos adicionales (por ejemplo, 8 núcleos requieren 2 x 250 GB de almacenamiento local).
*	El almacenamiento local máximo está limitado por los núcleos. 
*	El almacenamiento local equilibrado está disponible de forma global; sin embargo, el tipo de almacenamiento (SSD local o HDD local) depende de la ubicación del centro de datos. 
*	No puede desconectar los discos primarios ni los secundarios.

Los siguientes centros de datos dan soporte a los servidores virtuales de almacenamiento local equilibrado con la unidad de disco duro local:

| Centros de datos disponibles - HDD local |       |
| ---------------------- | ----- |
| Dallas (DAL01)         | Dallas (DAL05)   |
| Dallas (DAL06)         | Houston (HOU02)  |
| Seattle (SEA01)        | San José (SJC01) |
| Washington, DC (WDC01) |                  |
{: class="simple-tab-table"}
{: caption="Tabla 4. Centros de datos disponibles (HDD local) - América" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd1}
{: tab-title="Americas"}

| Centros de datos disponibles - HDD local |
| ---------------------- |
| Amsterdam (AMS01)      |
{: class="simple-tab-table"}
{: caption="Tabla 5. Centros de datos disponibles (HDD local) - Europa" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd2}
{: tab-title="Europe"}

| Centros de datos disponibles - HDD local |
| ---------------------- |
| Hong Kong (HKG02)      | 
| Singapur (SNG01)      |
{: class="simple-tab-table"}
{: caption="Tabla 6. Centros de datos disponibles (HDD local) - Asia Pacífico" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd3}
{: tab-title="Asia-Pacific"}

Todos los sistemas operativos admitidos (como por ejemplo RHEL, CentOS, Windows, Ubuntu y otros), bases de datos admitidas y complementos de software también están disponibles con esta oferta.  

### SSD local 
{: #SSD}

<table>
<CAPTION>Tabla 7. Perfiles de almacenamiento local equilibrado utilizando la unidad de estado sólido local</CAPTION>
<THEAD>
<TR>
<th>Perfil</th>
<th>vCPU</th>
<th>RAM</th>
<th>Discos secundarios<sup>(*)</sup></th>
<th>Tipo de almacenamiento</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>SSD local</td>
</tr>
</TBODY>
</table>

#### Notas de almacenamiento
* <sup>(*)</sup>Los perfiles locales equilibrados se suministran automáticamente con un disco de arranque de almacenamiento local de 100 GB. A continuación, puede seleccionar un segundo disco (las opciones se muestran en la tabla anterior). Los discos locales adicionales son opcionales. Si necesita más de 500 GB, se necesitarán dos discos adicionales (por ejemplo, 8 núcleos requieren 2 x 250 GB de almacenamiento local).
*	El almacenamiento local máximo está limitado por los núcleos. 
*	El almacenamiento local equilibrado está disponible de forma global; sin embargo, el tipo de almacenamiento (SSD local o HDD local) depende de la ubicación del centro de datos. 
*	No puede desconectar los discos primarios ni los secundarios.

Los siguientes centros de datos dan soporte a los servidores virtuales de almacenamiento local equilibrado con la unidad de estado sólido local:

| Centros de datos disponibles - SSD local |        |
| ---------------------------------- | ------ |
| Dallas (DAL09)                     | Dallas (DAL10)         |
| Dallas (DAL12)                     | Dallas (DAL13)         |
| Queretaro (MEX01)                  | Montreal (MON01)       |
| Sao Paulo (SAO01)                  | San Jose (SJC03)       |
| San José (SJC04)                   | Toronto (TOR01)        |
| Washington, DC (WDC04)             | Washington, DC (WDC06) |
| Washington, DC (WDC07)             |                        |
{: class="simple-tab-table"}
{: caption="Tabla 8. Centros de datos disponibles (SSD local) - América" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd1}
{: tab-title="Americas"}

| Centros de datos disponibles - SSD local |       |
| ---------------------------------- | ----- |
| Amsterdam (AMS03)                  | Frankfurt (FRA02) |
| Londres (LON02)                     | Londres (LON04)    |
| Londres (LON06)                     | Milán (MIL01)     |
| Oslo (OSL01)                       | París (PAR01)     |
{: class="simple-tab-table"}
{: caption="Tabla 9. Centros de datos disponibles (SSD local) - Europa" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd2}
{: tab-title="Europe"}

| Centros de datos disponibles - SSD local |       |
| ---------------------------------- | ----- |
| Chennai (CHE01)                    | Melbourne (MEL01) |
| Seúl (SEO01)                      | Sídney (SYD01)    |
| Sídney (SYD04)                     | Tokio (TOK02)     |
{: class="simple-tab-table"}
{: caption="Tabla 10. Centros de datos disponibles (SSD local) - Asia Pacífico" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd3}
{: tab-title="Asia-Pacific"}

Todos los sistemas operativos admitidos (como por ejemplo RHEL, CentOS, Windows, Ubuntu y otros), bases de datos admitidas y complementos de software también están disponibles con esta oferta.

## Cálculo
{: #compute}

Los perfiles de cálculo son la mejor opción para cargas de trabajo con gran demanda de CPU, como las cargas de alto tráfico en la web, los procesos de producción por lotes y los servidores web frontales.

Están disponibles los siguientes perfiles de esta oferta:

| Perfil      | vCPU     | RAM       | Tipo de almacenamiento |
| ------------ | -------- | --------- | ------------ |
| C1.1x1       | 1        | 1 GB      | SAN          |
| C1.2x2       | 2        | 2 GB      | SAN          |
| C1.4x4       | 4        | 4 GB      | SAN          |
| C1.8x8       | 8        | 8 GB      | SAN          |
| C1.16x16     | 16       | 16 GB     | SAN          |
| C1.32x32     | 32       | 32 GB     | SAN          |
{: caption="Tabla 11. Perfiles de cálculo" caption-side="top"}

### Notas de almacenamiento
* Disco de arranque primario SAN (25 o 100 GB) con discos adicionales disponibles, hasta 2 TB cada uno (se permiten un total de cinco discos).
* Los precios de los servidores virtuales públicos que utilizan almacenamiento SAN incluyen CPU virtual, memoria y disco de arranque primario mínimo. Los precios de los discos adicionales dependen del tamaño del disco y de la cantidad seleccionada.  

Los perfiles de cálculo están disponibles en todos los centros de datos.

Todos los sistemas operativos admitidos (como por ejemplo RHEL, CentOS, Windows, Ubuntu y otros), bases de datos admitidas y complementos de software también están disponibles con esta oferta.

## Memoria
{: #memory}

Los perfiles de memoria son la mejor opción para cargas de trabajo que utilizan mucha memoria, como las cargas de trabajo con alto nivel de colocación en memoria caché, aplicaciones con uso intensivo de bases de datos o cargas de trabajo de análisis en memoria.

Están disponibles los siguientes perfiles de esta oferta:

| Perfil      | vCPU     | RAM       | Tipo de almacenamiento |
| ------------ | -------- | --------- | ------------ |
| M1.1x8       | 1        | 8 GB      | SAN          |
| M1.2x16      | 2        | 16 GB     | SAN          |
| M1.4x32      | 4        | 32 GB     | SAN          |
| M1.8x64      | 8        | 64 GB     | SAN          |
| M1.16x128    | 16       | 128 GB    | SAN          |
| M1.30x240    | 30       | 240 GB    | SAN          |
| M1.48x384    | 48       | 384 GB    | SAN          |
| M1.56x448    | 56       | 448 GB    | SAN          |
| M1.64x512    | 64       | 512 GB    | SAN          |
{: caption="Tabla 12. Perfiles de memoria" caption-side="top"}

### Notas de almacenamiento
* Disco de arranque primario SAN (25 o 100 GB) con discos adicionales disponibles, hasta 2 TB cada uno (se permiten un total de 5 discos).
* Los precios de los servidores virtuales públicos que utilizan almacenamiento SAN incluyen CPU virtual, memoria y disco de arranque primario mínimo. Los precios de los discos adicionales dependen del tamaño del disco y de la cantidad seleccionada.  

Los perfiles de memoria están disponibles en todos los centros de datos.

Todos los sistemas operativos admitidos (como por ejemplo RHEL, CentOS, Windows, Ubuntu y otros), bases de datos admitidas y complementos de software también están disponibles con esta oferta.

## GPU
{: #gpu}

Los perfiles de GPU son adecuados para cargas de trabajo de alto rendimiento que requieren más densidad de cálculo para reducir los costes y la gestión de los recursos. Los perfiles de GPU son ideales para procesos de inteligencia artificial, para aplicaciones de gran cantidad de datos y gráficos o para desarrollar nuevas aplicaciones que requieren un rápido rendimiento.

Basados en las GPU NVDIA Tesla, los perfiles {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” y "ac2" ofrecen tanto almacenamiento en bloque como SSD local. Puede elegir entre los siguientes perfiles de GPU disponibles:  

<table>
<CAPTION>Tabla 13. Perfiles de GPU P100</CAPTION>
<THEAD>
<TR>
<th>Perfil</th>
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

Los perfiles de GPU P100 están disponibles en los centros de datos _DAL13_, _LON06_ y _WDC07_.
{: note}

<table>
<CAPTION>Tabla 14. Perfiles de GPU V100</CAPTION>
<THEAD>
<TR>
<th>Perfil</th>
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

Los perfiles de GPU V100 están disponibles en los centros de datos _DAL10_, _DAL12_, _LON04_ y _WDC07_.
{: note}

### Requisitos previos de GPU
Revise los siguientes requisitos previos de GPU.

1. Los servidores virtuales del perfil de GPU solo están disponibles en un sistema operativo que soporte la modalidad de arranque de máquina virtual de hardware (HVM). Consulte la siguiente lista para ver los sistemas operativos que dan soporte a la modalidad de arranque HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Deben instalarse el software y los controladores NVIDIA adecuados. Para obtener más información sobre el software y los controladores NVIDIA, consulte [Instalación de paquetes de software y controladores de GPU](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages).  

El software que instale puede tener software de requisito previo y configuraciones específicas del sistema operativo.
{: note}

### Adición o eliminación de GPU 
Puede cambiar el número de GPU en el servidor virtual después de su pedido inicial. Sin embargo, esto depende del número de GPU que haya suministrado. Puede tener una de las opciones siguientes.

- Si se suministra una GPU, puede añadir otra GPU, o bien
- Si se suministran dos GPU, puede volver a una GPU.

