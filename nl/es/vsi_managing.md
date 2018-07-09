---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Gestión de servidores virtuales
{: #managing-virtual-servers}

Desde la lista de dispositivos puede gestionar servidores virtuales y otros dispositivos, como servidores nativos y cortafuegos de VLAN.
{:shortdesc}

En la lista de dispositivos, los servidores virtuales tienen el tipo de dispositivo *Virtual*. Los servidores nativos se indican con el tipo de dispositivo *Servidor*. Los hosts dedicados tienen el tipo de dispositivo *Host virtual dedicado*. Muchas de las interacciones disponibles para los dispositivos son similares, pero cada tipo de dispositivo tiene también interacciones específicas.

Dispone de las siguientes tareas de gestión de servidores virtuales desde la lista de dispositivos:
* Rearrancar -  apagar inmediatamente un dispositivo y luego volverlo a encender.
* Apagar / Encender - apagar o encender un dispositivo de forma remota.
* Cambiar el nombre - cambiar o actualizar el nombre de un dispositivo.
* Cancelar - finalizar el uso de un dispositivo. Los dispositivos se pueden cancelar inmediatamente o en el aniversario de facturación. Después de confirmar la cancelación de su dispositivo, la acción no puede deshacerse. No se realizan devoluciones por cancelaciones inmediatas.

Siga los siguientes pasos para realizar tareas de gestión para los servidores virtuales desde la lista de dispositivos en el Portal de clientes:  
1. Inicie una sesión en el [{{site.data.keyword.slportal_full}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas. 
2. En el menú **Dispositivos**, seleccione **Lista de dispositivos**.
3. Pulse **Acciones** para el dispositivo que desea gestionar y seleccione la tarea de gestión que desea.

**Sugerencias:** 
* Puede interactuar con servidores de {{site.data.keyword.slportal}} tanto en la vista Instantánea (un resumen de su dispositivo) y en la pantalla Detalles de dispositivo (una lista detallada completa). Para ver e interactuar con el servidor en la vista Instantánea, pulse la flecha situada junto a Nombre de dispositivo para expandir la vista. Para ver e interactuar con el servidor en la pantalla Detalles de dispositivo, pulse el nombre de dispositivo del servidor.
* Puede añadir notas a un dispositivo en cualquier momento desde el separador **Configuración**. Notas puede ayudarle a identificar detalles sobre el dispositivo, su uso y las acciones que se han llevado a cabo en el dispositivo.

## Qué sucede a continuación
* **Rearrancar**

    Un rearranque es una de las acciones de dispositivo más básicas. Rearrancar un dispositivo provoca que se apague inmediatamente para volverse a encender, y se realiza por muchas razonas, a menudo determinadas por las necesidades de negocio o del dispositivo de cada usuario. Los rearranques de dispositivo se pueden realizar desde la Lista de dispositivos y desde la Vista de dispositivos de un dispositivo individual. Los servidores virtuales se pueden rearrancar en cualquier momento.  

* **Encender/Apagar**

    Si el dispositivo se ha apagado, permanecerá en el estado apagado y se debe encender manualmente repitiendo los pasos anteriores. Los usuarios no pueden interactuar con un dispositivo cuando éste está apagado. Si el dispositivo se ha encendido, puede tener lugar interacción normal. Permanecerá activo hasta que se lleve a cabo otra acción. Si el servidor virtual soporta la característica de suspensión de facturación, la facturación se suspende para algunos recursos de cálculo. No puede completar todas las acciones de gestión en una instancia hasta que se reanude la facturación. La suspensión de facturación solo está soportada en suministros nuevos, no en instancias existentes. Para obtener más información, consulte [Acerca de la suspensión de facturación](vsi_about_suspend.html).

* **Cambiar el nombre**

  Después de renombrar el dispositivo, el nombre se actualizará automáticamente en el {{site.data.keyword.slportal}}. Al realizar una búsqueda en el {{site.data.keyword.slportal}}, utilice el nombre de dispositivo nuevo al intentar localizar el contenido asociado con él. Repita los pasos anteriores para renombrar el dispositivo de nuevo en cualquier momento.

* **Cancelar**

  Después de confirmar la cancelación, el dispositivo comenzará el proceso de cancelación. Si se solicitó una cancelación inmediata, el dispositivo se cancelará inmediatamente. Si se solicitó una cancelación de aniversario de facturación, el dispositivo permanecerá activo hasta el próximo aniversario de facturación. Tras su cancelación, el dispositivo ya no aparecerá en la Lista de dispositivos del {{site.data.keyword.slportal}}. Los elementos de facturación también se eliminarán de las facturas cuando se hayan pagado todos los saldos pendientes en el dispositivo, si los hay. Para preguntas sobre una factura para un dispositivo cancelado, abra una incidencia y seleccione Solicitud de contabilidad como el tema de incidencia. No se realizan devoluciones por cancelaciones inmediatas.
  
## Siguientes pasos
Si tiene que volver a un servidor virtual existente, consulte [Reconfiguración de un servidor virtual existente](../vsi/vsi_reconfigure.html).

