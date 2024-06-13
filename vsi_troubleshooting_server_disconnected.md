---

copyright:
  years: 2017, 2024
lastupdated: "2023-09-28"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why does the portal show that my server is disconnected even though it's running?
{: #vsi-troubleshoot-vs-portal-shows-server-disconnected-but-running}
{: troubleshoot}
{: support}

Your portal shows the server is disconnected, but your server is still running.
{: tsSymptoms}

This issue can be caused by one of the following reasons:
{: tsCauses}

* Your firewall or gateway rules are blocking ping.
* A security group is blocking ping.

To attempt to resolve the issue, try the following troubleshooting tasks:
{: tsResolve}

* Firewall or gateway rules are blocking the ping

If your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate) blocks ping traffic, then the status of your servers shows "disconnected" in the portal. Check that your firewall rules allow ping traffic from {{site.data.keyword.cloud}} IP ranges. For more information about IP ranges, see [{{site.data.keyword.cloud}} IP ranges](/docs/cloud-infrastructure?topic=cloud-infrastructure-ibm-cloud-ip-ranges).

* Security group is blocking the ping

If you're using a security group, make sure that you allow ping traffic from the {{site.data.keyword.cloud}} IP ranges. For more information, see [Creating security groups and rules](/docs/security-groups?topic=security-groups-creating-security-groups).
