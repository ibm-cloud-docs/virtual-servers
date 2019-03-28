---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Servicios de copia de seguridad
{: #back-up-services}

## IBM Cloud Backup

{{site.data.keyword.backup_full}} es un sistema de copia de seguridad automático basado en agente que se gestiona mediante el programa de utilidad de gestión basado en navegador {{site.data.keyword.backup_notm}} WebCC y que proporciona a los usuarios un método para realizar una copia de seguridad de los datos entre servidores en uno o varios centros de datos de la red de {{site.data.keyword.BluSoftlayer}}.  Los administradores pueden establecer que las copias de seguridad sigan una planificación horaria, diaria, semanal o personalizada que abarque sistemas completos, directorios específicos o incluso archivos individuales.  Los plugins adicionales permiten la compatibilidad con software como Microsoft Exchange y Microsoft SQL, así como con otros tipos de software de otros proveedores, y permite a los usuarios realizar una restauración de la configuración nativa si es necesario.

Para obtener más información sobre los servicios de {{site.data.keyword.backup_notm}}, consulte [Iniciación a los servicios de {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-gettingstarted#gettingstarted).

## R1Soft CDP

Continuous Data Protection (CDP) es un software de copia de seguridad de alto rendimiento creado por R1Soft que permite realizar copias de seguridad de dispositivos tanto físicos como virtuales. Idera CDP consta de tres componentes principales: el servidor CDP, el agente y los plugins de base de datos, que se pueden adquirir por separado desde los primeros dos componentes.  Dado que R1Soft CDP es una solución de copia de seguridad de terceros, las interacciones con CDP tienen lugar totalmente fuera de las interfaces de propiedad de {{site.data.keyword.Bluemix_short}}; sin embargo, las contraseñas de R1Soft CDP pueden ser rastreadas y almacenadas en {{site.data.keyword.slportal}}.  Las demás interacciones con R1Soft CDP están documentadas en el sitio web de R1Soft.

Para obtener más información sobre los servicios de copia de seguridad de R1Soft CDP, consulte la [documentación de R1Soft ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://wiki.r1soft.com/display/ServerBackupManager/Home){: new_window}.
