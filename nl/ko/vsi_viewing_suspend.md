---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-28"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 비용 청구 일시중단 기능 보기
{: #viewing-suspend-billing-feature}

## 시작하기 전에
먼저 디바이스 메뉴로 이동하여 태스크를 완료할 수 있는 올바른 계정 권한이 있는지 확인하십시오.  

* 콘솔의 디바이스 메뉴로 이동하십시오. 자세한 정보는 [디바이스로 이동](/docs/vsi?topic=virtual-servers-navigating-devices)을 참조하십시오.
* 필요한 계정 권한 및 디바이스 액세스 권한이 있는지 확인하십시오. 계정 소유자 또는 **사용자 관리** 클래식 인프라 권한이 있는 사용자만 권한을 조정할 수 있습니다.  

권한에 대한 자세한 정보는 [클래식 인프라 권한](/docs/iam?topic=iam-infrapermission#infrapermission) 및 [디바이스 액세스 관리](/docs/vsi?topic=virtual-servers-managing-device-access)를 참조하십시오.

## 비용 청구 일시중단 기능 보기 
가상 서버 인스턴스가 비용 청구 일시중단 기능을 지원하는지 여부를 판별하려면 다음 단계를 수행하십시오.

1. **디바이스** 메뉴에서 **디바이스 목록**을 선택하십시오. 
2. **디바이스 목록**에서 가상 서버 인스턴스의 이름을 클릭하십시오. 
3. **인스턴스 세부사항** 섹션에서 가상 서버 인스턴스가 비용 청구 일시중단 기능을 지원하는지 여부를 확인할 수 있습니다. 

| 필드                                 | 값                     |
| --------------------------------------| ------------------------- |
| 비용 청구 일시중단: 전원을 끄면 사용으로 설정됨 | 기능이 지원됩니다.     |
| 비용 청구 일시중단: 사용 불가능          | 기능이 지원되지 않습니다. |
{: caption="표 1. 비용 청구 일시중단 세부사항" caption-side="top"}

## SoftLayer API를 통해 비용 청구 일시중단 기능 보기

다음 명령은 {{site.data.keyword.slapi_short}}를 통해 가상 서버 인스턴스가 비용 청구 일시중단 기능을 지원하는지 여부를 확인하는 요청 예입니다.

다음 JSON 요청 및 응답이 일반적인 예입니다.
{:note}

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
1. [비용 청구 일시중단](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [가상 서버 관리](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

