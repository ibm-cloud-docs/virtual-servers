---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Suministro de instancias dedicadas

Dispone de dos opciones para suministrar las instancias dedicadas. La primera es a través del catálogo de {{site.data.keyword.Bluemix}} y la segunda a través del {{site.data.keyword.slportal_full}}. El catálogo y el {{site.data.keyword.slportal}} requieren ID de inicio exclusivos. El nombre de usuario y la contraseña del catálogo no funcionarán para iniciar una sesión en el portal y viceversa. Consulte [Registro en {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} para configurar su catálogo de {{site.data.keyword.Bluemix_notm}} o sus credenciales de {{site.data.keyword.slportal}}.
{:shortdesc}

## Suministro de instancias de servidor virtual dedicadas
{: #provision-dedicated-instances}
Puede suministrar su instancia de servidor virtual dedicada mediante el catálogo de {{site.data.keyword.cloud_notm}} o el {{site.data.keyword.slportal}}. 

### Suministro de una instancia de servidor virtual dedicada a través del catálogo de IBM Cloud 
Para suministrar una instancia de servidor virtual dedicada a través del catálogo de {{site.data.keyword.cloud_notm}}, siga los pasos siguientes:

  1. Inicie una sesión en el catálogo de [{{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/catalog/){: new_window} con sus credenciales exclusivas. 
  2. En la sección **Infraestructura de cálculo**, pulse el mosaico **Servidores virtuales**.
  3. Seleccione la opción **Servidor virtual dedicado**.
  4. Pulse **Crear**.
  5. En la sección **Host dedicado**, seleccione **Asignar automáticamente**. A continuación, {{site.data.keyword.cloud_notm}} asigna automáticamente la instancia a un host del centro de datos seleccionado.
  
     **Nota**: Para los hosts dedicados, seleccione **Especificar host** o **Crear host**. Para obtener más información sobre los hosts dedicados y las instancias de host dedicadas, consulte [Servidores virtuales dedicados](../vsi/vsi_dedicated.html).
     
  5. Rellene la información relevante correspondiente a su instancia de servidor virtual dedicada. 
  6. Después de revisar el resumen del pedido, pulse el recuadro de selección **Acuerdos de servicios de terceros**. 
  7. Pulse **Suministrar**.

### Suministro de una instancia de servidor virtual dedicada a través del portal de clientes
Para suministrar una instancia de servidor virtual dedicada a través del {{site.data.keyword.slportal}}, siga los pasos siguientes:

1. Inicie una sesión en el [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
2. Localice la sección **Pedido** y pulse **Dispositivos**. Se abrirá la ventana **Solicitar producto de SoftLayer y servicios**. 
3.  Seleccione **Por hora** o **Mensualmente** en Servidores virtuales dedicados. Se le dirigirá a la página *Configurar el servidor de nube*. 

4.	Especifique la información siguiente:
       
    <table>
    <CAPTION>Tabla 1. Selecciones de instancias de host dedicadas</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Cantidad</td>
    <td>El número de instancias dedicadas que se van a desplegar.</td>
    </tr>
    <tr>
    <td>Colocación</td>
    <td>
    <ul>
    <li>Asignar automáticamente – {{site.data.keyword.Bluemix_notm}} asigna automáticamente la instancia a un host del centro de datos seleccionado.</li>
    <li>Especificar host – Se utiliza con instancias de host dedicadas. Consulte [Servidores virtuales dedicados](../vsi/vsi_dedicated.html) para obtener más información sobre los hosts dedicados y las instancias de host dedicado.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Centro de datos</td>
    <td>Seleccione el centro de datos en el que se deben suministrar las instancias.</td>
    </tr>
    <tr>
    <td>Instancia de cálculo</td>
    <td> Seleccione la memoria y CPU para cada instancia en una orden de suministro.</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> Seleccione la RAM para cada instancia en una orden de suministro.</td>
    </tr>
    <tr>
    <td>Sistema operativo</td>
    <td>Seleccione el sistema operativo para la instancia. Tenga en cuenta que aparecerá un mensaje de error si existe un conflicto entre el servidor y el sistema operativo. Por ejemplo, si se selecciona Linux en un servidor Microsoft SQL.</td>
    </tr>
    <tr>
    <td>Primer disco</td>
    <td>Seleccione SAN o Local para cada instancia de un pedido.</td>
    </tr>
    <tr>
    <td>Discos adicionales</td>
    <td>Puede suministrar hasta cuatro discos de arranque adicionales, SAN o locales, por instancia dedicada.</td>
    </tr>
    <td>Opciones de red</td>
    <td> Seleccione las opciones adecuadas o utilice los valores predeterminados.</td>
    </tr>
    <tr>
    <td>Complementos</td>
    <td> Seleccione las opciones adecuadas o utilice los valores predeterminados.</td>
    </tr>
    <tr>
    </TBODY>
    </table> 

5.	Pulse el botón **Añadir a pedido**. Se le redirigirá a la página de pago.
6.  Especifique la información siguiente en la página de *Pago* bajo *Configuración avanzada del sistema*:

    <table>
    <CAPTION>Tabla 2. Configuración avanzada del sistema de la instancia dedicada</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Selección de VLAN</td>
    <td>Añada el nuevo servidor a una VLAN bajo su cuenta si ya ha solicitado al menos un servidor.</td>
    </tr>
    <tr>
    <td>Scripts de suministro</td>
    <td>Proporcione un script que le permita automatizar algunos pasos después del suministro.</td>
    </tr>
    <tr>
    <td>Claves SSH</td>
    <td>Especifique una clave pública de la clave SSH, que le permitirá iniciar una sesión en el servidor después de que se suministre.</td>
    </tr>
    <tr>
    <td>Metadatos de usuario</td>
    <td>Metadatos opcionales para los scripts de suministro personalizados.</td>
    </tr>
    <tr>
    <td>Nombre de host</td>
    <td>Especifique un nombre permanente o temporal para el servidor, como por ejemplo server1.</td>
    </tr>
    <tr>
    <td>Dominio</td>
    <td>Escriba un nombre de subdominio de que no esté en conflicto con un nombre de dominio de Internet, como por ejemplo test.acme.com.</td>
    </tr>
    </TBODY>
    </table>

7.  Pulse los recuadros de selección **Términos de los servicios en la nube** y **Acuerdo de servicios de terceros**.
8. Confirme o especifique la información sobre el pago y pulse el botón **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.

    Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico de suministro completado incluirá un enlace que le llevará directamente a la página **Detalles del dispositivo** después de iniciar una sesión en {{site.data.keyword.Bluemix_notm}}. Otra opción sería iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

## Siguientes pasos
Una vez suministrado el servidor virtual, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión de servidores virtuales](../vsi/vsi_managing.html).

