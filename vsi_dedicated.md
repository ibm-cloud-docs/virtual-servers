---

copyright:
  years: 2017, 2025
lastupdated: "2025-04-09"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# About dedicated virtual servers for Classic
{: #dedicated-virtual-servers}

The {{site.data.keyword.Bluemix}} Classic infrastructure dedicated host is a virtualized, single-tenant, dedicated server. It provides you with maximum control over your Classic workload placement and flexible post-provisioning options. You can decide which pre-determined {{site.data.keyword.cloud_notm}} data center your virtual servers are placed in and have capacity by allocating your hosts directly to your account.
{: shortdesc}

The offering includes the following features:

* Affinity and anti-affinity. You can specify host-to-virtual server and virtual server-to-virtual server relationships that need to remain, which are known as affinity and anti-affinity rules. These rules help you make sure that your workloads are placed based on your workload requirements.
* Post-deployment management. You can migrate virtual servers between dedicated hosts based on your workload requirements.
* Workload visibility. You can view resource consumption—core, RAM, and local storage—for each host, giving you maximum control over your workload management.

You have the choice of two deployment models: dedicated hosts and dedicated instances. Classic dedicated hosts help with control over workload placement and dedicated instances offer single-tenant isolation. See the following table to compare dedicated host and instance features.

| Dedicated virtual server feature | Dedicated hosts instances | Dedicated instances |
| ------- | ------- | ------- |
| Single-tenant isolation | ![Checkmark icon](../icons/checkmark-icon.svg) | ![Checkmark icon](../icons/checkmark-icon.svg) |
| Virtual server placement control | ![Checkmark icon](../icons/checkmark-icon.svg) |   |
| Resource visibility | ![Checkmark icon](../icons/checkmark-icon.svg) |   |
| Instance billing |   | ![Checkmark icon](../icons/checkmark-icon.svg) |
| Host billing| ![Checkmark icon](../icons/checkmark-icon.svg) |   |
| Post-deployment control | ![Checkmark icon](../icons/checkmark-icon.svg) |   |
| Capacity reservations | ![Checkmark icon](../icons/checkmark-icon.svg) |   |
{: caption="Table 1: Control features" caption-side="top"}

Classic dedicated instances do not provide some of the control features offered by dedicated hosts. See the following table for more details.
{: note}

Pricing of the host is inclusive of core, RAM, Local SSD, and network speeds. Premium operating system (OS), storage area network (SAN) storage, and software add-ons are priced per instance with existing pricing and licensing in an hourly or monthly model.

Keep the following list in mind when you order a dedicated host and dedicated host instance for Classic:

* The size of your host is determined by your workloads. The default is 56 Cores X 242 GB RAM X 1.2 TB, but you can choose from more configurations.
* You can order only two hosts at a time. For example, if you need six hosts, then you need to place three separate orders.
* Each host needs its own unique name and you can automatically assign your POD.
* Network speeds up to 20 Gbps are achievable through extra configuration. For more information about network performance, see [Configuring virtual server settings to improve network performance](/docs/virtual-servers?topic=virtual-servers-configuring-network-performance).

## Next steps
{: #next-steps-dedicated-virtual-servers}

After you reviewed and decided upon your deployment options, it is time to provision your virtual server. To get started, see [Provisioning dedicated hosts and instances](/docs/virtual-servers?topic=virtual-servers-provisioning-dedicated-hosts-instances).
