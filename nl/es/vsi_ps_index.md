---

copyright:
  years: 2014, 2018
lastupdated: "2018-10-18"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# Scripts de suministro
{: #provisioning-scripts}

Un script de suministro es un script que puede descargarse o descargarse en un dispositivo, o descargarse y ejecutarse en el dispositivo, durante el proceso de suministro. Para las cuentas existentes, los scripts de suministro se gestionan dentro del {{site.data.keyword.slportal_full}}. Durante el proceso de pedido, puede especificar manualmente scripts para las nuevas cuentas o scripts de los que todavía no se ha realizado un seguimiento.

De forma alternativa, puede utilizar una imagen cloud-init habilitada y proporcionar datos de usuario para realizar las tareas de configuración o ejecutar scripts automáticamente. Para obtener más información, consulte [Suministro con una imagen habilitada con cloud-init](/docs/infrastructure/image-templates?topic=image-templates-provisioning-with-a-cloud-init-enabled-image#provisioning-with-a-cloud-init-enabled-image).
{: tip}

Durante el proceso de suministro, los scripts que están asociados con un URL HTTP se descargan al dispositivo. Después del suministro, un administrador debe ejecutar el script manualmente en el dispositivo. Los scripts que están asociados con un URL HTTPS se descargan y se ejecutan automáticamente. Actualmente, los scripts de suministro están disponibles en los sistemas operativos estándar de Linux (Cent, RHEL, Fedora, Debian o Ubuntu), Windows y FreeBSD. Otros sistemas como Vyatta, Netscaler, XenServer y VMware no están soportados. El script de suministro puede ser cualquier tipo de archivo que ejecute el sistema operativo, incluidos los archivos binarios combinados o cualquier idioma soportado por el sistema operativo.

Para obtener más información, consulte [Gestión de un script de suministro](/docs/vsi?topic=virtual-servers-managing-a-provisioning-script).
