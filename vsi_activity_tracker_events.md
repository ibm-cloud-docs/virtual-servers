---

copyright:
  years: 2016, 2021
lastupdated: "2021-05-19"

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

As a security officer, auditor, or manager, you can use the {{site.data.keyword.cloudaccesstrailfull}} service to track how users and applications interact with virtual server instances in {{site.data.keyword.Bluemix}}. The account owner and users that are linked with the account can trigger virtual server events that are logged in {{site.data.keyword.cloudaccesstrailshort}}.
{: shortdesc}

The {{site.data.keyword.cloudaccesstrailshort}} service records user-initiated activities that change the state of a service in
{{site.data.keyword.Bluemix_notm}}. For more information, see [Auditing events for IAM](/docs/activity-tracker?topic=activity-tracker-at_events_iam).

To get started with monitoring your user's actions, see [Getting started with {{site.data.keyword.at_full_notm}}](/docs/activity-tracker?topic=activity-tracker-getting-started).

An initiator can be a user, a service, or an application. For a user to generate events, the user must have access to **Infrastructure** resources in {{site.data.keyword.Bluemix}} console.
{: tip}

## Virtual server instance events
{: #vsi}

You can audit a virtual server instance through its lifecycle by using the {{site.data.keyword.cloudaccesstrailshort}} service.

The following table lists the actions that generate an event:

| Action | Description |
|----------|---------|
| `audit-log.vsi.provision`             | An event is generated when an initiator provisions an instance.  |
| `audit-log.vsi-port.disable`          | An event is generated when an initiator disables a port in an instance. |
| `audit-log.vsi-port.enable`           | An event is generated when an initiator enables a port in an instance. |
| `audit-log.vsi-port-speed.update`     | An event is generated when an initiator updates the port speed in an instance. |
| `audit-log.vsi-image-template.create` | An event is generated when an initiator creates an image template for an instance.  |
| `audit-log.vsi.power-off`             | An event is generated when an initiator powers off an instance.  |
| `audit-log.vsi.soft-power-off`        | An event is generated when an initiator does a soft power off on an instance. |
| `audit-log.vsi.force-power-off`       | An event is generated when an initiator does a force power off on an instance. |
| `audit-log.vsi.reboot`                | An event is generated when an initiator reboots an instance. |
| `audit-log.vsi.soft-reboot`           | An event is generated when an initiator does a soft reboot on an instance. |
| `audit-log.vsi.hard-reboot`           | An event is generated when an initiator does a hard reboot on an instance. |
| `audit-log.vsi.power-on`              | An event is generated when an initiator powers on an instance. |
| `audit-log.vsi.rename`                | An event is generated when an initiator renames an instance. |
| `audit-log.vsi.rescue`                | An event is generated when an initiator rescues an instance. |
| `audit-log.vsi-security-group.add`    | An event is generated when an initiator adds a security group to an instance. |
| `audit-log.vsi-security-group.remove` | An event is generated when an initiator removes a security group from an instance. |
| `audit-log.vsi.reload`                | An event is generated when an initiator performs an operating system (OS) reload for an instance. |
| `audit-log.vsi.boot`                  | An event is generated when an initiator boots an instance from an image. |
| `audit-log.vsi.reclaim`               | An event is generated when an initiator cancels an instance. |
| `audit-log.vsi.pause`                 | An event is generated when an initiator pauses an instance. |
{: caption="Table 1. Virtual server instance actions" caption-side="top"}

## Viewing events
{: #ui}

The {{site.data.keyword.cloudaccesstrailshort}} events are available in the {{site.data.keyword.cloudaccesstrailshort}} **account domain** that
is available in the {{site.data.keyword.Bluemix_notm}} region where the events are generated. For more information, see [Viewing account
events](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-manage_events).

{{site.data.keyword.cloudaccesstrailshort}} events are automatically forwarded to the {{site.data.keyword.cloudaccesstrailshort}} service
in the same region where the action happens.
