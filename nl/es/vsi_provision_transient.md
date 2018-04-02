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
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Suministro de instancias transitorias
{: #ordering-vs-transient}
Puede suministrar sus instancias de servidor virtual transitorio mediante el {{site.data.keyword.slportal_full}}.
{:shortdesc}

## Antes de empezar
Antes de empezar, revise los siguientes requisitos previos.

  1. Asegúrese de tener configuradas las credenciales del {{site.data.keyword.slportal}}.

  2. Revise las consideraciones de capacidad para instancias de servidores virtuales.  Para obtener más información, consulte [Consideraciones de capacidad](ts_capacity_bp.html).

## Inicio de sesión
Asegúrese de que ha iniciado sesión en el {{site.data.keyword.slportal}}:

  1. Acceda al [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.

Se abrirá la página principal del {{site.data.keyword.slportal}}.

## Suministro de una instancia de servidor virtual transitorio
{: #ordering-transient-instance}
Una vez completados los requisitos previos, suministre una instancia de servidor virtual transitorio. Puede suministrar sus instancias transitorias de dos maneras: a través del menú **Dispositivos** o el icono **Dispositivos**.

### Suministro de una instancia de servidor virtual transitorio a través del icono Dispositivos
Para suministrar la instancia de servidor virtual transitorio a través del icono *Dispositivos*, siga estos pasos:

1.  En {{site.data.keyword.slportal}}, localice la sección **Pedido** y pulse **Dispositivos**.
2.  En *Servidor virtual público* dentro de la página *Dispositivos*, pulse **Transitorio** para la oferta de servidor virtual.
3.  En la página *Configurar su servidor de nube*, especifique toda la información pertinente.
4.  Pulse **Añadir a pedido** para continuar.
5.  Confirme o edite la información de dominio correspondiente al servidor.
5.  Pulse los recuadros de selección **Términos del servicio de la nube** y **Acuerdo de servicio de terceros**.
6.  Confirme o especifique la información sobre el pago y pulse **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.

 Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*.

### Suministro de una instancia de servidor virtual transitorio a través del menú Dispositivos
{: #ordering-transient-devices-menu}

También puede suministrar instancias de servidor virtual transitorio a través del menú *Dispositivos* de la página principal del {{site.data.keyword.slportal}}.

1. Pulse **Dispositivos > Lista de dispositivos**.

   La página Dispositivos muestra todos los tipos de dispositivos -host dedicados, servidores virtuales, servidores nativos y controladores de distribución de aplicaciones NetScaler- de su cuenta.
2. Pulse el enlace **Solicitar dispositivos** en la esquina superior derecha.
3. En *Servidor virtual público* dentro de la página *Dispositivos*, pulse **Transitorio** para la oferta de servidor virtual.
4. En la página *Configurar su servidor de nube*, especifique toda la información pertinente.
5. Pulse **Añadir a pedido** para continuar.
6. Confirme o edite la información de dominio correspondiente al servidor.
7. Pulse los recuadros de selección **Términos del servicio de la nube** y **Acuerdo de servicio de terceros**.
8. Confirme o especifique la información sobre el pago y pulse **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.

Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*.

También puede suministrar un servidor virtual transitorio mediante la {{site.data.keyword.slapi_short}}. Para ver un ejemplo, consulte [Suministro de una instancia transitoria mediante Crear objeto](../vsi/vsi_provision_api.html#api-rest-transient).
{:tip}

## Siguientes pasos
Una vez suministrado el servidor virtual, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión del servidor virtual](../vsi/vsi_managing.html).
