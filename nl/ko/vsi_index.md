---



copyright:
  years: 2017
lastupdated: "2017-08-23"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 가상 서버 시작하기
{{site.data.keyword.BluVirtServers}}는 수 분 내에 배치할 수 있습니다. 가상 서버는 사용자의 워크로드에 적합한 지역에 사용자가 선택한 가상 서버 이미지로부터 배치됩니다.
{:shortdesc}

가상 서버를 작성할 때는 시간별 또는 월별 비용 청구, 공용(멀티 테넌시) 환경 또는 전용(싱글 테넌트) 환경, 고성능 로컬 디스크 또는 엔터프라이즈 SAN 스토리지 간에 선택할 수 있습니다. 

## 시작하기 전에

시작하기 전에 다음 전제조건을 검토하십시오. 

  1. 가상 서버를 주문하려면 업그레이드된 계정이 있어야 합니다. 이 프로세스는 어느 정도 시간이 소요될 수 있으며 계속하려면 사용자의 요청이 승인되어야 합니다. 계정을 업그레이드하는 데 대한 자세한 정보는 [Bluemix 및 SoftLayer 비용 청구 계정 업그레이드 및 통합](https://console.ng.bluemix.net/docs/admin/softlayerlink.html)을 참조하십시오. 
  2. 배치 옵션을 검토하고 선택하십시오. 자세한 정보는 다음 주제를 참조하십시오.  
     
|              배치 옵션                                    |  설명                                               |
| --------------------------------------------------------- | --------------------------------------------------- |
|[공용 가상 서버](../vsi/vsi_public.html)            | IBM이 관리하는 멀티 테넌시 가상 서버 배치 |
|[전용 가상 서버](../vsi/vsi_dedicated.html)      | 싱글 테넌트 가상 서버 배치            |
{: caption="표 1. 배치 옵션" caption-side="top"}   

## 가상 서버 프로비저닝 

배치 옵션을 결정한 후에는 프로비저닝 프로세스를 시작하십시오. 

|              프로비저닝 지시사항                                           |  설명                                                   |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[공용 인스턴스 프로비저닝](../vsi/vsi_provision_public.html)                | 다양한 옵션으로 공용 인스턴스를 프로비저닝함             |
|[전용 호스트 및 인스턴스 프로비저닝](../vsi/vsi_provision_dedicated.html)| 개인용 인스턴스 또는 전용 인스턴스를 전용 호스트에 프로비저닝함|
{: caption="표 2. 프로비저닝 정보" caption-side="top"}
   
## 다음 단계

가상 서버가 프로비저닝되어 사용 가능한 상태가 되면 {{site.data.keyword.slportal_full}} 또는 {{site.data.keyword.slapi_full}}를 사용하여
가상 서버를 구성할 수 있습니다. 자세한 정보는 [가상 서버 구성](../vsi/vsi_configuring.html)을 참조하십시오. 
