---

copyright:
  years: 2018
lastupdated: "2018-10-05"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Suministro de instancias y capacidad reservada
{: #provisioning-reserved-capacity-and-instances}

## Antes de empezar

Puede suministrar sus instancias y su capacidad reservada a través del catálogo de {{site.data.keyword.cloud}}. Debe suministrar su capacidad reservada antes que las instancias de servidor virtual.

**Nota**: si no es el administrador de la cuenta, su cuenta de usuario debe incluir el permiso **Gestionar capacidades reservadas**. El administrador de la cuenta puede otorgar permiso al usuario desde el separador **Permisos del portal** de la consola. Para obtener más información sobre la actualización de permisos, consulte [Gestión del acceso a la infraestructura](/docs/iam?topic=iam-mngclassicinfra).

## Inicio de sesión en el catálogo de IBM Cloud

Siga los pasos siguientes para iniciar una sesión en el catálogo de {{site.data.keyword.cloud_notm}} para comenzar a suministrar su capacidad reservada y sus instancias.

  1. Inicie una sesión en el catálogo de [{{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/catalog/){: new_window} con sus credenciales exclusivas.

## Suministro de capacidad reservada

En el catálogo de {{site.data.keyword.cloud_notm}}, siga los pasos siguientes para suministrar su capacidad reservada.

  1. En la sección **Infraestructura de cálculo**, pulse el mosaico **Servidores virtuales**.
  2. Seleccione la opción **Servidor virtual reservado**.
  3. Pulse **Crear**.
  4. Para crear nueva capacidad reservada, seleccione **Nueva capacidad +**. En la página **Capacidad reservada**, escriba o seleccione la siguiente información:

| Campo                   | Valor               |                                                                                                                                                                                                                                                                                                                                 
| ----------------------- | ------------------- |
| Nombre                    | Se necesita un nombre para la capacidad reservada. |                                                                                                                                                                                                                                                                                                       
| Capacidad de servidor virtual | Seleccione el número de instancias que desea asignar a esta capacidad reservada (límite de 20 instancias). |                                                                                                                                                                                                                                                
| Ubicación                | Seleccione la ubicación específica que se necesita para sus cargas de trabajo. Las ubicaciones están compuestas por regiones; cada región es un área geográfica distinta. **Nota:** no puede seleccionar ubicaciones individuales para cada instancia de servidor virtual que suministre dentro de esta capacidad reservada. Su selección es la ubicación para todas las instancias de servidor virtual que suministre dentro de esta capacidad reservada. |
| POD                     | Seleccione el POD específico de su ubicación. |
| Plazos del plan              | Elija entre un contrato de uno o de tres años de duración. |                                                                                                                                                                                                                                                                                            
| Perfil                 | Seleccione entre los perfiles más utilizados o todas las combinaciones de vCPU y RAM disponibles de almacenamiento respaldado por SAN (equilibrado, memoria o cálculo). **Nota:** no puede combinar distintos tamaños de perfil dentro del conjunto de instancias de servidor virtual asignado a esta capacidad ni cambiarlo posteriormente. El conjunto de instancias de servidor virtual que reserve deben tener el mismo tamaño. |
{: caption="Tabla 1. Selecciones de suministro de capacidad reservada" caption-side="top"}


## Suministro de instancias reservadas

Después de suministrar su capacidad reservada, es el momento de suministrar las instancias de servidor virtual reservado. Las instancias de servidor virtual reservado se pueden suministrar en cualquier momento durante la duración del contrato ya que su capacidad está garantizada. Siga los pasos siguientes para suministrar sus instancias reservadas:

1. En el catálogo de {{site.data.keyword.cloud_notm}}, seleccione el mosaico **Servidores virtuales** en la sección **Infraestructura de cálculo**.
2. Seleccione la opción **Servidor virtual reservado**.
3. Pulse **Crear**.
4. Para suministrar una instancia de servidor virtual reservado, escriba o seleccione la siguiente información:

| Campo                     | Valor               |                                                                                                                                                                                                                                                                                                                                 
| ------------------------- | ------------------- |
| Nombre                      | Se necesita un nombre para la instancia de servidor virtual reservado. |                                                                                                                                                                                                                                                                                                       
| Facturación                   | Seleccione una facturación por hora o mensual. |                                                                                                                                                                                                                                                
| Capacidad reservada         | Seleccione su capacidad reservada o seleccione **Nueva capacidad +** para suministrar capacidad reservada adicional. |                                                                                                                                                                                                     
| Complementos                   | Elija el almacenamiento, red o software adicional que desee. |                                                                                                                                                                                                                                                                                            
{: caption="Tabla 1. Selecciones de suministro de capacidad reservada" caption-side="top"}

## Siguientes pasos

Cuando el servidor virtual se haya suministrado y esté disponible, puede configurar los servidores virtuales mediante la consola de
{{site.data.keyword.cloud_notm}} o {{site.data.keyword.slapi_short}}. Para obtener más información, consulte [Configuración de servidores virtuales](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).

Si tiene preguntas sobre las instancias y la capacidad reservada, consulte [Preguntas frecuentes: instancias y capacidad reservada](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances). 
