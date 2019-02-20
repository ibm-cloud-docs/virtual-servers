---



copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Configuring virtual servers
{: #configuring-virtual-servers}

When you have access to your virtual server, ensure that you configure it to meet the needs of your environment.
{:shortdesc}

## Log in
Log in to the [{{site.data.keyword.slportal_full}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} with the credentials that you received in an email when your account was initially created.

## Locate your virtual server
Find your virtual server in the Device List in the {{site.data.keyword.slportal}}. From the Device List, you can manage devices, upgrade devices, or generate bandwidth usage charts. For more information, see [Managing virtual servers](/docs/vsi/vsi_managing.html).

## Record IP addresses and credentials
Keep a log of IP addresses and credentials for the server in a safe location so that you can access them quickly without having to log in to the {{site.data.keyword.slportal}}.
- Individual device IP addresses can be viewed from the Device List.
- Individual device root passwords can be viewed in the device’s Snapshot View. Click the arrow next to the device name to expand the view.
- Multiple device IP addresses can be viewed by using the Download CSV action within the Device List. Select Download CSV from the Settings cog to download a full list of devices and details in spreadsheet format.

## Update software credentials
All software that was loaded onto your device during the provisioning process was assigned temporary credentials. These credentials are viewed and managed on the Passwords tab of each device in the {{site.data.keyword.slportal}}. Use these temporary credentials to access your software for the first time. As a best practice, change the password to your software after you access it for the first time. Use a strong password that consists of a combination of letters, numbers, and symbols.

Optionally, password updates can be stored on the Passwords tab for each device; however, understand that when you store passwords within the {{site.data.keyword.slportal}}, any person with access to the account and appropriate permissions can view passwords that are stored on the Passwords screen.

For more information about viewing and managing your software credentials, see [Managing infrastructure access](/docs/iam/mnginfra.html).

## Access your server on the private network
The private network is the precursor to interacting with your devices through remote desktop (RDP) using SSH and KVM over IP. The VPN Access tool allows for private network connection to either the closest SSL VPN endpoint or to the endpoint of your choice. VPN access is also required to interact with several services that are offered. For more information, see [Getting started with Virtual Private Networking (VPN)](/docs/infrastructure/iaas-vpn/getting-started.html).

## Set up monitoring
Monitoring is primarily used as a resource to check your server’s uptime, but it can also be useful for knowing when to scale. Both Standard Monitoring and Nimsoft Monitoring services are available to cover various monitoring needs. Standard Monitoring, sometimes referred to as “Basic Monitoring,” is generally used in the ping-and-respond method by using either a slow or service ping that is initiated by using the {{site.data.keyword.slportal}}. Nimsoft Monitoring is also referred to as “Advanced Monitoring” and is available in three tiers: Basic, Advanced, and Premium. This service is also accessible through the {{site.data.keyword.slportal}}. For more information, see [Monitoring](/docs/infrastructure/SLmonitoring/monitoring_index.html).

## Secure your system
Hardware firewalls are available to ensure that your device is always secure. Hardware firewalls are provisioned on demand with no downtime. If rules are established properly, a firewall can protect your server from unwanted activity. After you order a firewall, it must be enabled and rules must be set.

For more information, see the following security topic collections.

* [Hardware Firewalls (Shared)](/docs/infrastructure/hardware-firewall-shared/getting-started.html)
* [Hardware Firewalls (Dedicated)](/docs/infrastructure/hardware-firewall-dedicated/getting-started.html)

Security groups are another option for limiting network traffic on your virtual servers. You can use security groups to enact a set of IP filter rules that define how to handle incoming and outgoing traffic to both the public and private interfaces of a virtual server instance. For more information, see [Getting started with security groups](/docs/infrastructure/security-groups/sg_index.html).

## Schedule backups
Backups ensure that your data is safely stored outside of your device and protected if it is lost. The following backup services are available to store your data in a secure location in case you ever need to reload your information onto your device:
<<<<<<< HEAD
- EVault backup is an automated, agent-based backup system. This is a popular “set-and-forget” solution for managing your device. It is compatible with Microsoft software including Exchange and SQL through extra plug-ins. EVault users interact with this service through EVault’s WebCC web-based application. For more information, see [Getting Started with Backup Services](/docs/infrastructure/Backup/index.html).
- R1Soft Continuous Data Protection is backup software that can be installed on your server or self-managed virtual machine. It is recommended if you want a single interface to manage all of your backups. You interact with R1Soft CDP through your proprietary management system, which allows agents to be installed on virtual machines and offers database plug-ins for extra functions. For more information, see [Getting Started with Backup Services](/docs/infrastructure/Backup/index.html).
=======
- {{site.data.keyword.backup_notm}} is an automated, agent-based backup system. This is a popular “set-and-forget” solution for managing your device. It is compatible with Microsoft software including Exchange and SQL through extra plug-ins. {{site.data.keyword.backup_notm}} users interact with this service through {{site.data.keyword.backup_notm}}’s WebCC web-based application. For more information, see [Getting started with {{site.data.keyword.backup_notm}} services](/docs/infrastructure/Backup.index.html).
- R1Soft Continuous Data Protection is backup software that can be installed on your server or self-managed virtual machine. It is recommended if you want a single interface to manage all of your backups. You interact with R1Soft CDP through your proprietary management system, which allows agents to be installed on virtual machines and offers database plug-ins for extra functions. For more information, see [Getting started with {{site.data.keyword.backup_notm}} services](/docs/infrastructure/Backup.index.html).
>>>>>>> origin/master

## Next Steps
After your virtual server is configured, you can start managing it. For more information, see [Managing your virtual server](/docs/vsi/vsi_managing.html).
