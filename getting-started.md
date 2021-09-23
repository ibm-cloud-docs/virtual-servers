---

copyright:
  years: 2017, 2021
lastupdated: "2021-09-09"

keywords: virtual servers, classic, provisioning process, IBM Cloud Virtual Servers, virtual machines

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Getting started with virtual servers
{: #getting-started-tutorial}

You can deploy {{site.data.keyword.BluVirtServers}} in a matter of minutes. The virtual servers for classic infrastructure are deployed from your choice of virtual server images and in the geographic region that makes sense for your workloads.
{: shortdesc}

Newer version available. Try our Virtual Servers for VPC. For more information, see [Virtual Private Cloud](/docs/vpc?topic=vpc-getting-started).
{: tip}

When you create a virtual server in the classic infrastructure, you can choose between a public (multi-tenancy) environment or a dedicated (single-tenancy) environment. Then, depending on the chosen environment, you must also select hourly, monthly or transient virtual servers. In the case of public virtual servers, you also choose to use either SAN-based storage or local storage.

## Before you begin
{: #before-you-begin-virtual-servers}

Before you begin, review the following prerequisites.

1. You must have an upgraded account to order virtual servers. This process can take some time and requires your request to be approved before you can continue. For more information about upgrading your account, see [Switching to IBMid](/docs/account?topic=account-upgrading-account).
2. Review and choose your deployment options. For more information, see the following topics:

|              Deployment options                           |  Description                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Public virtual server](/docs/virtual-servers?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)            | IBM-managed, multi-tenancy virtual server deployments|
|[Transient virtual server](/docs/virtual-servers?topic=virtual-servers-about-vs-transient)| IBM-managed, multi-tenancy virtual server deployments offered at a reduced cost and best suited for flexible workloads |
|[Reserved virtual server](/docs/virtual-servers?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | IBM-managed, multi-tenancy virtual server deployments with guaranteed capacity for a contract term |
|[Dedicated virtual server](/docs/virtual-servers?topic=virtual-servers-dedicated-virtual-servers)      | IBM-managed, single-tenancy virtual server deployments            |
{: caption="Table 1. Deployment options" caption-side="top"}

## Provisioning a virtual server
{: #provisioning-a-virtual-server-getting-started}

After you decide upon a deployment option, begin the provisioning process.

|              Provisioning instructions                                         |  Description                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisioning public instances](/docs/virtual-servers?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                | Provision public instances with various options             |
|[Provisioning transient instances](/docs/virtual-servers?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                | Provision transient instances with various options            |
|[Provisioning reserved capacity and instances](/docs/virtual-servers?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | Provision reserved capacity and instances with various options |
|[Provisioning dedicated hosts and instances](/docs/virtual-servers?topic=virtual-servers-dedicated-hosts-and-dedicated-instances) | Provision private instances or dedicated instances on dedicated hosts|
{: caption="Table 2. Provisioning information" caption-side="top"}

## Next steps
{: #next-steps-getting-started}

After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.cloud_notm}} console. For more information, see [Configuring virtual servers](/docs/virtual-servers?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
