---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-25"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Configuring virtual servers
{: #configuring-virtual-servers}

When you have access to your virtual server, be sure to change your password and consider setting up SSH for a more secure authentication solution. There are many other options for configuring your virtual server to meet the needs of your environment.
{:shortdesc}

## Log in
Log in to the [{{site.data.keyword.cloud}} console ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/classic?){: new_window} with the credentials that you received in an email when your account was initially created. Alternatively, you can log in to the [{{site.data.keyword.slportal}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){:new_window}.

## Locate your virtual server
Find your virtual server in the Device List in the {{site.data.keyword.cloud_notm}} console. From the Device List, you can manage devices, upgrade devices, or generate bandwidth usage charts. For more information, see [Managing virtual servers](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).

## Change your password
Change your password using strong password guidelines. See [Viewing and managing device user names and passwords](/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device#view-update-user-name-password-for-device).

## Configure SSH
SSH provides better security solution than password authentication. See [Getting started with SSH keys](/docs/infrastructure/ssh-keys?topic=ssh-keys-getting-started-tutorial#getting-started-tutorial).

## Record IP addresses and credentials
Keep a log of IP addresses and credentials for the server in a safe location so that you can access them quickly without having to log in to the {{site.data.keyword.cloud_notm}} console.
- Individual device IP addresses can be viewed from the Device List.
- Individual device root passwords can be viewed in the device’s Snapshot View. Click the arrow next to the device name to expand the view.
- Multiple device IP addresses can be viewed by using the Download CSV action within the Device List. Select Download CSV from the Settings cog to download a full list of devices and details in spreadsheet format.

## Update software credentials
All software that was loaded onto your device during the provisioning process was assigned temporary credentials. These credentials are viewed and managed on the Passwords tab of each device in the {{site.data.keyword.cloud_notm}} console. Use these temporary credentials to access your software for the first time. As a best practice, change the password to your software after you access it for the first time. Use a strong password that consists of a combination of letters, numbers, and symbols.

Optionally, password updates can be stored on the Passwords tab for each device; however, understand that when you store passwords within the {{site.data.keyword.cloud_notm}} console, any person with access to the account and appropriate permissions can view passwords that are stored on the Passwords screen.

For more information about viewing and managing your software credentials, see [Managing classic infrastructure access](/docs/vsi?topic=iam-mngclassicinfra).

## Access your server on the private network
The private network is the precursor to interacting with your devices through remote desktop (RDP) using SSH and KVM over IP. The VPN Access tool allows for private network connection to either the closest SSL VPN endpoint or to the endpoint of your choice. VPN access is also required to interact with several services that are offered. For more information, see [Getting started with Virtual Private Networks (VPN)](/docs/iaas-vpn?topic=VPN-getting-started).

## Set up monitoring
Monitoring is primarily used as a resource to check your server’s uptime, but it can also be useful for knowing when to scale. Both Standard Monitoring and Nimsoft Monitoring services are available to cover various monitoring needs. Standard Monitoring, sometimes referred to as “Basic Monitoring,” is generally used in the ping-and-respond method by using either a slow or service ping that is initiated by using the {{site.data.keyword.cloud_notm}} console. Nimsoft Monitoring is also referred to as “Advanced Monitoring” and is available in three tiers: Basic, Advanced, and Premium. This service is also accessible through the {{site.data.keyword.cloud_notm}} console. For more information, see [Monitoring](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring#monitoring).

## Configure security groups
You can use security groups to limit network traffic on your virtual servers. Use security groups to enact a set of IP filter rules that define how to handle incoming and outgoing traffic to both the public and private interfaces of a virtual server instance. For more information, see [Getting started with security groups](/docs/infrastructure/security-groups?topic=security-groups-getting-started).

## Configure firewalls
Hardware firewalls are also available for even more protection. Hardware firewalls are provisioned on demand with no downtime. If rules are established properly, a firewall can protect your server from unwanted activity. After you order a firewall, it must be enabled and rules must be set.

For more information, see the following information.

* [Hardware Firewalls (Shared)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Hardware Firewalls (Dedicated)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)

## Schedule backups
Backups ensure that your data is safely stored outside of your device and protected if it is lost. The following backup services are available to store your data in a secure location in case you ever need to reload your information onto your device:
- {{site.data.keyword.backup_notm}} is an automated, agent-based backup system. This is a popular “set-and-forget” solution for managing your device. It is compatible with Microsoft software including Exchange and SQL through extra plug-ins. {{site.data.keyword.backup_notm}} users interact with this service through {{site.data.keyword.backup_notm}}’s WebCC web-based application. For more information, see [Getting started with {{site.data.keyword.backup_notm}} services](/docs/infrastructure/Backup?topic=Backup-getting-started).
- R1Soft Continuous Data Protection is backup software that can be installed on your server or self-managed virtual machine. It is recommended if you want a single interface to manage all of your backups. You interact with R1Soft CDP through your proprietary management system, which allows agents to be installed on virtual machines and offers database plug-ins for extra functions. For more information, see [Getting started with {{site.data.keyword.backup_notm}} services](/docs/infrastructure/Backup?topic=Backup-getting-started).

## Next steps
After your virtual server is configured, you can start managing it. For more information, see [Managing your virtual server](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
