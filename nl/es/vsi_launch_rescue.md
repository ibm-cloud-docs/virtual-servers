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
{:table: .aria-labeledby="caption"}


# Inicio de Rescue Kernel
{: #launching-rescue}

Rescue Kernel es un entorno de rescate diseñado para ofrecerle la posibilidad de colocar en línea un servidor nativo o un servidor virtual para solucionar problemas del sistema que normalmente solo se solucionarían mediante una recarga del SO. Rescue Kernel se debe iniciar en la consola de {{site.data.keyword.cloud}}. Siga estos pasos para iniciar Rescue Kernel para un dispositivo.
{:shortdesc}

## Antes de empezar
En primer lugar, acceda al menú de dispositivo y asegúrese de que tiene los permisos de cuenta correctos para completar las tareas.

* Acceda al menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos.

Para obtener más información sobre los permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/vsi?topic=virtual-servers-managing-device-access).

## Inicio de Rescue Kernel

1. En el menú **Dispositivos**, seleccione **Lista de dispositivos**.
2. En la **Lista de dispositivos**, pulse el nombre de dispositivo que desee rescatar.
3. En el menú *Acciones*, seleccione **Modalidad de rescate**.
4. Pulse **Sí** para transmitir el dispositivo a Rescue Kernel inmediatamente.

## Inicio de Rescue Kernel para una instancia de Windows

1. En el menú **Dispositivos**, seleccione **Lista de dispositivos**.
2. En la **Lista de dispositivos**, pulse el nombre de dispositivo que desee rescatar.
3. En el menú *Acciones*, seleccione **Arrancar desde imagen**.
4. Seleccione **Arrancar desde esta imagen** junto a la imagen pública, *WindowsRescueStandalone.iso*.

## Siguientes pasos
Después de iniciar Rescue Kernel, el dispositivo se apaga y se rearranca en el kernel de rescate correspondiente al sistema operativo del dispositivo. Este proceso puede tardar varios minutos.

Puede acceder al dispositivo de forma remota desde la dirección IP del dispositivo. Puede acceder al dispositivo en Rescue Kernel utilizando las credenciales de root o admin para los dispositivos registrados en la consola de {{site.data.keyword.cloud_notm}}. Si utiliza Rescue Kernel, puede resolver y descubrir problemas igual que lo haría en un dispositivo arrancado de manera normal. Si es necesario, puede montar unidades en SO de Rescue Kernel. Para salir de Rescue Kernel y devolver el dispositivo a su entorno ordinario, rearranque el dispositivo en la consola de
{{site.data.keyword.cloud_notm}} o rearranque desde el SO de Rescue Kernel.

Para obtener más información sobre el rearranque de un dispositivo, consulte [Gestión de servidores virtuales](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
