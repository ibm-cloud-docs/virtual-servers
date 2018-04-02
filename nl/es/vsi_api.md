---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Referencia de API
{: #api-reference} 

{{site.data.keyword.slapi_full}} es la interfaz de desarrollo que proporciona a los desarrolladores y a los administradores del sistema la interacción directa con el sistema de fondo de {{site.data.keyword.cloud}}. {{site.data.keyword.slapi_short}} alimenta muchas de las características del {{site.data.keyword.slportal_full}}, lo que normalmente significa que si una acción se puede ejecutar en el {{site.data.keyword.slportal}}, también se puede ejecutar en la API. Puesto que puede interactuar mediante programación con todas las partes del entorno de {{site.data.keyword.BluSoftlayer_full}} dentro de la API, {{site.data.keyword.slapi_short}} le permite automatizar las tareas. Por ejemplo, puede utilizar la API *SoftLayer_Virtual_Guest/createObject* para desplegar una instancia del servidor virtual.
{:shortdesc}

La {{site.data.keyword.slapi_short}} es un sistema de llamada a procedimiento remoto. Cada llamada implica el envío de datos a un punto final de API y la recepción de datos estructurados. El formato utilizado para enviar y recibir datos con la {{site.data.keyword.slapi_short}} depende de la implementación de la API que se elija. Actualmente la {{site.data.keyword.slapi_short}} utiliza SOAP, XML-RPC o REST para la transmisión de datos.

Para obtener más información sobre la {{site.data.keyword.slapi_short}} y las API del servidor virtual, consulte los recursos siguientes en {{site.data.keyword.sldn_full}}:
* [Visión general de {{site.data.keyword.slapi_short}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://sldn.softlayer.com/article/softlayer-api-overview){: new_window} 
* [Iniciación a la {{site.data.keyword.slapi_short}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://sldn.softlayer.com/article/getting-started){: new_window}
* [Referencia de API: SoftLayer_Virtual_Guest::createObject ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://sldn.softlayer.com/reference/services/softlayer_virtual_guest/createobject){: new_window}
* [Referencia de API: SoftLayer_Product_Order::placeOrder ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://sldn.softlayer.com/reference/services/SoftLayer_Product_Order/placeOrder){: new_window}

Para ver ejemplos de uso de la API, consulte los siguientes recursos:
* [Cliente Python de la {{site.data.keyword.slapi_short}}: Cómo trabajar con servidores virtuales ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [Ejemplos de {{site.data.keyword.slapi_short}} - Notas del release ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/){: new_window}
* [Ejemplos de Python ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/python/){: new_window}

## Ejemplos de uso de servidores virtuales dedicados
* [Obtención de asignación de host dedicado ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/python/getdedihostallocation/){: new_window}
* [Obtención de invitados de host dedicado ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/python/getdedicatedhostguests/){: new_window}
* [Migración de una instancia de servidor virtual entre hosts dedicados ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/python/migratededicatedinstance/){: new_window}

## Ejemplos de uso de servidores virtuales públicos
* [Ejemplos de la API softlayer_virtual_guest ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
