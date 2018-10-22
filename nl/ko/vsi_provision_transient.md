---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-03"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 임시 인스턴스 프로비저닝
{: #ordering-vs-transient}
{{site.data.keyword.cloud}} 카탈로그 또는 {{site.data.keyword.slportal}}을 통해 임시 가상 서버 인스턴스를 프로비저닝할 수 있습니다.
{:shortdesc}

## 시작하기 전에
시작하기 전에 다음 전제조건을 검토하십시오.

  1. {{site.data.keyword.cloud_notm}} 카탈로그 또는 {{site.data.keyword.slportal}} 인증 정보 중 하나가 설정되어 있는지 확인하십시오.
  
  **참고:** {{site.data.keyword.Bluemix_notm}} 카탈로그의 경우에는 가상 서버를 주문하려면 업그레이드된 계정이 있어야 합니다. 계정 업그레이드에 대한 자세한 정보는 [IBM ID로 전환](https://console.bluemix.net/docs/admin/softlayerlink.html)을 참조하십시오.

  2. 가상 서버 인스턴스 용량 고려사항을 검토하십시오. 자세한 정보는 [용량 고려사항](ts_capacity_bp.html)을 참조하십시오.

## 임시 가상 서버 인스턴스 프로비저닝 
전제조건을 완료하고 나면 임시 가상 서버 인스턴스의 프로비저닝을 시작할 수 있습니다. {{site.data.keyword.cloud_notm}} 카탈로그 또는 {{site.data.keyword.slportal}}을 통해 인스턴스를 프로비저닝할 수 있습니다.

### IBM Cloud 카탈로그를 통해 임시 가상 서버 인스턴스 프로비저닝
{{site.data.keyword.cloud_notm}} 카탈로그를 통해 임시 가상 서버 인스턴스를 프로비저닝하려면 다음 단계를 완료하십시오.

  1. 고유 인증 정보를 사용하여 [{{site.data.keyword.cloud_notm}} 카탈로그 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/catalog/){: new_window}에 로그인하십시오.  
  2. **컴퓨팅 인프라** 섹션에서 **Virtual Server** 타일을 클릭하십시오.
  3. **임시 Virtual Server** 옵션을 선택하십시오.
  4. **작성**을 클릭하십시오.
  5. 가상 서버 인스턴스에 대한 모든 관련 정보를 완료하십시오.
  6. 주문 요약을 검토한 후에 **서드파티 서비스 계약** 선택란을 클릭하십시오.
  7. **프로비저닝**을 클릭하십시오. 
  
### 고객 포털을 통해 임시 가상 서버 인스턴스 프로비저닝
{{site.data.keyword.slportal}}을 통해 임시 가상 서버 인스턴스를 프로비저닝하려면 다음 단계를 완료하십시오.

  1. 고유 인증 정보를 사용하여 [{{site.data.keyword.slportal}} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}에 로그인하십시오.
  2. **주문** 섹션을 찾고 **디바이스**를 클릭하십시오.
  3. *디바이스* 페이지의 *공용 Virtual Server*에서 Virtual Server 오퍼링에 대해 **임시**를 클릭하십시오.
  4. *클라우드 서버 구성* 페이지에서 모든 관련 정보를 입력하십시오.
  5. **주문에 추가**를 클릭하여 계속 진행하십시오.
  6. 서버의 도메인 정보를 확인하거나 편집하십시오.
  7. **클라우드 서비스 이용 약관** 및 **서드파티 서비스 계약** 선택란을 클릭하십시오.
  8. 지불 정보를 확인하거나 입력하고 **주문 제출**을 클릭하십시오. 사용자의 프로비저닝 주문 번호가 있는 화면으로 이동됩니다. 이는 프로비저닝 주문 영수증이기도 하므로 사용자는 이 화면을 인쇄할 수 있습니다.

 일련의 이메일(프로비저닝 주문 확인, 프로비저닝 주문 승인 및 처리, 프로비저닝 완료)이 관리자에게 발송됩니다. 프로비저닝 완료 이메일에는 *디바이스 세부사항* 페이지 링크가 포함됩니다.

{{site.data.keyword.slapi_short}}를 사용해서도 임시 가상 서버를 프로비저닝할 수 있습니다. 해당 예는 [오브젝트 작성을 사용하여 임시 인스턴스 프로비저닝](../vsi/vsi_provision_api.html#api-rest-transient)을 참조하십시오.
{:tip}

## 다음 단계
가상 서버가 프로비저닝된 후에는 이 서버의 관리를 시작할 수 있습니다. 자세한 정보는 [가상 서버 관리](../vsi/vsi_managing.html)를 참조하십시오.
