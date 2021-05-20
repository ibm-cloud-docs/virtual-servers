---

copyright:
  years: 2014, 2021
lastupdated: "2021-05-19"

keywords: Upgrading port speed in Linux

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:screen: .screen}
{:tip .tip}
{:table: .aria-labeledby="caption"}

# Upgrading port speed in Linux
{: #upgrading-port-speed-in-linux}

The default port speed for customer servers (for both public and private networks) is 10 Mbps. If you want to upgrade either of your port speeds to 100 Mbps or 1000 Mbps, open a support case with the Sales department. You need to approve the monthly charge before a technician changes the port speed limits on the network.

These commands affect the connectivity of your server. Always manage network connections by first connecting to the IP that you are NOT working on.
{:tip}

You can check the current speed of your connection by running the following commands:

    ```
    # ethtool eth#   (eth1 for public, eth0 for private)
    ```
    {: pre}

Output displays the current configurations for that connection:

    ```
    root@noc-training-linux [~]# ethtool eth1
    ```
    {: screen}

Settings for eth1:

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

To change the speed, edit the following file using your favorite text editor:

    /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 for public, ifcfg-eth0 for private)

You will find the following line:

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

This entry allows the auto-negotiation, speed, and duplex to be forced on boot, keeping a consistent configuration through a restart.
The speed can be modified to match your new port speed. This modification requires a network restart before the new speed is applied.

All connections forced to 1000 Mbps must have autoneg enabled in the ifcfg-eth# file.
{: tip}
