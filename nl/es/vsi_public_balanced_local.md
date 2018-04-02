---



copyright:
  years: 2017
lastupdated: "2017-11-08"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Almacenamiento local equilibrado
Los tipos de almacenamiento local equilibrado están principalmente dirigidos a grandes clústeres de bases de datos que requieren alto rendimiento de E/S o latencia baja. Esta oferta ofrece un mayor rendimiento ya que los recursos no se suscriben en exceso. El rendimiento de la red está comprendido entre estándar y premium.

La oferta está disponible en distintos tipos y centros de datos, con las siguientes opciones de almacenamiento local:

* [HDD local](vsi_public_balanced_local.html#HDD)
* [SSD local](vsi_public_balanced_local.html#SSD)

## HDD local {: #HDD}
 
<table>
<CAPTION>Tabla 1. Tipos de almacenamiento local equilibrado utilizando la unidad de disco duro local</CAPTION>
<THEAD>
<TR>
<th>Tipo</th>
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

**Notas sobre el almacenamiento:**
* <sup>(*)</sup>Los tipos locales equilibrados se suministran automáticamente con un disco de arranque de almacenamiento local de 100 GB. A continuación, puede seleccionar un segundo disco (las opciones se muestran en la tabla anterior). Los discos locales adicionales son opcionales. Si necesita más de 500 GB, se necesitarán dos discos adicionales (por ejemplo, 8 núcleos requieren 2 x 250 GB de almacenamiento local).
*	El almacenamiento local máximo está limitado por los núcleos. 
*	El almacenamiento local equilibrado está disponible de forma global; sin embargo, el tipo de almacenamiento (SSD local o HDD local) depende de la ubicación del centro de datos. 
*	No puede desconectar discos primario ni secundario.

Los siguientes centros de datos dan soporte a los servidores virtuales de almacenamiento local equilibrado con la unidad de disco duro local:

|Centros de datos (HDD local) |        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   | 
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02        |        |  
{: caption="Tabla 1. Centros de datos soportados (HDD local)" caption-side="top"}

Todos los sistemas operativos admitidos (como por ejemplo RHEL, CentOS, Windows, Ubuntu y otros), bases de datos admitidas y complementos de software también están disponibles con esta oferta.  

## SSD local {: #SSD}
<table>
<CAPTION>Tabla 1. Tipos de almacenamiento local equilibrado utilizando la unidad de estado sólido local</CAPTION>
<THEAD>
<TR>
<th>Tipo</th>
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

**Notas sobre el almacenamiento:**
* <sup>(*)</sup>Los tipos locales equilibrados se suministran automáticamente con un disco de arranque de almacenamiento local de 100 GB. A continuación, puede seleccionar un segundo disco (las opciones se muestran en la tabla anterior). Los discos locales adicionales son opcionales. Si necesita más de 500 GB, se necesitarán dos discos adicionales (por ejemplo, 8 núcleos requieren 2 x 250 GB de almacenamiento local).
*	El almacenamiento local máximo está limitado por los núcleos. 
*	El almacenamiento local equilibrado está disponible de forma global; sin embargo, el tipo de almacenamiento (SSD local o HDD local) depende de la ubicación del centro de datos. 
*	No puede desconectar discos primario ni secundario.

Los siguientes centros de datos dan soporte a los servidores virtuales de almacenamiento local equilibrado con la unidad de estado sólido local:

|Centros de datos (SSD local) |        |         |
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
{: caption="Tabla 2. Centros de datos soportados (SSD local)" caption-side="top"}

Todos los sistemas operativos admitidos (como por ejemplo RHEL, CentOS, Windows, Ubuntu y otros), bases de datos admitidas y complementos de software también están disponibles con esta oferta.  
