---

copyright:
  years: 2017, 2020
lastupdated: "2020-03-06"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# About dedicated virtual servers
{: #dedicated-virtual-servers}

The {{site.data.keyword.Bluemix}} infrastructure dedicated host offering is a virtualized, single-tenant, dedicated server. It provides you with maximum control over workload placement and flexible post-provisioning options. You can decide which pre-determined {{site.data.keyword.cloud_notm}} data center your virtual servers are placed in and can be assured capacity by allocating your host(s) directly to your account.
{:shortdesc}

The offering includes the following features:

* Affinity and anti-affinity. You can specify host-to-virtual server and virtual server-to-virtual server relationships that should remain, which are known as affinity and anti-affinity rules. These rules help you make sure that your workloads are placed appropriately based on your workload requirements.
* Post-deployment management. You can migrate virtual servers between dedicated hosts based on your workload requirements.
* Workload visibility. You can view resource consumption—core, RAM, and local storage—for each host, giving you maximum control over your workload management.

You have the choice of two deployment models: dedicated hosts and dedicated instances. Dedicated hosts help with control over workload placement and dedicated instances offer single-tenant isolation.

Dedicated instances do not provide some of the control features offered by dedicated hosts.  See the following table for more details.
{:note}

| Dedicated virtual server feature | Dedicated hosts instances | Dedicated instances |
| ------- | ------- | ------- |
| Single-tenant isolation | ![Checkmark icon](../icons/checkmark-icon.svg) | ![Checkmark icon](../icons/checkmark-icon.svg) |
| Virtual server placement control | ![Checkmark icon](../icons/checkmark-icon.svg) |   |
| Resource visibility | ![Checkmark icon](../icons/checkmark-icon.svg) |   |
| Instance billing |   | ![Checkmark icon](../icons/checkmark-icon.svg) |
| Host billing<sup>(1)</sup> | ![Checkmark icon](../icons/checkmark-icon.svg) |   |
| Post-deployment control | ![Checkmark icon](../icons/checkmark-icon.svg) |   |
| Capacity reservations | ![Checkmark icon](../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="Table 1. Control features" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup>Pricing of host is inclusive of core, RAM, Local SSD, and network speeds. Premium operating system (OS), storage area network (SAN) storage, and software add-ons will be priced per instance with existing pricing and licensing in an hourly or monthly model.

Keep in mind the following when you’re ordering a dedicated host(s) and dedicated host instances:

* The size of your host(s) is determined by your workloads that you will be running on it. The default is 56 Cores X 242 GB RAM X 1.2 TB, but you can choose from additional configurations.
* You can order only two hosts at a time. For example, if you need six hosts, you will need to place three separate orders.
* Each host will need its own unique name and you can automatically assign your POD.
* Network speeds up to 20 Gbps are achievable through additional configuration. For more information about network performance, see [Configuring virtual server settings for improved network performance](/docs/virtual-servers?topic=virtual-servers-configuring-network-performance).

## Next steps
{: #next-steps-dedicated-virtual-servers}

After you have reviewed and decided upon your deployment options, it is time to provision your virtual server. To get started, see [Provisioning dedicated hosts and instances](/docs/virtual-servers?topic=virtual-servers-provisioning-dedicated-hosts-instances).
