---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestión de scripts de suministro
{: #managing-a-provisioning-script}

Puede utilizar los scripts de suministro para especificar un URL a un script que se ejecuta en un dispositivo recién suministrado. Un script de suministro puede ser cualquier archivo que el sistema operativo (SO) pueda ejecutar, incluidos archivos binarios combinados o cualquier idioma admitido por el SO. No hay restricciones para el nombre del script; sin embargo, utilizar un convenio de denominación similar cada script hace que sea más fácil identificar. Los scripts de suministro deben estar asociados con un nombre de dominio completo y deben ser accesibles utilizando los protocolos HTTP o HTTPS. El tipo de protocolo que se utiliza afecta a la respuesta automatizada del sistema cuando el script de suministro se descarga al dispositivo.  
{:shortdesc}

* El uso del **protocolo HTTP** requiere que un administrador ejecute el script manualmente una vez se haya descargado.
* El uso de **protocolo HTTPS** descarga y ejecuta el script automáticamente, si es posible. Si el URL no está asociado a un script válido, el script se descarga y no es necesario realizar ninguna otra acción.

## Antes de empezar
En primer lugar, acceda al menú de dispositivo y asegúrese de que tiene los permisos de cuenta correctos para completar las tareas. 

* Acceda al menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos. 

Para obtener más información sobre los permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/vsi?topic=virtual-servers-managing-device-access).

## Adición de un script de suministro
{: #add-provisioning-script}

1. Desde el menú **Dispositivos**, seleccione **Gestionar > Scripts de suministro**.
2. Seleccione **Añadir script de suministro**. 
3. Especifique un nombre identificativo para el script de suministro en el campo **Nombre**.
4. Especifique el nombre de dominio completo que está asociado con el script en el campo **URL**.
5. Pulse **Añadir** para añadir el script de suministro a la cuenta. 

## Edición de detalles de script de suministro
{: #edit-provisioning-script-details}

1. Desde el menú **Dispositivos**, seleccione **Gestionar > Scripts de suministro**.
2. Pulse en cualquier lugar de la columna **Nombre** o **URL** del script de suministro para abrir el script para editarlo.
3. Actualice el nombre o URL.
   Cuando actualice un URL, debe utilizar un nombre de dominio completo o el cambio no se guardará.
   {:note}
4. Pulse en cualquier lugar de la pantalla para guardar el cambio.

## Siguientes pasos

Los scripts de suministro que están asociados con una cuenta se pueden modificar o eliminar en cualquier momento. Los scripts de suministro se guardan en la consola de {{site.data.keyword.cloud_notm}} hasta que se eliminan y se pueden asociar a cualquier dispositivo nuevo que se haya pedido a través de la consola de {{site.data.keyword.cloud_notm}}. Si el script está asociado con un URL HTTP, se descarga en el nuevo dispositivo durante el suministro y el administrador debe iniciar sesión en el dispositivo para ejecutar el script manualmente. Los scripts que están asociados con los URL HTTPS se descargan y, cuando proceda, se ejecutan en el nuevo dispositivo sin que se necesite interacción adicional. 

Si edita un script, las actualizaciones válidas se visualizan inmediatamente en la pantalla. Los cambios realizados en los scripts de suministro existentes no afectan a los dispositivos ya suministrados.

