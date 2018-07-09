---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-26"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Acerca de la suspensión de facturación (Beta)
{: #requirements}

Cuando se desactiva un servidor virtual que da soporte a la característica de suspensión de facturación, no se acumulan los costes correspondientes a determinados recursos de cálculo. La facturación se detiene automáticamente cuando el servidor está apagado. La característica de suspensión de facturación le ayuda a reducir el coste e impide que tenga que volver a suministrar un servidor virtual cuando vuelva a necesitar sus recursos. La suspensión de facturación solo está soportada en suministros nuevos, no en instancias existentes.
{:shortdesc}

Para tener acceso a la característica de suspensión de facturación, debe suministrar la nueva instancia de servidor virtual utilizando la {{site.data.keyword.slapi_short}} para especificar el paquete de facturación de suspensión. La nueva instancia de servidor virtual debe estar configurada con los siguientes valores:

* SAN por horas
* Una de las siguientes familias:
  * Equilibrado
  * Cálculo
  * Memoria
* Uno de los siguientes centros de datos de {{site.data.keyword.cloud}} :

| Centros de datos |         |
| ------------ | ------- | 
|SEO01         |  WDC01  |
|SAO01         |  WDC04  |
|TOK02         |  WDC06  |
|DAL01         |  WDC07  |
|DAL05         |  LON02  |
|DAL06         |  LON04  |
|DAL09         |  LON06  |
|DAL10         |  FRA02  |
|DAL12         |  FRA04  |
|DAL13         |  FRA05  |
{: caption="Tabla 1. Centros de datos soportados" caption-side="top"}

Puede utilizar la característica de suspensión de facturación como una alternativa más rápida para suministrar y dejar de suministrar una instancia de servidor virtual.
{:tip}

## Suministro

Para la versión beta, para suministrar una instancia de servidor virtual que soporte la característica de suspensión de facturación, debe utilizar la {{site.data.keyword.slapi_short}}. Para ver ejemplos de API, consulte [ Suministro de una instancia pública mediante Colocar objeto de pedido](../vsi/vsi_provision_api.html#provisioning-a-public-instance-using-place-order-object). 

También debe especificar el ID de paquete de suspensión de facturación específico durante el proceso de suministro. Puede consultar el ID de paquete de suspensión de facturación en la {{site.data.keyword.slapi_short}} utilizando el nombre de clave `SUSPEND_CLOUD_SERVER`. Para obtener un ejemplo de la búsqueda de paquetes de servidor, consulte [Descripción y creación de un pedido utilizando la CLI de pedidos de {{site.data.keyword.slapi_short}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Detalles de facturación

Es importante comprender qué costes se detienen y qué costes persisten cuando se apaga la instancia de servidor virtual.

| Recurso                      | Fact. detenida   | Fact. persiste |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          |          X        |                  |
| RAM                           |          X        |                  |
| Velocidad de puerto                    |          X        |                  |
| Licencias de sistema operativo     |          X        |                  |
| Complementos de supervisión          |          X        |                  |
| IP públicas secundarias |                   |         X        |
| Almacenamiento                       |                   |         X        |
{: caption="Tabla 1. Detalles de facturación de recursos" caption-side="top"}   

**Nota:** Cuando suministra una instancia de servidor virtual que soporta la característica de suspensión de facturación, los tiempos de uso se calculan por minuto, tanto para el tiempo en uso como para el tiempo de suspensión de la instancia del servidor virtual. Incluso si nunca inicia la característica de suspensión de facturación apagando la instancia, la facturación se calcula por minuto del ciclo de vida de la instancia. 

### Cargo por uso mínimo
Las instancias de servidor virtual que soportan la característica de facturación de suspensión tienen un cargo por uso mínimo al mes. Si el uso es superior al 25%, se le facturará dicho uso. Si el uso es inferior al 25%, se le facturará el 25% de las horas que la instancia haya existido dentro del ciclo de facturación actual. 

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

Cuando se suspende la facturación en una instancia de servidor virtual, el almacenamiento asociado persiste, pero no puede acceder a los datos mientras la instancia de servidor virtual está apagada. Cuando se reanuda la facturación en la instancia, puede acceder a sus datos y la facturación normal empieza de nuevo.

### Direcciones IP

Todas las direcciones IP públicas se conservan automáticamente cuando se suspende la facturación para la instancia de servidor virtual.

Puede ver si el dispositivo se ha detenido, así como la fecha en la que ha cambiado el estado, a través de la {{site.data.keyword.slapi_short}} o accediendo a la página Detalles del dispositivo en el {{site.data.keyword.slportal_full}}.

### Limitaciones

El número de instancias simultáneas soportadas forman parte de su cuota del dispositivo en toda la cuenta. Para obtener más información sobre los límites de instancias simultáneas, consulte [Preguntas frecuentes: servidores virtuales](vsi_faqs_vs.html#concurrent).

## Siguientes pasos
Después de suministrar un servidor virtual que soporta la suspensión de facturación, puede empezar a suspender y reanudar la facturación en el dispositivo.
Cuando se suspende la facturación en una instancia de servidor virtual, no puede completar todas las mismas acciones en la instancia hasta que reanude la facturación para el dispositivo.

Para suspender la facturación en una instancia de servidor virtual, apague el servidor virtual. Para obtener más información, consulte [Gestión de servidores virtuales](vsi_managing.html).
