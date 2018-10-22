---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-03"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Suministro de instancias transitorias
{: #ordering-vs-transient}
Puede suministrar sus instancias de servidor virtual transitorio mediante el catálogo de {{site.data.keyword.cloud}} o el {{site.data.keyword.slportal}}.
{:shortdesc}

## Antes de empezar
Antes de empezar, revise los siguientes requisitos previos.

  1. Asegúrese de que tiene configuradas credenciales del catálogo de {{site.data.keyword.cloud_notm}} o del {{site.data.keyword.slportal}}.
  
  **Nota:** Para el catálogo de {{site.data.keyword.Bluemix_notm}}, debe tener una cuenta actualizada para solicitar servidores virtuales. Para obtener más información sobre cómo actualizar su cuenta, consulte [Cambio a un IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).

  2. Revise las consideraciones de capacidad para instancias de servidores virtuales. Para obtener más información, consulte [Consideraciones de capacidad](ts_capacity_bp.html).

## Suministro de una instancia de servidor virtual transitorio 
Cuando cumpla los requisitos previos, puede empezar a suministrar una instancia de servidor virtual transitorio. Puede suministrar su instancia mediante el catálogo de {{site.data.keyword.cloud_notm}} o el {{site.data.keyword.slportal}}.

### Suministro de instancias de servidor virtual transitorio mediante el catálogo de IBM Cloud
Para suministrar una instancia de servidor virtual transitorio a través del catálogo de {{site.data.keyword.cloud_notm}}, siga los pasos siguientes:

  1. Inicie una sesión en el catálogo de [{{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/catalog/){: new_window} con sus credenciales exclusivas.  
  2. En la sección **Infraestructura de cálculo**, pulse el mosaico **Servidores virtuales**.
  3. Seleccione la opción **Servidor virtual transitorio**.
  4. Pulse **Crear**.
  5. Rellene la información relevante correspondiente a su instancia de servidor virtual.
  6. Después de revisar el resumen del pedido, pulse el recuadro de selección **Acuerdos de servicios de terceros**.
  7. Pulse **Suministrar**.
  
### Suministro de instancias de servidor virtual transitorio través del portal de clientes
Para suministrar una instancia de servidor virtual transitorio a través del {{site.data.keyword.slportal}}, siga los pasos siguientes:

  1. Inicie una sesión en el [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
  2. Localice la sección **Pedido** y pulse **Dispositivos**.
  3. En *Servidor virtual público* dentro de la página *Dispositivos*, pulse **Transitorio** para la oferta de servidor virtual.
  4. En la página *Configurar su servidor de nube*, especifique toda la información pertinente.
  5. Pulse **Añadir a pedido** para continuar.
  6. Confirme o edite la información de dominio correspondiente al servidor.
  7. Pulse los recuadros de selección **Términos de los servicios en la nube** y **Acuerdo de servicio de terceros**.
  8. Confirme o especifique la información sobre el pago y pulse **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.

 Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*.

También puede suministrar un servidor virtual transitorio mediante la {{site.data.keyword.slapi_short}}. Para ver un ejemplo, consulte [Suministro de una instancia transitoria mediante Crear objeto](../vsi/vsi_provision_api.html#api-rest-transient).
{:tip}

## Siguientes pasos
Una vez suministrado el servidor virtual, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión del servidor virtual](../vsi/vsi_managing.html).
