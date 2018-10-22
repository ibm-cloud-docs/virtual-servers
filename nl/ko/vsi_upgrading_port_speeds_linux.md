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

# Linux에서 포트 속도 업그레이드

고객 서버에 대한 기본 포트 속도(공용 및 사설 네트워크 모두)는 10Mbps입니다. 해당 포트 속도 중 하나를 100Mbps 또는 1000Mbps로 업그레이드하려면 영업 부서와 같이 티켓을 여십시오. 영업에서 월별 비용 승인을 요청하고 기술자가 네트워크에서 포트 속도 한계를 변경합니다.

다음 명령은 서버 연결에 영향을 줍니다. 항상 작업 중이지 않은 IP에 먼저 연결하여 네트워크 연결을 관리하십시오.
{:tip}

다음 명령을 실행하여 연결의 현재 속도를 확인할 수 있습니다.

    ```
    # ethtool eth#   (eth1 for public, eth0 for private)
    ```
    {: pre}

해당 연결에 대한 현재 구성이 출력으로 표시됩니다.

    ```
    root@noc-training-linux [~]# ethtool eth1
    ```
    {: screen}

eth1 설정:

        지원되는 포트: [ MII ]
        지원되는 링크 모드:   10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        자동 협상 지원: Yes
        표시되는 링크 모드:  10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        자동 협상 표시: Yes
        속도: 100Mb/s
        양방향: Full
        포트: MII
        PHYAD: 3
        트랜시버: external
        자동 협상: on
        Wake-on 지원: g
        Wake-on: d
        링크 발견: yes
        root@noc-training-linux [~]#

속도를 변경하려면 자주 사용하는 문서 편집기로 다음 파일을 편집하십시오.

    /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 for public, ifcfg-eth0 for private)

다음 행이 표시됩니다.

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

그러면 자동 협상이 허용되며 부팅 시 속도 및 양방향이 강제 설정되고 다시 부팅해도 구성의 일관성이 유지됩니다.
새 포트 속도와 일치하도록 속도를 수정할 수 있습니다. 그러려면 새 속도를 사용하기 전에 네트워크를 다시 부팅해야 합니다.

1000Mbps로 강제 설정된 모든 연결의 경우 ifcfg-eth# 파일에서 autoneg가 사용되도록 설정되어야 합니다.
{: tip}
