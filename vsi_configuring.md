---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-23"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Configuring virtual servers
{: #configuring-virtual-servers}

When you have access to your virtual server, make sure that you change your password and consider setting up SSH for a more secure authentication solution. You have many other options for configuring your virtual server to meet the needs of your environment.
{: shortdesc}

Before you configure a virtual server, review your options for connecting to the server and how to manage passwords and credentials. For more information, see [Getting started with IBM Cloud Virtual Private Networking](/docs/iaas-vpn?topic=iaas-vpn-getting-started) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).
{: note}

## Log in
{: #log-in}

Log in to the [{{site.data.keyword.cloud}} console](https://cloud.ibm.com/classic?){: external} with the credentials that you received in an email when your account was initially created.

### Locate your virtual server
{: #locate-your-virtual-server}

Find your virtual server in the Device List in the {{site.data.keyword.cloud_notm}} console. From the Device List, you can manage devices, upgrade devices, or generate bandwidth usage charts. For more information, see [Managing virtual servers](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).

### Change your password
{: #change-your-password}

Change your password by using strong password guidelines. See [Viewing and managing device usernames and passwords](/docs/virtual-servers?topic=virtual-servers-view-update-user-name-password-for-device#view-update-user-name-password-for-device).

### Manage SSH keys
{: #configure-ssh}

SSH provides a better security solution than password authentication. See [Getting started with SSH keys](/docs/ssh-keys?topic=ssh-keys-getting-started-tutorial#getting-started-tutorial).

### Record IP addresses and credentials
{: #record-ip-addresses-and-credentials}

Keep a log of IP addresses and credentials for the server in a safe location so that you can access them quickly without having to log in to the {{site.data.keyword.cloud_notm}} console.
- Individual device IP addresses can be viewed from the Device List.
- Individual device root passwords can be viewed in the device’s Snapshot View. Click the arrow next to the device name to expand the view.
- Multiple device IP addresses can be viewed by using the Download CSV action within the Device List. Select Download CSV from the Settings cog to download a full list of devices and details in spreadsheet format.

### Update software credentials
{: #update-software-credentials}

All software that was loaded onto your device during the provisioning process was assigned temporary credentials. These credentials are viewed and managed on the Passwords tab of each device in the {{site.data.keyword.cloud_notm}} console. Use these temporary credentials to access your software for the first time. As a best practice, change the password to your software after you access it for the first time. Use a strong password that consists of a combination of letters, numbers, and symbols.

Optionally, password updates can be stored on the Passwords tab for each device. However, understand that when you store passwords within the {{site.data.keyword.cloud_notm}} console, any person with access to the account and appropriate permissions can view passwords that are stored on the Passwords screen.

For more information about viewing and managing your software credentials, see [Managing classic infrastructure access](/docs/account?topic=account-mngclassicinfra).

### Access your server on the private network
{: #access-your-server-on-the-private-network}

The private network is the precursor to interacting with your devices through remote desktop (RDP) by using SSH and KVM over IP. The VPN Access tool allows for private network connection to either the closest SSL VPN endpoint or to the endpoint of your choice. VPN access is also required to interact with several services that are offered. For more information, see [Getting started with Virtual Private Networks (VPN)](/docs/iaas-vpn?topic=iaas-vpn-getting-started).

## Set up monitoring
{: #set-up-monitoring}

Monitoring is primarily used as a resource to check your server’s uptime, but it can also be useful for knowing when to scale. {{site.data.keyword.mon_full_notm}} services are available to cover various monitoring needs. Standard Monitoring, sometimes referred to as “Basic Monitoring,” is generally used in the ping-and-respond method by using either a slow or service ping that is initiated by using the {{site.data.keyword.cloud_notm}} console. {{site.data.keyword.mon_full_notm}} keeps you aware of any issues with your devices. {{site.data.keyword.mon_full_notm}} gives you insight into the performance and health of your applications, services, and platforms. Your administrators, DevOps teams, and developers have a full-stack telemetry with advanced features to help them monitor and troubleshoot, define alerts, and design custom dashboards. For more information, see [{{site.data.keyword.mon_full_notm}}](/docs/cloud-infrastructure?topic=cloud-infrastructure-monitoring-iaas).

## Configure security groups
{: #configure-security-groups}

You can use security groups to limit network traffic on your virtual servers. Use security groups to enact a set of IP filter rules that define how to handle incoming and outgoing traffic to both the public and private interfaces of a virtual server instance. For more information, see [Getting started with security groups](/docs/security-groups?topic=security-groups-getting-started).

## Configure firewalls
{: #configure-firewalls}

Hardware firewalls are also available for even more protection. Hardware firewalls are provisioned on demand with no downtime. If rules are established properly, a firewall can protect your server from unwanted activity. After you order a firewall, it must be enabled and rules must be set.

For more information, see the following information.

* [Hardware Firewalls (Shared)](/docs/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)

## Schedule backups
{: #schedule-backups}

Backups make sure that your data is safely stored outside of your device and protected if it is lost. The following backup services are available to store your data in a secure location in case you ever need to reload your information onto your device:

- {{site.data.keyword.backup_notm}} is an automated, agent-based backup system. This backup system is a popular “set-and-forget” solution for managing your device. It is compatible with Microsoft software that includes Exchange and SQL through extra plug-ins. {{site.data.keyword.backup_notm}} users interact with this service through {{site.data.keyword.backup_notm}}’s WebCC web-based application. For more information, see [Getting started with {{site.data.keyword.backup_notm}} services](/docs/Backup?topic=Backup-getting-started).
- R1Soft&reg; Continuous Data Protection is backup software that can be installed on your server or self-managed virtual machine. It is recommended if you want a single interface to manage all of your backups. You interact with R1Soft&reg; CDP through your proprietary management system, which allows agents to be installed on virtual machines and offers database plug-ins for extra functions. For more information about R1Soft&reg; CDP backup services, see the [R1Soft&reg; Documentation](https://wiki.r1soft.com/display/ServerBackup.html){: external}.

## Next steps
{: #next-steps-configuring-virtual-servers}

After your virtual server is configured, you can start managing it. For more information, see [Managing your virtual server](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
