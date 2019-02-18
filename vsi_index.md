---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-05"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Getting started tutorial
You can deploy {{site.data.keyword.BluVirtServers}} in a matter of minutes. The virtual servers are deployed from your choice of virtual server images and in the geographic region that makes sense for your workloads.
{:shortdesc}

Try our virtual servers on a virtual private cloud! For more information, see [IBM Cloud Virtual Servers for VPC](/docs/vsi-is/getting-started.html#gettingstartedvsigen).
{:tip}

When you create a virtual server, you can choose between a public (multi-tenancy) environment or a dedicated (single-tenancy) environment. Then, depending on the chosen environment, you must also select hourly, monthly, or transient virtual servers. In the case of public virtual servers, you also choose to use either SAN-based storage or local storage.

## Before you begin

Before you begin, review the following prerequisites.

  1. You must have an upgraded account to order virtual servers. This process can take some time and requires your request to be approved before you can continue. For more information about upgrading your account, see [Switching to IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).
  2. Review and choose your deployment options. For more information, see the following topics:

|              Deployment options                           |  Description                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Public virtual server](/docs/vsi/vsi_public.html)            | IBM-managed, multi-tenancy virtual server deployments|
|[Transient virtual server](/docs/vsi/vsi_about_transient.html)| IBM-managed, multi-tenancy virtual server deployments offered at a reduced cost and best suited for flexible workloads |
|[Reserved virtual server](/docs/vsi/vsi_about_reserved.html)  | IBM-managed, multi-tenancy virtual server deployments with guaranteed capacity for a contract term |
|[Dedicated virtual server](/docs/vsi/vsi_dedicated.html)      | IBM-managed, single-tenancy virtual server deployments            |
{: caption="Table 1. Deployment options" caption-side="top"}   

## Provisioning a virtual server

After you decide upon a deployment option, begin the provisioning process.

|              Provisioning Instructions                                         |  Description                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisioning public instances](/docs/vsi/vsi_provision_public.html)                | Provision public instances with various options             |
|[Provisioning transient instances](/docs/vsi/vsi_provision_transient.html)                | Provision transient instances with various options            |
|[Provisioning reserved capacity and instances](/docs/vsi/vsi_provision_reserved.html)            | Provision reserved capacity and instances with various options |
|[Provisioning dedicated hosts and instances](/docs/vsi/vsi_provision_dedicated.html)| Provision private instances or dedicated instances on dedicated hosts.|
{: caption="Table 2. Provisioning information" caption-side="top"}

## Next Steps

After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.slportal_full}} or {{site.data.keyword.slapi_full}}. For more information, see [Configuring virtual servers](/docs/vsi/vsi_configuring.html).
