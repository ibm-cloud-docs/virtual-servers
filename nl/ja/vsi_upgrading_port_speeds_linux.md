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

# Linux でのポート速度のアップグレード

(パブリック・ネットワークとプライベート・ネットワークの両方で) カスタマー・サーバーのデフォルトのポート速度は 10 Mbps です。 いずれかのポート速度を 100 Mbps または 1000 Mbps にアップグレードするには、営業部でチケットをオープンしてください。 営業担当が月額料金を承認するように依頼し、技術者がネットワークのポート速度制限を変更します。

以下のコマンドが、サーバーの接続に影響を与えます。 ネットワーク接続を管理する場合は必ず、作業中ではない IP に最初に接続してください。
{:tip}

以下のコマンドを実行すると、接続の現在の速度を確認できます。

    ```
    # ethtool eth#   (eth1 for public, eth0 for private)
    ```
    {: pre}

出力には、その接続の現在の構成が表示されます。

    ```
    root@noc-training-linux [~]# ethtool eth1
    ```
    {: screen}

eth1 の設定:

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

速度を変更するには、任意のテキスト・エディターを使用して以下のファイルを編集します。

    /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 for public, ifcfg-eth0 for private)

以下の行があります。

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

これによりオートネゴシエーションが可能になり、ブート時に速度と全二重が強制的に設定され、リブートしても一貫した構成が維持されます。
速度は、新しいポート速度と一致するように変更できます。 このためには、新しい速度を使用する前にネットワークをリブートする必要があります。

強制的に 1000 Mbps にされたすべての接続で、ifcfg-eth# ファイル内の autoneg が有効になっている必要があります。
{: tip}
