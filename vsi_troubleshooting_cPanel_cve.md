---

copyright:
  years: 2026, 2026
lastupdated: "2026-05-12"

keywords: troubleshoot virtual server, virtual server troubleshooting, cPanel CVE

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# What do I do if I suspect my server is affected by a cPanel vulnerability?
{: #troubleshoot-cPanel-cve}
{: troubleshoot}
{: support}

If you suspect that an {{site.data.keyword.BluVirtServers}} for Classic is affected by a cPanel security vulnerability, you need to update to the most recent cPanel version and change the server password. If the server is compromised, you need to also reload the operating system or restore from backup.
{: shortdesc}

You received a notification from {{site.data.keyword.cloud}} alerting you to a CVE from cPanel that might compromise your server. Or you discover that you can't access the server, unable to log in as root, or with WHM.
{: tsSymptoms}

cPanel, a third-party vendor that provides an add-on for {{site.data.keyword.BluVirtServers}} for Classic, published a critical CVE on 28 April 2026 for an authentication bypass vulnerability that might compromise your root password and cPanel environment.
{: tsCauses}

Review the article provided by cPanel: [Security: CVE-2026-41940 - cPanel and WHM / WP2 Security Update 28 April 2026](https://support.cpanel.net/hc/en-us/articles/40073787579671-Security-CVE-2026-41940-cPanel-WHM-WP2-Security-Update-04-28-2026){: external}.
{: tsResolve}

Follow its instructions to update your environment immediately with the most recent patch and to determine whether your server is compromised. As a best practice, change the root password for the server. If you determine that the server is compromised, then you need to reload the operating system or restore from backup to recover the server.

## Update to the most recent cPanel version
{: #update-latest-cpanel-version}

Follow the instructions in the [CVE-2026-41940 article](https://support.cpanel.net/hc/en-us/articles/40073787579671-Security-CVE-2026-41940-cPanel-WHM-WP2-Security-Update-04-28-2026){: external} to update your environment immediately with the most recent patch. The version of cPanel that is available through the {{site.data.keyword.cloud}} portal is the most recent patched version.

## Access the server and change the password
{: #access-server-and-change-password}

To maintain a secure environment, change the root password. If you can't log in as root, reset the password from the {{site.data.keyword.cloud}} console.

To reset the password, follow these steps:

1. Start rescue mode on the device. Refer to [Starting rescue mode](/docs/virtual-servers?topic=virtual-servers-launching-rescue) for steps.
1. Connect to the {{site.data.keyword.cloud}} SSL VPN.
1. Access the server by using KVM. Follow the steps for your device type.
    - Virtual Servers for Classic: [Accessing the KVM console for virtual servers](/docs/virtual-servers?topic=virtual-servers-access-kvm-console)
1. Run the following commands in rescue mode by using KVM or KVM IPMI console:

   ```bash
   mount /dev/xvda2 /mnt
   mount /dev/xvda1 /mnt/boot/
   mount --bind /dev /mnt/dev
   mount --bind /sys /mnt/sys
   mount --bind /proc /mnt/proc
   chroot /mnt
   passwd
   ```
   {: codeblock}

1. When you run the `passwd` command, you can set a new password for the device. Make sure that you record your password. You can also update it on the details screen in the {{site.data.keyword.cloud}} console. For more information, see [Update software credentials](/docs/virtual-servers?topic=virtual-servers-configuring-virtual-servers#update-software-credentials).

## Recover a compromised server
{: #recover_server_compromised}

If you determine that the server is compromised, you can restore from a backup or reload the operating system. Refer to the [CVE-2026-41940 article](https://support.cpanel.net/hc/en-us/articles/40073787579671-Security-CVE-2026-41940-cPanel-WHM-WP2-Security-Update-04-28-2026){: external} for how to review if the server is compromised. See also the cPanel article [What do I do if I believe that my server was hacked?](https://support.cpanel.net/hc/en-us/articles/360057223334-What-do-I-do-if-I-believe-my-server-has-been-hacked){: external}.

To restore from backup, follow the instructions for the [Back up and recovery](/docs/virtual-servers?topic=virtual-servers-backup-services) solution that you selected.

To reload the operating system, go to the **Device list**, select the server to show the _Device details_ page, and select **Actions** > **OS reload**. For more information, see [Reloading the operating system](/docs/virtual-servers?topic=virtual-servers-reloading-the-os).

   - You might need to change the operating system version during the operating system reload if your current one is past the end of support. For more information, see [End of support for operating systems considerations](/docs/virtual-servers?topic=virtual-servers-about-software#supported-operating-systems-for-ibm-cloud-servers).
   - To use the most recent cPanel version on Linux systems, select Ubuntu 22.04 during the operating system reload because CentOS and Rocky Linux are not supported by cPanel.
   - An operating system reload clears all data from the device. If needed, use a backup of the server to restore it after the operating is reloaded.

## Getting help
{: #getting-help}

If you need help with recovery, go to the IBM Cloud Support Center to [get support](/docs/support?topic=support-using-avatar&interface=ui#getting-support) by creating a case or reporting an issue, as defined by your support plan.
