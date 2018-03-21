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

# 在 Linux 中升级端口速度

客户服务器的缺省端口速度（对于公用和专用网络）为 10 Mbps。如果您希望将任一端口速度升级到 100 Mbps 或 1000 Mbps，请向销售部门开具凭单。销售人员会要求您批准按月收费，然后技术人员会更改网络上的端口速度限制。

以下命令会影响服务器的连接。因此，务必首先连接到未在处理的 IP 来管理网络连接。
{:tip}

可以通过运行以下命令来检查连接的当前速度：

    ```
    # ethtool eth#   （eth1 表示公用，eth0 表示专用）
    ```
    {: pre}

输出将显示该连接的当前配置：

    ```
    root@noc-training-linux [~]# ethtool eth1
    ```
    {: screen}

eth1 的设置：

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

要更改速度，请使用首选文本编辑器来编辑以下文件：

    /etc/sysconfig/network-scripts/ifcfg-eth#   （ifcfg-eth1 表示公用，ifcfg-eth0 表示专用）

您将找到以下行：

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

这允许在引导时强制执行自动协商、速度和双工，并使配置在重新引导之后保持一致。
可以修改速度以与新的端口速度相匹配。这需要重新引导网络后才可使用新速度。

如果强制使所有连接为 1000 Mbps，那么必须在 ifcfg-eth# 文件中启用 autoneg。
{: tip}
