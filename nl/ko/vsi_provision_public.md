---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 공용 인스턴스 프로비저닝
{: #ordering-vs-public}

## 시작하기 전에
공용 가성 서버 인스턴스를 프로비저닝하는 데는 두 가지 옵션이 있습니다. 첫 번째는 {{site.data.keyword.Bluemix}} 카탈로그를 통한 방법이며 두 번째는 {{site.data.keyword.slportal_full}}을 통합 방법입니다. 카탈로그 및 {{site.data.keyword.slportal}}은 고유 로그인 ID를 필요로 합니다. 카탈로그 사용자 이름 및 비밀번호로는 포털에 로그인할 수 없으며 그 반대 또한 마찬가지입니다.
{:shortdesc}

시작하기 전에 다음 전제조건을 검토하십시오.

  1. {{site.data.keyword.Bluemix_notm}} 카탈로그 또는 {{site.data.keyword.slportal}} 신임 정보를 설정해 둔 상태인지 확인하십시오. 
  
     **참고:** {{site.data.keyword.Bluemix_notm}} 카탈로그의 경우에는 가상 서버를 주문하려면 업그레이드된 계정이 있어야 합니다. 계정 업그레이드에 대한 자세한 정보는 [IBM ID로 전환](https://console.bluemix.net/docs/admin/softlayerlink.html)을 참조하십시오.
  
  2. 사용 가능한 배치 옵션을 검토하십시오. 자세한 정보는 [배치 옵션: 공용 가상 서버](../vsi/vsi_public.html)를 참조하십시오.

## 로그인 
{{site.data.keyword.Bluemix_notm}} 카탈로그 또는 {{site.data.keyword.slportal}}을 통해 로그인했는지 확인하십시오. 

  <table>
   <CAPTION>표 1. 로그인 위치 선택</CAPTION>
   <THEAD>
   <TR>
   <th>로그인할 위치</th>
   <th>수행할 작업</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud 카탈로그</td>
   <td>
   <ol>
   <li>새 브라우저 창을 열고 <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>를 입력하십시오.</li>
   <li><b>로그인</b> 링크(오른쪽 하단에 있음)를 클릭하십시오. </li>
   <li>이메일 또는 IBM ID를 입력하고 <b>계속</b>을 클릭하십시오.</li>
   <li>비밀번호를 입력하고 <b>로그인</b>을 클릭하십시오.</li>
   <li><b>인프라 </b> > <b>계산</b>을 선택하십시오.</li>
   <li><b>Virtual Server</b> 타일을 클릭하십시오.</li>
   <li><b>공용 Virtual Server</b> 옵션을 선택하십시오.</li>
   <li><b>작성</b>을 클릭하십시오. {{site.data.keyword.slportal}}의 기본 페이지가 열립니다.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Customer Portal</td>
   <td>
   <ol>
   <li>새 브라우저 창을 열고 <a href="https://control.softlayer.com">https://control.softlayer.com</a>을 입력하십시오.</li>
   <li>사용자 이름 및 비밀번호를 입력하고 <b>로그인</b>을 클릭하십시오. 또는 <b>IBM ID로 로그인</b>을 클릭하십시오. 그 후 이메일 또는 IBM ID를 입력하고 <b>계속</b>을 클릭하십시오. 비밀번호를 입력하고 <b>로그인</b>을 클릭하십시오. {{site.data.keyword.slportal}}의 기본 페이지가 열립니다.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## 공용 가상 서버 인스턴스 프로비저닝
{: #ordering-public-instance}
전제조건을 만족하는 경우에는 공용 가상 서버 인스턴스 프로비저닝을 시작할 수 있습니다. 공용 인스턴스는 두 가지 방법(**디바이스** 메뉴 또는 **디바이스** 아이콘)으로 프로비저닝할 수 있습니다.

### 디바이스 아이콘을 통한 공용 가상 서버 인스턴스 프로비저닝
*디바이스* 아이콘을 통해 공용 가상 서버 인스턴스를 프로비저닝하려면 다음 단계를 완료하십시오.

1.  {{site.data.keyword.slportal}}에서 **주문** 섹션을 찾고 **디바이스**를 클릭하십시오.
2.  디바이스 페이지에서 Virtual Server 오퍼링 중 하나에 대해 **시간별** 또는 **월별**을 클릭하십시오.
3.  *클라우드 서버 구성* 페이지에서 모든 관련 정보를 입력하십시오.
4.  **주문에 추가** 단추를 클릭하여 계속 진행하십시오.
5.  서버의 도메인 정보를 확인하거나 편집하십시오.
5.  **클라우드 서비스 이용 약관** 및 **써드파티 서비스 계약** 선택란을 클릭하십시오.
6.  지불 정보를 확인하거나 입력하고 **주문 제출** 단추를 클릭하십시오. 사용자의 프로비저닝 주문 번호가 있는 화면으로 이동됩니다. 이는 프로비저닝 주문 영수증이기도 하므로 사용자는 이 화면을 인쇄할 수 있습니다.

 일련의 이메일(프로비저닝 주문 확인, 프로비저닝 주문 승인 및 처리, 프로비저닝 완료)이 관리자에게 발송됩니다. 프로비저닝 완료 이메일은 {{site.data.keyword.Bluemix_notm}}에 로그인한 후 *디바이스 세부사항* 페이지로 이동하는 링크를 포함합니다. {{site.data.keyword.slportal}}에 직접 로그인할 수도 있습니다.

### 디바이스 메뉴를 통한 공용 가상 서버 인스턴스 프로비저닝
{: #ordering-public-devices-menu}

기본 {{site.data.keyword.slportal}} 페이지에서 *디바이스* 메뉴를 통해 공용 가상 서버 인스턴스를 프로비저닝할 수도 있습니다. 

1. **디바이스 > 디바이스 목록**을 클릭하십시오.

   디바이스 페이지는 계정에 속한 모든 디바이스 유형(전용 호스트, 가상 서버, 베어메탈 서버 및 NetScaler 애플리케이션 제공 제어기)을 표시합니다.
2. 오른쪽 상단에 있는 **디바이스 주문** 링크를 클릭하십시오.
3. 디바이스 페이지에서 Virtual Server 오퍼링 중 하나에 대해 **시간별** 또는 **월별**을 클릭하십시오.
4. *클라우드 서버 구성* 페이지에서 모든 관련 정보를 입력하십시오.
5. **주문에 추가** 단추를 클릭하여 계속 진행하십시오.
6. 서버의 도메인 정보를 확인하거나 편집하십시오.
7. **클라우드 서비스 이용 약관** 및 **써드파티 서비스 계약** 선택란을 클릭하십시오.
8. 지불 정보를 확인하거나 입력하고 **주문 제출** 단추를 클릭하십시오. 사용자의 프로비저닝 주문 번호가 있는 화면으로 이동됩니다. 이는 프로비저닝 주문 영수증이기도 하므로 사용자는 이 화면을 인쇄할 수 있습니다.

일련의 이메일(프로비저닝 주문 확인, 프로비저닝 주문 승인 및 처리, 프로비저닝 완료)이 관리자에게 발송됩니다. 프로비저닝 완료 이메일은 {{site.data.keyword.Bluemix_notm}}에 로그인한 후 *디바이스 세부사항* 페이지로 이동하는 링크를 포함합니다. {{site.data.keyword.slportal}}에 직접 로그인할 수도 있습니다.

### 다음 단계
가상 서버가 프로비저닝된 후에는 이 서버의 관리를 시작할 수 있습니다. 자세한 정보는 [가상 서버 관리](../vsi/vsi_managing.html)를 참조하십시오.
