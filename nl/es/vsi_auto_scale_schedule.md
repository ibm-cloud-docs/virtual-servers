---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestión de picos de tráfico con escalado automático basado en planificación
{: #managing-schedule-based-auto-scaling}

Los picos de tráfico web pueden ser algo bueno y malo. Los picos son buenos en el sentido de que hay más personas que utilizan su sitio; aunque pueden resultar negativos porque un aumento en la actividad puede afectar a los tiempos de respuesta. El escalado automático de {{site.data.keyword.cloud}} le proporciona la capacidad de escalar automáticamente los servidores para dar soporte a sus necesidades empresariales. Puede utilizar el escalado automático basado en planificación para controlar estos picos de tráfico. 
{:shortdesc}

## Antes de empezar
En primer lugar, acceda al menú de dispositivo y asegúrese de que tiene los permisos de cuenta correctos para completar las tareas.

* Acceda al menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Si no es el administrador de la cuenta, su cuenta de usuario debe incluir el permiso para utilizar el escalado automático. Para obtener más información sobre la actualización de permisos para utilizar el escalado automático, consulte [Configuración de permisos de usuario para el escalado automático](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos. 

Para obtener más información sobre los permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/vsi?topic=virtual-servers-managing-device-access).

## Adición de un grupo de escalado automático
{: #add-auto-scale-group}

En este caso de ejemplo, un sitio web social basado en Texas, Dallas, experimenta picos de actividad durante los fines de semana. Dos servidores virtuales son el mínimo requerido por el sitio de lunes a viernes; sin embargo, cada fin de semana se necesitan dos servidores virtuales adicionales para estar preparado antes el aumento del tráfico. Los pasos siguientes le llevan a través de cómo configurar el escalado automático para dar soporte al escalado basado en planificación.

1. En el menú **Dispositivos**, seleccione **Escalado automático**.
2. Seleccione **Añadir grupo de escalado automático**.
3. Configure un grupo de escalado automático especificando en primer lugar un **Nombre de grupo**, como por ejemplo Grupo de escalado de fin de semana y, a continuación, seleccione el centro de datos.
4. Seleccione la política de terminación del servidor. Por ejemplo, si elige **Más antiguo**, se selecciona el servidor con la fecha proporcionada más antigua al escalar hacia abajo.
5. Indique si el grupo va a ser un grupo de escalado de varias VLAN y cómo equilibrar el escalado hacia abajo entre los pares de VLAN configurados.
6. Seleccione las VLAN públicas y privadas en las que desea que se suministren los servidores. Si se va a acceder a los servidores desde internet público (si la VLAN está ejecutando servidores web), deje **Solo red privada** sin marcar.
7. Establezca el **Recuento mínimo de miembros** en 2 y el **Recuento máximo de miembros** en 4. Establezca el **Periodo de recuperación** en 0. Como se trata de un escalado basado en planificación, no hay estadísticas recopiladas para desencadenar acciones de escalado.

## Definición de la configuración de miembros para el grupo
{: #define-member-configuration}

1. Localice **Configuración de miembro** y especifique un **Nombre de host** y un **Dominio** para el servidor de escalado. A los servidores posteriores que se agreguen al grupo se les añaden sufijos exclusivos al nombre de host.
2. Especifique la configuración de hardware de las instancias de cálculo (núcleos, RAM, etc.).
3. Seleccione un sistema operativo si desea instalar el sistema operativo mínimo. También puede utilizar una imagen pública o una imagen privada para suministrar las instancias.
4. Si las instancias requieren pasos adicionales para instalar software adicional, especifique el URL de un script posterior a la instalación para instalar el software. (Si utiliza un equilibrador de carga para el grupo, los scripts posteriores a la instalación se ejecutan antes de que se coloque un miembro detrás de un equilibrador de carga).

## Configuración de políticas
{: #set-up-policies}

En este caso de ejemplo, el sitio web social está utilizando el escalado basado en planificación. Se necesitan dos políticas: una para escalar los servidores hacia arriba los viernes por la tarde, y una segunda para escalar los servidores hacia abajo los domingos por la noche. La primera política consiste en escalar hacia arriba los servidores.

1. Localice **Políticas** y pulse **Añadir política**. Especifique el **Nombre de política**, (Escalado hacia arriba de viernes).
2. Seleccione la opción de recuperación de grupo para el **Periodo de recuperación**.
3. Pulse **Añadir desencadenante** y especifique un desencadenante de repetición seleccionando **Cada** en el primer menú desplegable, y a continuación seleccione **Viernes** y **22:00**\* en los menús desplegables siguientes. (El recuadro de selección **Edición avanzada** le permite especificar la frecuencia de desencadenante en la notación de tipo crontab).
4. Pulse el recuadro desplegable **Escalar por** en **Acción** y seleccione **Relativo**. Escriba 2 en el **campo Miembros**.
5. Pulse **Añadir política** de nuevo para especificar la segunda política que escala los servidores hacia abajo los domingos por la noche. El periodo de recuperación es el mismo que la recuperación del grupo. El desencadenante es cada domingo a las 1:00*, con una acción de escala relativa de -2.
6. La hora especificada en el campo **Desencadenantes** se basa en la hora UTC, por lo que es necesario seleccionar 22:00 para 17:00 Central Daylight Time y 1:00 para 20:00 Central Daylight Time. Durante Central Standard Time, las horas podrían ser 9:00 y 12:00 respectivamente porque UTC/GMT no reconoce el horario de verano. Consulte el sitio [World Time Server ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} para ver un convertidor de horas.

## Adición de un equilibrador de carga local

Si tiene un equilibrador de carga local configurado, puede utilizarlo para equilibrar la carga del grupo de escalado automático.

1. Localice **Equilibradores de carga locales** y pulse **Añadir equilibrador de carga**.
2. Pulse **Ver valores de VIP** (se abre una página distinta) para ver los equilibradores de carga locales disponibles en su cuenta y ordenar uno nuevo si es necesario. Un equilibrador de carga necesita tener un grupo de servicios asociado para utilizarse con un grupo de escalado automático. Asegúrese de que el equilibrador de carga esté ubicado en el centro de datos del grupo de escalado automático.
3. Pulse **Añadir equilibrador de carga** en la página **Añadir grupo de escalado automático**, pulse la flecha desplegable de la IP virtual IP y seleccione el equilibrador de carga.
4. Pulse las flechas desplegables correspondientes a **Grupo de servicio**, **Puerto de servicio** y **Tipo de comprobación de estado de servicio** y seleccione los valores adecuados.
5. Pulse **Añadir grupo** para guardar el grupo.
6. Si todos los centros de datos, redes, etc., están correctamente especificados, se creará el grupo de escalado automático. Pulse el grupo en la pantalla **Ver todos los grupos** para ver los detalles del grupo.

El resultado de configurar un escalado basado en planificación es que se proporcionan automáticamente dos miembros para que cumplan el requisito mínimo del sitio web. Los viernes a las 17:00 Central Time, se suministran dos miembros más automáticamente cuando se activa el primer desencadenante de política. Luego, los domingos a las 20:00 Central Time, se reclaman dos miembros gracias al segundo desencadenante de política. Si especifica un equilibrador de carga, todos los miembros que se crean durante la creación o el viernes están detrás del equilibrador de carga después de que se ejecute el script personalizado posterior a la instalación.
