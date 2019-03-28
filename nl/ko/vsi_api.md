---

copyright:
  years: 2017
lastupdated: "2017-10-25"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# API 참조
{: #api-reference}

{{site.data.keyword.slapi_full}}는 개발자 및 시스템 관리자가 {{site.data.keyword.cloud}}의 백엔드 시스템과 직접 상호작용할 수 있게 해 주는 개발 인터페이스입니다. {{site.data.keyword.slapi_short}}는 {{site.data.keyword.slportal_full}}의 여러 기능을 작동시키며, 이는 일반적으로 {{site.data.keyword.slportal}}에서 상호작용이 가능한 경우, API에서도 이를 실행할 수 있음을 의미합니다. 프로그래밍 방식으로 API 내에서 {{site.data.keyword.BluSoftlayer_full}} 환경의 모든 부분과 상호작용할 수 있으므로, {{site.data.keyword.slapi_short}}는 태스크를 자동화할 수 있게 해 줍니다. 예를 들면, *SoftLayer_Virtual_Guest/createObject* API를 사용하여 가상 서버 인스턴스를 배치할 수 있습니다.
{:shortdesc}

{{site.data.keyword.slapi_short}}는 원격 프로시저 호출(RPC) 시스템입니다. 각 호출에는 API 엔드포인트로 데이터를 전송하고 구조화된 데이터를 수신하는 과정이 포함됩니다. {{site.data.keyword.slapi_short}}와의 사이에 데이터를 전송하고 수신할 때 사용되는 형식은 사용자가 선택한 API 구현에 따라 달라집니다. {{site.data.keyword.slapi_short}}는 현재 데이터 전송에 SOAP, XML-RPC 또는 REST를 사용합니다.

{{site.data.keyword.slapi_short}} 및 가상 서버 API에 대한 자세한 정보를 얻으려면 {{site.data.keyword.sldn_full}}의 다음 리소스를 참조하십시오.
* [{{site.data.keyword.slapi_short}} 개요 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/reference/softlayerapi/){: new_window}
* [{{site.data.keyword.slapi_short}} 시작하기 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/article/getting-started/){: new_window}
* [API 참조: SoftLayer_Virtual_Guest::createObject ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/){: new_window}
* [API 참조: SoftLayer_Product_Order::placeOrder ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/){: new_window}

API 사용 예는 다음 리소스를 참조하십시오.
* [{{site.data.keyword.slapi_short}} 주문 CLI를 사용한 주문 이해 및 빌드 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/article/understanding-ordering/){: new_window}
* [{{site.data.keyword.slapi_short}} Python 클라이언트: 가상 서버 관련 작업 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [{{site.data.keyword.slapi_short}} 예 - 릴리스 정보 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/){: new_window}
* [Python 예 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/python/){: new_window}

## 전용 가상 서버 사용 예
* [전용 호스트 할당 가져오기 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/python/getDediHostAllocation/){: new_window}
* [전용 호스트 게스트 가져오기 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/python/getDedicatedHostGuests/){: new_window}
* [전용 호스트 간 가상 서버 마이그레이션 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/python/migrateDedicatedHost.py/){: new_window}

## 공용 가상 서버 사용 예
* [softlayer_virtual_guest API 예 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
