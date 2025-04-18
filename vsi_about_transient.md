---

copyright:
  years: 2017, 2025
lastupdated: "2025-04-08"

keywords: transient

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Transient virtual servers for Classic
{: #about-vs-transient}

Classic {{site.data.keyword.cloud}} transient virtual servers are a good option if you have flexible workloads and want cost savings. You can save money by running your workload on a transient virtual server. Classic transient virtual servers are provisioned when unused capacity is available. Therefore, when data center resources are needed for full, on-demand accounts, you can also lose those resources. Transient virtual servers are deprovisioned on a first-on, first-off basis when those resources need to be reclaimed.
{: shortdesc}

Classic transient virtual servers offer the following flexibility:

* **Global availability**

   Transient virtual servers are available in data centers across the globe.

* **Cost savings**

   Transient virtual servers are ideal for nonproduction workloads. For example, you might use a transient virtual server to test and develop applications, or test scalability in Classic environments that don't require constant uptime.

Transient virtual servers are public virtual servers that use SAN-backed storage. The following families of public virtual servers are available for this offering.

| Families  | Description |
| --------- | ----------- |
| [Balanced](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#balanced) | Best for common cloud workloads that require a balance of performance and scalability. Uses network-attached storage.|
| [Compute](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#compute) | Best for moderate to high web traffic workloads.|
| [Memory](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#memory)  | Best for memory caching and real-time analytics workloads. |
{: caption="Public virtual server family selections" caption-side="top"}

## Notifications
{: #notifications-transient-virtual-servers}

When configured, you can receive automated reclaim notifications that help you prepare and reduce lost data. For more information, see [Configuring automated reclaim notifications](/docs/virtual-servers?topic=virtual-servers-configuring-notifications-for-reclaims-of-transient-virtual-servers#configuring-notifications-for-reclaims-of-transient-virtual-servers).

## Limitations
{: #limitations-transient-virtual-servers}

Consider the following limitations before you provision a transient virtual server.

* The number of supported, concurrent virtual servers are part of your account-wide device quota. For more information about concurrent virtual server limits, see [FAQ: Virtual servers](/docs/virtual-servers?topic=virtual-servers-faqs-virtual-servers#faqs-virtual-servers).
* You can't change transient virtual server configurations.
* Resources can be reclaimed at any time, without notification.
* Transient virtual servers cannot use local storage.
* Transient virtual servers cannot use GPU-based or variable compute profiles.

## Next steps
{: #next-steps-transient-virtual-servers}

After you review and select your virtual server profile, it's time to provision your transient virtual server. To get started, see [Provisioning transient virtual servers](/docs/virtual-servers?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient).
