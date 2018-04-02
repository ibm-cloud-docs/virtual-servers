---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Preguntas frecuentes: servidores virtuales  

## ¿Qué tipos de servidores virtuales se pueden utilizar?
{{site.data.keyword.BluSoftlayer_full}} ofrece un par de tipos de servidores virtuales. La oferta estándar es un servidor virtual basado en público, que es un entorno multiarrendatario, adecuado para diversas necesidades. Si busca un entorno de un solo arrendatario, tenga en cuenta la oferta de servidor virtual dedicado. La opción de servidor virtual dedicado resulta ideal para aplicaciones con requisitos más estrictos de recursos. Para obtener más información sobre las ofertas actuales de servidor virtual, consulte [Iniciación a los servidores virtuales](../vsi/vsi_index.html).

## ¿Dónde puedo encontrar información sobre precios para los tipos de instancias públicas?
Para obtener información sobre precios, consulte [Crear su servidor virtual ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers){: new_window}.

## ¿Puedo añadir almacenamiento de disco a mi servidor virtual por hora o mensual?
Puede actualizar o degradar el almacenamiento de disco para cualquier servidor virtual actualizando las opciones de almacenamiento en los campos de *Primer disco* a *Quinto disco* en la pantalla *Configuración* del dispositivo que desea actualizar. Para obtener más información, consulte [Reconfiguración de un servidor virtual existente](../vsi/vsi_reconfigure.html).

## ¿Con cuántos servidores virtuales por hora puedo empezar?

De forma predeterminada, una cuenta tiene un límite de 20 instancias que se pueden ejecutar en servidores virtuales públicos, servidores virtuales dedicados y servidores nativos, en un momento determinado.  Si desea aumentar este límite, póngase en contacto con el equipo de soporte para ofrecer más detalles sobre lo que hace y sobre cuántas instancias necesita.

## ¿Cómo se me facturará el ancho de banda de mis servidores virtuales por hora?

La facturación virtual por hora está desglosada para el tráfico de entrada y de salida. Todo el tráfico de entrada a su servidor virtual es gratuito. El tráfico de salida se mide y se factura por GB, y los totales se evalúan al final del periodo de facturación.

## ¿En qué casos se migra mi servidor virtual a un host diferente?

En casos limitados un servidor virtual puede necesitar migrarse a un host diferente. Si es necesaria una migración, el servidor virtual se cerrará, se migrará y, luego, se reiniciará. Un servidor virtual puede ser migrado en los casos siguientes:

* Un hipervisor debe ser actualizado, un host está fuera de servicio, o un host no puede asumir nuevas instancias. Si un host está marcado para cualquiera de estos cambios, cuando uno de sus servidores virtuales rearranca desde el {{site.data.keyword.slportal_full}}, el rearranque desencadena automáticamente la migración del servidor virtual a un host distinto.
* Mantenimiento de infraestructura. Puede recibir un correo electrónico que indica que es necesario el mantenimiento en un sistema que alberga el servidor virtual. Su servidor virtual puede necesitar migrarse como parte del mantenimiento de infraestructura.
* Una actualización a una instancia existente. Para un rendimiento coherente, si actualiza una instancia podría ser migrada a un host diferente para asegurarse de que recibe la CPU y la memoria dedicadas adecuadas.

Durante una ventana de mantenimiento, puede ver una opción **Migrar host** visualizada en el menú **Acciones** del dispositivo en el {{site.data.keyword.slportal}}. **Migrar host** le permite migrar el servidor virtual a un nuevo host que le convenga durante un periodo de mantenimiento especificado. Si no inicia la migración durante el período de mantenimiento, el servidor virtual se migrará automáticamente para completar el mantenimiento necesario. La opción **Migrar host** no persistirá y sólo estará disponible durante los periodos de mantenimiento que se comunican a través de notificaciones de mantenimiento.

También puede ver la opción **Migrar host** si uno de los servidores virtuales es necesario que tenga un cierto nivel de hipervisor que no está disponible en el host actual.

## ¿Qué ocurre con mis datos cuando se suprime mi almacenamiento portátil?

Cuando se suprime el almacenamiento, se eliminan todos los punteros a los datos en dicho volumen, por lo que los datos serán completamente inaccesibles. Si el almacenamiento físico se vuelve a suministrar a otra cuenta, se asignará un nuevo conjunto de punteros. La nueva cuenta no tiene ningún modo de acceder a los datos que pudieran haberse guardado en el almacenamiento físico. El nuevo conjunto de punteros muestra todo 0. Cuando se escriben nuevos datos en el volumen/LUN, se sobrescriben los datos inaccesibles que aún existan.

## ¿Puedo utilizar una suscripción a Hat Cloud Access para crear un servidor virtual?

Sí. Al importar una imagen, puede especificar que proporcionará la licencia de sistema operativo. Para obtener más información, consulte [Utilizar Red Hat Cloud Access](../infrastructure/image-templates/use-red-hat-cloud-access.html). A continuación, puede solicitar un servidor virtual de la plantilla de imagen y utilizar su suscripción existente de [Red Hat Cloud Access ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window}.

## ¿Qué diferencia hay entre un servidor virtual y un servidor privado virtual (VPS)?

Un servidor virtual es parecido a un servidor privado virtual (VPS) o servidor dedicado virtual (VDS) con los que quizás ya está familiarizado. Estos entornos de "servidor virtual" permite suministrar distintos entornos de forma privada y segura en un solo nodo de hardware, pero VDS y VPS tienen una capacidad más limitada. Las opciones VPS y VDS suelen limitarse a una arquitectura de un solo servidor, de modo que los únicos recursos que se pueden añadir o dividir entre cada servidor virtual de un VDS o VPS son los recursos que están físicamente instalados en dicho servidor.

Los servidores virtuales se suministran en una arquitectura de nube de varios servidores que sondea todos los recursos de hardware disponibles para que los utilicen las instancias individuales. Los servidores virtuales pueden aprovechar una plataforma compartida de almacenamiento primario basado en SAN de alta capacidad o un almacenamiento de disco local de alto rendimiento. Puesto que cada instancia forma parte del entorno de nube mayor, la comunicación entre todos los servidores virtuales es instantánea.

## No puedo conectar con la API de virtualización. ¿Cómo lo puedo solucionar?

Este error suele producirse porque una contraseña ha quedado obsoleta. Para solucionarlo, actualice la contraseña raíz o de Administrador para el sistema operativo del servidor virtual en el {{site.data.keyword.slportal_full}}.
