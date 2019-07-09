---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# Provisioning a virtual server instance from a 3rd party image
{: #ordering-3P}

You can provision virtual server instance from an image that was created by a 3rd party vendor. 3rd party images are avaialble through the {{site.data.keyword.cloud}} catalog Cloud Images link.
{:shortdesc}

## Before you begin
Before you begin, ensure that you have your {{site.data.keyword.cloud_notm}} catalog credentials set up.

  **Note:** For the {{site.data.keyword.Bluemix_notm}} catalog, you must have an upgraded account to order virtual servers. For more information about upgrading your account, see [Switching to IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).

## Selecting a virtual server image
1. Log in to the [{{site.data.keyword.cloud_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/){: new_window} by using your unique credentials.
2. In the **Cloud Image** section, locate and click the 3rd party image you want to deploy.
3. Review the custom image details and click **Continue**. The **Virtual server instance - custom image** page is displayed with your custom image pre-selected.


## Review and choose your deployment options.
For more information, see the following topics:

|              Deployment options                           |  Description                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Public virtual server](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)            | IBM-managed, multi-tenancy virtual server deployments|
|[Transient virtual server](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)| IBM-managed, multi-tenancy virtual server deployments offered at a reduced cost and best suited for flexible workloads |
|[Reserved virtual server](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | IBM-managed, multi-tenancy virtual server deployments with guaranteed capacity for a contract term |
|[Dedicated virtual server](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)      | IBM-managed, single-tenancy virtual server deployments            |
{: caption="Table 1. Deployment options" caption-side="top"}

## Begin the provisioning process
After you decide upon a deployment option, begin the provisioning process. Refer to the following topics.

Because you started the provisioning process with a custom image, you cannot change the image type during the provisioning process.
{:note}

|              Provisioning Instructions                                         |  Description                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisioning public instances](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                | Provision public instances with various options             |
|[Provisioning transient instances](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                | Provision transient instances with various options            |
|[Provisioning reserved capacity and instances](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | Provision reserved capacity and instances with various options |
|[Provisioning dedicated hosts and instances](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)| Provision private instances or dedicated instances on dedicated hosts.|
{: caption="Table 2. Provisioning information" caption-side="top"}


## Next Steps
After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.slportal_full}} or {{site.data.keyword.slapi_full}}. For more information, see [Configuring virtual servers](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
