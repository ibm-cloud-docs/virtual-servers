---

copyright:
  years: 2014, 2023
lastupdated: "2023-06-19"

keywords: Upgrading port speed in Linux

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Upgrading port speed in Linux
{: #upgrading-port-speed-in-linux}

Use the following information to update your port speed in Linux.
{: shortdesc}

The following commands affect the connectivity of your server. Always manage network connections by first connecting to the IP that you are not working on.

You can check the current speed of your connection by running the following commands:

   ```text
   # ethtool eth#   (eth1 for public, eth0 for private)
   ```
   {: pre}

Output displays the current configurations for that connection:

   ```text
   root@noc-training-linux [~]# ethtool eth1
   ```
   {: screen}

Settings for eth1:
   
   ```text
   Supported ports: [ MII ]
   Supported link modes:   10baseT/Half 10baseT/Full
                           100baseT/Half 100baseT/Full
                           1000baseT/Full
   Supports auto-negotiation: Yes
   Advertised link modes:  10baseT/Half 10baseT/Full
                           100baseT/Half 100baseT/Full
                           1000baseT/Full
   Advertised auto-negotiation: Yes
   Speed: 100Mb/s
   Duplex: Full
   Port: MII
   PHYAD: 3
   Transceiver: external
   Auto-negotiation: on
   Supports Wake-on: g
   Wake-on: d
   Link detected: yes
   root@noc-training-linux [~]#
   ```
   {: screen}

To change the speed, edit the following file by using your favorite text editor:

   ```text
   /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 for public, ifcfg-eth0 for private)
   ```
   {: pre}

You see find the following line:

   ```text
   ETHTOOL_OPTS="autoneg off speed 100 duplex full"
   ```
   {: screen}

This entry allows the auto-negotiation, speed, and duplex to be forced on boot, keeping a consistent configuration through a restart.
The speed can be modified to match your new port speed. This modification requires a network restart before the new speed is applied.

All connections forced to 1000 Mbps must have autoneg enabled in the ifcfg-eth# file.
{: tip}
