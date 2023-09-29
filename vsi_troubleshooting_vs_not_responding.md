---

copyright:
  years: 2017, 2023
lastupdated: "2023-09-28"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I access my virtual server
{: #vsi-troubleshoot-vs-device-not-responding}
{: troubleshoot}
{: support}

You are unable to access your virtual server and the server is not pinging.
{: tsSymptoms}

The ping traffice might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, or Fortigate).
{: tsCauses}

To attempt to resolve the issue, try the following troubleshooting tasks:
{: tsResolve}

* Try to access the server through the KVM console. For more information, see [Accessing the KVM console for virtual servers](docs/virtual-servers?topic=virtual-servers-access-kvm-console).
* If you can't access the server through the KVM console, then the ping traffic might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate). Ask your administrator to check the firewall rules. For help with setting up firewall rules, contact support.
* If you're using security group, you need to allow ICMP traffic. For more information, see [Creating security groups and rules](/docs/security-groups?topic=security-groups-creating-security-groups).
