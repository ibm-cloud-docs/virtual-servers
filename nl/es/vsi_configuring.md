---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Configuración de servidores virtuales
{: #configuring-virtual-servers}

Cuando tenga acceso al servidor virtual, asegúrese de cambiar la contraseña y plantéese configurar SSH para mejorar la seguridad de la solución de autenticación. Existen otras muchas opciones para configurar su servidor virtual para que cumpla las necesidades de su entorno.
{:shortdesc}

## Inicie una sesión
Inicie sesión en la [consola de {{site.data.keyword.cloud}}
![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/classic?){: new_window} con las credenciales que ha recibido en un correo electrónico cuando su cuenta se creó inicialmente. También puede iniciar la sesión en el [{{site.data.keyword.slportal}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){:new_window}.

## Localice su servidor virtual
Busque su servidor virtual en la lista de dispositivos en la consola de {{site.data.keyword.cloud_notm}}. Desde la lista de dispositivos puede gestionar dispositivos, actualizar dispositivos o generar gráficos de uso de ancho de banda. Para obtener más información, consulte [Gestión de servidores virtuales](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).

## Cambiar la contraseña
Cambie su contraseña utilizando las directrices para crear una contraseña fuerte. Consulte
[Visualización y gestión de nombres de usuario y contraseñas de dispositivos](/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device#view-update-user-name-password-for-device).

## Configurar SSH
SSH proporciona una mejor solución de seguridad que la autenticación por contraseña. Consulte
[Iniciación a las claves SSH](/docs/infrastructure/ssh-keys?topic=ssh-keys-getting-started-tutorial#getting-started-tutorial).

## Registre las direcciones IP y las credenciales
Conserve un registro de las direcciones IP y credenciales correspondientes al servidor en un lugar seguro para poder consultarlo rápidamente sin tener que iniciar una sesión en la consola de {{site.data.keyword.cloud_notm}}.
- Las direcciones IP de dispositivos individuales se pueden ver en la lista de dispositivos.
- Las contraseñas root de los dispositivos individuales se pueden ver en la vista de instantáneas del dispositivo. Pulse la flecha que hay junto al nombre del dispositivo para expandir la vista.
- Se pueden ver varias direcciones IP de dispositivos mediante la acción Descargar CSV de la lista de dispositivos. Seleccione Descargar CSV en la rueda dentada de Configuración para descargar una lista completa de dispositivos y sus detalles en formato de hoja de cálculo.

## Actualice las credenciales de software
Se asignan credenciales a todo el software que se ha cargado en el dispositivo durante el proceso de suministro. Estas credenciales se pueden ver y gestionar desde el separador Contraseñas de cada dispositivo en la consola de {{site.data.keyword.cloud_notm}}. Utilice estas credenciales temporales para acceder al software por primera vez. Se recomienda cambiar la contraseña del software después de acceder al mismo por primera vez. Utilice contraseñas seguras que contengan una combinación de letras, números y símbolos.

Opcionalmente, las actualizaciones de contraseñas se pueden almacenar en el separador Contraseñas para cada dispositivo; sin embargo, tenga en cuenta que si almacena contraseñas en la consola de {{site.data.keyword.cloud_notm}}, cualquier persona con acceso a la cuenta y los permisos adecuados puede ver las contraseñas guardadas en la pantalla Contraseñas.

Para obtener más información sobre la visualización y gestión de las credenciales de software, consulte
[Gestión del acceso a la infraestructura clásica](/docs/vsi?topic=iam-mngclassicinfra).

## Acceda a su servidor en la red privada
La red privada es el precursor de la interactuación con los dispositivos a través del escritorio remoto (RDP) mediante SSH y KVM sobre IP. La herramienta de acceso VPN permite la conexión de red privada con el punto final SSL VPN más cercano o con el punto final que elija. También se necesita acceso VPN para interactuar con diversos servicios que se ofrecen. Para obtener más información, consulte [Iniciación a las redes privadas virtuales (VPN)](/docs/infrastructure/iaas-vpn?topic=VPN-gettingstarted-with-virtual-private-networking).

## Configure la supervisión
La supervisión se utiliza principalmente como recurso para comprobar la disponibilidad del servidor, pero también resulta útil para saber cuándo realizar un escalado. Dispone de servicios de supervisión estándar y Nimsoft que cubren diversas necesidades de supervisión. La supervisión estándar, a veces denominada “supervisión básica”, se suele utilizar en el método ping y respuesta cuando se utiliza un ping lento o de servicio que se inicia mediante la consola de {{site.data.keyword.cloud_notm}}. La supervisión Nimsoft, también denominada “supervisión avanzada”, está disponible a tres niveles: básico, avanzado y premium. También se puede acceder a este servicio a través de la consola de {{site.data.keyword.cloud_notm}}. Para obtener más información, consulte [Supervisión](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring#monitoring).

## Configurar grupos de seguridad
Puede utilizar grupos de seguridad para limitar el tráfico de red en los servidores virtuales. Utilice grupos de seguridad para instaurar un conjunto de reglas de filtro de IP que definen cómo gestionar el tráfico de entrada y el de salida a la interfaz pública y privada de una instancia de servidor virtual. Para obtener más información, consulte [Iniciación a los grupos de seguridad](/docs/infrastructure/security-groups?topic=security-groups-getting-started).

## Configurar cortafuegos
También están disponibles los cortafuegos de hardware para obtener una protección aún mayor. Los cortafuegos de hardware se suministran bajo demanda sin tiempo de inactividad. Si se establecen las reglas correctamente, un cortafuegos puede proteger el servidor frente a una actividad no deseada. Después de solicitar un cortafuegos, se debe habilitar y se deben establecer reglas.

Para obtener más información, consulte la información siguiente.

* [Cortafuegos de hardware (compartido)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Cortafuegos de hardware (dedicado)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)

## Planifique copias de seguridad
Las copias de seguridad garantizan que los datos se guardan de forma segura fuera de su dispositivo y están protegidos en caso de pérdida. Dispone de los siguientes servicios de copia de seguridad para guardar los datos en un lugar seguro en caso de que tenga que volver a cargar la información en el dispositivo:
- {{site.data.keyword.backup_notm}} es un sistema de copia de seguridad automático basado en agente. Se trata de una conocida solución automatizada de muy fácil activación (“set-and-forget”) para la gestión del dispositivo. Es compatible con el software de Microsoft, incluidos Exchange y SQL mediante plugins adicionales. Los usuarios de {{site.data.keyword.backup_notm}} interactúan con este servicio a través de la aplicación basada en la web WebCC de {{site.data.keyword.backup_notm}}. Para obtener más información, consulte [Iniciación a los servicios de {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).
- R1Soft Continuous Data Protection es un software de copia de seguridad que se puede instalar en el servidor o en una máquina virtual autogestionada. Se recomienda utilizarlo si desea una sola interfaz para gestionar todas sus copias de seguridad. Puede interactuar con R1Soft CDP a través de su propio sistema de gestión, lo que permite instalar agentes en máquinas virtuales y ofrece plugins de base de datos para funciones adicionales. Para obtener más información, consulte [Iniciación a los servicios de {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).

## Siguientes pasos
Una vez configurado el servidor virtual, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión del servidor virtual](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
