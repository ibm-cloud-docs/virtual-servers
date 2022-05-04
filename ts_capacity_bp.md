---

copyright:
  years: 2017, 2022
lastupdated: "2022-05-03"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:external: target="_blank" .external}
{:support: data-reuse='support'}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Troubleshooting your virtual server
{: #troubleshooting-virtual-server}

The following topics cover common difficulties that you might encounter, and offers some helpful tips.

## Why can't I log in to a virtual server through SSH?
{: #troubleshoot-vs-cannot-ssh-into-server}
{: troubleshoot}
{: support} 

If you can't log in to a server through SSH, it might be caused by one of the following reasons.

* [Remote logins through SSH for root are disabled](#remote-ssh-logins-disabled)
* [Port not configured for SSH](#port-number-configuration)
* [Firewall is blocking SSH traffic](#firewall-blocking-ssh-traffic)
* [Security group is blocking SSH traffic](#security-group-blocking-ssh-traffic)

### Remote logins through SSH for root are disabled
{: #remote-ssh-logins-disabled}

Remote logins through SSH for root might be disabled in the SSH configuration (_/etc/ssh/sshd_config_) of your server. Use the following instructions to enable SSH for root login.

For security reasons, we recommended that you don't enable root for remote SSH logins. Instead, create a nonroot user for remote SSH login.
{: important} 

1. Log in to KVM IPMI console for your virtual server. 
2. As root, edit the _sshd_config_ file in _/etc/ssh/sshd_config_ 

   `nano /etc/ssh/sshd_config`
   {: pre}
    
3. Add a line in the **Authentication** section of the file that says _PermitRootLogin yes_. This line might exist and be commented out with a "#". In this example, remove the "#".

  
   `#LoginGraceTime 2m`

   `PermitRootLogin yes`

   `#StrictModes yes`

   `#MaxAuthTries 6`

   `#MaxSessions 10`

Save the updated /etc/ssh/sshd_config file.    

Restart sshd service on an Ubuntu or Debian Linux by using the following command:    
*sudo systemctl restart ssh.service*  

RHEL and CentOS Linux users, run the following command:  
*sudo systemctl restart sshd.service* 

### Port not configured for SSH
{: #port-number-configuration}

Check the port number that is configured for SSH in the _/etc/ssh/sshd_config_ file. By default, SSH is configured with port 22. However, for security reasons, your administrator might change the port.

### Firewall is blocking SSH traffic
{: #firewall-blocking-ssh-traffic}

SSH port traffic might be blocked by your firewall. For more information, see [Allowing SSH and pinging to a public subnet](/docs/vsrx?topic=vsrx-allowing-ssh-and-pinging-to-a-public-subnet).

### Security group is blocking SSH traffic
{: #security-group-blocking-ssh-traffic}

If you use a security group to protect your virtual servers, you need to allow SSH traffic. For more information, see [Creating security groups and rules](/docs/security-groups?topic=security-groups-creating-security-groups).

## Why is my server not responding? (server not pinging)
{: #troubleshoot-vs-device-not-responding}
{: troubleshoot}
{: support} 

If you can't access your server, you can use the following prechecks to help get a response.

* Try to access the server through the KVM IPMI console.  
* If you can't access the server through the KVM IPMI console, then the ping traffic might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate). Ask your administrator to check the firewall rules. For help with setting up firewall rules, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).  
* If you're using security group, you need to allow ICMP traffic. For more information, see [Creating security groups and rules](/docs/security-groups?topic=security-groups-creating-security-groups).  

## Why can't I access KVM through a browser?
{: #troubleshoot-vs-KVM-not-accessible-browser}
{: troubleshoot}
{: support}

If you are unable to connect to the KVM console, review the following troubleshooting tips for help. For more information about accessing the KVM, see [Accessing the KVM console for virtual servers](/docs/virtual-servers?topic=virtual-servers-access-kvm-console).

* [Browser or Java needs updating](#update-browser-and-java)
* You haven’t [established a VPN connection](#vpn-connection)
* Your [credentials are invalid](#check-credentials)
* You need to [install TightVNC viewer](#install-tightVNC-viewer)

### Browser or Java needs updating
{: #update-browser-and-java}

Make sure that you're using a supported browser. For more information about {{site.data.keyword.cloud}}-supported browsers, see [Browsers](/docs/overview?topic=overview-prereqs-platform#browsers-platform).

The KVM Console opens in a new browser tab or window. If the KVM Console doesn't open, check the browser for any blocked new windows.

If you can't access KVM through your browser, you might need to update your browser and or Java. Update your browser and Java and try to access KVM.

### A VPN connection isn't established
{: #vpn-connection}

Make sure that a connection is established by using the VPN. If a connection isn't established, a warning displays that a VPN connection is required. For more information, see [Getting started with IBM Cloud Virtual Private Networking](/docs/iaas-vpn?topic=iaas-vpn-getting-started).

### Your credentials are invalid
{: #check-credentials}

Check that the credentials for the device are valid. Contact the account administrator to verify credentials, if necessary.

### You need to install TightVNC viewer
{: #install-tightVNC-viewer}

If you still can't access KVM, you need to install TightVNC viewer. For more information about installing TightVNC viewer, see [How to connect to {{site.data.keyword.BluVirtServers}} KVM console](/docs/virtual-servers?topic=virtual-servers-access-kvm-console). 

If you still can't access KVM, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).

## Why isn't RDP working?
{: #troubleshoot-vs-RDP-not-working}
{: troubleshoot}
{: support}

If you can access your server through KVM, but RDP isn't working, it might be caused by one of the following reasons. 

* [Blocked RDP traffic](#blocked-RDP-traffic)
* [Inadequate client access licenses](#inadequate-client-access-licenses)
* [Pending Windows updates](#pending-windows-updates)
* [A security group is blocking RDP traffic](#security-group-blocking-rdp-traffic)

### RDP traffic is blocked
{: #blocked-RDP-traffic}

RDP traffic (port 3389) might be blocked by the Windows firewall, hardware firewall, or gateway (Vyatta, AT&T, Juniper, Fortigate). Check that your firewall allows RDP port 3389.

### The server has inadequate client access licenses
{: #inadequate-client-access-licenses}

RDP might not work because of inadequate client access licenses that are installed on the server. For more information, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).

### The server has pending Windows updates
{: #pending-windows-updates}

If your server has pending Windows updates, install the latest updates, restart the server, and try to access RDP.  

### RDP traffic is blocked by a security group
{: #security-group-blocking-rdp-traffic}

If you're using a security group, make sure that you allow RDP (port 3389) traffic. For more information, see [Creating security groups and rules](/docs/security-groups?topic=security-groups-creating-security-groups).

## Why can't I connect to a server through the public IP?
{: #troubleshoot-vs-cannot-connect-public-ip}
{: troubleshoot}
{: support}

Public traffic might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate). 

If the firewall isn't an issue, check whether the public gateway IP is configured for the public network card and try pinging the public gateway. For more help, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).

## Why is the internet disconnected?
{: #troubleshoot-vs-internet-disconnected}
{: troubleshoot}
{: support}

If your internet is disconnected, it might be caused by one of the following reasons.

* [Internet is blocked by firewall or gateway](#internet-blocked-by-firewall-or-gateway)
* [Public gateway IP configuration](#public-gateway-ip-configuration)
* [No ping from DNS servers](#ping-DNS-servers)

### Internet is blocked by firewall or gateway
{: #internet-blocked-by-firewall-or-gateway}

If you can't access the internet, your internet access might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate).

### Public gateway IP isn't configured for the network card
{: #public-gateway-ip-configuration}

If firewall is not an issue, check whether the public gateway IP is configured for the public network card and try pinging the public gateway. For more help, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).

### No ping from DNS servers
{: #ping-DNS-servers}

Check whether you can ping IBM DNS servers (_10.0.80.11_, _10.0.80.12_), if you configured DNS servers for the public network card.

If you have Linux servers, add the following entries in the _/etc/resolv.conf_ file:

`nameserver 10.0.80.11` and `nameserver 10.0.80.12` 

## Why does the portal show that my server is disconnected even though it's running?
{: #troubleshoot-vs-portal-shows-server-disconnected-but-running}
{: troubleshoot}
{: support}

If your portal shows that the server is disconnected, but the server is running, it might be caused by one of the following reasons.

* [Your firewall or gateway rules are blocking ping](#firewall-or-gateway-rules-blocking-ping)
* [A security group is blocking ping](#security-group-blocking-ping)

### Firewall or gateway rules are blocking the ping
{: #firewall-or-gateway-rules-blocking-ping}

If your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate) blocks ping traffic, then the status of your servers shows "disconnected" in the portal. Check that your firewall rules allow ping traffic from {{site.data.keyword.cloud}} IP ranges. For more information about IP ranges, see [{{site.data.keyword.cloud}} IP ranges](/docs/cloud-infrastructure?topic=cloud-infrastructure-ibm-cloud-ip-ranges).

### Security group is blocking the ping
{: #security-group-blocking-ping}

If you're using a security group, make sure that you allow ping traffic from the {{site.data.keyword.cloud}} IP ranges. For more information, see [Creating security groups and rules](/docs/security-groups?topic=security-groups-creating-security-groups)

## Why is my migration not working?
{: #troubleshoot-migration-stuck}

If your migration is stuck or didn't complete properly, create a [support case](/docs/get-support?topic=get-support-get-supportfaq#open-support-case) for assistance. 

## Resource considerations for virtual server instances
{: #capacity-considerations}
{: troubleshoot}
{: support}

### What's happening
{: #what-s-happening}

When you provision a virtual server, you might receive the following error message:

_Insufficient capacity to complete the request._

When provisioning fails, all the virtual server instances within that particular request fail.
{: tip}

### Why it's happening
{: #why-error}

An error occurs when the router or data center has insufficient available resources to fulfill the service request. Resource availability changes frequently, so you might wait and try again later.

### How to fix it
{: #how-to-fix-error}

You can attempt to provision again by using the following strategies:

* Provision specifying a different router.  
* Provision without specifying a router.
* Provision in a different data center.

   You can provision GPUs only in the following data centers: dal10, dal12, dal13, lon04, lon06, wdc07, tok02, syd04, and fra02
   {: note}

* Provision fewer instances.
* Spread out instances by provisioning to multiple data centers.
* Provision smaller instance sizes.
* Alter the instance storage from SAN to LOCAL or LOCAL to SAN.

## Why can't I view the password for a recently provisioned virtual server even though you have the correct permissions?
{: #troubleshoot-view-password}
{: troubleshoot}
{: support}

### Why it's happening
{: #why-cant-view-password}

 This problem can occur if a firewall prevents the provisioning framework from updating the password value.

### How to fix it
{: #how-to-fix-view-password}

* _Option 1_: Update the firewall to allow the IBM Cloud service IP ranges as described in the firewall [documentation](/docs/vsrx?topic=hardware-firewall-shared-ibm-cloud-ip-ranges){: external}. These ranges allow for provisioning, monitoring, and management. Restart the server so the provisioning network to populate the password in the portal.
* _Option 2_: Bypass the VLAN of the server from the firewall. Then, restart the server to allow provisioning network to populate the password in the portal and then route the VLAN back in the firewall.

## Why is my virtual server read-only?
{: #troubleshoot-vs-why-vs-read-only}
{: troubleshoot}
{: support} 

### Why it's happening
{: #why-vs-read-only}

A virtual server might receive a read-only issue because of unplanned networking incidents or outages.

### How to fix it
{: #how-to-fix-vs-read-only}

To bring back your server from a read-only status, you need to restart the server to rescue kernel and you need to run a file system check on all your file systems.

1. From your device list, click the **name of the server** > **Actions menu** > **Rescue kernel**.
2. When your server restarts in rescue mode, log in to the server by using SSH with the root user credentials.
3. Run a file system check by using the following command:
   `fsck -y -C /dev/xvda1`
4. Run the same command if you have more files systems such as _/dev/xvda2_, _/dev/xvda3_, and so on. 

For more help, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp) or open a support case. 

Running a file system check might cause data loss, so make sure that your data is backed up.
{: note}
