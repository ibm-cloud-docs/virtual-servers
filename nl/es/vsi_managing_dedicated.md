---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Gestión de hosts e instancias dedicados
{: #managing-dedicated-hosts-instances}

La página de detalles del dispositivo es donde puede gestionar el host y las instancias dedicados, realizar el seguimiento de las incidencias y supervisar la disponibilidad del host. Puede acceder y ver las instancias de host dedicadas de dos formas desde la lista de dispositivos: como parte de su host o como instancias individuales.
{:shortdesc}

## Separador Configuración de host
Puede realizar varias tareas desde el separador **Configuración** del host dedicado, incluida la gestión de las instancias de host dedicadas. En el menú desplegable Acciones, puede cambiar el nombre del host o cancelarlo. Todas las instancias de host dedicadas asignadas se deben cancelar o migrar para que se pueda cancelar un host; de lo contrario, se recibe un mensaje de error.

Se pueden conservar notas en el host y sus instancias, por ejemplo que la migración de myDallasHost a myTorHost está prevista para XX/XX/XXXX. Las ventanas General, Sistema y Red de la página le ofrecen un resumen de los detalles del host. Tenga en cuenta que a ventana Almacenamiento hace referencia a la capacidad de almacenamiento local.

La ventana Instancias contiene las instancias asignadas a un host específico, así como la posibilidad de añadir instancias al host. Pulse el menú Acciones de una instancia para realizar las siguientes tareas:

* Rearrancar
* Encender y apagar
* Cambiar el nombre
*	Ver registros de auditoría
*	Actualizar o degradar
*	Cancelar
*	Migrar

## Separador Incidencias de host
Utilice el separador Incidencias para abrir incidencias de soporte para el host y cualquiera de sus instancias pulsando Añadir una incidencia para este enlace del dispositivo.

## Separador Asignaciones de host
El separador Asignaciones le permite ver núcleos disponibles, RAM y almacenamiento local para el host dedicado. La porción azul de la "tarta" representa la parte que se utiliza y la porción blanca la que está disponible.

## Separador Instancia de host dedicada
Se puede acceder a la página de detalles del dispositivo de la instancia de host dedicada desde la página Detalles del dispositivo del host o directamente desde la lista de dispositivos. Hay más separadores a nivel de instancia de host dedicada; Configuración e Incidencias son parecidos a los separadores que hay a nivel de host. El enlace Modificar configuración del dispositivo, del separador Configuración, le permite realizar cambios en el sistema (núcleo, RAM y almacenamiento local) y en la configuración de la red (ancho de banda y velocidades de puerto de enlace ascendente).

Uso muestra un gráfico en el tiempo sobre el uso de CPU por fecha. Puede renovar el gráfico para ver el uso de CPU correspondiente a una determinada fecha y hora, lo que resulta útil cuando se intenta determinar si se tiene que añadir capacidad de proceso.

Ancho de banda es otro gráfico en el tiempo que le permite especificar parámetros para ver cuánto ancho de banda se ha utilizado a lo largo del tiempo. El separador Almacenamiento muestra cualquier bloque adicional o almacenamiento de archivos de la instancia.

## Cancelar un host dedicado
Puede cancelar un host dedicado en cualquier momento. Un requisito previo para cancelar un host es que se hayan migrado a otro host dedicado las instancias dedicadas asignadas al mismo o que se hayan cancelado las instancias.
### Cancelar un host dedicado desde la lista de dispositivos
Siga los pasos siguientes para cancelar un host dedicado desde la lista de dispositivos.

1. Seleccione **Dispositivo** > **Lista de dispositivos**.
2. Busque el host dedicado que desea cancelar y pulse el menú desplegable **Acciones**.
3. Seleccione **Cancelar host**.
4. Aparecerá una ventana emergente que contiene una lista de las instancias dedicadas asignadas al host. Deberá migrar o cancelar las instancias, si aún no lo han hecho, antes de cancelar el host. Pulse **Aceptar**.

Recibirá un mensaje que indica que el host dedicado se ha cancelado. Habrá un enlace con la incidencia de soporte para cancelar el host dedicado.
### Cancelar un host dedicado desde la página Detalles del dispositivo
Siga los pasos siguientes para cancelar un host dedicado desde la página Detalles del dispositivo.

1. Seleccione **Dispositivo** > **Lista de dispositivos**.
2. Busque el host dedicado que desea cancelar y realice una doble pulsación sobre el mismo.
3. Verifique que todas las instancias dedicadas asignadas al host dedicado se han migrado o cancelado.
4. Pulse el menú desplegable **Acciones** y seleccione **Cancelar host**.

Recibirá un mensaje que indica que el host dedicado se ha cancelado. Habrá un enlace con la incidencia de soporte para cancelar el host dedicado.

### Cancelar una instancia dedicada

Para poder cancelar un host dedicado, se deben haber cancelado las instancias dedicadas asignadas al mismo. Las instancias dedicadas se pueden cancelar directamente desde la lista de dispositivos, desde la página Detalles del dispositivo de su host asignado o desde su propia página Detalles del dispositivo.

1. Seleccione la instancia dedicada que desea cancelar y pulse el menú desplegable **Acciones**.
2. Seleccione **Cancelar dispositivo**.
3. Aparecerá un mensaje de aviso. Pulse el menú desplegable **Motivo** y seleccione el motivo por el que va a cancelar la instancia dedicada y pulse **Continuar**.

Recibirá un mensaje que indica que la instancia dedicada se ha cancelado. Habrá un enlace con la incidencia de soporte para cancelar la instancia dedicada.
