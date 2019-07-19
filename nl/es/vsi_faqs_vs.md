---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-09"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# Preguntas frecuentes: servidores virtuales  
{: #faqs-virtual-servers}

## ¿Qué tipos de servidores virtuales se pueden utilizar?
{: faq}
{{site.data.keyword.BluSoftlayer_full}} ofrece un par de tipos de servidores virtuales dentro de su infraestructura clásica. La oferta estándar es un servidor virtual basado en público, que es un entorno multiarrendatario, adecuado para diversas necesidades. Si busca un entorno de un solo arrendatario, tenga en cuenta la oferta de servidor virtual dedicado. La opción de servidor virtual dedicado resulta ideal para aplicaciones con requisitos más estrictos de recursos. Para obtener más información sobre las ofertas actuales de servidor virtual, consulte [Iniciación a los servidores virtuales](/docs/vsi?topic=virtual-servers-getting-started-with-virtual-servers#getting-started-with-virtual-servers).

IBM Cloud ofrece la infraestructura de Virtual Private Cloud (VPC), que es la siguiente generación de la plataforma en la nube. Cree su propio espacio en {{site.data.keyword.cloud_notm}} para ejecutar un entorno aislado dentro de la nube pública utilizando VPC. VPC proporciona la seguridad de una nube privada, con la agilidad y la facilidad de una nube pública. Para obtener más información, consulte
[Acerca de Virtual Private Cloud](https://cloud.ibm.com/docs/vpc-on-classic?topic=vpc-on-classic-about).

## ¿Dónde puedo encontrar información sobre precios para los tipos de instancias públicas?
{: faq}

Para obtener información sobre precios, consulte [Crear su servidor virtual ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/cloud/virtual-servers){: new_window}.

## ¿Dónde puedo encontrar información sobre precios para las instancias públicas virtuales?
{: faq}

La estimación del coste de un servidor de {{site.data.keyword.cloud_notm}} para dar soporte a su carga de trabajo comienza en el [catálogo de {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/catalog). En el catálogo, seleccione
**Calcular** y elija el tipo de servidor: servidor nativo, servidor virtual o servidor virtual para VPC (Virtual Private Cloud). Para obtener información sobre los precios, consulte la
[Calculadora de suministro de servidores virtuales
![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

## ¿Puedo añadir almacenamiento de disco a mi servidor virtual por hora o mensual?
{: faq}

Puede actualizar o degradar el almacenamiento de disco para cualquier servidor virtual actualizando las opciones de almacenamiento en los campos de *Primer disco* a *Quinto disco* en la pantalla *Configuración* del dispositivo que desea actualizar. Para obtener más información, consulte [Reconfiguración de un servidor virtual existente](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).

## ¿Cuántos servidores virtuales por hora puedo iniciar?
{: #concurrent}
{: faq}

El número de instancias que puede ejecutar dependerá del nivel de madurez de la cuenta. De forma predeterminada, una cuenta con una antigüedad superior a 45 días tiene un límite de 20 instancias que se pueden ejecutar en servidores virtuales públicos, servidores virtuales dedicados y servidores nativos, en un momento determinado. Una cuenta más reciente tendrá un límite menor. Si desea aumentar el límite, póngase en contacto con el equipo de soporte para ofrecer más detalles sobre lo que hace y sobre cuántas instancias necesita.

## ¿Cómo se me facturará el ancho de banda de mis servidores virtuales por hora?
{: faq}

La facturación virtual por hora está desglosada para el tráfico de entrada y de salida. Todo el tráfico de entrada a su servidor virtual es gratuito. El tráfico de salida se mide y se factura por GB, y los totales se evalúan al final del periodo de facturación.

## ¿En qué casos se migra mi servidor virtual a un host diferente?
{: faq}

En casos limitados un servidor virtual puede necesitar migrarse a un host diferente. Si es necesaria una migración, el servidor virtual se cerrará, se migrará y, luego, se reiniciará. Un servidor virtual puede ser migrado en los casos siguientes:

* Un hipervisor debe ser actualizado, un host está fuera de servicio, o un host no puede asumir nuevas instancias. Si un host está marcado para cualquiera de estos cambios, cuando uno de sus servidores virtuales rearranca desde la consola de {{site.data.keyword.cloud_notm}}, el rearranque desencadena automáticamente la migración del servidor virtual a un host distinto.
* Mantenimiento de infraestructura. Puede recibir un correo electrónico que indica que es necesario el mantenimiento en un sistema que alberga el servidor virtual. Su servidor virtual puede necesitar migrarse como parte del mantenimiento de infraestructura.
* Una actualización a una instancia existente. Para un rendimiento coherente, si actualiza una instancia podría ser migrada a un host diferente para asegurarse de que recibe la CPU y la memoria dedicadas adecuadas.
* Un host dedicado falla. Las instancias dedicadas se migran a otro host vacío sin utilizar nada de la capacidad existente que pudiera tener.

Durante una ventana de mantenimiento, puede ver una opción **Migrar host** visualizada en el menú **Acciones** del dispositivo en la consola de {{site.data.keyword.cloud_notm}}. **Migrar host** le permite migrar el servidor virtual a un nuevo host que le convenga durante un periodo de mantenimiento especificado. Si no inicia la migración durante el período de mantenimiento, el servidor virtual se migrará automáticamente para completar el mantenimiento necesario. La opción **Migrar host** no persistirá y sólo estará disponible durante los periodos de mantenimiento que se comunican a través de notificaciones de mantenimiento.

También puede ver la opción **Migrar host** si uno de los servidores virtuales es necesario que tenga un cierto nivel de hipervisor que no está disponible en el host actual.

## ¿Qué ocurre con mis datos cuando se suprime mi almacenamiento portátil?
{: faq}

Cuando se suprime el almacenamiento, se eliminan todos los punteros a los datos en dicho volumen, por lo que los datos serán inaccesibles. Si el almacenamiento físico se vuelve a suministrar a otra cuenta, se asignará un nuevo conjunto de punteros. La nueva cuenta no tiene ningún modo de acceder a los datos que pudieran haberse guardado en el almacenamiento físico. El nuevo conjunto de punteros muestra todo 0. Cuando se escriben nuevos datos en el volumen/LUN, se sobrescriben los datos inaccesibles que aún existan.

## ¿Puedo utilizar una suscripción a Hat Cloud Access para crear un servidor virtual?
{: faq}

Sí. Al importar una imagen, puede especificar que proporcionará la licencia de sistema operativo. Para obtener más información, consulte [Utilizar Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription#using-your-own-os-license-or-subscription). A continuación, puede solicitar un servidor virtual de la plantilla de imagen y utilizar su suscripción existente de [Red Hat Cloud Access ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window}.

## ¿Qué diferencia hay entre un servidor virtual y un servidor privado virtual (VPS)?
{: faq}

Un servidor virtual es parecido a un servidor privado virtual (VPS) o servidor dedicado virtual (VDS) con los que quizás ya está familiarizado. Estos entornos de "servidor virtual" permite suministrar distintos entornos de forma privada y segura en un solo nodo de hardware, pero VDS y VPS tienen una capacidad más limitada. Las opciones de VPS y VDS generalmente quedan reducidas a una arquitectura de un solo servidor. Los únicos recursos que se pueden añadir o dividir entre cada servidor virtual en un VDS o un VPS son los recursos que están instalados físicamente en dicho servidor individual.

Los servidores virtuales se suministran en una arquitectura de nube de varios servidores que sondea todos los recursos de hardware disponibles para que los utilicen las instancias individuales. Los servidores virtuales pueden hacer uso de una plataforma compartida de almacenamiento primario basado en SAN de alta capacidad o un almacenamiento de disco local de alto rendimiento. Puesto que cada instancia forma parte del entorno de nube mayor, la comunicación entre todos los servidores virtuales es instantánea.

## ¿Por qué recibo un error de capacidad al suministrar un servidor virtual?
{: faq}

Cuando suministra un servidor virtual, es posible que reciba un mensaje de error diciendo que la capacidad es insuficiente para completar la solicitud. Cuando el suministro falla, todas las instancias de servidor virtual de dicha solicitud particular fallan. Se produce un error de capacidad cuando no hay suficientes recursos disponibles en el direccionador o centro de datos para completar la solicitud de servicio. Existen una serie de motivos por las cuales podría recibir este error. La disponibilidad de recursos cambia con frecuencia, por lo que puede esperar y volver a intentarlo más tarde. [Consideraciones sobre recursos para instancias de servidor virtual](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).

## ¿Cómo inicio sesión en mi servidor?
{: faq}

Inicie sesión en la consola y acceda al menú **Dispositivos**. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices). En la **Lista de dispositivos**, seleccione la instancia. Puede ver y gestionar los nombres de usuario y contraseñas a utilizar para iniciar sesión en el dispositivo. Para obtener más información, consulte [Visualización y gestión de nombres de usuario y contraseñas](https://test.cloud.ibm.com/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device). 

## ¿Cómo utilizo VPN para acceder a la red privada de IBM Cloud?
{: faq}

Puede iniciar sesión en la VPN a través de [la interfaz web](https://www.softlayer.com/VPN-Access){: external} o utilizar un
[cliente de VPN autónomo](/docs/infrastructure/iaas-vpn?topic=VPN-standalone-vpn-clients) para Linux, macOS o Windows. Para obtener más información sobre qué hacer una vez que esté conectado a la VPN, consulte
[Utilizar la VPN SSL](/docs/infrastructure/iaas-vpn?topic=VPN-use-ssl-vpn).

## ¿Cómo rearranco mi servidor virtual?
{: faq}

Los rearranques del dispositivo pueden llevarse a cabo desde la **Lista de dispositivos** o desde la vista de instantánea de una instancia individual. Acceda a la instancia de servidor virtual en la **Lista de dispositivos** de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices). Seleccione **Acciones** para el dispositivo que desee gestionar y seleccione **Rearrancar**.

## ¿Cómo utilizo Rescue Kernel?
{: faq}

El arranque en Rescue Kernel es útil si experimenta un problema con el servidor. Para iniciar Rescue Kernel, seleccione el nombre de dispositivo desde la **Lista de dispositivos** de la consola. En el menú **Acciones**, seleccione **Modalidad de rescate** o seleccione **Arrancar desde imagen** para una instancia de Windows. Para obtener más información, consulte
[Inicio de Rescue Kernel](/docs/vsi?topic=virtual-servers-launching-rescue).

## ¿Dónde encuentro el estado de la red?
{: faq}

Puede acceder a la página **Estado** directamente en
[{{site.data.keyword.cloud_notm}} - Estado](https://cloud.ibm.com/status){: external} para ver el estado actual de los recursos de todas las ubicaciones de
{{site.data.keyword.cloud_notm}}. Puede filtrar la lista seleccionando componentes y ubicaciones específicos (por ejemplo, puede seleccionar servidores virtuales y ver la conectividad de red).

## ¿Cómo solicito un informe de conformidad?
{: faq}

Para obtener información sobre cómo visualizar o solicitar información de conformidad, incluyendo informes SOC, consulte
[¿Cómo sé que mis datos son seguros?](/docs/overview?topic=overview-security)

