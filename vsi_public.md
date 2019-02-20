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

|              Deployment options                           |  Description                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Public virtual server](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)            | IBM-managed, multi-tenancy virtual server deployments|
|[Transient virtual server](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)| IBM-managed, multi-tenancy virtual server deployments offered at a reduced cost and best suited for flexible workloads |
|[Reserved virtual server](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | IBM-managed, multi-tenancy virtual server deployments with guaranteed capacity for a contract term |
|[Dedicated virtual server](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)      | IBM-managed, single-tenancy virtual server deployments            |
{: caption="Table 1. Deployment options" caption-side="top"} 

## Provisioning a virtual server

After you decide upon a deployment option, begin the provisioning process.

|              Provisioning Instructions                                         |  Description                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisioning public instances](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                | Provision public instances with various options             |
|[Provisioning transient instances](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                | Provision transient instances with various options            |
|[Provisioning reserved capacity and instances](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | Provision reserved capacity and instances with various options |
|[Provisioning dedicated hosts and instances](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)| Provision private instances or dedicated instances on dedicated hosts.|
{: caption="Table 2. Provisioning information" caption-side="top"}

## Next Steps

After you review and decide upon your virtual server flavor, it's time to provision your public virtual server. To get started, review the following information:
1. [Provisioning selections](/docs/vsi/vsi_public_selections.html)
2. [Provisioning public instances](/docs/vsi/vsi_provision_public.html)



