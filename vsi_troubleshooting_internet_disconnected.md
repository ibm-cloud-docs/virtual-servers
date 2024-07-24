---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-24"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why is the internet disconnected?
{: #vsi-troubleshoot-vs-internet-disconnected}
{: troubleshoot}
{: support}

Your internet is disconnected.
{: tsSymptoms}

This issue can be caused by one of the following reasons:
{: tsCauses}

* Internet is blocked by a firewall or gateway
* Public gateway IP configuration
* No ping from DNS servers

To attempt to resolve the issue, try the following troubleshooting tasks:
{: tsResolve}

* The internet is blocked by a firewall or gateway.

   If you can't access the internet, your internet access might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate).

* Public gateway IP isn't configured for the network card.

   If firewall is not an issue, check whether the public gateway IP is configured for the public network card and try pinging the public gateway. For more help, contact [support](/docs/get-support?topic=get-support-get-supportfaq#contactsupport).

* No ping from DNS servers.

   Check whether you can ping IBM DNS servers (_10.0.80.11_, _10.0.80.12_), if you configured DNS servers for the public network card.

   If you have Linux servers, add the following entries in the _/etc/resolv.conf_ file:

   `nameserver 10.0.80.11`

   `nameserver 10.0.80.12`
