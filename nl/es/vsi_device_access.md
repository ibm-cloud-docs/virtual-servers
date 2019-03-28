---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Gestión del acceso a dispositivos
{: #managing-device-access}

Para acceder y gestionar los detalles de un dispositivo específico, debe tener otorgados los permisos adecuados a su cuenta de usuario.  Después de que el administrador de la cuenta le otorgue acceso de cuenta de usuario a un dispositivo, puede ver los detalles del dispositivo utilizando el {{site.data.keyword.slportal_full}} o la API.  La información o acción que verá depende del tipo de dispositivo, así como de los permisos que tenga otorgados su cuenta de usuario.
{:shortdesc}

**Nota:** Si la cuenta tiene dispositivos a los que no se les ha otorgado acceso, verá un nombre "Dispositivo desconocido" cuando intente acceder a dichos dispositivos.

Puede asignar acceso al dispositivo a cualquier usuario de su cuenta, pero no a usted mismo. Sólo un administrador de la cuenta tiene acceso a todos los dispositivos de su cuenta de cliente y puede establecer el acceso para todos los demás usuarios de su cuenta.

Debe tener los siguientes permisos para acceder a los detalles del dispositivo para servidores virtuales públicos o servidores virtuales dedicados.

**Ver detalles de servidores virtuales**

Le permite ver las direcciones IP, el tipo de sistema operativo, las contraseñas y más de un determinado servidor virtual.  También le permite actualizar las contraseñas del servidor virtual en el portal. Un usuario debe tener este acceso para ver instancias públicas, instancias dedicadas e instancias de host dedicadas.

**Ver detalles de host virtual dedicado**

Le permite ver las direcciones IP, el tipo de sistema operativo, las contraseñas y más de un determinado host dedicado.  También le permite migrar instancias dedicadas a otro host dedicado. Un usuario debe tener este acceso para ver los hosts dedicados.

## Adición de permiso para ver instancias de servidor virtual
Siga los pasos siguientes para añadir permisos para *Ver detalles del servidor virtual* a cualquiera de los usuarios hijo. Sólo un administrador de la cuenta puede otorgar permisos a otros usuarios en su cuenta.  

1. Acceda al [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
2. Seleccione **Cuenta > Usuarios** en la barra de navegación para acceder a la pantalla Usuarios.
3. Pulse el nombre de usuario pertinente para acceder al perfil de usuario.
4. Pulse el icono **Permisos del portal** para acceder a la pantalla Permisos del portal.
5. En el separador *Dispositivo*, seleccione **Ver detalles del servidor virtual** para añadir este permiso al perfil de usuario.

Para proporcionar acceso a un nivel de dispositivo específico, siga los pasos siguientes.

1. Pulse el icono **Acceso a dispositivo** para acceder a la pantalla Acceso a dispositivo.
2. Pulse el separador **Acceso rápido**.
   Nota: otra opción es seleccionar en su lugar un dispositivo individual.
3. En la lista desplegable *Tipo de dispositivo*, seleccione **Todos los servidores virtuales**.
4. Marque el recuadro de selección **Otorgar automáticamente acceso cuando se añadan nuevos dispositivos** si el usuario asociado debe tener siempre acceso a este tipo de dispositivo.
5. Verifique que se han seleccionado los dispositivos correctos.
6. Pulse **Actualizar acceso a dispositivo**.

## Adición de permiso para ver hosts dedicados
Siga los pasos siguientes para añadir permisos para *Ver detalles de host dedicado virtual* a cualquiera de los usuarios hijo. Sólo un administrador de la cuenta puede otorgar permisos a otros usuarios en su cuenta.

1. Acceda al [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
2. Seleccione **Cuenta > Usuarios** en la barra de navegación para acceder a la pantalla Usuarios.
3. Pulse el nombre de usuario pertinente para acceder al perfil de usuario.
4. Pulse el icono **Permisos del portal** para acceder a la pantalla Permisos del portal.
5. En el separador *Dispositivo*, seleccione **Ver detalles de host dedicado virtual** para añadir este permiso al perfil de usuario.

Para proporcionar acceso a un nivel de dispositivo específico, siga los pasos siguientes.

1. Pulse el icono **Acceso a dispositivo** para acceder a la pantalla Acceso a dispositivo.
2. Pulse el separador **Acceso rápido**.
   Nota: otra opción es seleccionar en su lugar dispositivos individuales.
3. En la lista desplegable *Tipo de dispositivo*, seleccione **Todos los hosts dedicados**.
4. Marque el recuadro de selección **Otorgar automáticamente acceso cuando se añadan nuevos dispositivos** si el usuario asociado debe tener siempre acceso a este tipo de dispositivo.
5. Verifique que se han seleccionado los dispositivos correctos.
6. Pulse **Actualizar acceso a dispositivo**.

**Nota:** también puede utilizar el servicio de la API SoftLayer_User_Customer::addBulkDedicatedHostAccess para otorgar a un usuario acceso a uno o varios hosts dedicados. Para obtener más información, consulte [Adición de acceso masivo a host dedicado ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/reference/services/SoftLayer_User_Customer/addBulkDedicatedHostAccess/){: new_window}.  

## Siguientes pasos
Los permisos de usuario se actualizan inmediatamente después de que se envíen los cambios. Si se han otorgado permisos, el usuario puede ver o interactuar con las características seleccionadas. Si se han retirado permisos, el usuario ya no puede ver ni interactuar con las características seleccionadas. Los permisos se pueden volver a actualizar en cualquier momento.
