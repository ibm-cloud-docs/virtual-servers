---

copyright:
  years: 2017, 2019
lastupdated: "2019-08-13"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# FAQs: Servers (general)
{: #faqs-servers-general-}

## What is the difference between "Boot from Image" and "Load from Image"?
{:faq}

Boot from Image and Load from Image both utilize existing image templates, which are applied to a device to either replace the existing operating system or to supplement the operating system in an attempt to remedy an existing issue. The main difference between the Boot and Load process is the type of image that is used. When performing either the Boot or Load from Image process, ensure you have backed up all data you may want to recover.

   * Boot from Image is a way to boot a device using an ISO supplied by {{site.data.keyword.BluSoftlayer_full}} for system recovery or an ISO that has been uploaded using the *Import Image* feature in the {{site.data.keyword.cloud_notm}} console. The ISO may be a clean version of the device operating system or a recovery disk that can be used in an attempt to remedy an issue with the device.
   * Load from Image is a method of OS Reload that utilizes an image template that has either been captured from a device or uploaded using the *Image Import* feature in the {{site.data.keyword.cloud_notm}} console. The *Load from Image* option performs the reload using a VHD, which wipes the device of all data and replaces the existing operating system and files with a "like new" version of the selected image.

## Why can I not connect to the KVM console?
{:faq}

If you are unable to connect to the KVM console, review these troubleshooting tips to assist in resolving the issue. Should additional issues occur, contact support. For more information on contacting support, see [Getting help and support](/docs/vsi?topic=virtual-servers-gettinghelp#gettinghelp).

   * The KVM console is a Java applet. Java must be installed prior to accessing the console. For more information on installing Java, see [Free Java Download ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.java.com/en/download/){: new_window}.  
   * If Java is installed, ensure that a connection is established using VPN. If a connection is not established, a warning is displayed when attempting to connect to the KVM console that a VPN connection is required.
   * The KVM console might generate one or more pop-up boxes during the connection process. Enable pop-ups from the {{site.data.keyword.cloud_notm}} console to ensure a connection can be made.
   * You might receive an error "Java applications are blocked by your security settings." For bare metal iKVM devices, you must add an exception for the IP Address of the IPMI device. For virtual server instances, be sure to allow "https://cloud.ibm.com" and the IP address of the KVM. For more information, see [Why are Java applications blocked by your security settings with the latest Java? ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.java.com/en/download/help/java_blocked.xml){: new_window}.
   * If the above conditions have been met and you receive an error that states, "Missing required Permissions manifest in main.jar", then Java applets have not been enabled in the Java Control Panel. This setting was introduced as a security precaution from Oracle in Java SE v7. Enable applets in the Control Panel to resolve this issue.

     If using Mac OSX in conjunction with Google Chrome, refer to Information and System Requirements for Installing and Using Mac Java 7 on the Java website.
     {:note}

   * If you are trying to connect to a virtual server instance through the standard Java applet and are still experiencing errors, you can also try using the VNC viewer of your choice. As an example, you could use [TightVNC](https://www.tightvnc.com/docs.php){: external} for Windows or Linux or [TigerVNC](https://tigervnc.org/){: external} for Mac OSX, where you would input the KVM IP and port as `KVMIP::KVMPORT`. 

If you have completed all of the checks above and still are unable to connect to the KVM console, contact support for additional assistance in troubleshooting the issue. If a connection to the console has been made but issues occur connecting to the device, ensure the credentials being used to access the device are valid. Contact the account administrator to verify credentials, if necessary.

## I lost my password to my server. How can I recover it?
{:faq}

If the root or administrator password to your server is suddenly not working, check the following items. If necessary, use the instructions to launch rescue mode and reset your password.

   * Are you copying and pasting the password? If not, please try to. Please also paste the password in a notepad to ensure no spaces are accidentally being copied with the password.
   * If the server has cPanel on it, is it possible that cPHulk has blocked your IP address due to failed logins? If so, you can access the server using the KVM or IPMI and whitelist your IP address in cPHulk with "/scripts/cphulkdwhitelist" followed by your IP address.
   * Has someone recently tried to change the password for the server by modifying the password in the {{site.data.keyword.cloud_notm}} console? Changing the password in the {{site.data.keyword.cloud_notm}} console only changes what you see as the password. It does not change the password the server is using. If this has happened, you can contact Support and they can usually recover the original, working password.
   * You might need to boot into your operating system's rescue mode to be able to reset your password. For more information, see [Launching rescue mode](/docs/vsi?topic=virtual-servers-launching-rescue#launching-rescue).

If these have all been checked and you are still unable to connect to the server using the password, please contact support using a ticket and request a password reset. Support will need to reboot the server in order to reset the password, so please ensure that you are prepared to approve the reboot and/or provide a maintenance time frame in which you would like it done. Most password resets can be accomplished in 15 minutes. In the {{site.data.keyword.cloud_notm}} console, you can create a ticket by going to **Support > Create a case** and use the subject *Accounts & access*.

## Are LVM partitions supported as a valid filesystem?
{:faq}

LVM (Logical Volume Management) provides logical management of file systems in Linux. In the {{site.data.keyword.BluSoftlayer}} environment, LVM is not supported as a bootable partitioning scheme. Virtual server instances cannot be ordered with LVM, and importing images that use LVM as a boot partition will fail to provision. If you require LVM on the boot partition, the bare metal offering can support LVM on boot for certain operating systems. With proper OS support and configuration, secondary VSI Disks can be used for LVM partitions; however, it is important to note that LVM is not a supported filesystem for Flex Image or Image Templates. If you have further questions, please open a ticket with the support team who can assist you.

## Preconfigured 161.26.0.0/16 Routes on Customer Hosts
{:faq}

{{site.data.keyword.BluSoftlayer_notm}} is enabling a new route on all newly provisioned servers to support future products.
   * The route points any address in the 161.26.0.0/16 range (161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255) to the back-end private network.
   * This IP block is assigned to {{site.data.keyword.BluSoftlayer_notm}} by IANA and will not be advertised on the public Internet.
   * Only {{site.data.keyword.BluSoftlayer_notm}} systems will be addressed out of this space.
   * ACLs on customer servers, virtual servers, and Vyatta gateways will need to be updated to allow customer's hosts to use Infrastructure services configured with IP addresses out of this range.

## How to add the new routing for various OSes
{:faq}

   <table>
   <CAPTION>Table 1. Adding a routes by OS</CAPTION>
   <THEAD>
   <TR>
   <th>Operating system</th>
   <th>Steps</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Windows 2003 Standard and Enterprise</td>
   <td>
   Add the persistent route from the command line by typing:
   <blockquote>route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p</blockquote>
   <b>Note:</b> Replace 10.0.0.1 with your private gateway IP address.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Server Core
   </td>
   <td>
   Add the persistent route from the command line by typing:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Note:</b> Replace 10.0.0.1 with your private gateway IP address.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Web, Standard, Enterprise, and Datacenter</td>
   <td>
   Add the persistent route from the command line by typing:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Note:</b> Replace 10.0.0.1 with your private gateway IP address.
   </td>
   </tr>
    <tr>
   <td>RedHat, Fedora, and CentOS</td>
   <td>
   Create a new route by editing/creating the following file: <i>/etc/sysconfig/network-scripts/route-eth0</i>
   <p>After you create that file, you must add the following information inside it: <i>161.26.0.0/16 via 10.0.0.1</i>
   </p>
   <b>Note:</b> Replace 10.0.0.1 with your private gateway IP address.
   </td>
   </tr>
   <tr>
   <td>Ubuntu and Debian</td>
   <td>
   In your <i>/etc/network/interfaces</i> file, add the following line at the end of the file:
   <blockquote>
   up route add -net 161.26.0.0/16 gw 10.0.0.1
   </blockquote>
   <b>Note:</b> Replace 10.0.0.1 with your private gateway IP address.
   </td>
   </tr>
   <tr>
   <td>Vyatta</td>
   <td><i>set protocols static route 161.26.0.0/16 next-hop 172.16.0.26</i>
   <p>
   <b>Note:</b> Replace 172.16.0.26 with the gateway of the subnet that the machine is on, which should be the same as the gateway defined for the 10.0.0./8 route.</p>
   </td>
   </tr>
   <tr>
   <td>ESXi</td>
   <td>Use the following command to add the route to the ESXi host:
   <blockquote>
   esxcfg-route -a 161.26.0.0/16 10.0.0.1
   </blockquote>
   <b>Note:</b> Replace 10.0.0.1 with your private gateway IP address.</td>
   </tr>
   <tr>
   <td>CoreOS</td>
   <td>Create a static route file in /etc/systemd/network named 10-static.network that looks like this:
   <blockquote>
   [Route]
   Gateway=10.0.0.1
   Destination=161.26.0.0/16
   </blockquote>
   <b>Note:</b> Replace 10.0.0.1 with your private gateway IP address.</td>
   </tr>
   </TBODY>
   </table>

   <a name="top"></a>

## Can I have the monitoring system issue an automatic reboot AND alert a support technician in the event that the server stops responding?
{:faq}

Yes, with the order of our **Automated Reboot from Monitoring Failure** service, you can set up the monitoring system to automatically reboot the server and issue a ticket for a support technician if a monitoring alert is issued. As an additional service, we provide **NOC Monitoring**, in which you will receive personal notification in the event a monitoring issue occurs. To learn more about both of these offerings, please refer to [Server Monitoring ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud/infrastructure/monitoring?cm_mc_uid=46846454197915580355142&cm_mc_sid_50200000=71138741559658182022){:new_window}.

## What is a cvsup mirror?
{:faq}

You can update against a local cvsup mirror that was run for you. Ensure your supfile has the following entry:

```
*default host=cvsup.service.softlayer.com
```
{:pre }

The distfiles are also mirrored and available from freebsd.org. You can add the following line into your */etc/make.conf* file to attempt to download from the local repository first:

```
MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"
```
{:screen }

If the file is not found there, it will follow the individual port Makefile and move to the next mirror.
