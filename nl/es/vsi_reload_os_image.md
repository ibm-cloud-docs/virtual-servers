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

# Recarga del sistema operativo mediante una plantilla de imagen
Al igual que la recarga de SO estándar, la recarga de un dispositivo desde una plantilla de imagen permite a los usuarios restaurar o reconfigurar un dispositivo en función de una plantilla de imagen existente que está asociada a la cuenta utilizada del Portal de clientes. Durante el proceso de recarga de SO estándar, las opciones de configuración para el dispositivo se pueden seleccionar individualmente, mientras que la característica Cargar desde imagen carga la configuración exacta que aparece en la plantilla de imagen. Puede añadir características opcionales antes de realizar la recarga.
Siga los pasos siguientes para realizar una recarga de SO desde una plantilla de imagen utilizando la característica Cargar desde imagen del Portal de clientes.
{:shortdesc}

## Realización de la recarga mediante una plantilla de imagen
1. Realice una copia de seguridad de todos los datos del dispositivo.
  
   **Nota:** las recargas de SO dan lugar a la eliminación de todos los datos del disco duro. Si no se realiza una copia de seguridad de los datos antes de iniciar la recarga de SO, no se podrán recuperar. Bluemix (Softlayer) no hace copia de seguridad de los datos almacenados en dispositivos del cliente y no se hace responsable de ninguna pérdida de datos asociada con el proceso de recarga de SO.
  
2. En la página Lista de dispositivos, seleccione **Cargar desde imagen** en el menú **Acciones** del dispositivo deseado.

3. Marque el recuadro de selección de la plantilla de imagen que desee y seleccione la plantilla de imagen que se cargará en el dispositivo.

   **Nota:** antes de completar la recarga, la plantilla de imagen se copia en el centro de datos que contiene el dispositivo, si no se encuentra ya en el mismo centro de datos. Si la plantilla de imagen se debe copiar en el centro de datos apropiado, puede que se aplique una tarifa adicional si la plantilla no se suprime de la ubicación después de que se realice la recarga de SO.
  
4. Determine si desea añadir alguna característica opcional. Las características opcionales que seleccione se añaden al dispositivo como parte del proceso de recarga.
   
   <table>
   <CAPTION>Tabla 1. Características opcionales</CAPTION>
   <THEAD>
   <TR>
   <th>Características opcionales</th>
   <th>Pasos</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   </tr>
   <tr>
   <td>Sí, deseo añadir característica opcionales.</td>
   <td>
   <ol>
   <li>Pulse <b>Cargar imagen seleccionados</b>.</li>
   <li>Revise la configuración de la imagen y continúe o cancele.</li>
   <li>Pulse <b>Confirmar recarga de SO</b> para confirmar la acción y comenzar el proceso de recarga de SO.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Sí, no deseo añadir característica opcionales.</td>
   <td>Pulse <b>Ver características opcionales</b>.</td>
   </tr>
   </TBODY>
   </table>

5. Configure las opciones adicionales procedentes. Consulte la siguiente información para obtener más detalles.
   
   <dl>
   <dt>Script posterior a la instalación</dt>
   <dd>Añade un script de instalación existente o posterior a la instalación.</dd>
   <dt>Clave SSH</dt>
   <dd>Añade una clave SSH al dispositivo tras la acción de recarga. </dd>
   <dt>Restablecer contraseña de IPMI</dt>
   <dd> Esta opción sólo está disponible para dispositivos físicos. </dd>
   <dt>Aplicar actualizaciones de BIOS de placa base</dt>
   <dd>Esta opción sólo está disponible para dispositivos físicos. </dd>
   <dt>Aplicar actualizaciones de firmware en todos los discos duros</dt>
   <dd>Esta opción sólo está disponible para dispositivos físicos.</dd>
   <dt>Añadir agrupación de repuesto después de la recarga de SO</dt>
   <dd>Esta opción solo está disponible en dispositivos físicos y requiere aprobación interna antes de estar disponible en una cuenta.</dd>
   <dt>Borrar todos los discos duros</dt>
   <dd> Esta opción solo está disponible en dispositivos físicos y requiere que el administrador de la cuenta defina permisos de usuario especiales.</dd>
   <dt>Recarga de SO con conservación de disco</dt>
   <dd>Conserva todos los datos en el disco primario actual durante el proceso de recarga de SO. El resultado de la conservación de disco es que la unidad primaria se convierte en un dispositivo de almacenamiento portátil. Esta opción solo está disponible en dispositivos virtuales y genera cargos adicionales según el patrón de facturación (por horas o meses) del dispositivo. Se pueden cancelar estos cargos cancelando el dispositivo de almacenamiento portátil en cualquier momento después de su creación.</dd>
   </dl>

6. Pulse **Cargar imagen seleccionados**.

7. Revise la configuración de la imagen y pulse **Siguiente** para continuar con la pantalla siguiente o **Cancelar** para cancelar la acción.

   **Nota:** después de pulsar **Siguiente**, todos los puertos de red correspondientes al dispositivo se cierran sistemáticamente y el dispositivo deja de estar disponible durante un máximo de 15 minutos. Durante este tiempo, la acción se puede cancelar en cualquier momento pulsando **Cancelar**. El siguiente paso se debe completar en 15 minutos después de pulsar **Siguiente** o se deberán volver a realizar los pasos anteriores. Este proceso supone una protección para garantizar que no se añaden datos adicionales a un dispositivo entre la confirmación de la configuración y la iniciación de la recarga de SO.

8. Pulse **Confirmar recarga de SO** para confirmar la acción y comenzar el proceso de recarga de SO. Pulse **Cancelar** si desea cancelar la acción.

## Qué hacer a continuación
Después de iniciar el proceso de recarga de SO, el dispositivo queda fuera de línea y comienza el proceso de recarga de SO.
El periodo de tiempo en el que se realiza la recarga de SO depende de la configuración actual y nueva del dispositivo.
Si la recarga tarda más de 24 horas, póngase en contacto con nuestro equipo de soporte. Cuando el dispositivo vuelva a estar en línea, funcionará según lo especificado en la nueva configuración para la recarga de SO. Todos los datos anteriormente guardados en el dispositivo se pierden, pero se pueden restaurar si se ha hecho una copia de seguridad antes de la recarga. Si no se ha hecho una copia de seguridad, no se podrán recuperar los datos.

 Para volver a registrar el dispositivo con eValut, consulte [Volver a registrar el dispositivo con eVault ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
