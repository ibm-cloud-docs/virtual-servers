---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-17"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Suministro de instancias públicas
{: #ordering-vs-public}

## Antes de empezar
Tiene dos opciones para suministrar instancias de servidor virtual público. La primera es a través de la consola de
{{site.data.keyword.cloud}} y la segunda a través del {{site.data.keyword.slportal}}. La consola y el {{site.data.keyword.slportal}} requieren ID de inicio exclusivos. No puede utilizar el nombre de usuario y la contraseña de la consola para iniciar sesión en el portal y viceversa.
{:shortdesc}

Para la consola de {{site.data.keyword.cloud_notm}}, debe tener una cuenta actualizada para solicitar servidores virtuales. Para obtener más información sobre cómo actualizar su cuenta, consulte [Cuenta de Pago según uso](/docs/account?topic=account-accounts#paygo).
{:note}

Antes de empezar, revise los siguientes requisitos previos.

  1. Revise las opciones de despliegue que tiene disponibles. Para obtener más información, consulte [Servidores virtuales públicos](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers).

  2. Revise las consideraciones de capacidad para instancias de servidores virtuales.  Para obtener más información, consulte
[Consideraciones sobre recursos para instancias de servidor virtual](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).
  
  3. Abra la página de la [instancia de servidor virtual ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} desde la consola de {{site.data.keyword.cloud_notm}}.

## Suministro de una instancia de servidor virtual público  
{: #ordering-public-instance}

Para suministrar una instancia de servidor virtual, debe tener en cuenta la información siguiente.

Debe haber iniciado sesión para poder ver todas las opciones disponibles. 
{:tip}

### Instancia pública

| Campo    | Detalles     |
| -------- | ----------- |
| Facturación  | En función de su instancia de servidor virtual, puede seleccionar una facturación por hora o mensual. La principal diferencia, aparte del coste, es que las instancias por hora no incluyen la asignación de ancho de banda. Al final de un período de facturación, se calcula el uso del ancho de banda y el número de horas que cada instancia ha estado activa en la cuenta. Por ejemplo, si cancela una instancia por hora tras 10 días, solo pagará las horas correspondientes a esos 10 días. Si cancela una instancia mensual después de 10 días, pagará el mes completo. Si está interesado en la característica de suspensión de facturación, que solo está disponible para instancias por hora, consulte
[Acerca de suspender la facturación](/docs/vsi?topic=virtual-servers-about-suspend-billing). |
| Nombre de host | Puede contener etiquetas formadas por caracteres alfanuméricos y guiones, separadas por puntos. Las etiquetas no pueden ser solo numéricas, comenzar o acabar con un guión, ni tener guiones o puntos consecutivos. |
| Dominio | Debe tener dos o más etiquetas formadas por caracteres alfanuméricos y guiones, separadas por puntos. Las etiquetas no pueden comenzar o acabar con un guión, ni tener guiones o puntos consecutivos. La última etiqueta solo puede tener letras. |
| Grupo de colocación | Puede seleccionar un grupo de colocación para la instancia. Si añade un grupo de colocación, la regla de "dispersión" implica que las instancias estarán en diferente hardware físico. Para obtener más información, consulte [Grupos de colocación](/docs/vsi?topic=virtual-servers-placement-groups). |
| Ubicación  | Las ubicaciones se componen de regiones (áreas geográficas específicas) y de zonas (centros de datos tolerantes a errores dentro de una región). Seleccione la ubicación donde desea que se cree la instancia de servidor virtual. |
| Perfiles populares | Plantéese seleccionar una de las configuraciones de perfil populares, que dan soporte a los casos de uso más comunes. Los perfiles contienen instancias preconfiguradas que están listas para utilizar en cuestión de minutos. |
| Todos los perfiles | Para obtener más información sobre las opciones de perfil disponibles para las instancias públicas, consulte
[Servidores virtuales públicos](/docs/vsi?topic=virtual-servers-about-public-virtual-servers). |
| Claves SSH     | Las claves SSH permiten el acceso a una instancia sin utilizar una contraseña desde los clientes correspondientes para cada clave pública que está implementada en la instancia. Si decide añadir una clave SSH, proporcione una clave pública de su clave SSH, que podrá utilizar para iniciar sesión en la instancia después de su suministro. |
| Imagen        |  Una imagen es el sistema operativo desplegado para su instancia. Tiene varias opciones gratuitas, como CentOS y Ubuntu. También dispone de opciones de pago, como Windows Server y Red Hat Enterprise Linux (RHEL). Es importante señalar que Windows necesita un disco primario de 100 GB. |
{: caption="Tabla 1. Opciones de instancia pública" caption-side="top"}

### Complementos de instancia pública 

Si elige cualquier complemento de SO, panel de control o software, deberá ser compatible con su imagen para evitar un error al solicitar la instancia. Por ejemplo, no puede suministrar una imagen de RedHat con una base de datos de Microsoft.
{:important}

| Campo     | Detalles     |
| --------- | ----------- |
| Complementos de SO | Si selecciona la facturación mensual, puede seleccionar los complementos de imagen siguientes:<br><br> **R1Soft Server Backup Manager** proporciona copias de seguridad de servidor de disco a disco de alto rendimiento, con gestión central y repositorio de datos. Si selecciona el complemento R1Soft, debe adquirir un paquete R1Soft Backup Agent, que es un complemento CDP en la sección **Servicios**. La selección de uno sin el otro provoca un error en el pedido. Para obtener más información sobre R1Soft e IBM Cloud, consulte
[R1Soft Server Backup Manager ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/cloud/backup-and-restore?mhq=R1Soft%20Server%20Backup%20Manager&mhsrc=ibmsearch_a){: new_window}.<br><br>**Veeam Backup and Replication** combina una copia de seguridad automatizada con funciones de restauración y réplica. Veeam proporciona también una supervisión avanzada, creación de informes y planificación de la capacidad. Para obtener más información sobre Veeam Backup and Replication, consulte
[Veeam Backup and Replication con almacenamiento de IBM ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www-356.ibm.com/partnerworld/gsd/solutiondetails.do?solution=54724&lc=en&stateCd=P&tab=2){: new_window}.<br><br>**VMware vCenter** automatiza el despliegue de las capas de VMware vSphere y VMware vCenter Server subyacentes que necesita para disponer de una solución VMware flexible y personalizable. Para obtener más información sobre vCenter on IBM Cloud, consulte [Acerca de vCenter Server on IBM Cloud ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/downloads/cas/L7RKPZND?mhq=vmware%20vcenter&mhsrc=ibmsearch_a){: new_window}.|
| Software de panel de control | Si selecciona la facturación mensual, puede añadir un panel de control para el alojamiento web. |
| Software de base de datos      | Puede seleccionar un software de base de datos para su instalación. {{site.data.keyword.cloud_notm}} admite cualquier software de base de datos que se despliegue durante el proceso de suministro. También puede instalar su propio software de base de datos una vez desplegado el servidor. |
| Servicios | Algunos servicios están seleccionados de forma automática, en función de sus selecciones de facturación e imagen. Puede elegir cualquiera de los complementos de servicio restantes para su instancia. |
| Script de suministro | Se suelen utilizar scripts de suministro para aplicar una configuración específica del cliente a un servidor y para ayudar a automatizar la estrategia de escalado. Un script de suministro puede ser cualquier archivo que el sistema operativo (SO) pueda ejecutar, incluidos archivos binarios combinados o cualquier idioma admitido por el SO. No se pueden utilizar scripts de suministro en imágenes cloud-init. Para obtener más información, consulte
[Scripts de suministro](/docs/vsi?topic=virtual-servers-provisioning-scripts). |
| Datos de usuario        | Puede añadir datos de usuario que realizan tareas de configuración comunes o ejecutan scripts automáticamente. Los datos de usuario se pueden utilizar en imágenes cloud-init y que no sean cloud-init.  |
{: caption="Tabla 2. Complementos de instancia pública" caption-side="top"}

### Disco de almacenamiento adjunto

Si necesita almacenamiento adicional, puede conectar discos de almacenamiento a la instancia. El tipo de discos de almacenamiento que hay disponibles dependerá el perfil que seleccione. Por ejemplo, los perfiles locales equilibrados y unos pocos de los perfiles de GPU utilizan discos con copia de seguridad local. Si selecciona la facturación mensual, puede añadir
{{site.data.keyword.backup_notm}} y elegir la opción que mejor se ajuste a sus necesidades. Para obtener más información, consulte
[Servicios de {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).

### Interfaz de red

| Campo    | Detalles     |
| -------- | ----------- |
| Velocidades de puerto de enlace ascendente | Puede seleccionar la velocidad de enlace ascendente de la instancia, hasta 1 GB/s. Estos enlaces ascendentes virtuales están respaldados por enlaces ascendentes físicos redundantes en las redes dedicadas y pública de IBM. La velocidad pública y dedicada es siempre la misma velocidad en el momento del pedido, pero puede actualizar o degradar un enlace si es necesario. |
| Grupo de seguridad privado y público  | Puede utilizar los grupos de seguridad para instaurar un conjunto de reglas de filtro de IP que definen cómo gestionar el tráfico de entrada y el de salida a la interfaz pública y privada de su instancia. Para obtener más información, consulte
[Acerca de los grupos de seguridad de IBM](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups). |
| VLAN privada y pública | La instancia de servidor virtual se coloca en una VLAN asignada de forma automática de forma predeterminada. Puede elegir una VLAN distinta si ya tiene una en el centro de datos seleccionado. Para obtener más información, consulte
[Acerca de las VLAN](/docs/infrastructure/vlans?topic=vlans-about-vlans). |
| Subred privada y pública | La selección de una subred es opcional y solo se utiliza cuando necesita que el dispositivo utilice una dirección IP desde la subred. Si selecciona una subred, verifique que dispone de suficientes direcciones IP para completar la solicitud. Si no tiene suficientes direcciones IP para la subred, el pedido se puede retrasar o cancelar. Para obtener más información, consulte
[Acerca de las subredes e IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
{: caption="Tabla 3. Opciones de interfaz de red" caption-side="top"}

### Complementos de interfaz de red

| Campo    | Detalles     |
| -------- | ----------- |
| Ancho de banda | Se incluyen 250 GB con instancias mensuales que tengan un enlace ascendente público. Puede adquirir asignaciones mayores a un coste reducido comparado con en comparación con la tasa que se carga por el exceso. |
| Cortafuegos de hardware y software  | Los servicios de cortafuegos evitan el tráfico no deseado en sus servidores, reducen la probabilidad de que se produzca un ataque y permiten que los recursos del servidor se dediquen a las tareas para las que se han diseñado. |
| Dirección IP primaria | Automáticamente se asigna una dirección IP primaria a la instancia. |
| Direcciones IP secundarias públicas | Estas subredes son de su propiedad en la duración completa de la instancia de servidor virtual. Puede cancelar la subred de forma independiente pero, si cancela la instancia, la subred también se eliminará. Para obtener más información, consulte
[Acerca de las subredes e IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
| Direcciones IPv6 estáticas públicas y direcciones IPv6 | Puede seleccionar una dirección IPv6 o direcciones IPv6 estáticas públicas para su instancia. |
| Gestión de VPN | Esta opción está automáticamente seleccionada para su instancia con usuarios de VPN SSL ilimitados. Para obtener más información, consulte [Acerca de VPN](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn). |
{: caption="Tabla 4. Complementos de interfaz de red" caption-side="top"}


## Suministro de una instancia pública a través del portal de clientes
Para suministrar una instancia de servidor virtual público a través del {{site.data.keyword.slportal}}, siga los pasos siguientes:

  1. Inicie una sesión en el [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
  2. Localice la sección **Pedido** y pulse **Dispositivos**.
  3. En la página Dispositivos, pulse **SAN por hora**, **Local por hora**, **Mensual** o **Transitorio** para elegir una de las ofertas de servidor virtual.
  4. En la página *Configurar su servidor de nube*, especifique toda la información pertinente.
  5. Pulse **Añadir a pedido** para continuar.
  6. Confirme o edite la información de dominio correspondiente al servidor.
  7. Pulse los recuadros de selección **Términos de los servicios en la nube** y **Acuerdo de servicio de terceros**.
  8. Confirme o especifique la información sobre el pago y pulse **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.

## Siguientes pasos
Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*, después de iniciar una sesión en {{site.data.keyword.Bluemix_notm}}.

Cuando el servidor virtual se haya suministrado y esté disponible, puede configurar los servidores virtuales mediante la consola de
{{site.data.keyword.cloud_notm}} o {{site.data.keyword.slapi_short}}. Para obtener más información, consulte [Configuración de servidores virtuales](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
