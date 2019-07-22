---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# 서드파티 이미지에서 가상 서버 인스턴스 프로비저닝
{: #ordering-3P}

서드파티 공급업체가 작성한 이미지에서 가상 서버 인스턴스를 프로비저닝할 수 있습니다. 서드파티 이미지는 {{site.data.keyword.cloud}} 카탈로그 클라우드 이미지 링크를 통해 사용 가능합니다.
{:shortdesc}

## 시작하기 전에
시작하기 전에 {{site.data.keyword.cloud_notm}} 카탈로그 인증 정보가 설정되어 있는지 확인하십시오.

{{site.data.keyword.Bluemix_notm}} 카탈로그의 경우, 가상 서버를 주문하려면 업그레이드된 계정이 있어야 합니다. 계정 업그레이드에 대한 자세한 정보는 [IBM ID로 전환](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)을 참조하십시오.
{:note}

## 가상 서버 이미지 선택
1. 고유 인증 정보를 사용하여 [{{site.data.keyword.cloud_notm}} 카탈로그 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/catalog/){: new_window}에 로그인하십시오.
2. **클라우드 이미지** 섹션에서 배치할 서드파티 이미지를 찾아 클릭하십시오. 
3. 사용자 정의 이미지 세부사항을 검토하고 **계속**을 클릭하십시오. 사용자 정의 이미지가 미리 선택된 상태에서 **가상 서버 인스턴스 - 사용자 정의 이미지** 페이지가 표시됩니다. 

## 배치 옵션 검토 및 선택
자세한 정보는 다음 주제를 참조하십시오.

|배치 옵션                           |설명                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[공용 가상 서버](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)            |IBM 관리 멀티 테넌시 가상 서버 배치|
|[임시 가상 서버](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)|감소된 비용으로 유연성 있는 워크로그에 최적화되어 제공되는 IBM 관리 멀티 테넌시 가상 서버 배치 |
|[예약된 가상 서버](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | 계약 기간 동안 용량이 보장되는 IBM 관리 멀티 테넌시 가상 서버 배치 |
|[전용 가상 서버](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)      |IBM 관리 싱글 테넌시 가상 서버 배치            |
{: caption="표 1. 배치 옵션" caption-side="top"}

## 가상 서버 프로비저닝
배치 옵션을 결정한 후에는 프로비저닝 프로세스를 시작하십시오. 자세한 정보는 다음 주제를 참조하십시오. 

사용자 정의 이미지를 포함하여 프로비저닝 프로세스를 시작했으므로 프로비저닝 프로세스 중에는 이미지 유형을 변경할 수 없습니다.
{:note}

|              프로비저닝 지시사항                                         |설명                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[공용 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                |다양한 옵션으로 공용 인스턴스를 프로비저닝             |
|[임시 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                |다양한 옵션으로 임시 인스턴스 프로비저닝            |
|[예약된 용량 및 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | 다양한 옵션으로 예약된 용량 및 인스턴스 프로비저닝 |
|[전용 호스트 및 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)|사설 인스턴스 또는 전용 인스턴스를 전용 호스트에 프로비저닝함|
{: caption="표 2. 프로비저닝 정보" caption-side="top"}


## 다음 단계
가상 서버가 프로비저닝되어 사용 가능한 상태가 되면 {{site.data.keyword.cloud_notm}} 콘솔 또는 {{site.data.keyword.slapi_short}}를 사용하여
가상 서버를 구성할 수 있습니다. 자세한 정보는 [가상 서버 구성](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers)을 참조하십시오.
