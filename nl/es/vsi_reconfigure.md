---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Volver a configurar un servidor virtual existente
{: #reconfiguring-virtual-servers}

Una vez suministrado el servidor virtual, puede actualizar o degradar su configuración siempre que lo desee.  

**Nota importante:** hay varios servidores virtuales públicos disponibles de los perfiles predefinidos. Durante un tiempo limitado, puede modificar los servidores virtuales que estaban disponibles antes que los perfiles predefinidos. Luego tendrá que migrar o cancelar las instancias existentes y reordenar.

No puede modificar el núcleo individual, la RAM, ni el tamaño del disco de un servidor virtual que utilice perfiles. Debe elegir otro perfil que tenga los núcleos, la RAM y tamaño de disco predefinidos que necesite. El perfil de servidor virtual que seleccione determina los núcleos, la RAM y los tamaños de disco válidos.  

Los servidores virtuales dedicados tienen más opciones de personalización; por lo tanto, puede modificar los núcleos, RAM y tamaños de disco individuales.

Siga los siguientes pasos para volver a configurar un servidor virtual existente.
{:shortdesc}

## Modificación de un servidor virtual existente (que utilice perfiles predefinidos)
1. Acceda al [{{site.data.keyword.slportal_full}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
2. En la lista de dispositivos, pulse el nombre del servidor virtual que desea volver a configurar.
3. En el separador **Configuración**, pulse **Modificar** o **Modificar configuración del dispositivo** para actualizar los elementos siguientes.
  <dl>
  <dt>Tamaño</dt>
  <dd>Seleccione un nuevo tamaño.</dd>
  <p><note>Nota: si modifica un perfil que utiliza almacenamiento local, no puede conmutar a un perfil que utilice almacenamiento que no sea local. Paralelamente, si modifica un perfil que utiliza almacenamiento que no es local, no puede conmutar a un perfil que utilice almacenamiento local.
  </note></p>
  </dl>
4. Después de especificar los cambios para el servidor virtual, realice la actualización de la configuración.
  <dl>

  <dt>Fecha de actualización</dt>
  <dd>Puede pulsar el recuadro de selección Inmediatamente para realizar una actualización inmediata, o puede planificar una hora para que se active la actualización.</dd>

  <dt>Hora de actualización</dt>
  <dd>Especifique la fecha (AAAA-MM-DD) para activar la actualización.</dd>

  <dt>Notas</dt>
  <dd>Escriba las notas que desea adjuntar al dispositivo. </dd>
  </dl>

5. Pulse **Continuar**.
6. Revise la confirmación del pedido para comprobar que sea correcto.  Pulse **Editar** para editar la actualización.
7. Pulse **Confirmar** para confirmar el pedido y aplicar los cambios al dispositivo.

## Modificación de un servidor virtual existente (anterior a los perfiles predefinidos) o de un servidor virtual dedicado
1. En la lista de dispositivos, pulse el nombre del servidor virtual que desea volver a configurar.
2. En el separador **Configuración**, puede pulsar el enlace **Actualización de núcleo o RAM** para actualizar los elementos siguientes.

|   Opciones de actualización       |  Descripción                                                                                                |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| Fecha de actualización            | Especifique la fecha (AAAA-MM-DD) para activar la actualización.                                                |
| Hora de actualización            | Seleccione la hora de los recuadros desplegables para el momento del día en la que la actualización pasará a estar activa, o pulse el recuadro de selección **Inmediato** para una actualización inmediata.                                                                                        |
| Núcleos                   | Seleccione el número de núcleos para la actualización, si procede. |
| RAM                     | Seleccione la cantidad de RAM que desea aplicar al dispositivo para la actualización, si procede.   |
| Velocidades de puerto de enlace ascendente      | Seleccione las nuevas velocidades de puerto de enlace ascendente para el dispositivo, si procede. |
| Ancho de banda público        | Seleccione la cantidad (en GB) de ancho de banda público para el dispositivo, si procede.   |
| Primer disco – Quinto disco | Seleccione la opción de almacenamiento/espacio de disco para su primer disco, si procede. Véase **Notas de disco** para obtener más información.                                                                                                                               |
| Notas                   | Escriba las notas que desea adjuntar al dispositivo.                                                                 |
{: caption="Tabla 1. Opciones de despliegue" caption-side="top"}   

  **Notas de disco:**
  * Están disponibles tanto el almacenamiento local como el SAN.  Compruebe su selección para garantizar que su opción de almacenamiento sea correcta.
  * Para los servidores virtuales público, si está actualizando el almacenamiento local y necesita más núcleos o más RAM, puede perder su disco secundario. Cuando se modifica un perfil de servidor virtual que utiliza almacenamiento local, el perfil está predefinido de forma automática y los perfiles que no son comparables no se pueden seleccionar.
3. Pulse **Continuar**.
4. Revise la confirmación del pedido para comprobar que sea correcto.  Pulse **Editar** para editar la actualización.
5. Pulse **Confirmar** para confirmar el pedido y aplicar los cambios al dispositivo.
