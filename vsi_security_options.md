---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Firewalls
{: #virtual-server-security-options}

With {{site.data.keyword.BluVirtServers}}, you have several firewall options that provide an essential security layer.  The firewall options are provisioned on demand, without service interruptions. The firewall services prevent unwanted traffic from hitting your servers, reducing the likelihood of an attack and allowing your server resources to be dedicated for their intended use.
{:shortdesc}

Firewalls are available as an add-on feature for all servers on the Infrastructure public network.

As part of the ordering process, you can select device-specific hardware or a software firewall to provide protection. Alternatively, you can deploy dedicated firewall appliances to the environment and deploy the virtual server to a protected VLAN.  

A virtual server cannot be protected by two firewall appliances on the same interface. 
{:note}

For more information, see the following security topic collections.

* [Hardware Firewalls (Shared)](/docs/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Hardware Firewalls (Dedicated)](/docs/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)
