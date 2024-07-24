---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-24"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why is my server stuck in the provisioning process?
{: #vsi-troubleshoot-vs-stuck-provisioning}
{: troubleshoot}
{: support}

Your server is taking a long time to provision. Keep in mind that it can take up to 24 hours to complete the provision process.
{: tsSymptoms}

If your server is taking too long to provision, one of the following issues might be the reason.
{: tsCauses}

* Vyatta is blocking the connection. Make sure that Vyatta allows connections.
* If security groups are applied, a security group might be blocking passwords from populating.
* Outages or maintenance operations.

To attempt to resolve the issue, try the following troubleshooting tasks:
{: tsResolve}

* Verify that Vyatta allows connections.
* Don't add a security group until provisioning completes. For more information about security groups, see [Getting started with IBM security groups](/docs/security-groups?topic=security-groups-getting-started).
* Check your notifications for outage or maintenance announcements.

If you need more help, [contact support](/docs/get-support?topic=get-support-get-supportfaq#contactsupport).
