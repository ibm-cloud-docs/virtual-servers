---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-23"

keywords:

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# FAQ: Servers (general)
{: #faqs-servers-general-}

## My virtual server is down. What do I do?
{: #my-virtual-server-is-down-what-should-i-do}

If your virtual server is down, use the following steps to bring it back up:

1. Try to access the server by using the [KVM console](/docs/virtual-servers?topic=virtual-servers-access-kvm-console). Depending on the output, you might need to create a [support case](/docs/virtual-servers?topic=virtual-servers-virtual-server-help-and-support).
2. Try to power your server off and on. For more information, see [Powering a server on or off](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#power-on-off) or [Rebooting a device](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#reboot).

   * [Why can't I log in to a virtual server through SSH?](/docs/virtual-servers?topic=virtual-servers-vsi-troubleshoot-vs-cannot-ssh-into-server)
   * [Why is my server not responding?](/docs/virtual-servers?topic=virtual-servers-vsi-troubleshoot-vs-device-not-responding)
   * [Why does the portal show that my server is disconnected even though it's running?](/docs/virtual-servers?topic=virtual-servers-vsi-troubleshoot-vs-portal-shows-server-disconnected-but-running)

For more help, see [Getting help and support](/docs/virtual-servers?topic=virtual-servers-virtual-server-help-and-support).

## What do I do if my bare metal server is down?
{: #my-bare-metal-server-is-down-what-should-i-do}

If your bare metal server is down, use the following steps.

1. Remotely access the server by using [IPMI](/docs/bare-metal?topic=bare-metal-bm-faq#how-do-i-use-ipmi). Depending on the output, you might need to create a [support case](/docs/virtual-servers?topic=virtual-servers-virtual-server-help-and-support).

If your server does not power on, you might need to start your server in rescue mode. For more information, see [Rescue mode](/docs/virtual-servers?topic=virtual-servers-launching-rescue)

For more help, see [Getting help and support](/docs/virtual-servers?topic=virtual-servers-virtual-server-help-and-support).

## Why does my server status show "disconnected"?
{: #server-status-shows-disconnected}

If your server status shows "disconnected", it might mean that the network monitoring service can't ping your device. Your server might be disconnected for several reasons - such as a network configuration, firewall, or a hardware issue.

For more information about monitoring, see [Basic Monitoring](/docs/cloud-infrastructure?topic=cloud-infrastructure-monitoring-iaas#basic-monitoring).

If you need more help, see [Getting help and support](/docs/virtual-servers?topic=virtual-servers-virtual-server-help-and-support).

## What is the difference between "Boot from image" and "Load from image"?
{: #what-is-the-difference-between-boot-from-image-and-load-from-image-}

*Boot from image* and *Load from image* both use image templates, which are applied to a device to either replace or supplement the existing operating system to help remedy an existing issue. The main difference between the Boot and Load process is the type of image that is used. When either the boot or load from image process is used, make sure that you back up all data that you might want to recover.

* *Boot from image* starts a device by using an ISO supplied by {{site.data.keyword.BluSoftlayer_full}} for system recovery or an ISO that was uploaded by using the *Import image* feature in the {{site.data.keyword.cloud_notm}} console. The ISO might be a clean version of the device operating system or a recovery disk that is used in an attempt to remedy an issue with the device.
* *Load from image* is a method of OS reload that uses an image template that was either captured from a device or uploaded by using the *Image import* feature in the {{site.data.keyword.cloud_notm}} console. *Load from image* uses a VHD that wipes the device of all data and replaces the existing operating system and files with a "like new" version of the selected image.

## I lost my password to my server. How can I recover it?
{: #i-lost-my-password-to-my-server-how-can-i-recover-it-}

If the root or administrator password to your server is suddenly not working, check the following items. If necessary, use the instructions to start rescue mode and reset your password.

* Are you copying and pasting the password? If not, try to. Also, paste the password in a notepad to make sure that no spaces are copied with the password.
* If the server has cPanel, it's possible that cPHulk blocked your IP address due to failed logins. You can access the server by using the KVM or IPMI and allowlist your IP address. Use cPHulk with "/scripts/cphulkdwhitelist" followed by your IP address.
* Has someone recently tried to change the password for the server by modifying the password in the {{site.data.keyword.cloud_notm}} console? Changing the password in the {{site.data.keyword.cloud_notm}} console changes what you see as the password. It doesn't change the server password. If so, you can contact [Support](/docs/get-support?topic=get-support-using-avatar) and they can usually recover the original, working password.
* You might need to start into rescue mode to reset your password. For more information, see [Rescue mode](/docs/virtual-servers?topic=virtual-servers-launching-rescue#launching-rescue).

If still can't connect to the server by using the password, open a [support case](/docs/get-support?topic=get-support-using-avatar#getting-support) and request a password reset. Support needs to restart the server to reset the password, so prepare to approve the restart and set a maintenance time frame for completion. Most password resets are completed in ~15 minutes. In the {{site.data.keyword.cloud_notm}} console, you can create a support case by going to **Support > Create a case** and use the subject *Accounts and access*.

## How do I cancel a device?
{: #how-to-cancel-device}

You can cancel a device at any time. Go to the [Device List](https://cloud.ibm.com/classic/devices). Click **Actions** for the device that you want to cancel, and select the cancel option from the menu. For more information, see [Canceling virtual servers](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#cancel).

## Are LVM partitions supported as a valid file system?
{: #are-lvm-partitions-supported-as-a-valid-filesystem-}

LVM (Logical Volume Management) provides logical management of Linux file systems. In the {{site.data.keyword.BluSoftlayer}} environment, LVM isn't supported as a bootable partitioning scheme. Virtual server instances can't be ordered with LVM, and importing images that use LVM as a boot partition fail to provision. If you require LVM on the boot partition, bare metal servers can support LVM on boot for certain operating systems. With proper OS support and configuration, secondary virtual server instance disks can be used for LVM partitions. However, it is important to note that LVM isn't a supported file system for *Flex Image* or *Image Templates*. For more assistance, [contact support](/docs/get-support?topic=get-support-using-avatar).

## Preconfigured `161.26.0.0/16` routes on customer hosts
{: #preconfigured-161-26-0-0-16-routes-on-customer-hosts}

{{site.data.keyword.BluSoftlayer_notm}} is enabling a new route on all newly provisioned servers to support future products.

* The route points to any address in the 161.26.0.0/16 range (161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255) to the backend private network.
* This IP block is assigned to {{site.data.keyword.BluSoftlayer_notm}} by IANA and isn't advertised on the public internet.
* Only {{site.data.keyword.BluSoftlayer_notm}} systems are addressed out of this space.
* ACLs on customer servers, virtual servers, and Vyatta gateways need to be updated to allow customer's hosts to use Infrastructure services that are configured with IP addresses out of this range.

## How do I add the new routing for an operating system?
{: #how-to-add-the-new-routing-for-various-oses}

Use the following table for OS-specific routing information.

| Operating system | Steps |
|-----|-----|
| CentOS | Create a route by editing or creating the following file: `/etc/sysconfig/network-scripts/route-eth0` Replace 10.0.0.1 with your private gateway IP address. After you create that file, you must add the following information: _161.26.0.0/16 through 10.0.0.1 |
| Debian | In the `/etc/network/interfaces` file, add the following line at the end of the file: `up route add -net 161.26.0.0/16 gw 10.0.0.1` Replace 10.0.0.1 with your private gateway IP address. |
| Microsoft Windows |  Add the persistent route from the command line by entering the following address: `route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p` Replace 10.0.0.1 with your private gateway IP address. |
| Red Hat | Create a route by editing or creating the following file: `/etc/sysconfig/network-scripts/route-eth0` Replace 10.0.0.1 with your private gateway IP address. After you create that file, you must add the following information: _161.26.0.0/16 through 10.0.0.1 |
| Ubuntu | In the `/etc/network/interfaces` file, add the following line at the end of the file: `up route add -net 161.26.0.0/16 gw 10.0.0.1` Replace 10.0.0.1 with your private gateway IP address. |
| VMWare ESXi| Use the following command to add the route to the ESXi host: `esxcfg-route -a 161.26.0.0/16 10.0.0.1`. Replace 10.0.0.1 with your private gateway IP address. |
{: caption="Table 1. OS-specific routing information" caption-side="top"}

## What is a cvsup mirror?
{: #what-is-a-cvsup-mirror-}

You can update against a local cvsup mirror that was run for you. Make sure that the sup file has the following entry.

```text
*default host=cvsup.service.softlayer.com
```
{: pre }

The distfiles are also mirrored and available from [The FreeBSD Project](https://www.freebsd.org/){: external}. You can add the following line into your */etc/make.conf* file to attempt to download from the local repository.

```text
MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"
```
{: screen }

If the file is not found there, the path follows the individual port makefile and moves to the next mirror.
