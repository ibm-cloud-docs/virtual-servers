---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-12"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Selecciones de suministro
Debe realizar las siguientes selecciones cuando suministre un servidor virtual público.

## Ubicación
Puede seleccionar el centro de datos específico en el que desea realizar el despliegue. Para los despliegues nuevos, {{site.data.keyword.Bluemix}} identifica automáticamente el mejor centro de datos (en función de la disponibilidad) y crea las VLAN públicas y privadas adecuadas. Para adiciones a entornos existentes, puede seleccionar el centro de datos específico, la VLAN y la subred necesarios para su diseño. Para obtener más información sobre VLAN y subredes, consulte [Iniciación a las VLAN](/docs/infrastructure/vlans/getting-started.html).

La selección de una subred es opcional y solo se utiliza cuando necesita que el dispositivo utilice una dirección IP desde la subred. Si selecciona una subred, verifique que dispone de suficientes direcciones IP para completar la solicitud. Si no tiene suficientes direcciones IP para la subred, el pedido se puede retrasar o cancelar.
{:tip}

## Procesadores / RAM
Cuando realice el pedido, tiene varias opciones de procesador principal donde escoger. Las opciones del procesador principal siguen los estándares correspondientes a los despliegues de servidor virtual. Cada núcleo físico del servidor es de híper hebras ("hyper-threaded") y se presenta como dos CPU virtuales (vCPU) o núcleos. La oferta de servidor virtual proporciona 2,0 GHz o más por núcleo con un máximo de 56 núcleos disponibles en un solo servidor virtual.

La RAM es muy sencilla. La oferta dedica por completo la cantidad de RAM que seleccione al servidor virtual, con un máximo de 242 GB en un solo servidor virtual.

**Nota:** las instancias públicas y dedicadas tienen unos máximos de configuración ligeramente diferentes. Una asignación muy alta de núcleos o de memoria limita las opciones disponibles.

## Sistema operativo

También debe seleccionar el sistema operativo que desea desplegar en el servidor. Tiene varias opciones gratuitas, como CentOS y Ubuntu. También dispone de opciones de pago, como Windows Server y Red Hat Enterprise Linux (RHEL). Es importante señalar que Windows necesita un disco primario de 100 GB.

Para los clientes existentes, también puede desplegar en función de una plantilla de imagen mediante el {{site.data.keyword.slportal_full}}; para ello, vaya a **Dispositivos-> Gestionar-> Imágenes** y seleccione **Solicitar servidor virtual** en el menú *Acciones*.  Se seleccionará automáticamente el sistema operativo adecuado para el pedido.  Como alternativa, puede realizar el pedido en función de una imagen estándar y luego volver a cargar a una plantilla de imagen en cualquier momento.

## Almacenamiento

Puede elegir entre SAN o almacenamiento local para cada servidor virtual. Puede complementar SAN o el almacenamiento local con otros productos de almacenamiento, si es necesario. Tanto SAN como almacenamiento local se exponen en el servidor virtual como discos locales. Los cambios realizados en los discos, como conexión, desconexión, migración, etc., requieren que se rearranque el servidor virtual. Para obtener más información, consulte [Opciones de almacenamiento](../vsi/storage/vsi_about_storage.html).

## Facturación por hora y mensual

Puede elegir entre facturación por hora o mensual para un servidor virtual. La principal diferencia, aparte del coste, es que los servidores por hora no incluyen la asignación de ancho de banda. Al final de un período de facturación, se calcula el uso del ancho de banda y el número de horas cada servidor ha estado activo en la cuenta. Puede consultar un total acumulado en el {{site.data.keyword.slportal}} en la página Vista del servidor virtual con un enlace a una página de detalles que muestra cada elemento de la línea, el número de horas y el cargo acumulado por elemento.

## Ancho de banda

La oferta incluye 250 GB con los servidores virtuales por mes que tienen un enlace ascendente público. Puede adquirir asignaciones mayores a un coste reducido comparado con en comparación con la tasa que se carga por el exceso.

## Velocidad de puerto

Puede seleccionar la velocidad de enlace ascendente para el servidor virtual, con un máximo de 1 GB/s. Estos enlaces ascendentes virtuales están respaldados por enlaces ascendentes físicos redundantes en las redes dedicadas y pública de IBM. La velocidad pública y dedicada es siempre la misma velocidad en el momento del pedido, pero puede actualizar o degradar un enlace si es necesario.

## Software

Puede seleccionar el software que instalará {{site.data.keyword.Bluemix_notm}} durante el proceso de suministro. {{site.data.keyword.Bluemix_notm}} proporciona soporte para cualquier software que se despliega durante el proceso de suministro. También puede instalar su propio software una vez desplegado el servidor.

## Seguridad

Antes del despliegue, estudie las opciones de seguridad. Como parte del proceso del pedido, puede seleccionar un hardware específico del dispositivo o un software de cortafuegos para proporcionar protección. Como alternativa, puede desplegar dispositivos cortafuegos dedicados en el entorno y desplegar el servidor virtual en una VLAN protegida. 

**Nota:** un servidor virtual no puede estar protegido por dos dispositivos cortafuegos en la misma interfaz. 

También puede utilizar grupos de seguridad para aprobar un conjunto de reglas de filtro de IP que definan cómo se debe manejar el tráfico de entrada y de salida a interfaces públicas y privadas de una instancia de servidor virtual.

Para obtener más información, consulte las siguientes recopilaciones de temas de seguridad.

* [Cortafuegos de hardware (compartido)](../infrastructure/hardware-firewall-shared/getting-started.html)
* [Cortafuegos de hardware (dedicado)](../infrastructure/hardware-firewall-dedicated/getting-started.html)
* [Iniciación a los grupos de seguridad](/docs/infrastructure/security-groups/sg_index.html)

## Supervisión

Puede seleccionar entre varias opciones de supervisión para el servidor virtual. Las opciones incluyen la supervisión estándar, que supervisa a través de Ping y respuesta del servicio del protocolo de control de transmisión (TCP), y ofrece respuestas opcionales en el caso de que se produzcan errores. También puede añadir la supervisión avanzada, que utiliza el agente de software Nimsoft para ofrecer un conjunto más amplio de características para la supervisión del servidor virtual y del software instalado.

Para obtener más información, consulte [Supervisión](../infrastructure/SLmonitoring/monitoring_index.html).

## Copia de seguridad

Durante el proceso de pedido, puede añadir copias de seguridad Evault. También puede optar por adquirir una licencia de R1soft para el entorno de copia de seguridad de R1soft existente o utilizar una solución de seguridad de otro proveedor.

Para obtener más información, consulte [Volver a registrar el dispositivo con eVault](../infrastructure/Backup/how-do-i-re-register-evault.html).

## Scripts posteriores al suministro

Se pueden asociar scripts posteriores al suministro a cualquier pedido de servidor virtual. Se ejecutará un script desarrollado por el cliente después de que finalicen las otras tareas de suministro. Los scripts se suelen utilizar para aplicar una configuración específica del cliente a un servidor y para ayudar a automatizar la estrategia de escalado.

Para obtener más información, consulte [Adición de un script de suministro personalizado](vsi_add_script.html).

## Qué hacer a continuación
Cuando esté preparado para suministrar el servidor virtual público, consulte [Suministro de instancias públicas](vsi_provision_public.html).
