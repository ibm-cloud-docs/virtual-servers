---

copyright:
  years: 2018, 2025
lastupdated: "2025-04-09"

keywords: reserved virtual servers, cost savings, guaranteed capacity, classic

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Reserved virtual servers for Classic
{: #about-reserved-virtual-servers}

{{site.data.keyword.BluVirtServers}} reserved instances for Classic are a great option if you want guaranteed resources for future deployments and cost savings. You can choose between either a 1 or 3-year contract term for your reserved capacity. Within that reserved capacity, you can reserve a set of up to 20 virtual server instances of a specific size and provision those instances when you need them. You are guaranteed this capacity within the POD and data center of your choice for the life of the contract term.
{:shortdesc}

Classic reserved virtual servers offer many advantages, including the following benefits:

| Benefit | Description |
| ----- | ----- |
| Guaranteed capacity | When you reserve capacity, this capacity is guaranteed for the life of your contract term. |
| Global availability | Reserved virtual servers are available in data centers globally. |
| Reliable provisioning | You can provision and reclaim virtual server instances to your reserved capacities at any time. |
| Cost savings | Choosing either a 1 or 3-year contract term allows for consistent monthly payments and reduced costs compared to hourly or monthly virtual server billing cycles. |
{: caption="Reserved virtual server advantages" caption-side="top"}

Classic reserved virtual server instances are public instances that use SAN-backed storage. The following families of public instances are available for this offering.

| Family | Description |
| ------ | --------- |
| [Balanced](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#balanced) | Best for common cloud workloads that require a balance of performance and scalability. Uses network-attached storage.|
| [Compute](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#compute) | Best for moderate to high web traffic workloads.|
| [Memory](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#memory)  | Best for memory caching and real-time analytics workloads. |
{: caption="Public virtual server family selections" caption-side="top"}

## Limitations
{: #limitations-reserved-virtual-servers}

Consider the following limitations before you reserve capacity and provision a reserved virtual server instance:

* You can't use variable compute profiles.
* You can't change the configuration of the reserved virtual server.
* Reserved capacity cannot be canceled; however, you can reclaim virtual server instances in that capacity.

## Notifications
{: #notifications-reserved-virtual-servers}

You receive an email notification one month before the end of the term on your reserved virtual server capacity.

## Next steps
{: #next-steps-reserved-virtual-servers}

After you review and decided on your options, it's time to provision your reserved capacity and virtual servers. To get started, review the following information:

* [Provisioning reserved capacity and instances](/docs/virtual-servers?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)
* [FAQs: Reserved capacity and instances](/docs/virtual-servers?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances)
