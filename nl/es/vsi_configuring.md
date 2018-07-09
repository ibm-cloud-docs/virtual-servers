---



copyright:
  years: 2017, 2018
lastupdated: "2018-03-19"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Configuración de servidores virtuales
{: #configuring-virtual-servers}

Cuando tenga acceso a su servidor virtual, asegúrese de configurarlo de modo que se ajuste a las necesidades de su entorno.
{:shortdesc}

## Inicie una sesión 
Inicie una sesión en el [{{site.data.keyword.slportal_full}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} con las credenciales que ha recibido en un correo electrónico cuando se creó su cuenta inicialmente.

## Localice su servidor virtual
Busque su servidor virtual en la lista de dispositivos en el {{site.data.keyword.slportal}}. Desde la lista de dispositivos puede gestionar dispositivos, actualizar dispositivos o generar gráficos de uso de ancho de banda. Para obtener más información, consulte [Gestión de servidores virtuales](../vsi/vsi_managing.html).

## Registre las direcciones IP y las credenciales
Conserve un registro de las direcciones IP y credenciales correspondientes al servidor en un lugar seguro para poder consultarlo rápidamente sin tener que iniciar una sesión en el {{site.data.keyword.slportal}}. 
- Las direcciones IP de dispositivos individuales se pueden ver en la lista de dispositivos.
- Las contraseñas root de los dispositivos individuales se pueden ver en la vista de instantáneas del dispositivo. Pulse la flecha que hay junto al nombre del dispositivo para expandir la vista.
- Se pueden ver varias direcciones IP de dispositivos mediante la acción Descargar CSV de la lista de dispositivos. Seleccione Descargar CSV en la rueda dentada de Configuración para descargar una lista completa de dispositivos y sus detalles en formato de hoja de cálculo.

## Actualice las credenciales de software
Se asignan credenciales a todo el software que se ha cargado en el dispositivo durante el proceso de suministro. Estas credenciales se pueden ver y gestionar desde el separador Contraseñas de cada dispositivo en el {{site.data.keyword.slportal}}. Utilice estas credenciales temporales para acceder al software por primera vez. Se recomienda cambiar la contraseña del software después de acceder al mismo por primera vez. Utilice contraseñas seguras que contengan una combinación de letras, números y símbolos.

Opcionalmente, las actualizaciones de contraseñas se pueden almacenar en el separador Contraseñas para cada dispositivo; sin embargo, tenga en cuenta que si almacena contraseñas en el {{site.data.keyword.slportal}}, cualquier persona con acceso a la cuenta y los permisos adecuados puede ver las contraseñas guardadas en la pantalla Contraseñas.

Para obtener más información sobre cómo ver y gestionar sus credenciales de software, consulte [Gestión del acceso a la infraestructura](../iam/mnginfra.html).

## Acceda a su servidor en la red privada
La red privada es el precursor de la interactuación con los dispositivos a través del escritorio remoto (RDP) mediante SSH y KVM sobre IP. La herramienta de acceso VPN permite la conexión de red privada con el punto final SSL VPN más cercano o con el punto final que elija. También se necesita acceso VPN para interactuar con diversos servicios que se ofrecen. Para obtener más información, consulte [Iniciación a las redes privadas virtuales (VPN)](../infrastructure/iaas-vpn/getting-started.html).

## Configure la supervisión
La supervisión se utiliza principalmente como recurso para comprobar la disponibilidad del servidor, pero también resulta útil para saber cuándo realizar un escalado. Dispone de servicios de supervisión estándar y Nimsoft que cubren diversas necesidades de supervisión. La supervisión estándar, a veces denominada “supervisión básica”, se suele utilizar en el método ping y respuesta cuando se utiliza un ping lento o de servicio que se inicia mediante el {{site.data.keyword.slportal}}. La supervisión Nimsoft, también denominada “supervisión avanzada”, está disponible a tres niveles: básico, avanzado y premium. También se puede acceder a este servicio a través del {{site.data.keyword.slportal}}. Para obtener más información, consulte [Supervisión](../infrastructure/SLmonitoring/monitoring_index.html).

## Proteja su sistema
Dispone de cortafuegos de hardware para asegurarse de que el dispositivo está siempre protegido. Los cortafuegos de hardware se suministran bajo demanda sin tiempo de inactividad. Si se establecen las reglas correctamente, un cortafuegos puede proteger el servidor frente a una actividad no deseada. Después de solicitar un cortafuegos, se debe habilitar y se deben establecer reglas.

Para obtener más información, consulte las siguientes recopilaciones de temas de seguridad.

* [Cortafuegos de hardware (compartido)](../infrastructure/hardware-firewall-shared/getting-started.html)
* [Cortafuegos de hardware (dedicado)](../infrastructure/hardware-firewall-dedicated/getting-started.html)

Los grupos de seguridad constituyen otra opción para limitar el tráfico de la red en los servidores virtuales. Puede utilizar los grupos de seguridad para instaurar un conjunto de reglas de filtro de IP que definen cómo gestionar el tráfico de entrada y el de salida a la interfaz pública y privada de una instancia de servidor virtual. Para obtener más información, consulte [Iniciación a los grupos de seguridad](/docs/infrastructure/security-groups/sg_index.html).

## Planifique copias de seguridad 
Las copias de seguridad garantizan que los datos se guardan de forma segura fuera de su dispositivo y están protegidos en caso de pérdida. Dispone de los siguientes servicios de copia de seguridad para guardar los datos en un lugar seguro en caso de que tenga que volver a cargar la información en el dispositivo:
- La copia de seguridad EVault es un sistema de copia de seguridad automático basado en agente. Se trata de una conocida solución automatizada de muy fácil activación (“set-and-forget”) para la gestión del dispositivo. Es compatible con el software de Microsoft, incluidos Exchange y SQL mediante plugins adicionales. Los usuarios de EVault interactúan con este servicio a través de la aplicación basada en la web WebCC de EVault. Para obtener más información, consulte [Iniciación a los servicios de copia de seguridad](../infrastructure/Backup/index.html).
- R1Soft Continuous Data Protection es un software de copia de seguridad que se puede instalar en el servidor o en una máquina virtual autogestionada. Se recomienda utilizarlo si desea una sola interfaz para gestionar todas sus copias de seguridad. Puede interactuar con R1Soft CDP a través de su propio sistema de gestión, lo que permite instalar agentes en máquinas virtuales y ofrece plugins de base de datos para funciones adicionales. Para obtener más información, consulte [Iniciación a los servicios de copia de seguridad](../infrastructure/Backup/index.html).

## Siguientes pasos
Una vez configurado el servidor virtual, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión del servidor virtual](../vsi/vsi_managing.html).



