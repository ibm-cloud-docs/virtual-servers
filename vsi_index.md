---

copyright:
  years: 2017, 2019, 2020
lastupdated: "2020-03-23"

keywords: virtual servers, provisioning process, IBM Cloud Virtual Servers

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Getting started with virtual servers
{: #getting-started-tutorial}

You can deploy {{site.data.keyword.BluVirtServers}} in a matter of minutes. The virtual servers are deployed from your choice of virtual server images and in the geographic region that makes sense for your workloads.
{:shortdesc}

Newer version available. Try our Virtual Servers for VPC. For more information, see [Virtual Private Cloud](/docs/vpc?topic=vpc-getting-started).
{:tip}

When you create a virtual server in the classic infrastructure, you can choose between a public (multi-tenancy) environment or a dedicated (single-tenancy) environment. Then, depending on the chosen environment, you must also select hourly, monthly, or transient virtual servers. In the case of public virtual servers, you also choose to use either SAN-based storage or local storage.

## Before you begin
{: #before-you-begin-virtual-servers}

Before you begin, review the following prerequisites.

  1. You must have an upgraded account to order virtual servers. This process can take some time and requires your request to be approved before you can continue. For more information about upgrading your account, see [
Account types](/docs/account?topic=account-accounts).
  2. Review and choose your deployment options. For more information, see the following topics:

|              Deployment options                           |  Description                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Public virtual server](/docs/virtual-servers?topic=virtual-servers-about-public-virtual-servers)            | IBM-managed, multi-tenancy virtual server deployments|
|[Transient virtual server](/docs/virtual-servers?topic=virtual-servers-about-vs-transient)| IBM-managed, multi-tenancy virtual server deployments offered at a reduced cost and best suited for flexible workloads |
|[Reserved virtual server](/docs/virtual-servers?topic=virtual-servers-about-reserved-virtual-servers)  | IBM-managed, multi-tenancy virtual server deployments with guaranteed capacity for a contract term |
|[Dedicated virtual server](/docs/virtual-servers?topic=virtual-servers-dedicated-virtual-servers)      | IBM-managed, single-tenancy virtual server deployments            |
{: caption="Table 1. Deployment options" caption-side="top"}   

## Provisioning a virtual server
{: #provisioning-a-virtual-server-getting-started}

After you decide upon a deployment option, begin the provisioning process.

|              Provisioning instructions                                         |  Description                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisioning public instances](/docs/virtual-servers?topic=virtual-servers-ordering-vs-public)                | Provision public instances with various options             |
|[Provisioning transient instances](/docs/virtual-servers?topic=virtual-servers-ordering-vs-transient)                | Provision transient instances with various options            |
|[Provisioning reserved capacity and instances](/docs/virtual-servers?topic=virtual-servers-provisioning-reserved-capacity-and-instances)            | Provision reserved capacity and instances with various options |
|[Provisioning dedicated hosts and instances](/docs/virtual-servers?topic=virtual-servers-provisioning-dedicated-hosts-instances) | Provision private instances or dedicated instances on dedicated hosts|
{: caption="Table 2. Provisioning information" caption-side="top"}

## Recommendations
{: #recommendations}

IBM Cloud uses Citrix Hypervisor to power Classic VSI. As with most hypervisors, guest additions play critical roles in maintaining a stable and healthy computing environment. IBM Cloud uses this information to make informed decisions about routine server maintenance and will affect our ability to do them. Without this required guest additions, VSI may not be eligible for live migrations when a critical maintenance needs to be performed. This can lead to a disruptive maintenance for your VSI. 

To help ensure the smoothest operations of your VSI, please do not disable or remove the guest additions that are installed by default on IBM Cloud supplied images.

If you are bringing your own images to IBM Cloud Classic VSI, install the guest additions so that you will have the best performance possible. Below you will find links the latest vmtools we support:

Windows VSI:
http://downloads.service.networklayer.com/citrix/xen/citrix-vm-tools-9.1.5.zip
* Unzip the package
* Navigate to the Windows Installer, for example, _managementagent64_, and double-click to open the **Citrix XenServer Windows Management Agent Setup** wizard. Complete the installation wizard to install XenServer Tools.

Linux VSI:
http://downloads.service.networklayer.com/citrix/xen/CitrixHypervisor-LinuxGuestTools-7.20.0-1.tar.gz
* Untar the package and follow the directions in README.txt

NOTE: You will need to be connected via the VPN in order to access these.

If you wish to validate that the guest additions are working from the hypervisor point of view, please open a support ticket and ask for xentools VSI validation

## Next steps
{: #next-steps-getting-started}

After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.cloud_notm}} console. For more information, see [Configuring virtual servers](/docs/virtual-servers?topic=virtual-servers-configuring-virtual-servers).
