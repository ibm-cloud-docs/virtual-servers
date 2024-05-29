---

copyright:
  years: 2017, 2024
lastupdated: "2024-05-29"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# FAQs: Virtual servers
{: #faqs-virtual-servers}

## What types of virtual servers are available for use?
{: #what-types-of-virtual-servers-are-available-for-use-}
{: faq}

{{site.data.keyword.cloud}} offers a couple types of virtual servers within its Classic Infrastructure. The standard offering is a public-based virtual server, which is a multi-tenant environment that is suitable for various needs. If you're looking for a single-tenant environment, consider the dedicated virtual server offering. The dedicated virtual server option is ideal for applications with more stringent resource requirements. For more information about the current virtual server offerings, see [Getting started with virtual servers](/docs/virtual-servers?topic=virtual-servers-getting-started-tutorial).

{{site.data.keyword.vsi_is_full}} (VPC) is the next generation of virtual servers. You create your own space in the {{site.data.keyword.cloud_notm}} to run an isolated environment within the public cloud by using VPC. {{site.data.keyword.vpc_short}} provides the security of a private cloud with the agility and ease of a public cloud. For more information, see [About virtual server instances for VPC](/docs/vpc?topic=vpc-about-advanced-virtual-servers).

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
{: #how-do-i-cancel-virtual-server}
{: faq}

You can cancel a virtual server at any time. Go to the [Device List](https://cloud.ibm.com/classic/devices). Click **Actions** for the server that you want to cancel, and select the cancel option from the menu. For more information, see [Canceling virtual servers](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#cancel).

## Can I add disk storage to my hourly or monthly virtual server?
{: #can-i-add-disk-storage-to-my-hourly-or-monthly-virtual-server-}
{: faq}

You can upgrade or downgrade disk storage for any virtual server by updating your storage options in the *First Disk* through *Fifth Disk* fields in the *Configuration* screen of the device you want to update. For more information, see [Reconfiguring an existing virtual server](/docs/virtual-servers?topic=virtual-servers-reconfiguring-virtual-servers).

## How many hourly virtual servers can I start?
{: #concurrent}
{: faq}

The number of instances that you can run depends on the maturity level of your account. By default, an account older than 45 days has a limit of 20 instances that can run on public virtual servers, dedicated virtual servers, and bare metal servers, at any time. A newer account has a smaller limit. If you would like to increase your limit, contact support about what you are doing and how many concurrent instances you might need.

## How am I billed for bandwidth for my hourly virtual servers?
{: #how-will-i-be-billed-for-bandwidth-for-my-hourly-virtual-servers-}
{: faq}

Hourly virtual billing is broken down for inbound and outbound traffic. All inbound traffic to your virtual server is free of charge. Outbound traffic is metered and charged per GB, with totals assessed at the end of your billing period.

## What happens to my data when my portable storage is deleted?
{: #what-happens-to-my-data-when-my-portable-storage-is-deleted-}
{: faq}

Virtual server instance SAN is similar to file storage. Virtual server instance disks are just files on an NFS share that Xen presents to the instance as a block device, that is, a hard disk drive. When you delete an instance SAN disk, you delete the file, after which undelete is not possible. Any pointers to the data on that volume are removed, and the data becomes inaccessible. If the physical storage is reprovisioned to another account, a new set of pointers is assigned. A new account can't access any data that was on the physical storage. The new set of pointers shows all 0's. When new data is written to the volume or LUN, any inaccessible data that still exists is overwritten.

## Can I use a Red Hat Cloud Access subscription to create a virtual server?
{: #can-i-use-a-red-hat-cloud-access-subscription-to-create-a-virtual-server-}
{: faq}

Yes. When you import an image, you can specify that you provide the operating system license. For more information, see [Use Red Hat Cloud Access](/docs/image-templates?topic=image-templates-using-your-own-os-license-or-subscription). Then, you can order a virtual server from that image template and use your existing [Red Hat Cloud Access](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: external} subscription.

## What is the difference between a virtual server and a virtual private server (VPS)?
{: #what-is-the-difference-between-a-virtual-server-and-a-virtual-private-server-vps-}
{: faq}

A virtual server is similar to the virtual private server (VPS) or virtual dedicated server (VDS) platforms that you might already be familiar with. These "virtual server" environments allow for distinct environments to be provisioned privately and securely on a single hardware node, but VDS and VPS are more limited in their capabilities. VPS and VDS options are generally confined to a single-server architecture. The only resources that can be added or divided up between each virtual server on a VDS or VPS are the resources that are physically installed on that single server.

Virtual servers are provisioned on a multi-server cloud architecture that pools all available hardware resources for individual instances to use. Virtual servers can use a shared high-capacity SAN-based primary storage platform or high-performance local disk storage. Because each instance is part of the larger cloud environment, communication between all virtual servers is instantaneous.

## Why do I receive a capacity error when I provision a virtual server?
{: #why-do-i-receive-a-capacity-error-when-provisioning-a-virtual-server-}
{: faq}

When you provision a virtual server, you might receive an insufficient capacity to complete the request error. When provisioning fails, all the virtual server instances within that particular request fail. A capacity error occurs when the data center or router has insufficient resources to fulfill the service request. Resource availability changes frequently, so you might wait and try again later. For more information about strategies to avoid this error, see [Resource considerations for virtual server instances](/docs/virtual-servers?topic=virtual-servers-capacity-considerations).

## How do I log in to my server?
{: #how-do-i-log-in-to-my-server-}
{: faq}

Log in to your console and go to your **Devices** menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices). In the **Device List**, select your instance. You can view and manage the device usernames and passwords to use to log in. For more information, see [Viewing and managing device usernames and passwords](/docs/virtual-servers?topic=virtual-servers-view-update-user-name-password-for-device).

## How do I use VPN to access the IBM Cloud Private network?
{: #how-do-i-use-vpn-to-access-the-ibm-cloud-private-network-}
{: faq}

You can log in to the VPN through [the web interface](https://www.softlayer.com/VPN-Access){: external} or use a [stand-alone VPN client](/docs/iaas-vpn?topic=iaas-vpn-standalone-vpn-clients) for Linux, macOS, or Windows. For more information about what to do after you connect to the VPN, see [Use SSL VPN](/docs/iaas-vpn?topic=iaas-vpn-using-ssl-vpn).

## How do I restart my virtual server?
{: #how-do-i-reboot-my-virtual-server-}
{: faq}

Device restarts can take place from either the **Device List** or from the snapshot view of an individual instance. Go to your virtual server instance in the **Device List** in your console. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices). Select **Actions** for the device that you want to manage and select **Reboot**.

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

For information about viewing or requesting compliance information and SOC reports, see [Understanding IBM Cloud compliance](/docs/overview?topic=overview-compliance).

## How long does it take for maintenance to complete?
{: #how-long-maintenance}
{: faq}

The maintenance notification contains an estimated duration for the maintenance window. Keep in mind that the time frame is an estimate and maintenance tasks might take longer. Make sure that you allow an extra hour past the maintenance window for tasks to complete and for the server to return online. If the server remains offline longer than 2 hours past the estimate, contact [support](https://test.cloud.ibm.com/docs/virtual-servers?topic=virtual-servers-gettinghelp).

## Why do I need to migrate my virtual server?
{: #why-migrate-virtual-server}
{: faq}

Migrations happen for several reasons. The most common reasons are because of host failure and planned migrations due to maintenance.

## What happens if I don't perform a manual migrate for maintenance reasons?
{: #what-happens-ignore-maintenance-migration}
{: faq}

Sometimes you need to perform a public host migration for maintenance reasons. If you don't perform this manual migration within the allotted time, the migration happens automatically.

## Why can't I migrate my virtual server?
{: #why-cant-migrate-virtual-server}
{: faq}

You can migrate only private, dedicated hosts. For more information about migrating private, dedicated hosts, see [Migrating a dedicated host instance to another host](/docs/virtual-servers?topic=virtual-servers-migrating-dedicated-host).

## What servers support suspend billing?
{: #what-servers-support-suspend-billing}
{: faq}

Your virtual server instance must be configured with the following settings to support the suspend billing feature.

- Hourly SAN
- A public profile from one of the following families
   - Balanced
   - Compute
   - Memory
   - Variable compute

## How do I change the operating system on my virtual server?
{: #how-change-os-virtual-server}
{: faq}

You can perform an OS reload to change the operating system on your virtual server at any time. For more information about OS reloads, see [Reloading the OS](/docs/bare-metal?topic=bare-metal-reloading-the-os).

## Why do web pages load slowly on Linux?
{: #why-web-page-load-slowly-linux}
{: faq}

Slow loading web pages can be caused by several issues.

- Over-utilization of server resources. Check your monitoring tools to find any potential bottlenecks in server resources.
- Configuration file limits with Apache, PHP, or SQL. For more information, see [Apache configuration files](https://httpd.apache.org/docs/2.4/configuring.html).
- Network latency or packet loss.
   * DoS attack might be targeting services or oversaturating the network.

For more information about troubleshooting Linux network speed issues, see [Using iPerf to Troubleshoot Speed and Throughput Issues](https://www.ibm.com/cloud/blog/using-iperf-to-troubleshoot-speed-and-throughput-issues?mhsrc=ibmsearch_a&mhq=iperf){: external}.

## Why do I have RHEL package issues?
{: #why-rhel-package-issues}
{: faq}

If you experience one of the following RHEL package issues, see the possible solutions.

- Can't download new packages for RHEL servers
- Can't update packages through YUM
- Can't connect to internal {{site.data.keyword.cloud}} YUM repositories

Possible solutions

   1. Check the connectivity of server with IBM DNS servers.
      - Verify that the server is using IBM repositories within its /etc/resolv.conf file (10.0.80.11/12).
      - Test ping DNS server IPS (10.0.80.11 & 10.0.80.12).
   2. Check whether the private network is pinging. A private network is used for YUM updates and downloads, so IBM repositories need to be connected through a private interface.
   3. Allow the proper IP ranges for the back-end network through your gateway and or security groups. For more information, see [Red Hat Enterprise Linux server requirements](/docs/cloud-infrastructure?topic=cloud-infrastructure-ibm-cloud-ip-ranges#red-hat-enterprise-linux-server) and [Getting started with IBM security groups](/docs/security-groups?topic=security-groups-getting-started).
   4. Check your subscription status by using the following commands.

      - `subscription-manager status`

      Expected output

      ```text
      System Status Details
      Overall Status: Current
      ```
      {: screen}

      - `subscription-manager identity`

      If the registration status is “Unknown”, then you need to register the server. To register your server, open a [support case](/docs/virtual-servers?topic=virtual-servers-gettinghelp).

If you need more help, you can [create a case](/docs/virtual-servers?topic=virtual-servers-gettinghelp).
