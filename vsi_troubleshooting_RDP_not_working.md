---

copyright:
  years: 2017, 2024
lastupdated: "2024-08-02"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why isn't RDP working?
{: #vsi-troubleshoot-vs-RDP-not-working}
{: troubleshoot}
{: support}

You can't access your virtual server using RDP.
{: tsSymptoms}

If you can access your server through KVM, but RDP isn't working, it might be caused by one of the following reasons.
{: tsCauses}

- Blocked RDP traffic
- Inadequate client access licenses
- Pending Windows updates
- A security group is blocking RDP traffic
- Xentools removed network configuration
- RDP not running

To attempt to resolve the issue, try the following troubleshooting tasks:
{: tsResolve}

- RDP traffic is blocked

   RDP traffic (port 3389) might be blocked by the Windows&reg; firewall, hardware firewall, or gateway (Vyatta, AT&T, Juniper, Fortigate). Check that your firewall allows RDP port 3389.

   Run the following commands to check whether the ports are open in _powershell_.

   `Test-NetConnection -Port 3389`  \n
   `Get-NetFirewallPortFilter | Where LocalPort -eq 3389`

   For information about generating a per User CALs report, see [Cannot connect to RDS because no RD Licensing servers are available](https://learn.microsoft.com/en-us/troubleshoot/windows-server/remote/cannot-connect-rds-no-license-server){: external}.

- The server has inadequate client access licenses

   RDP might not work because of inadequate client access licenses that are installed on the server. If you don't have enough valid licenses, you might see one of the following messages.

   - `This remote session disconnected because no Remote Desktop License Servers are available to provide a license.`
   - `The remote session disconnected because of an error that is related to licensing in terminal server.`
   - `The remote session disconnected because no Remote Desktop client access licenses are available for this computer.`

   Check whether you used all of your available licenses. For more information, see [Track your Remote Desktop Services client access licenses](https://learn.microsoft.com/en-us/windows-server/remote/remote-desktop-services/rds-track-cals){: external}.

   Your 120 days RDS trial period expired. You can see how many days remain by using the following command.
      `tlsbln.exe`

- The server has pending Windows updates

   If your server has pending Windows updates, install the latest updates, restart the server, and try to access RDP.

- RDP traffic is blocked by a security group

   If you're using a security group, make sure that you allow RDP (port 3389) traffic. For more information, see [Creating security groups and rules](/docs/security-groups?topic=security-groups-creating-security-groups).

   Are your interfaces enabled and connected?
      `netsh interface show interface`

- Xentools removed network configuration

   Sometimes when you update Xentools, your network configuration is removed from both public and private network cards. If the network configuration is removed, you need to log in to the KVM console and put back the IP address, gateway, and DNS settings for both network cards. For more information about applying Xentools, see this [technote](https://www.ibm.com/support/pages/node/6462327){: external}.

- RDP not running

   - Check that RDP is running. Use the following command to see whether RDP is running.

      `Command: net start | find "Remote Desktop Services"`

   - Check whether the interaces are connected by using the following command.

      `netsh interface show interface`

   - Check whether MAC addresses are learned by using the following command.

      `getmac /v`

   For more information, see General Remote Desktop connection troubleshooting](https://learn.microsoft.com/en-us/troubleshoot/windows-server/remote/rdp-error-general-troubleshooting){: external}.
