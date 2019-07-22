---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-25"

keywords: reserved virtual servers, cost savings, guaranteed capacity 
subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 예약된 가상 서버
{: #about-reserved-virtual-servers}

{{site.data.keyword.BluVirtServers}} 예약된 인스턴스 오퍼링은 향후 배치 및 비용 절감을 위해 보장된 리소스를 원하는 경우 유용한 옵션입니다. 예약된 용량에 대해 1년 또는 3년 계약 기간 중 하나를 선택합니다. 예약된 용량 내에서 특정 크기의 최대 20개 가상 서버 인스턴스 세트를 예약하고 필요할 때 이러한 인스턴스를 프로비저닝할 수 있습니다. 계약 기간 동안 선택한 POD 및 데이터 센터 내에서 이 용량이 보장됩니다.

예약된 가상 서버 인스턴스는 다음을 포함한 다양한 이점을 제공합니다.

* **보장된 용량**

    용량을 예약하는 경우 계약 기간 동안 이 용량이 보장됩니다. 
    
* **글로벌 가용성**
    
    예약된 가상 서버 오퍼링은 전 세계의 데이터 센터에서 사용할 수 있습니다.

* **신뢰할 수 있는 프로비저닝**
   
   예약된 용량으로 가상 서버 인스턴스를 언제든지 프로비저닝하고 재확보할 수 있습니다.

* **비용 절감**
    
    1년 또는 3년 계약 기간 중 하나를 선택하면 시간별 또는 월별 가상 서버 비용 청구 주기와 비교하여 일정한 월별 지불 및 비용 절감의 이점을 누릴 수 있습니다.

예약된 가상 서버 인스턴스는 SAN 기반의 스토리지를 사용하는 공용 인스턴스입니다. 이 오퍼링에서는 다음 공용 인스턴스 제품군을 사용할 수 있습니다. 

| 제품군 |설명                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
|[밸런스됨](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) |성능과 확장성 사이에 균형이 잡혀야 하는 일반 클라우드 워크로드에 가장 적합합니다. NAS(Network-Attached Storage)를 사용합니다.|
|[컴퓨팅](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) |중간에서 높은 수준의 웹 트래픽 워크로드에 가장 적합합니다.|
|[메모리](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  |메모리 캐싱 및 실시간 분석 워크로드에 가장 적합합니다. |
{: caption="표 1. 공용 가상 서버 제품군 선택사항" caption-side="top"}

## 제한사항 

용량 예약 및 예약된 가상 서버 인스턴스를 프로비저닝하기 전에 다음 제한사항을 고려하십시오.
  
  * 인스턴스를 업그레이드하거나 다운그레이드할 수 없습니다.
  * 예약된 용량을 취소할 수 없습니다. 그러나, 해당 용량의 가상 서버 인스턴스를 재확보할 수는 있습니다.
    
## 알림

예약된 가상 서버 용량의 기간이 끝나기 한 달 전에 이메일 알림을 받습니다.

## 다음 단계

옵션을 검토하고 결정하고 나면, 예약된 용량 및 인스턴스를 프로비저닝할 시간입니다. 시작하려면 다음 정보를 검토하십시오.

   1. [예약된 용량 및 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)
   2. [FAQ: 예약된 용량 및 인스턴스](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances)
