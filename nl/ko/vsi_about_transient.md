---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

keywords: transient virtual servers, transient instances, transient offering, cost savings

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 임시 가상 서버
{: #about-vs-transient}
{{site.data.keyword.BluVirtServers}} 임시 오퍼링은 워크로드가 유연성이 있고 비용을 절감하려는 경우에 좋은 옵션입니다. 임시 가상 서버에서 워크로드를 실행하여 비용을 절감할 수 있습니다. 임시 인스턴스는 사용하지 않은 용량이 사용 가능할 때 프로비저닝됩니다. 따라서 데이터 센터 리소스가 전체 On-Demand 계정에 대해 필요한 경우, 해당 리소스는 유실 가능합니다. 임시 인스턴스는 해당 리소스가 재확보되어야 할 때 선착순(first-on first-off) 방식으로 프로비저닝 해제됩니다.   

임시 가상 서버는 다음과 같은 유연성을 제공합니다.

* **글로벌 가용성**

    임시 가상 서버 오퍼링은 전 세계의 데이터 센터에서 사용할 수 있습니다.

* **비용 절감**

    임시 가상 서버는 프로덕션이 아닌 워크로드에 적합합니다. 예를 들어, 임시 인스턴스를 사용하여 애플리케이션을 테스트 및 개발하거나 지속적으로 가동할 필요가 없는 환경에서 확장성을 테스트할 수 있습니다.

임시 인스턴스는 SAN 기반의 스토리지를 사용하는 공용 인스턴스입니다.

## 알림
{{site.data.keyword.slapi_short}}를 사용하여 임시 인스턴스에 대해 리소스가 사용 가능해질 때 알림을 수신할 수 있습니다. API를 사용하여 리소스가 사용 가능해질 때 임시 가상 서버를 프로그래밍 방식으로 프로비저닝할 수도 있습니다. 마찬가지로 API를 사용하여 리소스가 사용 불가능해질 때 인스턴스 프로비저닝을 프로그래밍 방식으로 중지할 수도 있습니다. 자세한 정보는 [자동화된 재확보 알림 구성](/docs/vsi?topic=virtual-servers-configuring-notifications-for-reclaims-of-transient-virtual-servers)을 참조하십시오.

## 제한사항
임시 가상 서버를 프로비저닝하기 전에 다음과 같은 제한사항을 고려하십시오.

* 지원되는 동시 인스턴스 수는 계정 전체의 디바이스 할당량 중 일부입니다. 동시 인스턴스 한계에 대한 자세한 정보는 [FAQ: 가상 서버](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#concurrent)를 참조하십시오.
* 임시 인스턴스는 업그레이드 또는 다운그레이드할 수 없습니다.
* 리소스는 알림 없이 언제든지 재확보할 수 있습니다.
* 임시 인스턴스는 로컬 스토리지를 사용할 수 없습니다.
* 임시 인스턴스는 SAN 기반의 스토리지(밸런스됨, 컴퓨팅, 메모리)만 사용할 수 있습니다.
* 임시 인스턴스는 GPU 기반 프로파일을 사용할 수 없습니다.


## 다음 단계

가상 서버 특성을 검토하고 선택한 후에는 임시 가상 서버를 프로비저닝합니다. 시작하려면 다음 정보를 검토하십시오.
1. [프로비저닝 선택사항](/docs/vsi?topic=virtual-servers-provisioning-selections)
2. [임시 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-ordering-vs-transient)
