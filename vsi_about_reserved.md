---

copyright:
  years: 2018, 2019
lastupdated: "2019-10-03"

keywords: reserved virtual servers, cost savings, guaranteed capacity 
subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Reserved virtual servers
{: #about-reserved-virtual-servers}

{{site.data.keyword.BluVirtServers}} reserved instances offering is a great option if you want guaranteed resources for future deployments and cost savings. You choose between either a one or three year contract term for your reserved capacity. Within that reserved capacity, you can reserve a set of up to 20 virtual server instances of a specific size and provision those instances when you need them. You are guaranteed this capacity within the POD and data center of your choice for the life of the contract term.

Reserved virtual server instances offer many advantages, including the following:

* **Guaranteed capacity**

    When you reserve capacity, this capacity is guaranteed for the life of your contract term. 
    
* **Global availability**
    
    The reserved virtual server offering is available in data centers across the globe.

* **Reliable provisioning**
   
   You can provision and reclaim virtual server instances to your reserved capacities at any time.

* **Cost savings**
    
    Choosing either a one or three year contract term allows for consistent monthly payments and reduced costs compared to hourly or monthly virtual server billing cycles.

Reserved virtual server instances are public instances that use SAN-backed storage. The following families of public instances are available for this offering.

| Families  | Description                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Balanced](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Best for common cloud workloads that require a balance of performance and scalability. Uses network-attached storage.|
| [Compute](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Best for moderate to high web traffic workloads.|
| [Memory](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Best for memory caching and real-time analytics workloads. |
{: caption="Table 1. Public virtual server family selections" caption-side="top"}

## Limitations 
{: #limitations-reserved-virtual-servers}

Consider the following limitations before reserving capacity and provisioning reserved virtual server instances:
  
  * You can't use variable compute profiles.
  * You can't upgrade or downgrade your instances.
  * Reserved capacity cannot be canceled; however, you can reclaim virtual server instances in that capacity.
    
## Notifications
{: #notifications-reserved-virtual-servers}

You will receive an email notification one month before the end of the term on your reserved virtual server capacity.

## Next steps
{: #next-steps-reserved-virtual-servers}

After you've reviewed and decided on your options, it's time to provision your reserved capacity and instances. To get started, review the following information:

   1. [Provisioning reserved capacity and instances](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)
   2. [FAQs: Reserved capacity and instances](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances)
