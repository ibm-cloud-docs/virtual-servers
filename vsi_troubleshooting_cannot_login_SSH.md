---

copyright:
  years: 2017, 2023
lastupdated: "2023-09-28"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I log in to a virtual server through SSH?
{: #vsi-troubleshoot-vs-cannot-ssh-into-server}
{: troubleshoot}
{: support}

You are unable to log into the virtual server using SSH.
{: tsSymptoms}

There are several different reasons why you can't log into the virtual server using SSH.
{: tsCauses}

* Remote logins through SSH for root are disabled.
* Port not configured for SSH
* Firewall is blocking SSH traffic
* Security group is blocking SSH traffic

To attempt to resolve the login issues using SSH, try the following troubleshooting tasks:
{: tsResolve}

* Remote logins through SSH for root are disabled

   Remote logins through SSH for root might be disabled in the SSH configuration (_/etc/ssh/sshd_config_) of your server. Use the following instructions to enable SSH for root login.

   For security reasons, we recommended that you don't enable root for remote SSH logins. Instead, create a nonroot user for remote SSH login.
   {: important}

   1. Log in to KVM IPMI console for your virtual server.
   1. As root, edit the _sshd_config_ file in _/etc/ssh/sshd_config_

      `nano /etc/ssh/sshd_config`
      {: pre}

   1. Add a line in the **Authentication** section of the file that says _PermitRootLogin yes_. This line might exist and be commented out with a "#". In this example, remove the "#".

      `#LoginGraceTime 2m`

      `PermitRootLogin yes`

      `#StrictModes yes`

      `#MaxAuthTries 6`

      `#MaxSessions 10`

   1. Save the updated /etc/ssh/sshd_config file.

   1. Restart sshd service.
  
      * For Ubuntu or Debian Linux, run `sudo systemctl restart ssh.service`.
      * RHEL and CentOS Linux users, run `sudo systemctl restart sshd.service`.

* Port not configured for SSH

   Check the port number that is configured for SSH in the `/etc/ssh/sshd_config` file. By default, SSH is configured with port 22. However, for security reasons, your administrator might change the port.

* Firewall is blocking SSH traffic

   SSH port traffic might be blocked by your firewall. For more information, see [Allowing SSH and pinging to a public subnet](/docs/vsrx?topic=vsrx-allowing-ssh-and-pinging-to-a-public-subnet).

* Security group is blocking SSH traffic

   If you use a security group to protect your virtual servers, you need to allow SSH traffic. For more information, see [Creating security groups and rules](/docs/security-groups?topic=security-groups-creating-security-groups).
