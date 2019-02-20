---



copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# About public virtual servers
The public {{site.data.keyword.BluVirtServers}} offerings are IBM-managed, multi-tenant virtual server deployments. They give you rapid scalability and higher-cost effectiveness with pre-defined sizes that meet all business requirements to get you up and running quickly.  
{:shortdesc}

Public virtual servers have many advantages, including the following:

* **Global availability**

    The public virtual server offering is available in data centers across the globe.

* **Configuration choices, rapid deployment, and scalability**

    The public virtual server offering gives you small or large virtual server options to meet various workload requirements.

Network traffic for public virtual servers, which encompasses VSI SAN and other network-attached storage, has no guarantee. If network traffic of a virtual server instance begins to have a significant, negative impact on other virtual servers, that instance may be restarted on a new host, or in extreme cases, completely disabled. This negative impact is often observed as traffic levels approach 20,000 to 30,000 packets per second (PPS).  For guaranteed networking, use of the Dedicated Virtual Server offering is recommended. For more information, see the single-tenant environment, [Dedicated virtual server](/docs/vsi/vsi_dedicated.html) offering.

Public instances reside on a hypervisor that is shared with other clients; however, the processors and memory are dedicated to the virtual server, making server performance reliable.

The following public virtual servers are available.

| Public virtual servers  | Description     |                                                                                          | ----------------------- | --------------- |
| [Balanced](/docs/vsi/vsi_public_balanced.html) | Best for common cloud workloads that require a balance of performance and scalability. Uses network-attached storage.|
| [Balanced local storage](/docs/vsi/vsi_public_balanced_local.html) | Best for large database clusters that require high, low latency I/O performance.|
| [Compute](/docs/vsi/vsi_public_compute.html) | Best for moderate to high web traffic workloads.|
| [Memory](/docs/vsi/vsi_public_memory.html)  | Best for memory caching and real-time analytics workloads. |
| [GPU](/docs/vsi/vsi_public_gpu.html)  | Best for high performance workloads. |
{: caption="Table 1. Supported public virtual servers" caption-side="top"}

## Next Steps

After you review and decide upon your virtual server flavor, it's time to provision your public virtual server. To get started, review the following information:
1. [Provisioning selections](/docs/vsi/vsi_public_selections.html)
2. [Provisioning public instances](/docs/vsi/vsi_provision_public.html)

After you review and decide upon your virtual server profile, it's time to provision your public virtual server. To get started, review the following information: 
1. [Provisioning selections](/docs/vsi/vsi_public_selections.html)
2. [Provisioning public instances](/docs/vsi/vsi_provision_public.html)

