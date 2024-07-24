---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-24"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I view the password for a recently provisioned virtual server?
{: #vsi-troubleshoot-view-password}
{: troubleshoot}
{: support}

You have the correct permissions but you can't see the password for a recently provisioned virtual server.
{: tsSymptoms}

This problem can occur if a firewall prevents the provisioning framework from updating the password value.
{: tsCauses}

To attempt to resolve the issue, try the following troubleshooting tasks:
{: tsResolve}

* Update the firewall to allow the IBM Cloud service IP ranges as described in the firewall [documentation](/docs/vsrx?topic=vsrx-ibm-cloud-ip-ranges). These ranges allow for provisioning, monitoring, and management. Restart the server so the provisioning network to populate the password in the portal.
* Bypass the VLAN of the server from the firewall. Then, restart the server to allow the provisioning network to populate the password in the portal and then route the VLAN back in the firewall.
