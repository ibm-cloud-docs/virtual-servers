---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestión de picos de tráfico con escalado automático basado en recursos
{: #managing-resourced-based-auto-scaling}

El lanzamiento de un producto nuevo o una rebaja en el precio de un producto existente puede provocar un pico de tráfico en su sitio web. Un pico en el tráfico puede afectar al tiempo de respuesta, lo que afecta a la experiencia de los clientes con su sitio web. El escalado automático de {{site.data.keyword.cloud}} le permite responder automáticamente a los picos de tráfico. Puede utilizar el escalado automático basado en recursos para controlar estos picos de tráfico.
{:shortdesc}

## Antes de empezar
En primer lugar, acceda al menú de dispositivo y asegúrese de que tiene los permisos de cuenta correctos para completar las tareas.

* Acceda al menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Si no es el administrador de la cuenta, su cuenta de usuario debe incluir el permiso para utilizar el escalado automático. Para obtener más información sobre la actualización de permisos para utilizar el escalado automático, consulte [Configuración de permisos de usuario para el escalado automático](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos. 

Para obtener más información sobre los permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/vsi?topic=virtual-servers-managing-device-access).

## Adición de un grupo de escalado automático
{: #adding-auto-scale-group}

Por ejemplo, un sitio web de comercio electrónico basado en Dallas, Texas, requiere que tres servidores virtuales estén en línea en todo momento. El negocio aumenta entre las horas de 9:00 y 17:00 cada día laborable, cuando la empresa mantiene ventas en línea. Para ayudar a mantener los tiempos de respuesta del sitio web, se necesitan tres servidores virtuales adicionales durante estos tiempos. Además, cuando el tráfico de entrada público tiene como promedio más de 5 MB por segundo en todos los servidores virtuales durante 10 minutos, deben suministrarse otros dos servidores virtuales. Cuando el tráfico esté por debajo de 5 MB por segundo, dichos servidores virtuales adicionales se deben cancelar y eliminar. El objetivo es no tener más de cinco servidores virtuales que manejen el aumento del tráfico, lo que evita que los servidores virtuales de la semana se vean afectados por el tráfico adicional de la semana. En los pasos siguientes se muestra cómo configurar el escalado automático para dar soporte al escalado basado en recursos.

1. En el menú **Dispositivos**, seleccione **Escalado automático**.
2. Seleccione **Añadir grupo de escalado automático**.
3. Configure un grupo de escalado automático especificando en primer lugar un **Nombre de grupo**, como por ejemplo Grupo de escalado de fin de semana y, a continuación, seleccione el centro de datos.
4. Seleccione la política de terminación del servidor. Por ejemplo, si elige **Más antiguo**, se selecciona el servidor con la fecha proporcionada más antigua al escalar hacia abajo.
5. Indique si el grupo va a ser un grupo de escalado de varias VLAN y cómo equilibrar el escalado hacia abajo entre los pares de VLAN configurados.
6. Seleccione las VLAN públicas y privadas en las que desea que se suministren los servidores. Si se va a acceder a los servidores desde internet público (si la VLAN está ejecutando servidores web), deje **Solo red privada** sin marcar.
7. Establezca el **Recuento mínimo de miembros** en 3 y el **Recuento máximo de miembros** en 6. Establezca el **Periodo de recuperación** en 0. Como se trata de un escalado basado en planificación, no hay estadísticas recopiladas para desencadenar acciones de escalado.

## Definición de la configuración de miembros para el grupo
{: #defining-member-configuration}

1. Localice **Configuración de miembro** y especifique un **Nombre de host** y un **Dominio** para el servidor de escalado. A los servidores posteriores que se agreguen al grupo se les añaden sufijos exclusivos al nombre de host.
2. Especifique la configuración de hardware de las instancias de cálculo (núcleos, RAM, etc.).
3. Seleccione un sistema operativo si desea instalar el sistema operativo mínimo. También puede utilizar una **Imagen pública** o una **Imagen privada** para suministrar las instancias.
4. Si las instancias requieren pasos adicionales para instalar software adicional, especifique el URL de un **Script posterior a la instalación** para instalar el software. (Si utiliza un equilibrador de carga para el grupo, los scripts posteriores a la instalación se ejecutan antes de que se coloque un miembro detrás de un equilibrador de carga).

## Configuración de políticas
{: #setting-up-policies}

En el caso de ejemplo, el sitio web de comercio electrónico está utilizando el escalado basado en recursos. Se necesitan dos políticas: una para tener una acción de escalado relativa de +3 para el periodo de tiempo necesario, y una segunda para tener una acción de absolución de 3 cuando el pico haya terminado. La primera política es añadir los recursos.

1. Desplácese hacia abajo hasta **Políticas** y pulse **Añadir política**. Especifique el **Nombre de política**, (Escalado hacia arriba de día laborable).
2. Seleccione la opción de recuperación de grupo para el **Periodo de recuperación**.
3. Pulse **Añadir desencadenante** y especifique un desencadenante de repetición seleccionando **Cada** en el primer menú desplegable; a continuación, resalte **Lunes, martes, miércoles, jueves,** y **Viernes** y **14:00**\* desde los recuadros desplegables siguientes. (El recuadro de selección **Edición avanzada** le permite especificar la frecuencia de desencadenante en la notación de tipo crontab).
4. Pulse el recuadro desplegable **Escalar por** en **Acción** y seleccione **Exacto**. Escriba 3 en el campo **Miembros**.
5. Pulse **Añadir política** de nuevo para especificar la segunda política que elimina los servidores todas las tardes. El periodo de recuperación es el mismo que la recuperación del grupo. El desencadenante es cada lunes, martes, miércoles, jueves y viernes a las 22:00\*, con una acción de escala exacta de 3. La hora especificada en el campo **Desencadenantes** se basa en la hora UTC, que es el motivo por el que necesita seleccionar 14:00 para 9:00 Central Daylight Time y 22:00 para 17:00 Central Daylight Time. Durante Central Standard Time, las horas podrían ser 13:00 y 21:00, porque UTC/GMT no reconoce el horario de verano. Consulte el sitio [World Time Server ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} para ver un convertidor de horas.
6. Configure otro grupo con recuperación de 0, llamado, por ejemplo, Grupo de ráfagas de tráfico, con un recuento mínimo de miembros de 0 y un máximo de 5. Utilice los mismos valores para la configuración del grupo y del miembro que el grupo Escalado hacia arriba de día laborable, excepto para el nombre de grupo.
7. Pulse **Añadir política** para añadir la segunda política que controla los dos servidores adicionales cuando el tráfico de entrada público tiene como promedio más de 5 MB por segundo en todos los servidores virtuales durante 10 minutos.
8. Especifique el **Nombre de política**, por ejemplo Grupo de ráfagas de tráfico.
9. Seleccione la opción de recuperación de grupo para el **Periodo de recuperación**.
10. Pulse **Añadir desencadenante**. Deje el valor predeterminado **Si mi** en el primer recuadro y seleccione **Mbps entrantes de red pública** para el segundo recuadro. Deje el signo > predeterminado en el tercer recuadro. En el cuarto recuadro, escriba **5** (5 MB), escriba **600** en el quinto recuadro y seleccione **Segundos** en el último recuadro para representar 10 minutos.
11. Pulse el recuadro desplegable **Escalar por** en **Acción** y seleccione **Relativo**. Escriba 2 en el campo **Miembros**.
12. Pulse **Añadir política** de nuevo para especificar la segunda política que elimina los servidores cuando haya descendido el tráfico a menos de 5 Mbps\*El periodo de recuperación será el mismo que la recuperación del grupo. El desencadenante es si los Mbps entrantes de red pública son menos de 5 (5 Mbps) durante un periodo de 600 segundos (10 minutos).

Cuando se crean ambos grupos, el grupo de Escalado hacia arriba de día laborable crea tres servidores (lo mínimo). Los días laborables, a las 9:00 Central Time, se añaden tres servidores más, y a las 17:00 Central Time, los servidores se eliminan. No hay ninguna otra forma de añadir o eliminar los miembros de dicho grupo. En un Grupo de ráfagas de tráfico completamente independiente, se añaden dos servidores cada 10 minutos, en los que el tráfico público entrante entre todos los miembros tiene como valor promedio 5 MB por segundo, hasta que llega al máximo de cinco del grupo. Después de que el tráfico público de entrada se mantenga por debajo de dicha cantidad durante 10 minutos, se eliminarán todos los servidores de este grupo.

