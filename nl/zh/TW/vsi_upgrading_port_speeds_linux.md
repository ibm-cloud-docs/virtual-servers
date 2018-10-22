---



copyright:
  years: 1994, 2017
lastupdated: "2017-12-12"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:screen: .screen}
{:tip .tip}
{:table: .aria-labeledby="caption"}

# 在 Linux 中升級埠速度

客戶伺服器的預設埠速度（適用於公用及專用網路）是 10 Mbps。如果您要將任一個埠速度升級為 100 Mbps 或 1000 Mbps，請向銷售部門開立問題單。銷售人員會要求您核准每月費用，而技術人員將會變更網路上的埠速度限制。

這些指令會影響伺服器的連線功能。請一律先連接至您未使用的 IP，來管理網路連線。
{:tip}

您可以執行下列指令來檢查現行連線速度：

    ```
    # ethtool eth#   (eth1 for public, eth0 for private)
    ```
    {: pre}

輸出將會顯示該連線的現行配置：

    ```
    root@noc-training-linux [~]# ethtool eth1
    ```
    {: screen}

eth1 的設定：

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

若要變更速度，請使用我的最愛文字編輯器來編輯下列檔案：

    /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 for public, ifcfg-eth0 for private)

您將會找到下行：

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

這容許在開機時強制執行自動協調、速度及雙工，並透過重新開機保持一致的配置。
速度可以修改成符合新的埠速度。這需要先將網路重新開機，再使用新速度。

在 ifcfg-eth# 檔案中，必須已啟用所有強制為 1000 Mbps 之連線的自動協調。
{: tip}
