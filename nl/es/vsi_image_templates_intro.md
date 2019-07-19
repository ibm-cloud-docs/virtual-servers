---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Plantillas de imagen
{: #image-templates}

Con las plantillas de imágenes de {{site.data.keyword.BluVirtServers}}, puede capturar la imagen de un dispositivo para duplicar rápidamente su configuración con cambios mínimos en el proceso de pedido.
{:shortdesc}

Las plantillas de imagen proporcionan una opción de creación de imágenes para todos los {{site.data.keyword.BluVirtServers_short}}, independientemente del sistema operativo. Las plantillas de imagen le permiten capturar una imagen de un servidor virtual existente y crear uno nuevo basado en la imagen capturada. Las plantillas de imagen no son compatibles con los servidores nativos.

## Cómo funcionan las plantillas de imágenes
Las dos acciones principales para cualquier plantilla de imagen son crear y desplegar. Cuando se solicita la creación de una imagen, el sistema automatizado de {{site.data.keyword.BluSoftlayer_full}} coloca el servidor fuera de línea. Mientras el servidor está fuera de línea, se crea una copia de seguridad comprimida de los datos, la información de configuración se registra y la plantilla de imagen se almacena en la SAN de {{site.data.keyword.BluSoftlayer_notm}}. Durante la etapa de despliegue de la plantilla de imagen, el sistema automático construye un nuevo servidor basado en los datos recopilados de la imagen seleccionada. El proceso de despliegue realiza ajustes en cuanto a volumen, restaura los datos copiados y luego realiza cambios finales en la configuración (por ejemplo, configuraciones de red) para el nuevo host.

Para obtener más información sobre las plantillas de imagen, consulte [Iniciación a las plantillas de imagen](/docs/infrastructure/image-templates?topic=image-templates-getting-started-with-image-templates).
