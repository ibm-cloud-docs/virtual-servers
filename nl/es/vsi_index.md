---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Iniciación a los servidores virtuales
Puede desplegar {{site.data.keyword.BluVirtServers}} en cuestión de minutos. Los servidores virtuales se despliegan desde las imágenes de servidor virtual que elija y en la región geográfica adecuada para sus cargas de trabajo.
{:shortdesc}

Cuando cree un servidor virtual, puede elegir entre un entorno público (multitenencia) o un entorno dedicado (tenencia única). A continuación, en función del entorno elegido, deberá seleccionar también servidores por hora, mensuales o virtuales transitorios. En el caso de los servidores virtuales públicos, también puede elegir utilizar almacenamiento basado en SAN o almacenamiento local.

## Antes de empezar

Antes de empezar, revise los siguientes requisitos previos.

  1. Debe tener una cuenta actualizada para poder solicitar servidores virtuales. Este proceso puede llevar un tiempo y requiere que se apruebe su solicitud para poder continuar. Para obtener más información sobre cómo actualizar su cuenta, consulte [Cambio a un IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).
  2. Revise y elija las opciones de despliegue. Para obtener más información consulte los siguientes temas:

|              Opciones de despliegue                           |  Descripción                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Servidor virtual público](../vsi/vsi_public.html)            | Despliegues de servidores virtuales multitenencia gestionados por IBM|
|[Servidor virtual transitorio](../vsi/vsi_about_transient.html)| Despliegues de servidores virtuales multitenencia gestionados por IBM ofrecidos a un coste reducido y más adecuados para cargas de trabajo flexibles |
|[Servidor virtual dedicado](../vsi/vsi_dedicated.html)      | Despliegues de servidores virtuales de tenencia única gestionados por IBM            |
{: caption="Tabla 1. Opciones de despliegue" caption-side="top"}   

## Suministro de un servidor virtual

Después de decidir una opción de despliegue, inicie el proceso de suministro.

|              Instrucciones de suministro                                         |  Descripción                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Suministro de instancias públicas](../vsi/vsi_provision_public.html)                | Suministro de instancias públicas con varias opciones             |
|[Suministro de instancias transitorias](../vsi/vsi_provision_transient.html)                | Suministro de instancias transitorias con varias opciones            |
|[Suministro de hosts e instancias dedicados](../vsi/vsi_provision_dedicated.html)| Suministro de instancias privadas o instancias dedicadas en hosts dedicados.|
{: caption="Tabla 2. Suministro de información" caption-side="top"}

## Siguientes pasos

Cuando el servidor virtual se haya suministrado y esté disponible, puede configurar los servidores virtuales mediante el
{{site.data.keyword.slportal_full}} o {{site.data.keyword.slapi_full}}. Para obtener más información, consulte [Configuración de servidores virtuales](../vsi/vsi_configuring.html).
