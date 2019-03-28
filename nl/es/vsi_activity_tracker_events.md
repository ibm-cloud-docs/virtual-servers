---

copyright:
  years: 2016, 2018
lastupdated: "2018-11-06"

subcollection: virtual-servers

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Sucesos de Activity Tracker
{: #at_events}

Como responsable de seguridad, auditor o gestor, puede utilizar el servicio {{site.data.keyword.cloudaccesstrailfull}} para realizar un seguimiento del modo en que los usuarios y las aplicaciones interactúan con instancias
de servidor virtual (VSI) en {{site.data.keyword.Bluemix}}. El propietario de la cuenta y los usuarios vinculados a la cuenta pueden activar sucesos de servidor virtual que se registran en {{site.data.keyword.cloudaccesstrailshort}}.
{:shortdesc}

El servicio {{site.data.keyword.cloudaccesstrailshort}} registra las actividades iniciadas por el usuario que cambian el estado de un servicio en {{site.data.keyword.Bluemix_notm}}. Para obtener más información, consulte [Acerca de {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov ).

Para empezar a supervisar las acciones del usuario, consulte [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started-with-cla#getting-started-with-cla).

Un iniciador puede ser un usuario, un servicio o una aplicación. Para que un usuario genere sucesos, el usuario debe tener acceso a los recursos de **Infraestructura** en la consola de {{site.data.keyword.Bluemix}}.
{: tip}

## Sucesos de instancia de servidor virtual
{: #vsi}

Puede auditar una instancia de servidor virtual (VSI) durante su ciclo de vida mediante el servicio {{site.data.keyword.cloudaccesstrailshort}}.

La tabla siguiente contiene las acciones que generan un suceso:

| Acción | Descripción |
|----------|---------|
| `audit-log.vsi.provision`             | Se genera un suceso cuando un iniciador suministra una VSI.  |
| `audit-log.vsi-port.disable`          | Se genera un suceso cuando un iniciador inhabilita un puerto en una VSI. |
| `audit-log.vsi-port.enable`           | Se genera un suceso cuando un iniciador habilita un puerto en una VSI. |
| `audit-log.vsi-port-speed.update`     | Se genera un suceso cuando un iniciador actualiza la velocidad de puerto en una VSI. |
| `audit-log.vsi-image-template.create` | Se genera un suceso cuando un iniciador crea una plantilla de imagen para una VSI.  |
| `audit-log.vsi.power-off`             | Se genera un suceso cuando un iniciador apaga una VSI.  |
| `audit-log.vsi.soft-power-off`        | Se genera un suceso cuando un iniciador realiza un apagado (soft power off) de una VSI. |
| `audit-log.vsi.force-power-off`       | Se genera un suceso cuando un iniciador realiza un apagado forzado de una VSI. |
| `audit-log.vsi.reboot`                | Se genera un suceso cuando un iniciador reinicia una VSI. |
| `audit-log.vsi.soft-reboot`           | Se genera un suceso cuando un iniciador realiza un reinicio (soft reboot) de una VSI. |
| `audit-log.vsi.hard-reboot`           | Se genera un suceso cuando un iniciador reinicia (hard reboot) una VSI. |
| `audit-log.vsi.power-on`              | Se genera un suceso cuando un iniciador enciende una VSI. |
| `audit-log.vsi.rename`                | Se genera un suceso cuando un iniciador cambia el nombre de una VSI. |
| `audit-log.vsi.rescue`                | Se genera un suceso cuando un iniciador rescata una VSI. |
| `audit-log.vsi-security-group.add`    | Se genera un suceso cuando un iniciador añade un grupo de seguridad a una VSI. |
| `audit-log.vsi-security-group.remove` | Se genera un suceso cuando un iniciador elimina un grupo de seguridad de una VSI. |
| `audit-log.vsi.reload`                | Se genera un suceso cuando un iniciador realiza una recarga de sistema operativo (SO) para una VSI. |
| `audit-log.vsi.boot`                  | Se genera un suceso cuando un iniciador arranca una VSI desde una imagen. |
| `audit-log.vsi.reclaim`               | Se genera un suceso cuando un iniciador cancela una VSI. |
| `audit-log.vsi.pause`                 | Se genera un suceso cuando un iniciador pone en pausa una VSI. |
{: caption="Tabla 2. Acciones de VSI" caption-side="top"}



## Visualización de sucesos
{: #ui}

Los sucesos de {{site.data.keyword.cloudaccesstrailshort}} están disponibles en el **dominio de la cuenta** de {{site.data.keyword.cloudaccesstrailshort}} que está disponible en la región de {{site.data.keyword.Bluemix_notm}} en la que se generan los sucesos. Para obtener más información, consulte [Visualización de sucesos de cuenta](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events).

Los sucesos de {{site.data.keyword.cloudaccesstrailshort}} se reenvían automáticamente al servicio {{site.data.keyword.cloudaccesstrailshort}} en la misma región en la que se produce la acción.
