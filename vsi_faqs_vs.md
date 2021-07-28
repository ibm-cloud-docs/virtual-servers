---

copyright:
  years: 2017, 2021
lastupdated: "2021-03-02"

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
{: #what-types-of-virtual-servers-are-available-for-use-}
{: faq}

{{site.data.keyword.cloud}} offers a couple types of virtual servers within its Classic Infrastructure. The standard offering is a public-based virtual server, which is a multi-tenant environment that is suitable for various needs. If you're looking for a single-tenant environment, consider the dedicated virtual server offering. The dedicated virtual server option is ideal for applications with more stringent resource requirements. For more information about the current virtual server offerings, see [Getting started with virtual servers](/docs/virtual-servers?topic=virtual-servers-getting-started-tutorial).

{{site.data.keyword.vsi_is_full}} (VPC) is the next generation of virtual servers. You create your own space in the {{site.data.keyword.cloud_notm}} to run an isolated environment within the public cloud by using VPC. {{site.data.keyword.vpc_short}} provides the security of a private cloud with the agility and ease of a public cloud. For more information, see [About Virtual Private Cloud](/docs/vpc-on-classic?topic=vpc-on-classic-about).

## Where can I find pricing information for public instance types?
{: #where-can-i-find-pricing-information-for-public-instance-types-}
{: faq}

For more information, see [Build your virtual server](https://www.ibm.com/cloud/virtual-servers){: external}.

## Where can I find pricing information for virtual public instances?
{: #where-can-i-find-pricing-information-for-virtual-public-instances-}
{: faq}

Estimating your cost for an {{site.data.keyword.cloud_notm}} server to support your workload begins in the [{{site.data.keyword.cloud_notm}} catalog](https://cloud.ibm.com/catalog){: external}. From the catalog, select **Compute** and choose the server type - Bare Metal Server, Virtual Server, or Virtual Server for VPC (Virtual Private Cloud). For more information, see the [Virtual servers provisioning calculator](https://www.ibm.com/cloud/virtual-servers/calculator/){: external}.

## Can I change the configuration of a virtual server?
{: #can-i-reconfigure-virtual-server}
{: faq}

After you provision a virtual server, you can upgrade or downgrade your server configuration at any time. For more information, see [Reconfiguring an existing virtual server](/docs/virtual-servers?topic=virtual-servers-reconfiguring-virtual-servers). If the item that you want to change is not available from the Device List, you can cancel and reorder or contact [IBM Cloud Sales](https://cloud.ibm.com/catalog?contactmodule) for assistance.

## How do I cancel a virtual server?
{: how-do-i-cancel-virtual-server}

You can cancel a virtual server at any time. Go to the [Device List](https://cloud.ibm.com/classic/devices). Click **Actions** for the server that you want to cancel, and select the cancel option from the menu. For more information, see [Canceling virtual servers](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#cancel).

## Can I add disk storage to my hourly or monthly virtual server?
{: #can-i-add-disk-storage-to-my-hourly-or-monthly-virtual-server-}
{: faq}

You can upgrade or downgrade disk storage for any virtual server by updating your storage options in the *First Disk* through *Fifth Disk* fields in the *Configuration* screen of the device you want to update. For more information, see [Reconfiguring an existing virtual server](/docs/virtual-servers?topic=virtual-servers-reconfiguring-virtual-servers).

## How many hourly virtual servers can I start?
{: #concurrent}
{: faq}

The number of instances that you can run depends on the maturity level of your account. By default, an account older than 45 days has a limit of 20 instances that can run on public virtual servers, dedicated virtual servers, and bare metal servers, at any time. A newer account has a smaller limit. If you would like to increase your limit, contact support about what you are doing and how many concurrent instances you might need.

## How will I be billed for bandwidth for my hourly virtual servers?
{: #how-will-i-be-billed-for-bandwidth-for-my-hourly-virtual-servers-}
{: faq}

Hourly virtual billing is broken down for inbound and outbound traffic. All inbound traffic to your virtual server is free of charge. Outbound traffic is metered and charged per GB, with totals assessed at the end of your billing period.

## What happens to my data when my portable storage is deleted?
{: #what-happens-to-my-data-when-my-portable-storage-is-deleted-}
{: faq}

Virtual server instance SAN is similar to file storage. Virtual server instance disks are just files on an NFS share that Xen presents to the instance as a block device, that is, a hard disk drive. When you delete an instance SAN disk, you delete the file, after which undelete is not possible. Any pointers to the data on that volume are removed, and the data becomes inaccessible. If the physical storage is reprovisioned to another account, a new set of pointers is assigned. There is no way for the new account to access any data that might have been on the physical storage. The new set of pointers shows all 0's. When new data is written to the volume/LUN, any inaccessible data that still exists gets overwritten.

## Can I use a Red Hat Cloud Access subscription to create a virtual server?
{: #can-i-use-a-red-hat-cloud-access-subscription-to-create-a-virtual-server-}
{: faq}

Yes. When you import an image, you can specify that you provide the operating system license. For more information, see [Use Red Hat Cloud Access](/docs/image-templates?topic=image-templates-using-your-own-os-license-or-subscription). Then, you can order a virtual server from that image template and use your existing [Red Hat Cloud Access](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: external} subscription.

## What is the difference between a virtual server and a virtual private server (VPS)?
{: #what-is-the-difference-between-a-virtual-server-and-a-virtual-private-server-vps-}
{: faq}

A virtual server is similar to the virtual private server (VPS) or virtual dedicated server (VDS) platforms you might already be familiar with. These "virtual server" environments allow for distinct environments to be provisioned privately and securely on a single hardware node, but VDS and VPS are more limited in their capabilities. VPS and VDS options are generally confined to a single-server architecture. The only resources that can be added or divided up between each virtual server on a VDS or VPS are the resources that are physically installed on that single server.

Virtual servers are provisioned on a multi-server cloud architecture that pools all available hardware resources for individual instances to use. Virtual servers can use a shared high-capacity SAN-based primary storage platform or high-performance local disk storage. Because each instance is part of the larger cloud environment, communication between all virtual servers is instantaneous.

## Why do I receive a capacity error when provisioning a virtual server?
{: #why-do-i-receive-a-capacity-error-when-provisioning-a-virtual-server-}
{: faq}

When you provision a virtual server, you might receive an error message stating that there is insufficient capacity to complete the request. When provisioning fails, all the virtual server instances within that particular request fail. A capacity error occurs when there are insufficient resources available in the router or data center to fulfill the service request. There are a number of reasons that you might receive this error. Resource availability changes frequently, so you might wait and try again later. For more information on strategies to avoid this error, see [Resource considerations for virtual server instances](/docs/virtual-servers?topic=virtual-servers-capacity-considerations).

## How do I log in to my server?
{: #how-do-i-log-in-to-my-server-}
{: faq}

Log in to your console and navigate to your **Devices** menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices). In the **Device List**, select your instance. You can view and manage the device usernames and passwords to use to log in. For more information, see [Viewing and managing device usernames and passwords](/docs/virtual-servers?topic=virtual-servers-view-update-user-name-password-for-device).

## How do I use VPN to access the IBM Cloud Private network?
{: #how-do-i-use-vpn-to-access-the-ibm-cloud-private-network-}
{: faq}

You can log in to the VPN through [the web interface](https://www.softlayer.com/VPN-Access){: external} or use a [stand-alone VPN client](/docs/iaas-vpn?topic=iaas-vpn-standalone-vpn-clients) for Linux, macOS, or Windows. For more information about what to do once you're connected to the VPN, see [Use SSL VPN](/docs/iaas-vpn?topic=iaas-vpn-using-ssl-vpn).

## How do I restart my virtual server?
{: #how-do-i-reboot-my-virtual-server-}
{: faq}

Device restarts can take place from either the **Device List** or from the snapshot view of an individual instance. Navigate to your virtual server instance in the **Device List** in your console. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices). Select **Actions** for the device you want to manage and select **Reboot**.

## How do I use rescue mode?
{: #how-do-i-use-rescue-mode-}
{: faq}

Booting into rescue mode is helpful if you're experiencing an issue with the server. To start rescue mode, select the device name from the **Device List** in your console. In the **Actions** menu, select **Rescue mode** or select **Boot from image** for a Windows instance. For more information, see [Launching rescue mode](/docs/virtual-servers?topic=virtual-servers-launching-rescue).

## Where do I find network status?
{: #where-do-i-find-network-status-}
{: faq}

You can access the **Status** page directly at [{{site.data.keyword.cloud_notm}} - Status](https://cloud.ibm.com/status){: external} to view the status of resources in all {{site.data.keyword.cloud_notm}} locations. You can filter the list by selecting specific components and locations (for example, you can select Virtual Servers and view the network connectivity).

## How do I request a compliance report?
{: #how-do-i-request-a-compliance-report-}
{: faq}

For information about viewing or requesting compliance information, including SOC reports, see [Understanding IBM Cloud compliance](/docs/overview?topic=overview-compliance).
