---

copyright:
  years: 2017, 2025
lastupdated: "2025-04-09"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Dedicated host pricing for Classic
{: #dedicated-virtual-server-pricing}

Pricing for Classic dedicated hosts is priced at an hourly and monthly rates.
{: shortdesc}

Classic dedicated host pricing is inclusive of all vCPU, RAM, local storage, and uplink port speed components as instances are provisioned onto dedicated hosts.

With dedicated hosts, extra local storage disks are available on the first, second, third, fourth, and fifth disks. Extra capacity of up to 400 GB on each secondary disk is also available.

You can provision hourly instances on hourly and monthly hosts. Monthly instances can be provisioned on only monthly hosts.

The following table is an example of a Classic dedicated host configuration.

| Host configuration | vCPU	| RAM (GB) | Local storage (TB SSD) |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |  56 	|   242    |        	1.2	          |
| 56x484x1.2         |  56  |   484    |          1.2           |
{: caption="Dedicated host configurations" caption-side="top"}

Pricing varies by region.
{: note}

SAN (network attached), premium operating systems, and add-ons are charged hourly or monthly, by the instance, depending on the instance provisioned on the dedicated host. Pricing for these components is consistent with the existing Classic offering on public instances and dedicated instances.

For example, a dedicated instance that is provisioned on a dedicated host with the following configuration isn't charged by the instance. vCPU, RAM, local storage, and uplink port speeds are included in dedicated host charges.

* 8 vCPU
* 16 GB RAM
* 100 GB Local SSD first disk
* 400 GB Local SSD second disk
* 400 GB Local SSD third disk
* 1 Gbps public and private network uplinks (dedicated host)
