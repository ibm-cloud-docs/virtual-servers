---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

keywords: public virtual servers, network traffic, virtual server deployment

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 공용 가상 서버
{: #about-public-virtual-servers}

공용 {{site.data.keyword.BluVirtServers}} 오퍼링은 IBM에서 관리하는 멀티 테넌트 가상 서버 배치입니다. 이 오퍼링은 사용자가 빠르게 서비스 사용을 시작할 수 있도록 모든 비즈니스 요구사항을 만족시키는 사전 정의된 크기를 통해 신속한 확장성과 비용에 비해 높은 효율성을 제공합니다.
{:shortdesc}

공용 가상 서버에는 다음 항목을 포함한 다양한 이점이 있습니다.

* **글로벌 가용성** 

    공용 가상 서버 오퍼링은 전세계의 데이터 센터에서 사용할 수 있습니다.

* **구성 선택사항, 신속한 배치 및 확장성** 

    공용 가상 서버 오퍼링은 사용자의 다양한 워크로드 요구사항을 만족시키는 소형 또는 대형 가상 서버 옵션을 제공합니다.

VSI SAN 및 기타 NAS(Network-Attached Storage)를 포함하는 공용 가상 서버에 대한 네트워크 트래픽이 반드시 보장되는 것은 아닙니다. 가상 서버 인스턴스의 네트워크 트래픽이 다른 가상 서버에 대해 중대하고 부정적인 영향을 주기 시작하는 경우 해당 인스턴스가 새 호스트에서 다시 시작되거나 극단적인 경우 완전히 사용 불가능할 수 있습니다. 이 부정적인 영향은 종종 약 20,000에서 30,000PPS(Packets Per Second)의 트래픽 레벨로 관찰됩니다.  보장된 네트워킹을 위해 전용 Virtual Server 오퍼링을 사용하는 것이 좋습니다. 자세한 정보는 싱글 테넌트 환경의 [전용 가상 서버](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers) 오퍼링을 참조하십시오.

이 오퍼링에서는 다음 공용 인스턴스 제품군을 사용할 수 있습니다.  

| 제품군 |설명                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
|[밸런스됨](/docs/vsi?topic=virtual-servers-balanced#balanced) |성능과 확장성 사이에 균형이 잡혀야 하는 일반 클라우드 워크로드에 가장 적합합니다. NAS(Network-Attached Storage)를 사용합니다. |
|[밸런스된 로컬 스토리지](/docs/vsi?topic=virtual-servers-balanced-local-storage#balanced-local-storage) | 대기 시간은 매우 짧으며 높은 I/O 성능을 필요로 하는 대형 데이터베이스 워크로드에 적합합니다. |
|[컴퓨팅](/docs/vsi?topic=virtual-servers-compute#compute) |중간에서 높은 수준의 웹 트래픽 워크로드에 가장 적합합니다.|
|[메모리](/docs/vsi?topic=virtual-servers-memory#memory)  |메모리 캐싱 및 실시간 분석 워크로드에 가장 적합합니다. |
|[GPU](/docs/vsi?topic=virtual-servers-gpu#gpu)  |고성능 워크로드에 가장 적합합니다.
{: caption="표 1. 공용 가상 서버 제품군 선택사항" caption-side="top"}

이러한 제품군 중 일부는 IBM Cloud Virtual Servers for VPC에도 사용할 수 있습니다. 자세한 정보는 [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started)를 참조하십시오.
{:tip}

## 다음 단계

가상 서버 프로파일을 검토하고 결정한 후에는 공용 가상 서버를 프로비저닝해야 합니다. 시작하려면 [공용 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)을 참조하십시오.
