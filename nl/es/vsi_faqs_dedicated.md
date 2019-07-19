---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Preguntas frecuentes: Instancias y hosts dedicados
{: #faqs-dedicated-hosts-and-instances}

## ¿Qué es un host dedicado?
{: faq}

Los hosts dedicados de {{site.data.keyword.Bluemix}} son servidores físicos dedicados a un grupo de usuarios. Los hosts dedicados ofrecen la capacidad de suministro del servidor virtual y un máximo control sobre la colocación.

## ¿Cuáles son las ventajas de utilizar hosts dedicados sobre instancias dedicadas?
{: faq}

Ambas ofertas tienen garantizada la tenencia única. Los hosts dedicados ofrecen la flexibilidad de especificar el host en el que se van a suministrar las instancias de host dedicadas, así como:
   * Control sobre el centro de datos de {{site.data.keyword.cloud}} en el que se colocará el servidor
   * Capacidad para gestionar los servidores a medida que cambian los requisitos de la carga de trabajo; por ejemplo, se pueden migrar servidores virtuales entre hosts dedicados del mismo POD

## ¿Puedo conservar mis instancias dedicadas existentes o tengo que configurar un host dedicado e instancias de host dedicadas?
{: faq}

Sí, puede conservar sus instancias dedicadas existentes.

## ¿Puedo intercambiar el suministro de instancias dedicadas (asignadas automáticamente) e instancias de host dedicadas?
{: faq}

No. Las instancias dedicadas existentes de asignación automática no se pueden volver a suministrar en hosts dedicados. Si necesita colocar en un servidor virtual, tiene que suministrarlas en hosts dedicados como instancias de host dedicadas.

## ¿Qué tipo de servidor, virtual o nativo, da soporte a la oferta de host dedicado?
{: faq}

La oferta recibe soporte en servidores virtuales; {{site.data.keyword.Bluemix_notm}} tiene una oferta para servidor nativo. Las diferencias entre hosts virtuales y servidores nativos son el tiempo de suministro y la gestión de la virtualización.

## ¿Cuál es el ciclo de vida de suministro de un host dedicado?
{: faq}

Los hosts dedicados se asignan a usuarios cuando se suministran. Permanecen ligados a la cuenta hasta que se reclama. Los hosts dedicados solo se ofrecen con precio bajo demanda, que puede ser por hora o mensual, por lo que, cuando se reclaman, se aplicarán los mismos modelos de facturación que otras ofertas de {{site.data.keyword.BluSoftlayer_full}} de facturación por hora o mensual.

## ¿Cómo se factura la oferta de host dedicado?
{: faq}

Puede adquirir hosts dedicados bajo demanda con facturación por hora o mensual. Los hosts que solo se facturan por hora solo permiten que se suministren instancias por hora; los hosts que solo se facturan al mes permiten suministrar instancias mensuales *y* por hora. El establecimiento de precios para hosts dedicados incluye núcleo, RAM, almacenamiento SSD local y velocidades de puerto de red. Los precios y licencias de los sistemas operativos premium, el almacenamiento de red de área de almacenamiento (SAN) y el complemento de software se cargan en función de la instancia desplegada (por hora o mensual) en el host dedicado. Para estos elementos se sigue el mismo modelo de precios que para las instancias públicas y dedicadas de {{site.data.keyword.Bluemix_notm}}.

## Estoy ejecutando un host dedicado bajo demanda; ¿cómo se me factura?
{: faq}

Se le factura la tasa bajo demanda por hora o mensual correspondiente a los hosts dedicados. Las instancias de hosts dedicadas suministradas en hosts dedicados pueden incurrir en los cargos indicados en la respuesta a **Cómo se factura una oferta de host dedicado**.

## ¿Cómo se especifica la tenencia cuando se suministran hosts dedicados e instancias de host dedicadas?
{: faq}

La tenencia predeterminada para instancias dedicadas es la de arrendatario único. Tiene la opción de suministrar instancias dedicadas en un host dedicado (instancias de host dedicadas) o en un host de asignación automática (instancias dedicadas). Las instancias dedicadas en hosts asignados automáticamente no ofrecen el mismo nivel de gestión que las de un host dedicado.

## ¿Puedo mezclar y combinar distintas configuraciones de instancias de host dedicadas en mi host dedicado?
{: faq}

Sí. Puede suministrar distintos tamaños de servidor virtual en hosts dedicados dentro de su asignación de capacidad.

## ¿Cómo puedo saber cuántas instancias de host dedicadas puedo ejecutar en cada host dedicado?
{: faq}

Cada host dedicado tiene una asignación específica de núcleo, RAM y almacenamiento SSD local. Puede ver las asignaciones de recursos en el separador Asignaciones para saber cuántas instancias de host dedicadas se suministran, la capacidad de host actual utilizada y la disponible.

## ¿Qué imágenes se pueden suministrar en hosts dedicados?
{: faq}

Puede suministrar imágenes de stock de servidor virtual de {{site.data.keyword.Bluemix_notm}} o importar sus propias imágenes, tal como se indica en el acuerdo con terceros.

## ¿Hay un límite sobre la cantidad de hosts dedicados que se pueden asignar a una sola cuenta?
{: faq}

Sí, las limitaciones de recursos son por cuenta y están definidos para toda la infraestructura de {{site.data.keyword.BluSoftlayer_notm}} como recursos de servicio. Puede tener varios pedidos por cuenta, pero solo dos hosts dedicados por pedido de suministro.

## ¿Se puede suscribir un exceso de capacidad en despliegues de hosts dedicados?
{: faq}

No; solo puede suministrar la capacidad indicada en hosts dedicados.
