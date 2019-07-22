---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# 전용 가상 서버 정보
{: #dedicated-virtual-servers}

{{site.data.keyword.Bluemix}} 인프라 전용 호스트 오퍼링은 가상화된 싱글 테넌트 전용 서버입니다. 이는 워크로드 배치에 대한 최대한의 제어 능력과 유연한 프로비저닝 후 옵션을 제공합니다. 사용자는 가상 서버를 사전 결정된 어느 {{site.data.keyword.cloud_notm}} 데이터 센터에 배치할지 결정하고 호스트를 계정에 직접 할당하여 용량을 확보할 수 있습니다.
{:shortdesc}

이 오퍼링에는 다음 기능이 포함되어 있습니다.

* 선호도 및 비선호도. 사용자는 선호도 및 비선호도 규칙이라고 하는, 유지해야 하는 호스트 대 가상 서버 및 가상 서버 대 가상 서버 관계를 지정할 수 있습니다. 이러한 규칙은 워크로드 요구사항에 따라 워크로드가 적절히 배치되도록 하는 데 도움을 줍니다.
* 배치 후 관리. 사용자는 워크로드 요구사항에 따라 전용 호스트 간에 가상 서버를 마이그레이션할 수 있습니다.
* 워크로드 가시성. 사용자는 각 호스트의 리소스 이용 코어, RAM 및 로컬 스토리지를 볼 수 있으며, 이는 워크로드 관리에 대한 사용자의 제어 능력을 최대화합니다.

사용자는 두 가지 배치 모델(전용 호스트 및 전용 인스턴스) 중 하나를 선택할 수 있습니다. 전용 호스트는 워크로드 배치 관리에 도움을 주며 전용 인스턴스는 싱글 테넌트 격리를 제공합니다.

전용 인스턴스는 전용 호스트에서 제공하는 제어 기능과 동일한 제어 기능을 제공하지 않습니다. 자세한 정보는 다음 표를 참조하십시오.
{:note}

|전용 가상 서버 기능 |전용 호스트 인스턴스 |전용 인스턴스 |
| ------- | ------- | ------- |
|싱글 테넌트 격리 | ![체크 표시 아이콘](../../icons/checkmark-icon.svg) | ![체크 표시 아이콘](../../icons/checkmark-icon.svg) |
|가상 서버 배치 제어 | ![체크 표시 아이콘](../../icons/checkmark-icon.svg) |   |
|리소스 가시성 | ![체크 표시 아이콘](../../icons/checkmark-icon.svg) |   |
|인스턴스 비용 청구 |   | ![체크 표시 아이콘](../../icons/checkmark-icon.svg) |
|호스트 비용 청구<sup>(1)</sup> | ![체크 표시 아이콘](../../icons/checkmark-icon.svg) |   |
|배치 후 제어 | ![체크 표시 아이콘](../../icons/checkmark-icon.svg) |   |
|용량 예약 | ![체크 표시 아이콘](../../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="표 1. 제어 기능" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup>호스트 가격에는 코어, RAM, 로컬 SSD 및 네트워크 속도가 포함됩니다. 프리미엄 운영 체제(OS), SAN(Storage Area Network) 스토리지 및 소프트웨어 추가 가능은 인스턴스당 기존 가격 및 라이센싱을 사용하여 시간별 또는 월별 모델로 가격이 책정됩니다.

전용 호스트 및 전용 호스트 인스턴스를 주문할 때는 다음 항목을 고려하십시오.

* 호스트의 크기는 해당 호스트에서 실행할 워크로드에 따라 결정됩니다. 기본값은 56개 코어 X 242GB RAM X 1.2TB지만 추가 구성에서 선택할 수 있습니다. 
* 한 번에 두 개의 호스트만 주문할 수 있습니다. 예를 들어, 여섯 개의 호스트가 필요한 경우에는 세 개의 개별 주문을 발주해야 합니다.
* 각 호스트에는 고유 이름이 필요하며 팟(Pod)은 자동으로 지정할 수 있습니다.

## 다음 단계

배치 옵션을 검토하고 결정한 후에는 가상 서버를 프로비저닝해야 합니다. 시작하려면 [전용 호스트 및 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)을 참조하십시오.
