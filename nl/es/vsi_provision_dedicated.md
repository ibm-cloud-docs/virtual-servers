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

# Suministro de hosts e instancias dedicados
{: #ordering-vs-dedicated}

Dispone de dos opciones para suministrar las instancias dedicadas. La primera es a través del catálogo de {{site.data.keyword.Bluemix}} y la segunda a través del {{site.data.keyword.slportal_full}}. El catálogo y el {{site.data.keyword.slportal}} requieren ID de inicio exclusivos. El nombre de usuario y la contraseña del catálogo no funcionarán para iniciar una sesión en el portal y viceversa. Consulte [Registro en {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} para configurar su catálogo de {{site.data.keyword.Bluemix_notm}} o sus credenciales de {{site.data.keyword.slportal}}.
{:shortdesc}

## Inicio de sesión en el catálogo de IBM Cloud
Siga los pasos siguientes para iniciar una sesión en el catálogo de {{site.data.keyword.Bluemix_notm}} para comenzar a suministrar sus hosts dedicados e instancias de host dedicadas. 

1. Abra una nueva ventana del navegador y escriba [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/){: new_window}.
2.	Pulse el enlace **Iniciar sesión ** (esquina superior derecha). 
3.	Escriba su correo electrónico o IBMid y pulse **Continuar**.
4.	Escriba su contraseña y pulse **Iniciar sesión**.
5.	Seleccione **Infraestructura > Cálculo**.
6.  Pulse el mosaico **Servidores virtuales**.
7.	Seleccione la opción **Servidores virtuales dedicados**.
8.  Pulse **Crear**. 

Se abrirá la página principal del {{site.data.keyword.slportal}}.

## Inicio de sesión en el Portal de clientes
Siga los pasos siguientes para iniciar una sesión en el {{site.data.keyword.slportal}} para comenzar el pedido de sus hosts dedicados e instancias de host dedicadas.

1.	Abra una nueva ventana del navegador y escriba [https://control.softlayer.com](https://control.softlayer.com){: new_window}. 
2.	Escriba su nombre de usuario y contraseña y pulse **Iniciar sesión** O BIEN pulse **Iniciar sesión con IBMid**.
3.	Escriba su correo electrónico o IBMid y pulse **Continuar**.
4.	Escriba su contraseña y pulse **Iniciar sesión**.

Se abrirá la página principal del {{site.data.keyword.slportal}}.

## Suministre su host dedicado 
Siga los pasos siguientes para suministrar sus hosts dedicados.

1.	Pulse el icono **Dispositivos**.
2.  Pulse el enlace **Servidor virtual dedicado por hora** o **Servidor virtual dedicado mensual**. 

   **Nota:** los servidores dedicados son servidores privados.

Se abrirá la página *Configurar el servidor de nube*. Desde esta página puede solicitar una instancia dedicada que esté o no asociada a un host dedicado. Encontrará más información sobre cómo solicitar instancias en [Suministro de instancias de host dedicadas](#provision-dedicated-instances).

4.	Pulse el botón **Crear host** en la parte derecha del formulario.
5.	Especifique la información siguiente:
    
    <table>
    <CAPTION>Tabla 1. Selecciones de suministro de host dedicado</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Cantidad</td>
    <td>Escriba el número de host dedicados que desea solicitar. Tenga en cuenta que solo se pueden desplegar dos hosts dedicados por solicitud de suministro.</td>
    </tr>
    <tr>
    <td>Ubicación</td>
    <td>Seleccione el centro de datos de {{site.data.keyword.cloud}} en el que desea colocar los hosts. Consulte Acerca de para ver la lista de centros de datos disponibles.</td>
    </tr>
    <td>Host dedicado</td>
    <td>El valor predeterminado es 56 núcleos X 242 RAM X 1,2 TB</td>
    </tr>
    </TBODY>
    </table>
    
    El resumen de su pedido se muestra en la parte derecha de la página *Configuración*. 
    
6.  Pulse el botón **Añadir a pedido**.
7.  Confirme las selecciones en la página de *Pago* y desplácese hasta *Configuración del sistema avanzado de host dedicado*.
8.  Especifique la información siguiente:

    <table>
    <CAPTION>Tabla 2. Configuración avanzada del sistema de host dedicado</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Selección de POD</td>
    <td>Pulse el recuadro desplegable y seleccione el POD donde desea colocar el host dedicado.</td>
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

9.  Pulse el recuadro de selección **Términos de los servicios en la nube**.
10. Confirme o especifique la información sobre el pago y pulse el botón **Enviar**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.

    Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico de suministro completado incluirá un enlace que le llevará directamente a la página **Detalles del dispositivo** después de iniciar una sesión en {{site.data.keyword.Bluemix_notm}}. Otra opción sería iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

## Suministre sus instancias de host dedicadas
{: #provision-dedicated-instances}
Puede suministrar sus instancias de host dedicadas de dos maneras: a través del menú **Dispositivos** o del icono **Dispositivos**.

### Suministro de sus instancias de host dedicadas a través del menú Dispositivos
{: #ordering-dedicated-devices-menu}

La primera opción consiste en suministrar las instancias de host dedicadas a través del menú **Dispositivos** de la página principal de {{site.data.keyword.slportal}}. Siga estos pasos para llevar a cabo este proceso.

1.	Pulse **Dispositivos > Lista de dispositivos**. 
 
    La página *Dispositivos* muestra todos los tipos de dispositivos -host dedicados, servidores virtuales, servidores nativos y controladores de distribución de aplicaciones NetScaler- de su cuenta. 

2.	Seleccione el host para las instancias de host dedicadas pulsando sobre su enlace en **Nombre de dispositivo**.
    
    Irá al separador **Configuración** de la página *Detalles del dispositivo*. El separador **Incidencias** muestra las incidencias de soporte activas y el separador **Asignaciones** muestra el uso de memoria correspondiente al periodo de facturación seleccionado. Consulte Utilización de los detalles del dispositivo para gestionar el host dedicado y las instancias para obtener más información sobre los separadores.

3.	Desplácese hasta la ventana **Instancias**.

    La forma en que se factura el host dedicado (al mes o por hora) determina la facturación de las instancias de host dedicadas. Tenga en cuenta que si tiene hosts de facturación mensual, puede suministrar instancias de host dedicadas de facturación tanto por hora como al mes. Dispone de dos enlaces -**Añadir por hora** y **Añadir mensualmente**— para suministrar sus instancias. Los hosts dedicados que se facturan por hora solo pueden suministrar instancias de host dedicadas que se facturen por hora y solo verá el enlace **Añadir por hora** enlace. 

4.	Pulse el enlace **Añadir por hora** si el host se factura por hora o mensualmente; pulse el enlace **Añadir mensualmente** si el host se factura al mes. Se le dirigirá a la página *Configurar el servidor de nube*. 

5.	Especifique la información siguiente:
       
    <table>
    <CAPTION>Tabla 3. Selecciones de instancias de host dedicadas</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Cantidad</td>
    <td>El número de instancias de host dedicadas que se van a desplegar en un solo host.</td>
    </tr>
    <tr>
    <td>Colocación</td>
    <td>
    <ul>
    <li>Asignar automáticamente – {{site.data.keyword.Bluemix_notm}} asigna automáticamente la instancia a un host (frente a la opción de que el usuario especifique una). La instancia se colocará en un centro de datos que tenga la capacidad necesaria. Si asigna la instancia automáticamente, no utilizará la capacidad de los hosts dedicados.</li>
    <li>Especificar host - El host dedicado asociado a la cuenta se mostrará en Host dedicado. </li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Host dedicado</td>
    <td>Seleccione en la lista el host dedicado en el que se deben suministrar las instancias.</td>
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
    <td>Puede suministrar hasta cuatro discos de arranque adicionales, SAN o locales, por instancia de host dedicada.</td>
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

6.	Pulse el botón **Añadir a pedido**.
7.  Especifique la información siguiente en la página de *Pago* bajo *Configuración avanzada del sistema*:

<table>
    <CAPTION>Tabla 4. Configuración avanzada del sistema de instancia de host dedicada</CAPTION>
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

8.  Pulse los recuadros de selección **Términos de los servicios en la nube** y **Acuerdo de servicios de terceros**.
9. Confirme o especifique la información sobre el pago y pulse el botón **Enviar**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla ya que también es su recibo del pedido de suministro.


Recibirá un correo electrónico cuando se hayan suministrado las instancias de host dedicadas.

### Suministro de sus instancias de host dedicadas a través del icono Dispositivos
La segunda opción para suministrar instancias de host dedicadas es utilizar el icono **Dispositivo** de la página de inicio del {{site.data.keyword.slportal}}. Siga estos pasos para llevar a cabo este proceso.

1.	Pulse el icono **Dispositivos** y seleccione **Por hora** o **Mensualmente** en Servidores virtuales dedicados.
2.	Siga los pasos del menú [Suministro de instancias de host dedicadas a través del menú Dispositivos](#ordering-dedicated-devices-menu), a partir del paso 5.

### Siguientes pasos
Una vez suministrado el servidor virtual, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión de servidores virtuales](../vsi/vsi_managing.html).


