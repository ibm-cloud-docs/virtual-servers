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


# Servidores virtuales dedicados
La oferta de host dedicado de la infraestructura {{site.data.keyword.Bluemix}} es un servidor dedicado, virtualizado y de un solo arrendatario. Le ofrece un control máximo sobre la colocación de la carga de trabajo y opciones flexibles posteriores al suministro. Puede decidir el centro de datos predeterminado de {{site.data.keyword.cloud}} en el que desea colocar los servidores virtuales y garantizar la capacidad asignando los hosts directamente a su cuenta.
{:shortdesc}

La oferta incluye las siguientes características: 

* Afinidad y antiafinidad. Puede especificar las relaciones que deben permanecer entre host y servidor virtual y entre servidor virtual y host, lo que se denomina reglas de afinidad y antiafinidad. Estas reglas le ayudan a asegurarse de que las cargas de trabajo se colocan correctamente en función de los requisitos de la carga de trabajo.
* Gestión posterior al despliegue. Puede migrar servidores virtuales entre hosts dedicados en función de los requisitos de la carga de trabajo.
* Visibilidad de la carga de trabajo. Puede ver el consumo de recursos del núcleo, la RAM y el almacenamiento local para cada host, lo que le ofrece un control máximo sobre la gestión de la carga de trabajo.

Puede elegir entre dos modelos de despliegue: hosts dedicados e instancias dedicadas. Los hosts dedicados le ayudan con control de la colocación de la carga de trabajo y las instancias dedicadas ofrecen aislamiento de un solo arrendatario. 

**Nota:** las instancias dedicadas no proporcionan algunas características de control que ofrecen los hosts dedicados.  Consulte la tabla siguiente para obtener más detalles. 
<table>
<CAPTION>Tabla 1. Características de control</CAPTION>
<THEAD>
<TR>
<th>Característica de servidor virtual dedicado</th>
<th>Instancias de host dedicadas</th>
<th>Instancias dedicadas</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>Aislamiento de un solo arrendatario</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td>Control de la colocación del servidor virtual</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Visibilidad de recursos</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Facturación por instancia</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td>Facturación por host<sup>(1)</sup></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Control posterior al despliegue</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Reservas de capacidad</td>
<td>X</td>
<td></td>
</tr>
</TBODY>
</table>


<sup>(1)</sup>El establecimiento de precios del host incluye núcleo, RAM, SSD local y velocidades de red. Los complementos de sistema operativo (OS) Premium, almacenamiento en la red de área de almacenamiento (SAN) y software se facturarán por instancia con los precios existentes y se suministrarán licencias según el modelo por hora o mensual.

Tenga en cuenta lo siguiente cuando solicite hosts dedicados e instancias de host dedicadas:

* La ubicación del host; puede elegir entre los siguientes centros de datos de {{site.data.keyword.cloud_notm}}:
      
| Centros de datos          ||
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
{: caption="Tabla 2. Centros de datos soportados" caption-side="top"}

* El tamaño del host viene determinado por las cargas de trabajo que vaya a ejecutar en el mismo. El valor predeterminado es 56 núcleos X 242 GB de RAM X 1,2 TB. 
* Los hosts se pueden solicitar como máximo de dos en dos. Por ejemplo, si necesita seis hosts, deberá realizar tres pedidos por separado.
* Cada host necesitará su propio nombre exclusivo y puede asignar automáticamente su POD.

## Siguientes pasos

Después de revisar y decidir las opciones de despliegue que le interesan, es hora de suministrar el servidor virtual. Para empezar, consulte [Suministro de hosts dedicados e instancias](../vsi/vsi_provision_dedicated.html).



  
