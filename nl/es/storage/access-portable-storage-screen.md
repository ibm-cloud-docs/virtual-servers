---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# Gestión del almacenamiento portátil
{: #accessing-portable-storage}

Los volúmenes de almacenamiento portátiles (PSV) son una solución de almacenamiento auxiliar exclusivamente para {{site.data.keyword.virtualmachinesshort}}. Dentro de la consola de {{site.data.keyword.cloud}}, puede acceder a los volúmenes de almacenamiento portátiles y mostrar todos los PSV. También puede conectar, desconectar, intercambiar y editar volúmenes.
{:shortdesc}

No puede conectar ni intercambiar volúmenes de almacenamiento portátiles con una instancia de servidor virtual que se proporcione a partir de una plantilla de imagen cifrada.
{:note}

## Antes de empezar
En primer lugar, acceda al menú de dispositivo o almacenamiento y asegúrese de que tiene los permisos de cuenta correctos para completar las tareas.

* Acceda al menú del dispositivo o almacenamiento de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos.

Para obtener más información sobre los permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/vsi?topic=virtual-servers-managing-device-access).

## Conexión de almacenamiento portátil

1. En el menú **Almacenamiento**, seleccione **Almacenamiento en bloque**.
2. En la sección **Almacenamiento portátil**, seleccione la opción de conexión del almacenamiento portátil que desee utilizar.
3. En la siguiente pantalla, elija el dispositivo que necesita el almacenamiento y seleccione **Conectar**.

## Gestión del almacenamiento portátil conectado a un servidor

El almacenamiento portátil conectado a un servidor aparece en la página *Detalles de dispositivos* del servidor.

1. En el menú **Dispositivos**, seleccione **Lista de dispositivos**.
2. En la **Lista de dispositivos**, seleccione una instancia de servidor virtual para ver sus detalles.
3. Pulse el separador **Almacenamiento** para ver el almacenamiento portátil actualmente conectado a la instancia.
4. En el menú **Acciones**, puede **Intercambiar** o **Desconectar** el almacenamiento.
