---

copyright:
  years: 2014, 2021
lastupdated: "2021-09-13"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}

# Upgrading port speed in Windows
{: #upgrading-port-speed-in-windows}

The default port speed for customer servers (for both public and private networks) is 10 Mbps. If you would like to upgrade either of your port speeds to 100 Mbps or 1000 Mbps, open a ticket with the request. You need to approve the minimal charge before a technician changes the port speeds on your network. For more information about opening support case, see [Getting support](/docs/get-support?topic=get-support-using-avatar).

After the upgrade is completed on the network side, hardcode the appropriate network interfaces on your server.

Always connect to your server on the network that you are NOT working on to avoid locking yourself out of the server.
{:note}

Complete the following steps to force the port speed on a Windows server. 

1. Select **Start > Select Control Panel > Select Network Connections**.
2. Click the network connection that you are trying to upgrade or downgrade.
   * For Public Port upgrades select **Local Area Connection 2** OR **FrontEnd**.
   * For Private Port upgrades select **Local Area Connection** OR **BackEnd**.
3. From the Connection Status window, verify that the network card you selected is the port that you want to upgrade.
4. Select the support tab (note the IP address):
   * For a Public Port upgrade the IP needs to be a public IP address.
   * For a Private Port upgrade the IP needs to be a 10.x.x.x address.
5. If the IP addresses do not match up, repeat steps 1-3 for the other Network Connection.

## LAN Status
{: #lan-status}

Select the **General Tab** again, and then select **Properties.** A new window appears.

In the **General** tab of the **Connection Properties** window, select **Configure**. The driver properties window appears.

1. Select the **Advanced** tab.
2. Select **Link Speed&Duplex** from the property list.
3. Select the **Value** tab to the right and set the port speed you are upgrading to with full duplex:
   * For 10 MBS Select: 10 Mbps / Full
   * For 100 MBS Select: 100 Mbps / Full
   * For 1000 MBS Select: Auto
4. Click OK.  

This change causes the server to immediately start with the new speed, so you might be briefly disconnected while the link renegotiates.
