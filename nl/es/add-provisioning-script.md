---

copyright:
  years: 2014, 2018
lastupdated: "2018-04-27"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestión de un script de suministro
{: #managing-a-provisioning-script}

Utilice los scripts de suministro para un URL para que se ejecute un script en un dispositivo recién suministrado. No hay restricciones para el nombre del script; sin embargo, utilizar un convenio de denominación similar cada script hace que sea más fácil identificar. Los scripts de suministro deben estar asociados con un nombre de dominio completo y deben ser accesibles utilizando los protocolos HTTP o HTTPS. El tipo de protocolo que se utiliza afecta a la respuesta automatizada del sistema cuando el script de suministro se descarga al dispositivo.

* El uso del **protocolo HTTP** requiere que un administrador ejecute el script manualmente una vez se haya descargado.
* El uso de **protocolo HTTPS** descarga y ejecuta el script automáticamente, si es posible. Si el URL no está asociado a un script ejecutable, el script se descarga y no es necesario realizar ninguna otra acción.

## Acceso a la pantalla de scripts de suministro
1. Acceda al [{{site.data.keyword.slportal_full}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} con sus credenciales exclusivas.
2. Seleccione **Dispositivos > Gestionar > Scripts de suministro** desde la navegación para acceder a la pantalla de scripts de suministro.


## Adición de un script de suministro
{: #add-provisioning-script}

1. Desde la pantalla **Scripts de suministro** del {{site.data.keyword.slportal}}, pulse **Añadir script de suministro** en la parte superior de la pantalla.
* Especifique un **nombre identificativo** para el script de suministro en el campo **Nombre**.
* Especifique el **nombre de dominio completo** que está asociado con el script en el campo **URL**.
* Pulse **Añadir** para añadir el script de suministro a la cuenta. Pulse **Cancelar** si desea cancelar la acción.

## Edición de detalles de script de suministro

1. En la pantalla **Scripts de suministro** del {{site.data.keyword.slportal}}, pulse en cualquier lugar de la columna **Nombre** o **URL** del script de suministro para abrir el script para editarlo.
3. Actualice el nombre o URL.
  * **Nota:** Cuando actualice un URL, debe utilizar un nombre de dominio completo o el cambio no se guardará.
4. Pulse en cualquier lugar de la pantalla para guardar el cambio.

## Siguientes pasos

Los scripts de suministro que están asociados con una cuenta se pueden modificar o eliminar en cualquier momento. Los scripts de suministro se guardan en el {{site.data.keyword.slportal}} hasta que se eliminan y se pueden asociar a cualquier dispositivo nuevo que se haya pedido a través del {{site.data.keyword.slportal}}. Si el script está asociado con un URL HTTP, se descarga en el nuevo dispositivo durante el suministro. Los scripts que están asociados con los URL HTTPS se descargan y, cuando proceda, se ejecutan en el nuevo dispositivo.

Después de editar un script, las actualizaciones válidas se visualizan inmediatamente en la pantalla. Los cambios realizados en los scripts de suministro existentes no afectan a los dispositivos ya suministrados.
