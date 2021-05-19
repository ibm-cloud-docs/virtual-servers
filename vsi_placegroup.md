---

copyright:
  years: 2018, 2021
lastupdated: "2021-05-19"

keywords: placement groups, high availability, spread rule

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Placement groups
{: #placement-groups}

High availability (HA) is an important aspect of any cloud deployment. Whether it’s the website for your e-commerce business or a production database that is used by your company’s key application—it needs to stay up. To this end, building out resilient infrastructure is something our IT architect clients work hard to implement in the pursuit of ever-higher percentages of “uptime.” Although uptime is closely monitored within IT organizations, it can fall under key levels or take on substantial outages, which are huge problems for the entire business.

Building in redundancy at each level of your infrastructure to eliminate any Single Point of Failure (SPOF) is key to performing well on this metric. For workloads that are running on virtual servers, you can implement failover solutions with multiple virtual servers to automatically cover for each other during a failure.

However, unless your public virtual servers are provisioned into different data centers, your virtual servers can't determine where they are placed in relation to each other. This unknown can be problematic if you’re 1) building for HA and 2) your virtual servers are on the same physical host, leaving them vulnerable to an outage on a single piece of hardware. While that placement is unlikely, IT managers can’t have the possibility of a SPOF for critical applications. Building across data centers is an option, but this option can introduce some network challenges that require extra appliances or increase latency, especially in regions with only a single data center.

The design of placement groups for {{site.data.keyword.cloud}} virtual servers solves this issue. Placement groups give you a measure of control over the host on which a new public virtual server is placed. With this release, a “spread” rule is implemented. Meaning that virtual servers within a placement group are all spread onto different hosts. You can build a high availability application within a data center and know that your virtual servers are isolated from each other.

Placement groups with the “spread” rule are available to create in select {{site.data.keyword.cloud_notm}} data centers. After a "spread" rule is created, you can provision a virtual server into that group and guarantee that won't be on the same host as any of your other virtual servers. The best part? There’s absolutely no charge for using this feature.

You can create your placement group, then assign up to five new virtual server instances. With the "spread" rule, each of your virtual servers are provisioned on different physical hosts.

## Next steps
{: #next-steps-placement-groups}

To create and manage placement groups, see [Managing placement groups](/docs/virtual-servers?topic=virtual-servers-vsi_managing_placegroup#vsi_managing_placegroup).
