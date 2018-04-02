---



copyright:
  years: 2017
lastupdated: "2017-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

#  Recarga del SO
Puede volver a cargar el sistema operativo (SO) en un dispositivo siempre que quiera para restaurar el orden de trabajo original del dispositivo o puede volver a configurar un dispositivo con otro software. Una recarga de SO elimina todos los datos del dispositivo y aplica una configuración "como nueva", basada en lo especificado durante el proceso de configuración de la configuración de la recarga de SO. Puesto que las recargas de SO borran todos los datos del dispositivo, si no ha hecho copia de seguridad de los datos antes de realizar la recarga, los datos se suprimirán de forma permanente y no se podrán recuperar.
{:shortdesc}

**Importante:** si desea conservar los datos, haga una copia de seguridad de todos los datos antes de realizar una recarga.

## Realización de la recarga
1. En la **Lista de dispositivos**, pulse el servidor que necesita una recarga de SO.
2. En el menú **Acciones** de la parte superior izquierda de la página, seleccione **Recarga de SO**.
3. Determine si desea recargar la configuración existente o recargar el dispositivo con una nueva configuración.

   <table>
   <CAPTION>Tabla 1. Opciones de recarga de SO</CAPTION>
   <THEAD>
   <TR>
   <th>Tipo de recargar</th>
   <th>Pasos</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Si desea realizar la recarga con una nueva configuración...</td>
   <td>
   <ol>
   <li>Pulse <b>Editar</b> para la categoría que requiere una actualización.</li>
   <li>Seleccione el nuevo software que desea aplicar al dispositivo en la lista desplegable <i>Seleccionar software</i>.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Si desea realizar la recarga con una configuración existente...</td>
   <td>Continúe en el paso siguiente.</td>
   </tr>
   </TBODY>
   </table>

4. Determine si se debe aplicar un script posteriores a la instalación una vez suministrado el dispositivo.

   Si desea aplicar un script posterior a la instalación, seleccione el script en la lista desplegable Script existente o especifique el URL completo del nuevo script.  De lo contrario, continúe en el paso siguiente.

5. Para los dispositivos físicos, determinar si las particiones instaladas se deben añadir o eliminar o no se deben modificar.
   
   <table>
   <CAPTION>Tabla 2. Opciones de acción de partición</CAPTION>
   <THEAD>
   <TR>
   <th>Acción de partición</th>
   <th>Pasos</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Para añadir particiones instaladas...</td>
   <td>
   <ul>
   <li>Pulse el enlace <b>Añadir otra partición</b>.</li>
   <li>Escriba el nombre exacto de la partición.</li>
   <li>Especifique el tamaño de la partición (en GB). Si desea, puede seleccionar Crecer para aumentar la partición de modo que llene el espacio de disco restante.
   <p><b>Nota:</b> sólo se puede seleccionar una partición para aumentarla. Esta partición es mayor que el tamaño especificado y llena toda la capacidad disponible. La capacidad de la partición seleccionada en Crecer se calcula restando el tamaño combinado de las demás particiones del número indicado en la capacidad total que se suministra en la sección Particiones instaladas.</p>
   </li>
   </ul>
   </td>
   </tr>
   <tr>
   <td>Para suprimir particiones instaladas...</td>
   <td>Pulse el icono <b>Suprimir</b> para suprimir la partición.</td>
   </tr>
   <tr>
   <td>Para no modificarla...</td>
   <td>Continúe en el paso siguiente.</td>
   </tr>
   </TBODY>
   </table>
    
6. Determine si desea aplicar una o varias claves SSH al dispositivo.

7. Marque los recuadros de selección adecuados para las opciones que desea aplicar al dispositivo durante o después de la recarga de SO.

   **Nota:** las opciones varían en función de dispositivo. No todas las opciones están disponibles para cada dispositivo.

8. Pulse el botón **Recargar configuración anterior** para continuar en la ventana emergente de revisión. Pulse el botón **Cancelar** si desea cancelar los cambios en el dispositivo y salir de la pantalla.

9. Verifique que todos los detalles de la sección Nueva configuración son correctos.  

10. Pulse el botón **Confirmar recarga de SO** para confirmar e iniciar la recarga de SO. Pulse el botón **Cancelar** para cancelar la acción.

## Qué hacer a continuación
Después de iniciar el proceso de recarga de SO, el dispositivo queda fuera de línea y comienza el proceso de recarga de SO.
El periodo de tiempo en el que se realiza la recarga de SO depende de la configuración actual y nueva del dispositivo.
Durante el proceso de configuración, el tiempo mínimo necesario para la recarga de SO se muestra en cada pantalla.
El tiempo que se muestra es una estimación hecha por el sistema y ofrece para su comodidad. Si la recarga tarda más de 24 horas, póngase en contacto con nuestro equipo de soporte. Cuando el dispositivo vuelva a estar en línea, funcionará según lo especificado en la nueva configuración para la recarga de SO. Todos los datos anteriormente guardados en el dispositivo se pierden, pero se pueden restaurar si se ha hecho una copia de seguridad antes de la recarga.
Si no se ha hecho una copia de seguridad, no se podrán recuperar los datos.
 
Para volver a registrar el dispositivo con eVault, consulte [Volver a registrar el dispositivo con eVault ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
