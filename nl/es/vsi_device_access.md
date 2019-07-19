---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Gestión del acceso a dispositivos
{: #managing-device-access}

Para acceder y gestionar los detalles de un dispositivo específico, debe tener otorgados los permisos adecuados en su cuenta de usuario.  Después de que el administrador de la cuenta le otorgue acceso de cuenta de usuario a un dispositivo, puede ver los detalles del dispositivo utilizando la consola de {{site.data.keyword.cloud}} o la {{site.data.keyword.slapi_short}}. La información o las acciones que verá dependerán del tipo de dispositivo, así como de los permisos que tenga otorgados su cuenta de usuario.
{:shortdesc}

Si la cuenta tiene dispositivos a los que no se les ha otorgado acceso, verá un nombre "Dispositivo desconocido" cuando intente acceder a dichos dispositivos.
{:note}

Puede asignar acceso al dispositivo a cualquier usuario de su cuenta, pero no a usted mismo. Sólo un administrador de la cuenta tiene acceso a todos los dispositivos de su cuenta de cliente y puede establecer el acceso para todos los demás usuarios de su cuenta. 

Debe tener los siguientes permisos para acceder a los detalles del dispositivo para servidores virtuales públicos o servidores virtuales dedicados.

* **Ver detalles de servidores virtuales**: le permite ver las direcciones IP, el tipo de sistema operativo, las contraseñas y más de un determinado servidor virtual.  También le permite actualizar las contraseñas del servidor virtual en el portal. Debe tener este acceso para ver instancias públicas, instancias dedicadas e instancias de host dedicadas.

* **Ver detalles de host dedicado virtual**: le permite ver las direcciones IP, el tipo de sistema operativo, las contraseñas y más de un determinado host dedicado.  También le permite migrar instancias dedicadas a otro host dedicado. Debe tener este acceso para ver los hosts dedicados.


## Adición de permisos para los usuarios
Si es el administrador de la cuenta y desea otorgar a los usuarios el permiso para ver los detalles del servidor virtual y los detalles del host dedicado, realice los pasos siguientes.

1. Inicie sesión en la página [Acceso (IAM) ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/iam#/users){: new_window} de la consola {{site.data.keyword.cloud}}. 
2. En el separador **Usuarios**, seleccione **Ver por: Mis usuarios de infraestructura clásica**.
3. Seleccione un usuario y luego pulse el separador **Infraestructura clásica**.
4. Expanda la categoría **Dispositivos** del separador **Permisos** y seleccione **Ver detalles de servidor virtual** y **Ver detalles de host dedicado virtual**.
5. Pulse **Aplicar**.

### Adición de permisos específicos a nivel de dispositivo
Si desea proporcionar a los usuarios acceso a un nivel de dispositivo específico, realice los pasos siguientes.

1. En el separador **Usuarios**, seleccione **Ver por: Mis usuarios de infraestructura clásica**. 
2. Seleccione un usuario y luego pulse el separador **Infraestructura clásica**.
3. En la sección **Seleccionar tipo** del separador **Dispositivos**, seleccione el permiso adecuado: **Todos los servidores nativos**, **Todos los hosts dedicados** o **Todos los servidores virtuales**. 
4. En la sección **Habilitar acceso futuro** del separador **Dispositivos**, seleccione el permiso adecuado: **Acceso automático a servidor nativo**, **Acceso automático a host dedicado** o **Acceso automático a servidor virtual**. Este permiso permite que los usuarios siempre tengan acceso al tipo de dispositivo cuando se añadan nuevos dispositivos.
5. Pulse **Establecer** para aplicar los nuevos permisos.

## Adición de permisos para los usuarios en el portal de clientes
Si es el administrador de la cuenta y desea otorgar a los usuarios el permiso para ver los detalles del servidor virtual y los detalles del host dedicado, realice los pasos siguientes.

1. Acceda al [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
2. Seleccione **Cuenta > Usuarios** en la barra de navegación para acceder a la pantalla Usuarios.
3. Pulse el nombre de usuario pertinente para acceder al perfil de usuario.
4. Pulse el icono **Permisos del portal** para acceder a la pantalla Permisos del portal.
5. En el separador **Dispositivo**, seleccione **Ver detalles del servidor virtual** y **Ver detalles de host dedicado virtual** para añadir estos permisos al perfil del usuario.

### Adición de permisos a un nivel de dispositivo específico en el portal de clientes
Para proporcionar acceso a un nivel de dispositivo específico, siga los pasos siguientes.

1. Pulse el icono **Acceso a dispositivo** para acceder a la pantalla Acceso a dispositivo.
2. Pulse el separador **Acceso rápido**. 
3. En la lista desplegable **Tipo de dispositivo**, seleccione **Todos los servidores virtuales** y **Todos los hosts dedicados**.
4. Marque el recuadro de selección **Otorgar automáticamente acceso cuando se añadan nuevos dispositivos** si el usuario asociado debe tener siempre acceso a este tipo de dispositivo.
5. Verifique que se han seleccionado los dispositivos correctos.
6. Pulse **Actualizar acceso a dispositivo**.

También puede utilizar el servicio de la API SoftLayer_User_Customer::addBulkDedicatedHostAccess para otorgar a un usuario acceso a uno o varios hosts dedicados. Para obtener más información, consulte [Adición de acceso masivo a host dedicado ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/reference/services/SoftLayer_User_Customer/addBulkDedicatedHostAccess/){: new_window}.  
{:note}

## Siguientes pasos
Los permisos de usuario se actualizan inmediatamente después de que se envíen los cambios. Si se han otorgado permisos, el usuario puede ver o interactuar con las características seleccionadas. Si se han retirado permisos, el usuario ya no puede ver ni interactuar con las características seleccionadas. Los permisos se pueden volver a actualizar en cualquier momento.

