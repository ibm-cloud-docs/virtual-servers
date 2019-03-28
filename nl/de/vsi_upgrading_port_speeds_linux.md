---

copyright:
  years: 2014, 2017
lastupdated: "2017-12-12"

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

# Portgeschwindigkeit in Linux erhöhen (Upgrade)
{: #upgrading-port-speed-in-linux}

Die Standardportgeschwindigkeit für Kundenserver (sowohl für öffentliche als auch private Netze) beträgt 10 Mbps. Wenn Sie Ihre Portgeschwindigkeit auf 100 Mbps oder 1000 Mbps erhöhen möchten, öffnen Sie bitte ein Ticket bei unserer Vertriebsabteilung. Der Vertrieb wird Sie bitten, die monatliche Gebühr zu bestätigen, und ein Techniker wird die Portgeschwindigkeitslimits für das Netz ändern.

Diese Befehle wirken sich auf die Konnektivität Ihres Servers aus. Verwalten Sie Netzverbindungen immer so, dass Sie zuerst eine Verbindung mit der IP-Adresse herstellen, an der Sie gerade NICHT arbeiten.
{:tip}

Durch Ausführen der folgenden Befehle können Sie die aktuelle Geschwindigkeit Ihrer Verbindung prüfen:

    ```
    # ethtool eth#   (eth1 für öffentlich, eth0 für privat)
    ```
    {: pre}

Die Ausgabe enthält die aktuelle Konfiguration für die Verbindung:

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

Um die Geschwindigkeit zu ändern, bearbeiten Sie die folgende Datei in Ihrem bevorzugten Texteditor:

    /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 für öffentlich, ifcfg-eth0 für privat)

Dort finden Sie die folgende Zeile:

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

Damit können Sie die automatische Vereinbarung, die Geschwindigkeit und die Duplexeinstellung für einen Warmstart erzwingen, wodurch beim Warmstart eine konsistente Konfiguration erhalten bleibt.
Die Geschwindigkeit kann so geändert werden, dass sie Ihrer neuen Portgeschwindigkeit entspricht. Bevor die neue Geschwindigkeit verwendet wird, ist ein Netzwarmstart erforderlich.

Für alle Verbindungen, für die 1000 Mbps erzwungen wird, muss die automatische Vereinbarung (autoneg) in der Datei ifcfg-eth# aktiviert sein.
{: tip}
