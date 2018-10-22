---



copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Preguntas frecuentes: Servidores (general)

## ¿Cuál es la diferencia entre "Arrancar desde imagen" y "Cargar desde imagen"?
Tanto Arrancar desde imagen como Cargar desde imagen utilizan plantillas de imagen existentes, que se aplican a un dispositivo para sustituir el sistema operativo existente o para complementar el sistema operativo con el fin de solucionar un problema existente. La principal diferencia entre los procesos de arranque y carga es el tipo de imagen que se utiliza. Cuando se realice un proceso de arranque o carga desde imagen, asegúrese de haber hecho una copia de seguridad todos los datos que desea recuperar.

   * El proceso de Arrancar desde imagen es una forma de arrancar un dispositivo utilizando un ISO suministrado por {{site.data.keyword.BluSoftlayer_full}} para la recuperación del sistema o un ISO que se ha cargado mediante la característica *Importar imagen* en el {{site.data.keyword.slportal_full}}. El ISO puede ser una versión nueva del sistema operativo del dispositivo o un disco de recuperación que se puede utilizar para solucionar un problema con el dispositivo.
   * Cargar desde imagen es un método de recarga de SO que utiliza una plantilla de imagen que se ha capturado desde un dispositivo o que se ha cargado utilizando la característica *Importar imagen* en el {{site.data.keyword.slportal}}. La opción *Cargar desde imagen* realiza la recarga utilizando un VHD, que borra todos los datos del dispositivo y sustituye el sistema operativo y los archivos existentes con una versión "como nueva" de la imagen seleccionada.

## ¿Por qué no puedo conectar con la consola de KVM?
Si no puede conectar con la consola de KVM, revise los consejos siguientes sobre resolución de problemas para ayudarle a resolver el problema. Si se producen problemas adicionales, póngase en contacto con el equipo de soporte. Para obtener más información sobre cómo ponerse en contacto con el equipo de soporte, consulte [Obtención de ayuda y soporte](../vsi/vsi_ts_index.html).

   * La consola de KVM es un applet Java. Java debe estar instalado para poder acceder a la consola. Para obtener más información sobre la instalación de Java, consulte [Descarga gratuita de Java ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.java.com/en/download/){: new_window}.  
   * Si Java está instalado, asegúrese de que la conexión se ha establecido utilizando VPN. Si no se ha establecido una conexión, aparece un aviso cuando se intenta conectar con la consola de KVM que indica que se necesita una conexión VPN.
   * La consola de KVM puede generar uno o varios recuadros emergentes durante el proceso de conexión. Habilite las ventanas emergentes del {{site.data.keyword.slportal}} para asegurarse de que pueda realizarse una conexión.
   * Es posible que reciba un error que indique que "Las aplicaciones Java están bloqueadas por los valores de seguridad". Para los dispositivos iKVM nativos, debe añadir una excepción para la dirección IP del dispositivo IPMI. Para dispositivos VSI, asegúrese de permitir "https://control.softlayer.com" y la dirección IP de KVM. Para obtener más información, consulte [¿Por qué las aplicaciones Java están bloqueadas por los valores de seguridad con el Java más reciente? ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.java.com/en/download/help/java_blocked.xml){: new_window}.
   * Si se cumplen las condiciones anteriores y recibe un error que indica que "que el manifiesto de permisos necesario en main.jar", significa que los applets Java no se han habilitado en el panel de control de Java. Este valor se ha incorporado como medida de seguridad de Oracle en Java SE v7. Habilite los applets en el panel de control para solucionar este problema.

     **Nota:** Si utiliza Mac OSX junto con Google Chrome, consulte la información y los requisitos del sistema para instalar y utilizar Mac Java 7 en el sitio web de Java.

   * Si está intentando conectar con un VSI a través de Java estándar y lo único que obtiene son errores, también puede intentarlo utilizando VNC.

Si ha completado todas las comprobaciones anteriores y sigue sin poder conectar con la consola de KVM, póngase en contacto con el equipo de soporte para obtener ayuda adicional para solucionar el problema. Si se ha establecido una conexión con la consola pero hay problemas al conectar con el dispositivo, asegúrese de que las credenciales utilizadas para acceder al dispositivo son válidos. Póngase en contacto con el administrador de la cuenta para verificar las credenciales, si es necesario.

## He perdido la contraseña para el servidor. ¿Cómo puedo recuperarla?
Si la contraseña del usuario root o del administrador de repente deja de funcionar, compruebe lo siguiente. Si es necesario, siga las instrucciones para iniciar un kernel de rescate y restablecer la contraseña.

   * ¿Está copiando y pegando la contraseña? Si no es así, inténtelo. Pegue también la contraseña en un bloc de notas para asegurarse de que no se copian espacios accidentalmente con la contraseña.
   * Si el servidor contiene cPanel, ¿es posible que cPHulk haya bloqueado la dirección IP debido a inicios de sesión fallidos? Si es así, puede acceder al servidor utilizando KVM o IPMI y colocar la dirección IP en la lista blanca en cPHulk con "/scripts/cphulkdwhitelist" seguido de la dirección IP.
   * ¿Ha intentado alguien cambiar la contraseña del servidor recientemente modificando la contraseña en el {{site.data.keyword.slportal}}? La modificación de la contraseña en el {{site.data.keyword.slportal}} solo cambia lo que se ve como contraseña. No cambia la contraseña que utiliza el servidor. Si ha sucedido esto, puede ponerse en contacto con el equipo de soporte; generalmente pueden recuperar la contraseña original que funcionaba.
   * Es posible que tenga que arrancar en la modalidad de rescate del sistema operativo para poder restablecer la contraseña. Para obtener más información, consulte [Inicio de un kernel de rescate](/docs/vsi/vsi_launch_rescue.html).

Si ha comprobado todo esto y sigue sin poder conectar con el servidor utilizando la contraseña, póngase en contacto con el equipo de soporte mediante una incidencia y solicite un restablecimiento de contraseña. El equipo de soporte deberá rearrancar el servidor para restablecer la contraseña, por lo que debe asegurarse de que está preparado para aprobar el rearranque y/o para ofrecer un intervalo de tiempo de mantenimiento en el que desea que se complete la operación. La mayoría de los restablecimientos se consiguen en 15 minutos. En el {{site.data.keyword.slportal}}, puede crear una incidencia yendo a **Soporte > Añadir incidencia** y utilizando el asunto *"Rearranques y acceso a la consola"*.

## ¿Se da soporte a las particiones LVM como sistema de archivo válido?
LVM (Logical Volume Management) proporciona funciones de gestión lógica de sistemas de archivos en Linux. En el entorno {{site.data.keyword.BluSoftlayer}}, LVM no recibe soporte como esquema de particionamiento arrancable. No se pueden solicitar instancias de servidor virtual con LVM ni se pueden suministrar imágenes de importación que utilicen LVM como partición de arranque. Si necesita LVM en la partición de arranque, la oferta nativa puede dar soporte a LVM en al arranque para ciertos sistemas operativos. Con el soporte y configuración adecuados del sistema operativo, se pueden utilizar discos VSI secundarios para particiones LVM; sin embargo, es importante señalar que LVM no es un sistema de archivos soportado para imágenes flex o para plantillas de imagen. Si tiene más preguntas, abra una incidencia con el equipo de soporte que pueda ayudarle.

## Rutas 161.26.0.0/16 preconfiguradas en hosts de clientes
{{site.data.keyword.BluSoftlayer}} habilita una nueva ruta en todos los servidores recién suministrados para dar soporte a productos futuros.
   * La ruta apunta a cualquier dirección del rango 161.26.0.0/16 (161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255) para la red privada de fondo.
   * IANA asigna este bloque de IP a {{site.data.keyword.BluSoftlayer_notm}} y no se anunciará en la Internet pública.
   * Sólo se direccionarán sistemas de {{site.data.keyword.BluSoftlayer_notm}} fuera de este espacio.
   * Las ACL de servidores de clientes, servidores virtuales y pasarelas Vyatta se tendrán que actualizar para que permitan a los hosts de los clientes utilizar servicios de la infraestructura configurados con direcciones IP fuera de este rango.

## Cómo añadir el nuevo direccionamiento para varios sistemas operativos

   <table>
   <CAPTION>Tabla 1. Adición de rutas por sistema operativo</CAPTION>
   <THEAD>
   <TR>
   <th>Sistema operativo</th>
   <th>Pasos</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Windows 2003 Standard y Enterprise</td>
   <td>
   Añada la ruta persistente desde la línea de mandatos escribiendo lo siguiente:
   <blockquote>route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p</blockquote>
   <b>Nota:</b> Sustituya 10.0.0.1 por la dirección IP de su pasarela privada.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Server Core
   </td>
   <td>
   Añada la ruta persistente desde la línea de mandatos escribiendo lo siguiente:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Nota:</b> Sustituya 10.0.0.1 por la dirección IP de su pasarela privada.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Web, Standard, Enterprise y Datacenter</td>
   <td>
   Añada la ruta persistente desde la línea de mandatos escribiendo lo siguiente:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Nota:</b> Sustituya 10.0.0.1 por la dirección IP de su pasarela privada.
   </td>
   </tr>
    <tr>
   <td>RedHat, Fedora y CentOS</td>
   <td>
   Cree una nueva ruta editando o creando el siguiente archivo: <i>/etc/sysconfig/network-scripts/route-eth0</i>
   <p>Después de crear este archivo, debe añadirle la siguiente información: <i>161.26.0.0/16 via 10.0.0.1</i>
   </p>
   <b>Nota:</b> Sustituya 10.0.0.1 por la dirección IP de su pasarela privada.
   </td>
   </tr>
   <tr>
   <td>Ubuntu y Debian</td>
   <td>
   En el archivo <i>/etc/network/interfaces</i>, añada la línea siguiente al final del archivo:
   <blockquote>
   up route add -net 161.26.0.0/16 gw 10.0.0.1
   </blockquote>
   <b>Nota:</b> Sustituya 10.0.0.1 por la dirección IP de su pasarela privada.
   </td>
   </tr>
   <tr>
   <td>Vyatta</td>
   <td><i>set protocols static route 161.26.0.0/16 next-hop 172.16.0.26</i>
   <p>
   <b>Nota:</b> Sustituya 172.16.0.26 por la pasarela de la subred en la que se encuentra la máquina, que debe coincidir con la pasarela definida para la ruta 10.0.0./8.</p>
   </td>
   </tr>
   <tr>
   <td>ESXi</td>
   <td>Utilice el siguiente mandato para añadir la ruta al host ESXi:
   <blockquote>
   esxcfg-route -a 161.26.0.0/16 10.0.0.1
   </blockquote>
   <b>Nota:</b> Sustituya 10.0.0.1 por la dirección IP de su pasarela privada.</td>
   </tr>
   <tr>
   <td>CoreOS</td>
   <td>Cree un archivo de ruta estática en /etc/systemd/network llamado 10-static.network parecido al siguiente:
   <blockquote>
   [Route]
   Gateway=10.0.0.1
   Destination=161.26.0.0/16
   </blockquote>
   <b>Nota:</b> Sustituya 10.0.0.1 por la dirección IP de su pasarela privada.</td>
   </tr>
   </TBODY>
   </table>
   
   <a name="top"></a>

## ¿Puedo hacer que el sistema de supervisión emita un rearranque automático Y advierta a un técnico de soporte en el caso de que el servidor deje de responder?

Sí; si solicita nuestro servicio de **Arranque automático después de un error de supervisión**, puede configurar el sistema de supervisión de modo que rearranque automáticamente el servidor y emita una incidencia para un técnico de soporte si se genera una alerta de supervisión. Como servicio adicional, ofrecemos la **Supervisión NOC**, por la que recibirá una notificación personal en el caso de que se produzca un problema de supervisión. Para obtener más información sobre estas dos ofertas, consulte [Supervisión del servidor ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://www.softlayer.com/services/monitoring/){:new_window}.

## ¿Qué es una duplicación cvsup?

Puede realizar una actualización hacia una duplicación cvsup local que se ejecute para usted. Asegúrese de que supfile tenga la siguiente entrada:

```
*default host=cvsup.service.softlayer.com
```
{:pre }

Los distfiles también se duplican y están disponibles desde freebsd.org. Puede añadir la siguiente línea en el archivo */etc/make.conf* para intentar descargar primero desde el repositorio local:

```
MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"
```
{:screen }

Si el archivo no está allí, seguirá el puerto individual Makefile y pasará a la siguiente duplicación.



