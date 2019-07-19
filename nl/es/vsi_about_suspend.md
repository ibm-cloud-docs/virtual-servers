---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-06"

keywords: virtual server, suspend billing feature, virtual server instances, suspend billing

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}

# Suspensión de la facturación
{: #requirements}

Cuando se desactiva un servidor virtual que da soporte a la característica de suspensión de facturación, no se acumulan los costes correspondientes a determinados recursos de cálculo. La facturación se detiene automáticamente cuando el servidor está apagado. La característica de suspensión de facturación le ayuda a reducir el coste e impide que tenga que volver a suministrar un servidor virtual cuando vuelva a necesitar sus recursos.
{:shortdesc}

La mayoría de las instancias de servidor virtual creadas antes del 1 de noviembre de 2018 no admiten la característica de suspensión de facturación. Para saber si la instancia del servidor virtual soporta la característica de suspensión de facturación, consulte [Visualización de la característica de suspensión de facturación](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature).

Esta característica está disponible en los centros de datos de todo el mundo. Para suministrar una instancia de servidor virtual que admita la característica de suspensión de facturación, la instancia de servidor virtual debe configurarse con los siguientes parámetros:

* SAN por horas
* Perfiles públicos de una de las siguientes familias:
  * Equilibrado
  * Cálculo
  * Memoria

Puede utilizar la característica de suspensión de facturación como una alternativa más rápida para suministrar y reclamar una instancia de servidor virtual.
{:tip}

La facturación solo se suspende cuando apaga la instancia del servicio virtual a través de la consola de {{site.data.keyword.cloud}}, la CLI o la {{site.data.keyword.slapi_short}}. Si apaga el servidor virtual directamente mediante el SO, no se suspende la facturación correspondiente a esa instancia.
{:note}

## Detalles de suministro

Puede suministrar una instancia de servidor virtual que admita la característica de suspensión de facturación a través del catálogo de {{site.data.keyword.cloud_notm}} (cloud.ibm.com), la CLI o {{site.data.keyword.slapi_short}}. No puede suministrar una instancia de servidor virtual que admita la característica de suspensión de facturación a través del catálogo de {{site.data.keyword.slportal}} (control.softlayer.com). Para obtener más información sobre el suministro de instancias de servidor virtuales públicas, consulte [Suministro de instancias públicas](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public).

Para el catálogo de {{site.data.keyword.cloud_notm}}, debe tener una cuenta actualizada para solicitar servidores virtuales. Para obtener más información sobre cómo actualizar su cuenta, consulte [Cambio a un IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

### Suministro a través de la API de Softlayer
Puede suministrar una instancia de servidor virtual que admita la característica de suspensión de facturación a través del catálogo de {{site.data.keyword.slapi_short}}. Para ver ejemplos de API, consulte [Suministro de una instancia pública mediante Colocar objeto de pedido](/docs/vsi?topic=virtual-servers-api-rest-public#provisioning-a-public-instance-using-place-order-object).

Debe especificar el ID de paquete de suspensión de facturación específico durante el proceso de suministro. Puede consultar el ID de paquete de suspensión de facturación en la {{site.data.keyword.slapi_short}} utilizando el nombre de clave `SUSPEND_CLOUD_SERVER`. Para obtener un ejemplo de la búsqueda de paquetes de servidor, consulte [Descripción y creación de un pedido utilizando la CLI de pedidos de {{site.data.keyword.slapi_short}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Detalles de facturación

Es importante comprender qué costes se detienen y qué costes persisten cuando se apaga la instancia de servidor virtual.

| Recurso                      | Fact. detenida   | Fact. persiste |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |                  |
| RAM                           | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |                  |
| Velocidad de puerto                    | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |                  |
| Licencias de sistema operativo     | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |                  |
| Complementos de supervisión            | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |                  |
| IP públicas secundarias |                   | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |
| Almacenamiento                       |                   | ![Icono de marca de selección](../../icons/checkmark-icon.svg) |
{: row-headers}
{: class="comparison-table"}
{: caption="Tabla 1. Detalles de facturación de recursos" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the resource. The column headers identify whether billing stops or persists when your instance is powered off. To understand whether billing stops or persists for a resource, navigate to the row in the table, and find the billing information you are interested in."}  

Cuando suministra una instancia de servidor virtual que soporta la característica de suspensión de facturación, los tiempos de uso se calculan por segundo, tanto para el tiempo en uso como para el tiempo de suspensión de la instancia del servidor virtual. Incluso si nunca inicia la característica de suspensión de facturación apagando la instancia, la facturación se calcula por segundo del ciclo de vida de la instancia.
{:note}

### Cargo por uso mínimo
Las instancias de servidor virtual que admiten la característica de suspensión de facturación pueden tener un cargo de uso mínimo que se aplica en algunos casos. Si el uso es superior al 25%, se le facturará dicho uso. Si el uso es inferior al 25%, se le facturará el 25% de las horas que la instancia haya existido dentro del ciclo de facturación actual.

### Factura
Cuando suspenda la facturación en un servidor virtual, verá algunos cambios en su factura. Los cargos relevantes ahora aparecen como detalles basados en el uso. Por ejemplo, es posible que vea las adiciones siguientes que reflejan las horas disponibles, las horas utilizadas y el número total de horas asignadas:

```
Uso de instancia de cálculo...
Uso de RAM...
Uso de sistema operativo...
```
{:screen}

## Detalles de recurso

### Almacenamiento

Cuando se suspende la facturación en una instancia de servidor virtual, la facturación del almacenamiento asociado persiste, pero no puede acceder a los datos almacenados mientras la instancia de servidor virtual está apagada. Cuando se reanuda la facturación en la instancia, puede acceder a sus datos de nuevo.

### Direcciones IP

Todas las direcciones IP públicas se conservan automáticamente cuando se suspende la facturación para la instancia de servidor virtual.

### Limitaciones

Las instancias de servidor virtual suspendidas siguen contando en su cuota del dispositivo en toda la cuenta. Para obtener más información sobre los límites de instancias, consulte [Preguntas frecuentes: servidores virtuales](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#concurrent).

## Siguientes pasos
Después de suministrar un servidor virtual que soporta la suspensión de facturación, puede empezar a suspender y reanudar la facturación en el dispositivo.

Cuando se suspende la facturación en una instancia de servidor virtual, no puede completar todas las mismas acciones en la instancia hasta que reanude la facturación para el dispositivo. Puede ver si el dispositivo se ha detenido, así como la fecha en la que ha cambiado el estado, a través de la {{site.data.keyword.slapi_short}} o accediendo a la página Detalles del dispositivo en el {{site.data.keyword.slportal}}.

Para suspender la facturación en una instancia de servidor virtual, apague el servidor virtual. Para obtener más información, consulte [Gestión de servidores virtuales](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
