---

copyright:
  years: 2017, 2023
lastupdated: "2023-09-28"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I connect to a server through the public IP?
{: #vsi-troubleshoot-vs-cannot-connect-public-ip}
{: troubleshoot}
{: support}

You can't connect to the virtual server using a public IP.
{: tsSymptoms}

Public traffic might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate).
{: tsCauses}

To resolve this issue, check the following:
{: tsResolve}

If the firewall isn't an issue, check whether the public gateway IP is configured for the public network card and try pinging the public gateway. For more help, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).
