---

copyright:
  years: 2017, 2020
lastupdated: "2020-03-20"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Dedicated host pricing
{: #dedicated-virtual-server-pricing}

Pricing for dedicated hosts is offered in an hourly and monthly model.
{:shortdesc}

Dedicated host pricing is inclusive of all vCPU, RAM, local storage, and uplink port speed components as instances are provisioned onto dedicated hosts. For more information about pricing, see the [Virtual servers provisioning calculator ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud/virtual-servers-cloud/pricing-configuration/){: new_window}.

With dedicated hosts, additional local storage disks are available on first, second, third, fourth, and fifth disks. There is also additional capacity up to 400 GB on each secondary disk.

Hourly instances can be provisioned on hourly and monthly hosts. Monthly instances can only be provisioned on monthly hosts.

| Host configuration | vCPU	| RAM (GB) | Local storage (TB SSD) |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |  56 	|   242    |        	1.2	          |
| 56x484x1.2         |  56  |   484    |          1.2           |
{: caption="Table 1. Dedicated host configurations" caption-side="top"}

Pricing varies by region.
{:note}

SAN (network attached), premium OSs, and SW add-ons are charged hourly or monthly, by the instance, depending on the instance provisioned on the dedicated host. Pricing for these components is consistent with the existing offering on public instances and dedicated instances. 

For example, a dedicated instance provisioned on a dedicated host with the following configuration isn't charged by the instance. vCPU, RAM, local storage, and uplink port speeds are included in dedicated host charges. 

* 8 vCPU
* 16 GB RAM
* 100 GB Local SSD first disk
* 400 GB Local SSD second disk
* 400 GB Local SSD third disk
* 1 Gbps public and private network uplinks (dedicated host) 

