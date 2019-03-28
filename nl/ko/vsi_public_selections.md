---

copyright:
  years: 2017, 2018
lastupdated: "2018-02-12"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 프로비저닝 선택사항
{: #provisioning-selections}

공용 가상 서버를 프로비저닝할 때는 다음 선택을 수행해야 합니다.

## 위치
배치할 특정 데이터 센터를 선택할 수 있습니다. 새 배치의 경우, {{site.data.keyword.Bluemix}}는 자동으로 최적의 데이터 센터(가용성을 기반으로)를 식별하고 적절한 공용 및 사설 VLAN을 작성합니다. 기존 환경에 추가하는 경우에는 디자인에 필요한 특정 데이터 센터, VLAN 및 서브넷을 선택할 수 있습니다. VLAN 및 서브넷에 대한 자세한 정보는 [VLAN 시작하기](/docs/infrastructure/vlans?topic=vlans-getting-started-with-vlans)를 참조하십시오.

서브넷 선택은 선택사항이며 디바이스가 서브넷의 IP 주소를 사용해야 하는 경우에만 사용됩니다. 서브넷을 선택하는 경우, 요청 처리를 위한 충분한 IP 주소가 있는지 확인하십시오. 서브넷에 대해 충분한 IP 주소가 없는 경우에는 주문이 지연되거나 취소될 수 있습니다.
{:tip}

## 프로세서/RAM
주문할 때는 코어 프로세서 옵션을 선택할 수 있습니다. 코어 프로세서 옵션은 가상 서버 배치의 표준을 따릅니다. 서버의 각 실제 코어는 하이퍼스레딩되며 두 개의 가상 CPU(vCPU) 또는 코어로 표시됩니다. 가상 서버 오퍼링은 코어당 2.0GHz 이상의 속도를 제공하며 하나의 가상 서버에서는 최대 56개 코어를 사용할 수 있습니다.

RAM은 매우 직관적입니다. 이 오퍼링은 선택한 양의 RAM을 사용자의 가상 서버에 할당하며, 하나의 가상 서버의 한계는 242GB입니다.

**참고:** 공용 인스턴스와 전용 인스턴스 간에는 약간의 구성 최대값 차이가 있습니다. 코어 또는 메모리를 지나치게 높게 할당하면 사용 가능한 옵션이 제한됩니다.

## 운영 체제

서버에 배치될 운영 체제 또한 선택할 수 있습니다. 선택할 수 있는 무료 옵션에는 CentOS 및 Ubuntu 등과 같은 몇 가지 옵션이 있습니다. Windows Server 및 Red Hat Enterprise Linux(RHEL)와 같은 유료 옵션 또한 사용 가능합니다. Windows는 100GB의 기본 디스크를 필요로 한다는 점을 참고하십시오.

기존 고객의 경우에는 **디바이스 -> 관리 -> 이미지**로 이동하여 *조치* 메뉴에서 **Virtual Server 주문**을 선택하여 {{site.data.keyword.slportal_full}}을 통해 이미지 템플리트를 기반으로 배치할 수도 있습니다.  이는 주문에 적합한 운영 체제를 자동으로 선택합니다.  또는, 표준 이미지를 기반으로 주문한 후 언제든지 이미지 템플리트로 다시 로드할 수도 있습니다.

## 스토리지

사용자는 각 가상 서버에 대해 SAN 또는 로컬 스토리지 옵션을 선택할 수 있습니다. SAN 또는 로컬 스토리지는 필요한 경우 다른 스토리지 제품으로 보완할 수 있습니다. SAN 및 로컬 스토리지는 모두 가상 서버에 로컬 디스크로 노출됩니다. 연결, 분리, 마이그레이션 등과 같은 모든 디스크에 대한 변경사항은 가상 서버 다시 부팅을 필요로 합니다. 자세한 정보는 [스토리지 옵션](/docs/vsi?topic=virtual-servers-storage-options#storage-options)을 참조하십시오.

## 시간별 또는 월별 비용 청구

가상 서버에 대해 시간별 또는 월별 비용 청구를 선택할 수 있습니다. 비용 외의 기본적인 차이점은 시간별 서버에 대역폭 할당이 포함되지 않는다는 점입니다. 비용 청구 기간의 끝에, 대역폭 사용량과 계정에서 각 서버가 활성 상태였던 시간이 계산됩니다. 현재 총계는 {{site.data.keyword.slportal}}에서 세부사항 페이지에 대한 링크가 있는 가상 서버 보기 페이지를 통해 볼 수 있으며 각 행 항목, 시간, 항목 당 현재 요금이 표시됩니다.

## 대역폭

이 오퍼링은 250GB와 공용 업링크가 있는 월별 가상 서버를 포함하고 있습니다. 초과 비용에 비해 저렴한 가격으로 더 큰 할당량을 구입할 수 있습니다.

## 포트 속도

가상 서버에 대해 최대 1GB까지 업링크 속도를 선택할 수 있습니다. 이러한 가상 업링크는 IBM 공용 및 전용 네트워크에 대한 중복 실제 업링크에 의해 지원됩니다. 공용 및 전용 속도는 주문 시에 항상 동일하며, 필요한 경우 링크를 업그레이드 또는 다운그레이드하는 옵션이 있습니다.

## 소프트웨어

프로비저닝 프로세스 중에 {{site.data.keyword.Bluemix_notm}}에 의해 설치되는 소프트웨어를 선택할 수 있습니다. {{site.data.keyword.Bluemix_notm}}에서는 프로비저닝 프로세스 중에 배치되는 모든 소프트웨어에 대해 지원을 제공합니다. 서버가 배치된 후 사용자가 자신의 소프트웨어를 설치할 수도 있습니다.

## 보안

배치하기 전에는 보안 옵션을 고려하십시오. 주문 프로세스의 일부로서, 사용자는 보호 기능을 제공하기 위해 디바이스 고유 하드웨어 또는 소프트웨어 방화벽을 선택할 수 있습니다. 또는, 환경에 전용 방화벽 어플라이언스를 배치하고 보호된 VLAN에 가상 서버를 배치할 수 있습니다.

**참고:** 가상 서버는 동일 인터페이스의 두 방화벽 어플라이언스로 보호될 수 없습니다.

보안 그룹을 사용하여 가상 서버 인스턴스의 공용 및 개인용 인터페이스에 대한 수신 및 발신 트래픽을 처리하는 방법을 정의하는 IP 필터 규칙 세트를 설정할 수도 있습니다.

자세한 정보는 다음 보안 주제 콜렉션을 참조하십시오.

* [Hardware Firewall (공유)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-getting-started-with-hardware-firewall-shared)
* [Hardware Firewalls (Dedicated)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-getting-started-with-hardware-firewall-dedicated)
* [보안 그룹 시작하기](/docs/infrastructure/security-groups?topic=security-groups-getting-started-with-security-groups)

## 모니터링
{: #about-monitoring}

가상 서버에 대해 다양한 모니터링 옵션을 선택할 수 있습니다. 옵션에는 ping 및 TCP 서비스 응답을 통해 모니터하며 고장 발생 시 선택적 응답이 있는 표준 모니터링이 포함되어 있습니다. 가상 서버 및 설치된 소프트웨어에 대해 더 많은 모니터링 기능 세트를 제공하는 Nimsoft 소프트웨어를 사용하는 고급 모니터링을 추가할 수도 있습니다.

자세한 정보는 [모니터링](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring)을 참조하십시오.

## 백업

주문 프로세스 중에 {{site.data.keyword.backup_notm}}을 추가할 수 있습니다. 기존 R1soft 백업 환경을 위해 R1soft 라이센스를 구입하거나 서드파티 백업 솔루션을 이용하도록 선택할 수도 있습니다.

자세한 정보는 [저장소 재등록](/docs/infrastructure/Backup?topic=Backup-reregister#reregister)을 참조하십시오.

## 프로비저닝 후 스크립트

프로비저닝 후 스크립트는 가상 서버 주문과 연관될 수 있습니다. 이는 다른 프로비저닝 태스크가 완료된 후 고객이 개발한 스크립트를 실행합니다. 이 스크립트는 일반적으로 서버에 고객 고유 구성을 적용하고 스케일링 전략의 자동화를 돕기 위해 이용됩니다.

자세한 정보는 [사용자 정의 프로비저닝 스크립트 추가](/docs/vsi?topic=virtual-servers-adding-post-script)를 참조하십시오.

## 다음 단계
공용 가상 서버를 프로비저닝할 준비가 완료된 경우에는 [공용 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-ordering-vs-public)을 참조하십시오.
