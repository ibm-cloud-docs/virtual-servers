---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# Acerca de los servidores virtuales dedicados
{: #dedicated-virtual-servers}

La oferta de host dedicado de la infraestructura {{site.data.keyword.Bluemix}} es un servidor dedicado, virtualizado y de un solo arrendatario. Le ofrece un control máximo sobre la colocación de la carga de trabajo y opciones flexibles posteriores al suministro. Puede decidir el centro de datos predeterminado de {{site.data.keyword.cloud_notm}} en el que desea colocar los servidores virtuales y garantizar la capacidad asignando los hosts directamente a su cuenta.
{:shortdesc}

La oferta incluye las siguientes características:

* Afinidad y antiafinidad. Puede especificar las relaciones que deben permanecer entre host y servidor virtual y entre servidor virtual y host, lo que se denomina reglas de afinidad y antiafinidad. Estas reglas le ayudan a asegurarse de que las cargas de trabajo se colocan correctamente en función de los requisitos de la carga de trabajo.
* Gestión posterior al despliegue. Puede migrar servidores virtuales entre hosts dedicados en función de los requisitos de la carga de trabajo.
* Visibilidad de la carga de trabajo. Puede ver el consumo de recursos del núcleo, la RAM y el almacenamiento local para cada host, lo que le ofrece un control máximo sobre la gestión de la carga de trabajo.

Puede elegir entre dos modelos de despliegue: hosts dedicados e instancias dedicadas. Los hosts dedicados le ayudan con control de la colocación de la carga de trabajo y las instancias dedicadas ofrecen aislamiento de un solo arrendatario.

Las instancias dedicadas no proporcionan algunas características de control que ofrecen los hosts dedicados.  Consulte la tabla siguiente para obtener más detalles.
{:note}

| Característica de servidor virtual dedicado | Instancias de host dedicadas | Instancias dedicadas |
| ------- | ------- | ------- |
| Aislamiento de un solo arrendatario | ![Icono de marca de selección](../../icons/checkmark-icon.svg) | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |
| Control de la colocación del servidor virtual | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |   |
| Visibilidad de recursos | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |   |
| Facturación por instancia |   | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |
| Facturación por host<sup>(1)</sup> | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |   |
| Control posterior al despliegue | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |   |
| Reservas de capacidad | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="Tabla 1. Características de control" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup>El establecimiento de precios del host incluye núcleo, RAM, SSD local y velocidades de red. Los complementos de sistema operativo (OS) Premium, almacenamiento en la red de área de almacenamiento (SAN) y software se facturarán por instancia con los precios existentes y se suministrarán licencias según el modelo por hora o mensual.

Tenga en cuenta lo siguiente cuando solicite hosts dedicados e instancias de host dedicadas:

* El tamaño del host viene determinado por las cargas de trabajo que vaya a ejecutar en el mismo. El valor predeterminado es 56 núcleos X 242 GB de RAM X 1,2 TB, pero puede elegir entre configuraciones adicionales.
* Los hosts se pueden solicitar como máximo de dos en dos. Por ejemplo, si necesita seis hosts, deberá realizar tres pedidos por separado.
* Cada host necesitará su propio nombre exclusivo y puede asignar automáticamente su POD.

## Siguientes pasos

Después de revisar y decidir las opciones de despliegue que le interesan, es hora de suministrar el servidor virtual. Para empezar, consulte [Suministro de hosts dedicados e instancias](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated).
