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


# Activity Tracker events
{: #at_events}

As a security officer, auditor, or manager, you can use the {{site.data.keyword.cloudaccesstrailfull}} service to track how users and
applications interact with virtual server instances (VSI) in {{site.data.keyword.Bluemix}}. The account owner and users that are linked
with the account can trigger virtual server events that are logged in {{site.data.keyword.cloudaccesstrailshort}}.
{:shortdesc}

The {{site.data.keyword.cloudaccesstrailshort}} service records user-initiated activities that change the state of a service in
{{site.data.keyword.Bluemix_notm}}. For more information, see
[About {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov ).

To get started monitoring your user's actions, see
[{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started-with-cla#getting-started-with-cla).

An initiator can be a user, a service, or an application. For a user to generate events, the user must have access to **Infrastructure** resources in {{site.data.keyword.Bluemix}} console.
{: tip}

<!--## Login events-->
<!--{: #login}-->

<!--The following table lists the action that generates a login event:-->

<!--| Action | Description |-->
<!--|----------|---------|-->
<!--| `audit-log.user.login`  | An event is generated when an initiator logs in to {{site.data.keyword.Bluemix}} through the {{site.data.keyword.Bluemix}} UI or the {{site.data.keyword.slportal}}. |-->
<!--{: caption="Table 1. Login action" caption-side="top"}-->


## Virtual server instance events
{: #vsi}

You can audit a virtual server instance (VSI) through its life cycle by using the {{site.data.keyword.cloudaccesstrailshort}} service.

The following table lists the actions that generate an event:

| Action | Description |
|----------|---------|
| `audit-log.vsi.provision`             | An event is generated when an initiator provisions a VSI.  |
| `audit-log.vsi-port.disable`          | An event is generated when an initiator disables a port in a VSI. |
| `audit-log.vsi-port.enable`           | An event is generated when an initiator enables a port in a VSI. |
| `audit-log.vsi-port-speed.update`     | An event is generated when an initiator updates the port speed in a VSI. |
| `audit-log.vsi-image-template.create` | An event is generated when an initiator creates an image template for a VSI.  |
| `audit-log.vsi.power-off`             | An event is generated when an initiator powers off a VSI.  |
| `audit-log.vsi.soft-power-off`        | An event is generated when an initiator does a soft power off on a VSI. |
| `audit-log.vsi.force-power-off`       | An event is generated when an initiator does a force power off on a VSI. |
| `audit-log.vsi.reboot`                | An event is generated when an initiator reboots a VSI. |
| `audit-log.vsi.soft-reboot`           | An event is generated when an initiator does a soft reboot on a VSI. |
| `audit-log.vsi.hard-reboot`           | An event is generated when an initiator does a hard reboot on a VSI. |
| `audit-log.vsi.power-on`              | An event is generated when an initiator powers on a VSI. |
| `audit-log.vsi.rename`                | An event is generated when an initiator renames a VSI. |
| `audit-log.vsi.rescue`                | An event is generated when an initiator rescues a VSI. |
| `audit-log.vsi-security-group.add`    | An event is generated when an initiator adds a security group to a VSI. |
| `audit-log.vsi-security-group.remove` | An event is generated when an initiator removes a security group from a VSI. |
| `audit-log.vsi.reload`                | An event is generated when an initiator performs an operating system (OS) reload for a VSI. |
| `audit-log.vsi.boot`                  | An event is generated when an initiator boots a VSI from an image. |
| `audit-log.vsi.reclaim`               | An event is generated when an initiator cancels a VSI. |
| `audit-log.vsi.pause`                 | An event is generated when an initiator pauses a VSI. |
{: caption="Table 2. VSI actions" caption-side="top"}



## Viewing events
{: #ui}

The {{site.data.keyword.cloudaccesstrailshort}} events are available in the {{site.data.keyword.cloudaccesstrailshort}} **account domain** that
is available in the {{site.data.keyword.Bluemix_notm}} region where the events are generated. For more information, see [Viewing account
events](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events).

{{site.data.keyword.cloudaccesstrailshort}} events are automatically forwarded to the {{site.data.keyword.cloudaccesstrailshort}} service
in the same region where the action happens.
