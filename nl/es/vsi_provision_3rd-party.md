---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# Suministro de una instancia de servidor virtual a partir de una imagen de terceros
{: #ordering-3P}

Puede suministrar una instancia de servidor virtual a partir de una imagen que haya creado un proveedor de terceros. Las imágenes de terceros están disponibles a través del enlace Imágenes en la nube del catálogo de {{site.data.keyword.cloud}}.
{:shortdesc}

## Antes de empezar
Antes de empezar, asegúrese de tener sus credenciales del catálogo de {{site.data.keyword.cloud_notm}} configuradas.

Para el catálogo de {{site.data.keyword.Bluemix_notm}}, debe tener una cuenta actualizada para solicitar servidores virtuales. Para obtener más información sobre cómo actualizar su cuenta, consulte [Cambio a un IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

## Selección de una imagen de servidor virtual
1. Inicie una sesión en el catálogo de [{{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/catalog/){: new_window} con sus credenciales exclusivas.
2. En la sección **Imágenes en la nube**, localice y pulse la imagen de terceros que desee desplegar.
3. Revise los detalles de la imagen personalizada y pulse **Continuar**. Aparecerá la página **Instancia de servidor virtual - Imagen personalizada** con la imagen personalizada preseleccionada.

## Revisión y elección de las opciones de despliegue
Para obtener más información consulte los siguientes temas:

|              Opciones de despliegue                           |  Descripción                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Servidor virtual público](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)            | Despliegues de servidores virtuales multitenencia gestionados por IBM|
|[Servidor virtual transitorio](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)| Despliegues de servidores virtuales multitenencia gestionados por IBM ofrecidos a un coste reducido y más adecuados para cargas de trabajo flexibles |
|[Servidor virtual reservado](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | Despliegues de servidor virtual multitenencia gestionado por IBM con capacidad garantizada durante el plazo contratado |
|[Servidor virtual dedicado](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)      | Despliegues de servidores virtuales de tenencia única gestionados por IBM            |
{: caption="Tabla 1. Opciones de despliegue" caption-side="top"}

## Suministro de un servidor virtual
Después de decidir una opción de despliegue, inicie el proceso de suministro. Para obtener más información, consulte los temas siguientes.

Debido a que ha iniciado el proceso de suministro con una imagen personalizada, no puede cambiar el tipo de imagen durante el proceso de suministro.
{:note}

|              Instrucciones de suministro                                         |  Descripción                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Suministro de instancias públicas](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                | Suministro de instancias públicas con varias opciones             |
|[Suministro de instancias transitorias](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                | Suministro de instancias transitorias con varias opciones            |
|[Suministro de instancias y capacidad reservada](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | Suministro de instancias y capacidad reservada con varias opciones |
|[Suministro de hosts e instancias dedicados](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)| Suministro de instancias privadas o instancias dedicadas en hosts dedicados.|
{: caption="Tabla 2. Suministro de información" caption-side="top"}


## Siguientes pasos
Cuando el servidor virtual se haya suministrado y esté disponible, puede configurar los servidores virtuales mediante la consola de
{{site.data.keyword.cloud_notm}} o {{site.data.keyword.slapi_short}}. Para obtener más información, consulte [Configuración de servidores virtuales](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
