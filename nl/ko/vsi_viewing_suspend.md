---



copyright:
  years: 2018
lastupdated: "2018-10-30"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 비용 청구 일시중단 기능 보기
{{site.data.keyword.slportal_full}}에서 또는 {{site.data.keyword.slapi_short}}를 통해 가상 서버 인스턴스가 비용 청구 일시중단 기능을 지원하는지 여부를 확인할 수 있습니다.

## 고객 포털에서 비용 청구 일시중단 기능 보기
{{site.data.keyword.slportal}} 사이트에서 가상 서버 인스턴스가 비용 청구 일시중단 기능을 지원하는지 여부를 판별하려면 다음 단계를 수행하십시오.

1. 고유 인증 정보를 사용하여 [{{site.data.keyword.slportal}} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}에 로그인하십시오. 
2. **디바이스** 메뉴에서 **디바이스 목록**을 선택하십시오. 
3. **디바이스 목록**에서 가상 서버 인스턴스의 이름을 클릭하십시오. 
4. **구성** 탭의 **시스템** 섹션에서 가상 서버 인스턴스가 비용 청구 일시중단 기능을 지원하는지 여부를 확인할 수 있습니다. 

| 필드                     | 값                     |
| --------------------------------------| ------------------------- |
| 비용 청구 일시중단: 전원을 끄면 사용으로 설정됨 | 기능이 지원됩니다.     |
| 비용 청구 일시중단: 사용 불가능                 | 기능이 지원되지 않습니다. |
{: caption="표 1. 비용 청구 일시중단 세부사항" caption-side="top"}

## Softlayer API를 통해 비용 청구 일시중단 기능 보기

다음 명령은 {{site.data.keyword.slapi_short}}에서 가상 서버 인스턴스가 비용 청구 일시중단 기능을 지원하는지 여부를 확인하는 요청 예입니다.

**참고**: 다음 JSON 요청 및 응답이 일반적인 예입니다. 

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

다음은 요청에 대한 JSON 응답 예입니다.

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

자세한 정보는 [SLDN API 문서 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}를 참조하십시오.

## 다음 단계

비용 청구 일시중단 기능에 대해 자세히 알아보려면 다음 정보를 검토하십시오.
1. [비용 청구 일시중단 정보](vsi_about_suspend.html)
2. [가상 서버 관리](vsi_managing.html)
