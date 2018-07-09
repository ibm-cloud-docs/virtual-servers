---
copyright:
  years: 2014, 2018
lastupdated: "2018-02-20"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Scripts de suministro

Un script de suministro es un script que puede descargarse o descargarse en un dispositivo, o descargarse y ejecutarse en el dispositivo, durante el proceso de suministro. Para las cuentas existentes, los scripts de suministro se gestionan dentro del {{site.data.keyword.slportal_full}}. Durante el proceso de pedido, puede especificar manualmente scripts para las nuevas cuentas o scripts de los que todavía no se ha realizado un seguimiento.

Durante el proceso de suministro, los scripts que están asociados con un URL HTTP se descargan al dispositivo. Después del suministro, un administrador debe ejecutar el script manualmente en el dispositivo. Los scripts que están asociados con un URL HTTPS se descargan y se ejecutan automáticamente. Actualmente, los scripts de suministro están disponibles en los sistemas operativos estándar de Linux (Cent, RHEL, Fedora, Debian o Ubuntu), Windows y FreeBSD. Otros sistemas como Vyatta, Netscaler, XenServer y VMware no están soportados. El script de suministro puede ser cualquier tipo de archivo que ejecute el sistema operativo, incluidos los archivos binarios combinados o cualquier idioma soportado por el sistema operativo.

Para obtener más información, consulte [Gestión de un script de suministro](add-provisioning-script.html).
