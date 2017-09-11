---



copyright:
  years: 2017
lastupdated: "2017-09-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Public virtual servers
The public {{site.data.keyword.BluVirtServers}} offerings are IBM-managed, multi-tenant virtual server deployments. They give you rapid scalability and higher-cost effectiveness with pre-defined sizes that meet all business requirements to get you up and running quickly.  Public virtual servers have many advantages, including the following:

* **Global availability** 

    The public virtual server offering is available in data centers across the globe.

* **Configuration choices, rapid deployment, and scalability** 

    The public virtual server offering gives you small or large virtual server options to meet various workload requirements.

**Note:** If you are looking for a single-tenant environment, consider the [Dedicated virtual server](../vsi/vsi_dedicated.html) offering.
{:shortdesc}

Public instances reside on a hypervisor that is shared with other clients. However, the processors and memory are dedicated to the virtual server, making server performance reliable. 

The following public virtual servers are available. 

| Public virtual servers  | Description                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Balanced local storage](../vsi/vsi_public_balanced_local.html) | Best for large database clusters that require high, low latency I/O performance.|
| [Balanced](../vsi/vsi_public_balanced.html) | Best for common cloud workloads that require a balance of performance and scalability. Uses network-attached storage.|
| [Compute](../vsi/vsi_public_compute.html) | Best for moderate to high web traffic workloads.|
| [Memory](../vsi/vsi_public_memory.html)  | Best for memory caching and real-time analytics workloads.
{: caption="Table 1. Supported public virtual servers" caption-side="top"}

## Next Steps

After you review and decide upon your virtual server size, it's time to provision your public virtual server. To get started, review the following information: 
1. [Provisioning selections](../vsi/vsi_public_selections.html)
2. [Provisioning public instances](../vsi/vsi_provision_public.html)
