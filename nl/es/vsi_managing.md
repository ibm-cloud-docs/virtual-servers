---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Gestión de servidores virtuales
{: #managing-virtual-servers}

Puede gestionar servidores virtuales, junto con otros dispositivos, desde la lista de detalles de dispositivos.
{:shortdesc}


## Antes de empezar
En primer lugar, acceda al menú de dispositivo y asegúrese de que tiene los permisos de cuenta correctos para completar las tareas.

* Acceda al menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos.

Para obtener más información sobre los permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/vsi?topic=virtual-servers-managing-device-access).

## Tipos de dispositivos
La lista de detalles de dispositivos le muestra los tipos de dispositivos siguientes:

| Dispositivo  | Tipo de dispositivo  |
| ------  | ------------ | 
| Servidores virtuales | Dispositivo |
| Servidores nativos | Servidor |
| Hosts dedicados | Host virtual dedicado | 
{: caption="Tabla 1. Tipos de dispositivos" caption-side="top"}

Las acciones que verá dependerán del tipo de dispositivo, así como de los permisos que tenga otorgados su cuenta de usuario.

Siga los siguientes pasos para realizar tareas de gestión para los servidores virtuales.

1. En el menú **Dispositivos**, seleccione **Lista de dispositivos**.
2. Pulse **Acciones** para el dispositivo que desea gestionar y seleccione la tarea correspondiente.

* Puede interactuar con servidores en la consola de {{site.data.keyword.cloud_notm}} tanto en la vista de instantánea (un resumen del dispositivo) como en la página de detalles del dispositivo (una lista detallada completa). Para ver e interactuar con el servidor en la vista de instantánea, pulse la flecha situada junto a Nombre de dispositivo para expandir la vista. Para ver e interactuar con el servidor en la página de
detalles del dispositivo, pulse el nombre de dispositivo del servidor.

* Puede añadir notas a un dispositivo en cualquier momento desde el separador **Configuración**. Notas puede ayudarle a identificar detalles sobre el dispositivo, su uso y las acciones que se han llevado a cabo en el dispositivo.
 {:tip}

## Rearrancar
Un rearranque es una de las acciones de dispositivo más básicas. Rearrancar un dispositivo provoca que se apague inmediatamente para volverse a encender, y se realiza por muchas razonas, a menudo determinadas por las necesidades de negocio o del dispositivo de cada usuario. Los rearranques de dispositivo se pueden realizar desde la Lista de dispositivos y desde la Vista de dispositivos de un dispositivo individual. Los servidores virtuales se pueden rearrancar en cualquier momento.

Un rearranque resulta muy útil cuando se experimenta un problema en el que el servidor no puede arrancar el sistema operativo debido a un problema en la configuración.  También puede rearrancar con Rescue Kernel. Tras rearrancar en Rescue Kernel, puede montar la unidad o unidades del servidor y, a continuación, arreglar el problema de configuración. Una vez que se ha solucionado el problema, simplemente rearranque el servidor desde la línea de mandatos, y el servidor rearrancará en el kernel predeterminado del servidor.
{:tip}

## Encender/apagar
Si el dispositivo se ha apagado, permanecerá en el estado apagado y se debe encender manualmente repitiendo los pasos anteriores. Los usuarios no pueden interactuar con un dispositivo cuando éste está apagado. Si el servidor virtual soporta la característica de suspensión de facturación, la facturación se suspende para algunos recursos de cálculo. No puede completar todas las acciones de gestión en una instancia hasta que se reanude la facturación. Para obtener más información, consulte [Suspensión de la facturación](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing). Para saber si la instancia del servidor virtual soporta la característica de suspensión de facturación, consulte [Visualización de la característica de suspensión de facturación](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature#viewing-suspend-billing-feature). Si el dispositivo se ha encendido, puede tener lugar interacción normal. Permanecerá activo hasta que se lleve a cabo otra acción.

## Cambiar el nombre
Tras renombrar el dispositivo, el nombre se actualizará automáticamente en la consola de
{{site.data.keyword.cloud_notm}}. Al realizar una búsqueda en la consola de {{site.data.keyword.cloud_notm}}, utilice el nombre de dispositivo nuevo al intentar localizar el contenido asociado con él. Repita los pasos anteriores para renombrar el dispositivo de nuevo en cualquier momento.

## Cancelar
Si cancela un dispositivo, terminará el uso de dicho dispositivo. Los dispositivos se pueden cancelar inmediatamente o en el aniversario de facturación. Después de confirmar la cancelación de su dispositivo, la acción no puede deshacerse. No se realizan devoluciones por cancelaciones inmediatas.

Después de confirmar la cancelación, el dispositivo comenzará el proceso de cancelación. Si se solicitó una cancelación inmediata, el dispositivo se cancelará inmediatamente. Si se solicitó una cancelación de aniversario de facturación, el dispositivo permanecerá activo hasta el próximo aniversario de facturación. Tras su cancelación, el dispositivo ya no aparecerá en la Lista de dispositivos de la consola de {{site.data.keyword.cloud_notm}}. Los elementos de facturación también se eliminarán de las facturas cuando se hayan pagado todos los saldos pendientes en el dispositivo, si los hay. Para preguntas sobre una factura para un dispositivo cancelado, abra una incidencia y seleccione Solicitud de contabilidad como el tema de incidencia. No se realizan devoluciones por cancelaciones inmediatas.

## Siguientes pasos
Si tiene que volver a un servidor virtual existente, consulte [Reconfiguración de un servidor virtual existente](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).
