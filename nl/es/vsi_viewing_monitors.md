---

copyright:
  years: 2017
lastupdated: "2017-10-23"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Visualización y gestión de supervisores
{: #viewing-and-managing-monitors}

La supervisión de un dispositivo permite a los usuarios iniciar el servicio y pings lentos para garantizar que el dispositivo está en línea y responde.
{:shortdesc}

Si no se recibe un eco durante el periodo de tiempo asignado (1 segundos para pings de servicio, 5 segundos para pings lentos), se envía una alerta a la dirección de correo electrónico especificada en la cuenta. El estado **Activo** en el campo **Estado** indica que se ha recibido un eco, mientras que **Inactivo**
indica que no se ha recibido un eco. Si ya ha configurado un supervisor básico, puede seguir los pasos siguientes para ver y gestionar la supervisión de un dispositivo.

   <table>
   <CAPTION>Tabla 1. Ver y gestionar la supervisión de un dispositivo</CAPTION>
   <THEAD>
   <TR>
   <th>Si la acción que se va a emprender es...</th>
   <th>Realice lo siguiente:</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Ver supervisores</td>
   <td>
   <ol>
   <li>En la lista de dispositivos, pulse el <b>Nombre de dispositivo</b> para acceder al dispositivo.</li>
   <li>Pulse el separador <b>Supervisión</b>. Aparece una página en la que se ven todos los pings actuales. (El separador <b>Supervisión</b> solo se puede ver si hay al menos un supervisor configurado.)</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Añadir un supervisor</td>
   <td>
   <ol>
   <li>En el separador <b>Supervisión</b> de la página Detalles del dispositivo, pulse <b>Gestionar supervisores</b> en la parte derecha de la página para gestionar los supervisores asociados a este dispositivo.</li>
   <li>En la página Supervisores, pulse el separador <b>Añadir supervisor</b>.</li>
   <li>Seleccione la dirección IP que desea supervisar en la lista desplegable <b>Dirección IP</b>.</li>
   <li>Seleccione el tipo de supervisor en la lista desplegable <b>Tipo de supervisor</b>.</li>
   <li>Configure las opciones de notificación. En la lista desplegable <b>¿Notificar?</b>, seleccione <b>Notificar a los usuarios</b> para informar a los usuarios sobre los problemas o <b>No hacer nada</b> para omitir la notificación a los usuarios.</li>
   <li>Seleccione el intervalo de tiempo para la notificación al usuario en la lista desplegable <b>Espera de notificación</b>.</li>
   <li>Pulse el botón <b>Añadir supervisor</b> para añadir el supervisor correspondiente al dispositivo. El nuevo supervisor aparece en la sección <b>Editar supervisores existentes</b> de la pantalla.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Editar un supervisor existente</td>
   <td>
   <ol>
   <li>En la página Supervisores, bajo la cabecera <b>Editar supervisores existentes</b>, pulse cualquiera de los detalles del supervisor para editar el supervisor.</li>
   <li>Puede actualizar cualquiera de los siguientes campos: Tipo de supervisor, Notificar, Espera de notificación.</li>
   <li>Pulse el botón <b>Actualizar</b> para actualizar los detalles. Pulse el botón <b>Cancelar</b> si desea cancelar la edición.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Eliminar un supervisor</td>
   <td>
   <ol>
   <li>En la página Supervisores, bajo la cabecera <b>Editar supervisores existentes</b>, pulse el icono Eliminar que hay junto a los detalles del supervisor.</li>
   <li>Pulse el botón <b>Sí</b> para eliminar el supervisor. Pulse el botón <b>No</b> si desea cancelar la acción.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Siguientes pasos

- Si se ha añadido un nuevo supervisor, aparecerá en el separador **Supervisión**. El supervisor enviará un ping al dispositivo cada cinco minutos y esperará una respuesta en función del tipo de ping seleccionado. Si no se recibe la respuesta esperada, se enviará un correo electrónico a la dirección de correo electrónico de notificación para la cuenta en el periodo de tiempo especificado, si se ha seleccionado la notificación.
- Si se ha editado un supervisor, este seguirá funcionando según lo especificado en los detalles de supervisión. Si se modifica el tipo, el periodo de tiempo para recibir el ping esperado será diferente. Si se han modificado las opciones de notificación, cambiará el modo en que se notificará a los usuarios sobre intentos fallidos en función de las nuevas selecciones. Se podrá seguir accediendo al supervisor desde el separador **Supervisión**.
- Si se elimina un supervisor, dejará de funcionar para el dispositivo. Toda la supervisión asociada al supervisor eliminado dejará de funcionar y el supervisor dejará de aparecer en el separador **Supervisión**.
