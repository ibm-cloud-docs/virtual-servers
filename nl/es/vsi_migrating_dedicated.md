---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Migración de una instancia de host dedicada a otro host
{: #migrating-dedicated-host}

Puede migrar instancias de host dedicadas de un host a otro dentro del mismo POD. Seleccione la instancia que desea migra en la página Detalles del dispositivo del host o en la página Detalles del dispositivo de la instancia. Tenga en cuenta que solo se pueden migrar dos instancias simultáneamente y que el tiempo necesario para la migración depende del disco. Los discos SAN se migran más rápidamente porque los discos locales requieren que se copie el disco. Las instancias migradas están fuera de línea mientras se migran; el host permanece activo para las demás instancias de host dedicadas.
{:shortdesc}

## Antes de empezar
En primer lugar, acceda al menú de dispositivo y asegúrese de que tiene los permisos de cuenta correctos para completar las tareas.

* Acceda al menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos.

Para obtener más información sobre los permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/vsi?topic=virtual-servers-managing-device-access).

## Migración desde el host dedicado
Siga los pasos siguientes para migrar instancias de host dedicadas a otro host dedicado dentro del mismo POD desde la página Detalles del dispositivo del *host dedicado original*. 

1. En el menú **Dispositivos**, seleccione **Lista de dispositivos**.
2. Seleccione el host o la instancia alojada en la lista.
3. Pulse la lista desplegable **Acciones** que hay junto a la instancia dedicada que se va a migrar.
4. Seleccione **Migrar** y especifique el host al que se migra la instancia; recuerde que el host de destino debe estar dentro del mismo POD que el host original.
5. Pulse **Migrar** para empezar la migración. 

La migración comenzará inmediatamente. Durante la migración, la instancia dedicada estará fuera hasta en su nuevo host. Puede ver la página de detalles del dispositivo del host de destino para asegurarse de que la instancia se migra correctamente.

## Migración desde la instancia dedicada
Siga los pasos siguientes para migrar instancias de host dedicadas a otro host dedicado dentro del mismo POD desde la página Detalles de la *instancia de host dedicada*.

1. En el menú **Dispositivos**, seleccione **Lista de dispositivos**.
2. Seleccione en la lista la instancia alojada que se va a migrar.
3. Pulse **Migrar**.
4. Seleccione el host de destino al que desea migrar la instancia; recuerde que el host de destino debe estar dentro del mismo POD que el host original.
5. Pulse **Migrar** para empezar la migración.

La migración comenzará inmediatamente. Durante la migración, la instancia dedicada estará fuera hasta en su nuevo host. Puede ver la página de detalles del dispositivo del host de destino para asegurarse de que la instancia se migra correctamente.

## Siguientes pasos
Después de migrar una instancia de host dedicada, confirme que la migración se ha realizado correctamente; para ello verifique que su estado aparece en verde en la página Detalles del dispositivo del nuevo host dedicado.

