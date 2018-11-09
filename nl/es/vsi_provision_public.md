---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Suministro de instancias públicas
{: #ordering-vs-public}

## Antes de empezar
Tiene dos opciones para suministrar instancias de servidor virtual público. La primera es a través del catálogo de {{site.data.keyword.Bluemix}} y la segunda a través del {{site.data.keyword.slportal}}. El catálogo y el {{site.data.keyword.slportal}} requieren ID de inicio exclusivos. El nombre de usuario y la contraseña del catálogo no funcionarán para iniciar una sesión en el portal y viceversa.
{:shortdesc}

Antes de empezar, revise los siguientes requisitos previos.

  1. Asegúrese de que tiene configuradas credenciales del catálogo de {{site.data.keyword.Bluemix_notm}} o del {{site.data.keyword.slportal}}.

     **Nota:** Para el catálogo de {{site.data.keyword.Bluemix_notm}}, debe tener una cuenta actualizada para solicitar servidores virtuales. Para obtener más información sobre cómo actualizar su cuenta, consulte [Cambio a un IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).

  2. Si aún no lo ha hecho, revise las opciones de despliegue que tiene a su disposición. Para obtener más información, consulte [Opciones de despliegue: servidor virtual público](../vsi/vsi_public.html).

  3. Revise las consideraciones de capacidad para instancias de servidores virtuales.  Para obtener más información, consulte [Consideraciones de capacidad](ts_capacity_bp.html).

## Suministro de una instancia de servidor virtual público
{: #ordering-public-instance}

Cuando cumpla los requisitos previos, puede empezar a suministrar una instancia de servidor virtual público. Puede suministrar su instancia pública mediante el catálogo de {{site.data.keyword.cloud_notm}} o el {{site.data.keyword.slportal}}.

### Suministro de una instancia de servidor virtual público a través del catálogo de IBM Cloud
Para suministrar una instancia de servidor virtual público a través del catálogo de {{site.data.keyword.cloud_notm}}, siga los pasos siguientes:

  1. Inicie una sesión en el catálogo de [{{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/catalog/){: new_window} con sus credenciales exclusivas. 
  2. En la sección **Infraestructura de cálculo**, pulse el mosaico **Servidores virtuales**.
  3. Seleccione la opción **Servidor virtual público**.
  4. Pulse **Crear**.
  5. Rellene la información relevante correspondiente a su instancia de servidor virtual. 
  6. Después de revisar el resumen del pedido, pulse el recuadro de selección **Acuerdos de servicios de terceros**. 
  7. Pulse **Suministrar**.
  
### Suministro de una instancia de servidor virtual público a través del portal de clientes
Para suministrar una instancia de servidor virtual público a través del {{site.data.keyword.slportal}}, siga los pasos siguientes:

  1. Inicie una sesión en el [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
  2. Localice la sección **Pedido** y pulse **Dispositivos**. 
  3. En la página Dispositivos, pulse **SAN por hora**, **Local por hora**, **Mensual** o **Transitorio** para elegir una de las ofertas de servidor virtual.
  4. En la página *Configurar su servidor de nube*, especifique toda la información pertinente.
  5. Pulse el botón **Añadir a pedido** para continuar.
  6. Confirme o edite la información de dominio correspondiente al servidor.
  7. Pulse los recuadros de selección **Términos de los servicios en la nube** y **Acuerdo de servicio de terceros**.
  8. Confirme o especifique la información sobre el pago y pulse el botón **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.

 Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*, después de iniciar una sesión en {{site.data.keyword.Bluemix_notm}}. También puede iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

## Siguientes pasos
Una vez suministrado el servidor virtual, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión del servidor virtual](../vsi/vsi_managing.html).
