---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-09"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# FAQs: Virtual servers  
{: #faqs-virtual-servers}

## What types of virtual servers are available for use?
{: faq}
{{site.data.keyword.BluSoftlayer_full}} offers a couple types of virtual servers within its Classic Infrastructure. The standard offering is a public-based virtual server, which is a multi-tenant environment, suitable for a variety of needs. If you're looking for a single-tenant environment, consider the Dedicated Virtual Server offering. The dedicated virtual server option is ideal for applications with more stringent resource requirements. For more information about the current virtual server offerings see, [Getting started with virtual servers](/docs/vsi?topic=virtual-servers-getting-started-with-virtual-servers#getting-started-with-virtual-servers).

IBM Cloud offers the Virtual Private Cloud (VPC) Infrastructure, which is the next generation cloud platform. You create your own space in the {{site.data.keyword.cloud_notm}} to run an isolated environment within the public cloud by using VPC. VPC provides the security of a private cloud with the agility and ease of a public cloud. For more information, see [About Virtual Private Cloud](https://cloud.ibm.com/docs/vpc-on-classic?topic=vpc-on-classic-about).

## Where can I find pricing information for public instance types?
{: faq}

For pricing information, see [Build your virtual server ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud/virtual-servers){: new_window}.

## Where can I find pricing information for virtual public instances?
{: faq}

Estimating your cost for an {{site.data.keyword.cloud_notm}} server to support your workload begins in the [{{site.data.keyword.cloud_notm}} catalog](https://cloud.ibm.com/catalog). From the catalog, select **Compute** and choose the server type - Bare Metal Server, Virtual Server, or Virtual Server for VPC (Virtual Private Cloud). For pricing information, see the [Virtual servers provisioning calculator ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

## Can I add disk storage to my hourly or monthly virtual server?
{: faq}

You can upgrade or downgrade disk storage for any virtual server by updating your storage options in the *First Disk* through *Fifth Disk* fields in the *Configuration* screen of the device you want to update. For more information, see [Reconfiguring an existing virtual server](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).

## How many hourly virtual servers can I start?
{: #concurrent}
{: faq}

The number of instances that you can run depends on the maturity level of your account. By default, an account older than 45 days has a limit of 20 instances that can run on public virtual servers, dedicated virtual servers, and bare metal servers, at any time. A newer account has a smaller limit. If you would like to increase your limit, contact support to tell us more about what you are doing and how many concurrent instances you might need.

## How will I be billed for bandwidth for my hourly virtual servers?
{: faq}

Hourly virtual billing is broken down for inbound and outbound traffic. All inbound traffic to your virtual server is free of charge. Outbound traffic is metered and charged per GB, with totals assessed at the end of your billing period.

## In what cases is my virtual server migrated to a different host?
{: faq}

In limited cases a virtual server might need to be migrated to a different host. If a migration is required, the virtual server is shut down, migrated, and then restarted. A virtual server might be migrated in the following cases:

* A hypervisor needs to be updated, a host is being decommissioned, or a host is not allowed to take on new instances. If a host is marked for any of these changes, when one of its virtual servers is rebooted from the {{site.data.keyword.cloud_notm}} console, the reboot automatically triggers the virtual server to be migrated to a different host.
* Infrastructure maintenance. You might receive an email indicating that maintenance is required on a system that is hosting your virtual server. Your virtual server might need to be migrated as part of the infrastructure maintenance.
* An upgrade to an existing instance. For consistent performance, if you upgrade an instance it might be migrated to a different host to ensure that it receives the appropriate dedicated CPU and memory.
* A dedicated host fails. Dedicated instances are migrated to another empty host without using any existing capacity that you might have.

During a maintenance window, you might see a **Migrate Host** option display in the **Actions** menu of your device in the {{site.data.keyword.cloud_notm}} console. **Migrate Host** allows you to migrate the virtual server to a new host at your convenience during a specified maintenance period. If you do not initiate the migration during the maintenance period, then the virtual server is automatically migrated to complete the required maintenance. The **Migrate Host** option does not persist and is only available during maintenance periods that are communicated through maintenance notifications.

You might also see the **Migrate Host** option if one of your virtual servers is required to have a certain level of hypervisor that is not available on the current host.

## What happens to my data when my portable storage is deleted?
{: faq}

When storage is deleted, any pointers to the data on that volume are removed, thus the data becomes inaccessible. If the physical storage is reprovisioned to another account, a new set of pointers is assigned. There is no way for the new account to access any data that might have been on the physical storage. The new set of pointers shows all 0's. When new data is written to the volume/LUN, any inaccessible data that still exists gets overwritten.

## Can I use a Red Hat Cloud Access subscription to create a virtual server?
{: faq}

Yes. When you import an image, you can specify that you will provide the operating system license. For more information, see [Use Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription#using-your-own-os-license-or-subscription). Then you can order a virtual server from that image template and use your existing [Red Hat Cloud Access ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} subscription.

## What is the difference between a virtual server and a virtual private server (VPS)?
{: faq}

A virtual server is similar to the virtual private server (VPS) or virtual dedicated server (VDS) platforms you might already be familiar with. These "virtual server" environments allow for distinct environments to be provisioned privately and securely on a single hardware node, but VDS and VPS are more limited in their capabilities. VPS and VDS options are generally confined to a single-server architecture. The only resources that can be added or divided up between each virtual server on a VDS or VPS are the resources that are physically installed on that single server.

Virtual servers are provisioned on a multi-server cloud architecture that pools all available hardware resources for individual instances to use. Virtual servers can use a shared high-capacity SAN-based primary storage platform or high-performance local disk storage. Because each instance is part of the larger cloud environment, communication between all virtual servers is instantaneous.

## Why do I receive a capacity error when provisioning a virtual server?
{: faq}

When you provision a virtual server, you might receive an error message stating that there is insufficient capacity to complete the request. When provisioning fails, all the virtual server instances within that particular request fail. A capacity error occurs when there are insufficient resources available in the router or data center to fulfill the service request. There are a number of reasons that you might receive this error. Resource availability changes frequently, so you might wait and try again later. For more information on strategies to avoid this error, see [Resource considerations for virtual server instances](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).

## How do I log in to my server?
{: faq}

Log in to your console and navigate to your **Devices** menu. For more information, see [Navigating to devices](/docs/vsi?topic=virtual-servers-navigating-devices). In the **Device List**, select your instance. You can view and manage the device user names and passwords to use to log in. For more information, see [Viewing and managing device user names and passwords](https://test.cloud.ibm.com/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device). 

## How do I use VPN to access the IBM Cloud private network?
{: faq}

You can log in to the VPN through [the web interface](https://www.softlayer.com/VPN-Access){: external} or use a [standalone VPN client](/docs/infrastructure/iaas-vpn?topic=VPN-standalone-vpn-clients) for Linux, macOS, or Windows. For more information about what to do once you're connected to the VPN, see [Use SSL VPN](/docs/infrastructure/iaas-vpn?topic=VPN-use-ssl-vpn).

## How do I reboot my virtual server?
{: faq}

Device reboots can take place from either the **Device List** or from the snapshot view of an individual instance. Navigate to your virtual server instance in the **Device List** in your console. For more information, see [Navigating to devices](/docs/vsi?topic=virtual-servers-navigating-devices). Select **Actions** for the device you want to manage and select **Reboot**.

## How do I use Rescue Kernel?
{: faq}

Booting into Rescue Kernel is helpful if you're experiencing an issue with the server. To launch Rescue Kernel, select the device name from the **Device List** in your console. In the **Actions** menu, select **Rescue mode** or select **Boot from image** for a Windows instance. For more information, see [Launching Rescue Kernel](/docs/vsi?topic=virtual-servers-launching-rescue).

## Where do I find network status?
{: faq}

You can access the **Status** page directly at [{{site.data.keyword.cloud_notm}} - Status](https://cloud.ibm.com/status){: external} to view the current status of resources in all {{site.data.keyword.cloud_notm}} locations. You can filter the list by selecting specific components and locations (for example, you can select Virtual Servers and view the network connectivity).

## How do I request a compliance report?
{: faq}

For information about viewing or requesting compliance information, including SOC reports, see [How do I know that my data is safe?](/docs/overview?topic=overview-security)

