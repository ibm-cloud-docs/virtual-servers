---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-29"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Degradación de velocidades de puerto
{: #downgrading-port-speeds}

Puede degradar temporalmente las velocidades de puerto de su instancia de servidor virtual sin abrir una incidencia. Solo puede degradar, desconectar o volver a conectar a un máximo de lo que ya esté pagando. No puede actualizar desde esta opción. Los cambios permanecerán en la consola hasta que los vuelva a cambiar. No se aplican cambios en la facturación por esto, y la degradación temporal del servidor no rebaja su factura. Si necesita un cambio permanente en la velocidad de puerto, debe abrir una incidencia de ventas.
{:shortdesc}

## Antes de empezar
En primer lugar, acceda al menú de dispositivo y asegúrese de que tiene los permisos de cuenta correctos para completar la tarea. 

* Acceda al menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos. 

Para obtener más información sobre los permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/vsi?topic=virtual-servers-managing-device-access).

## Degradación de velocidades de puerto
Complete los siguientes pasos para degradar las velocidades de puerto.

1. En el menú **Dispositivos**, seleccione **Lista de dispositivos**.
2. Seleccione el servidor que desea actualizar.
3. En el separador **Visión general**, vaya a **Detalles de red**.
4. Seleccione el menú desplegable en **Velocidad** (para la red privada o pública) para degradar o desconectar la velocidad de puerto.

Al cambiar las velocidades de puerto o desconectar sus puertos por cualquier motivo, debe cambiar manualmente el servidor.
{:tip}
