---



copyright:
  years: 2017
lastupdated: "2017-10-24"


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
Tiene dos opciones para suministrar instancias de servidor virtual público. La primera es a través del catálogo de {{site.data.keyword.Bluemix}} y la segunda a través del {{site.data.keyword.slportal_full}}. El catálogo y el {{site.data.keyword.slportal}} requieren ID de inicio exclusivos. El nombre de usuario y la contraseña del catálogo no funcionarán para iniciar una sesión en el portal y viceversa.
{:shortdesc}

Antes de empezar, revise los siguientes requisitos previos.

  1. Asegúrese de que tiene configuradas credenciales del catálogo de {{site.data.keyword.Bluemix_notm}} o del {{site.data.keyword.slportal}}. 
  
     **Nota:** Para el catálogo de {{site.data.keyword.Bluemix_notm}}, debe tener una cuenta actualizada para solicitar servidores virtuales. Para obtener más información sobre cómo actualizar su cuenta, consulte [Cambio a un IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).
  
  2. Si aún no lo ha hecho, revise las opciones de despliegue que tiene a su disposición. Para obtener más información, consulte [Opciones de despliegue: servidor virtual público](../vsi/vsi_public.html).

## Inicio de sesión 
Asegúrese de que ha iniciado una sesión a través del catálogo de {{site.data.keyword.Bluemix_notm}} o del {{site.data.keyword.slportal}}: 

  <table>
   <CAPTION>Tabla 1. Elija una ubicación de inicio de sesión</CAPTION>
   <THEAD>
   <TR>
   <th>Si desea iniciar sesión con...</th>
   <th>Realice lo siguiente:</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Catálogo de IBM Cloud</td>
   <td>
   <ol>
   <li>Abra una nueva ventana del navegador y escriba <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Pulse el enlace <b>Iniciar sesión </b> (esquina inferior derecha). </li>
   <li>Escriba su correo electrónico o IBMid y pulse <b>Continuar</b>.</li>
   <li>Escriba su contraseña y pulse <b>Iniciar sesión</b>.</li>
   <li>Seleccione <b>Infraestructura</b> > <b>Cálculo</b>.</li>
   <li>Pulse el mosaico <b>Servidores virtuales</b>.</li>
   <li>Seleccione la opción <b>Servidores virtuales públicos</b>.</li>
   <li>Pulse <b>Crear</b>. Se abrirá la página principal del {{site.data.keyword.slportal}}.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Portal de clientes</td>
   <td>
   <ol>
   <li>Abra una nueva ventana del navegador y escriba <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Escriba su nombre de usuario y contraseña y pulse <b>Iniciar sesión</b>. O bien, pulse <b>Iniciar sesión con IBMid</b>. A continuación, escriba su correo electrónico o IBMid y pulse <b>Continuar</b>. Escriba su contraseña y pulse <b>Iniciar sesión</b>. Se abrirá la página principal del {{site.data.keyword.slportal}}.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Suministro de una instancia de servidor virtual público
{: #ordering-public-instance}
Después de haber completado los requisitos previos, puede empezar a suministrar una instancia de servidor virtual público. Puede suministrar sus instancias públicas de dos maneras: a través del menú **Dispositivos** o del icono **Dispositivos**.

### Suministro de una instancia de servidor virtual público a través del icono Dispositivos
Para suministrar la instancia de servidor virtual público a través del icono *Dispositivos*, siga estos pasos:

1.  En {{site.data.keyword.slportal}}, localice la sección **Pedido** y pulse **Dispositivos**.
2.  En la página Dispositivos, pulse **Por hora** o **Mensualmente** para elegir una de las ofertas de servidor virtual.
3.  En la página *Configurar su servidor de nube*, especifique toda la información pertinente.
4.  Pulse el botón **Añadir a pedido** para continuar.
5.  Confirme o edite la información de dominio correspondiente al servidor.
5.  Pulse los recuadros de selección **Términos de los servicios en la nube** y **Acuerdo de servicio de terceros**.
6.  Confirme o especifique la información sobre el pago y pulse el botón **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.

 Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*, después de iniciar una sesión en {{site.data.keyword.Bluemix_notm}}. También puede iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

### Suministro de una instancia de servidor virtual público a través de menú Dispositivos
{: #ordering-public-devices-menu}

También puede suministrar instancias de servidor virtual público a través del menú *Dispositivos* de la página principal del {{site.data.keyword.slportal}}. 

1. Pulse **Dispositivos > Lista de dispositivos**.

   La página Dispositivos muestra todos los tipos de dispositivos -host dedicados, servidores virtuales, servidores nativos y controladores de distribución de aplicaciones NetScaler- de su cuenta.
2. Pulse el enlace **Solicitar dispositivos** en la esquina superior derecha.
3. En la página Dispositivos, pulse **Por hora** o **Mensualmente** para elegir una de las ofertas de servidor virtual.
4. En la página *Configurar su servidor de nube*, especifique toda la información pertinente.
5. Pulse el botón **Añadir a pedido** para continuar.
6. Confirme o edite la información de dominio correspondiente al servidor.
7. Pulse los recuadros de selección **Términos de los servicios en la nube** y **Acuerdo de servicio de terceros**.
8. Confirme o especifique la información sobre el pago y pulse el botón **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.

Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*, después de iniciar una sesión en {{site.data.keyword.Bluemix_notm}}. También puede iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

### Siguientes pasos
Una vez suministrado el servidor virtual, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión del servidor virtual](../vsi/vsi_managing.html).
