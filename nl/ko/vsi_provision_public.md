---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-17"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 공용 인스턴스 프로비저닝
{: #ordering-vs-public}

## 시작하기 전에
공용 가상 서버 인스턴스를 프로비저닝하는 데는 두 가지 옵션이 있습니다. 첫 번째는 {{site.data.keyword.cloud}} 콘솔을 통한 방법이며 두 번째는 {{site.data.keyword.slportal}}을 통한 방법입니다. 콘솔 및 {{site.data.keyword.slportal}}은 고유 로그인 ID를 필요로 합니다. 콘솔 사용자 이름 및 비밀번호를 사용하여 포털에 로그인할 수 없으며 그 반대 또한 마찬가지입니다.
{:shortdesc}

{{site.data.keyword.cloud_notm}} 콘솔의 경우, 가상 서버를 주문하려면 업그레이드된 계정이 있어야 합니다. 계정 업그레이드에 대한 자세한 정보는 [종량과금제](/docs/account?topic=account-accounts#paygo)를 참조하십시오.
{:note}

시작하기 전에 다음 전제조건을 검토하십시오.

  1. 사용 가능한 배치 옵션을 검토하십시오. 자세한 정보는 [공용 가상 서버](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)를 참조하십시오.

  2. 가상 서버 인스턴스 용량 고려사항을 검토하십시오.  자세한 정보는 [가상 서버 인스턴스에 대한 리소스 고려사항](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations)을 참조하십시오.
  
  3. {{site.data.keyword.cloud_notm}} 콘솔에서 [가상 서버 인스턴스 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} 페이지를 여십시오. 

## 공용 가상 서버 인스턴스 프로비저닝  
{: #ordering-public-instance}

가상 서버 인스턴스를 프로비저닝하려면 다음 정보를 고려해야 합니다. 

사용 가능한 모든 옵션을 보려면 로그인해야 합니다.
{:tip}

### 공용 인스턴스

| 필드    |세부사항 |
| -------- | ----------- |
| 비용 청구  |가상 서버 인스턴스에 따라 시간별 또는 월별 비용 청구 중 하나를 선택할 수 있습니다. 비용 외의 기본적인 차이점은 시간별 인스턴스에 대역폭 할당이 포함되지 않는다는 점입니다. 비용 청구 기간의 끝에, 대역폭 사용량과 계정에서 각 인스턴스가 활성 상태였던 시간이 계산됩니다. 예를 들어, 10일 후에 시간별 인스턴스를 취소하면 10일 동안의 시간에 대해서만 비용을 지불합니다. 10일 후에 월별 인스턴스를 취소하면 한 달의 비용을 지불합니다. 시간별 인스턴스에서만 사용 가능한 비용 청구 일시중단 기능에 관심이 있는 경우 [비용 청구 일시중단 정보](/docs/vsi?topic=virtual-servers-about-suspend-billing)를 참조하십시오. |
|호스트 이름 | 마침표로 구분하여 영문자 및 대시로 구성된 레이블을 포함할 수 있습니다. 레이블은 숫자로만 구성될 수 없고, 대시로 시작되거나 끝날 수 없으며 연속해서 대시 또는 마침표를 사용할 수 없습니다. |
|도메인 | 마침표로 구분하여 영문자 및 대시로 구성될 수 있는 둘 이상의 레이블이 있어야 합니다. 레이블은 대시로 시작되거나 끝날 수 없으며 연속해서 대시 또는 마침표를 사용할 수 없습니다. 마지막 레이블은 문자로만 구성되어야 합니다.|
| 배치 그룹 | 사용자 인스턴스에 적합한 배치 그룹을 선택할 수 있습니다. 배치 그룹을 추가하는 경우 "분산" 규칙은 인스턴스가 다른 실제 하드웨어에 있음을 의미합니다. 자세한 정보는 [배치 그룹](/docs/vsi?topic=virtual-servers-placement-groups)을 참조하십시오.|
| 위치  | 위치는 지역(특정 지리적 영역)과 구역(지역 내 결함 허용 데이터 센터)로 구성됩니다. 가상 서버 인스턴스를 작성할 위치를 선택하십시오. |
| 인기 있는 프로파일 | 가장 일반적인 유스 케이스를 지원하는 인기 있는 프로파일 구성에서 선택해 보십시오. 프로파일에는 몇 분 내에 사용할 수 있는 사전 구성된 인스턴스가 포함되어 있습니다. |
|모든 프로파일 | 공용 인스턴스에서 사용 가능한 프로파일 옵션에 대한 자세한 정보는 [공용 가상 서버](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)를 참조하십시오. |
|SSH 키     | SSH 키는 인스턴스에서 구현되는 각 공개 키에 대한 해당 클라이언트의 비밀번호를 사용하지 않고 인스턴스에 액세스할 수 있도록 합니다. SSH 키 추가를 결정한 경우 인스턴스가 프로비저닝된 후 인스턴스에 로그인할 수 있는 SSH 키의 공개 키를 제공하십시오.|
| 이미지 | 이미지는 사용자 인스턴스에 적합한 배치된 운영 체제입니다. 선택할 수 있는 무료 옵션에는 CentOS 및 Ubuntu 등과 같은 몇 가지 옵션이 있습니다. Windows Server 및 Red Hat Enterprise Linux(RHEL)와 같은 유료 옵션 또한 사용 가능합니다. Windows는 100의 기본 디스크를 필요로 한다는 점을 참고하십시오.|
{: caption="표 1. 공용 인스턴스 옵션" caption-side="top"}

### 공용 인스턴스 추가 기능 

OS, 제어판 또는 소프트웨어 추가 기능을 선택하는 경우 인스턴스 주문 시 오류가 발생하지 않도록 이미지와 호환되어야 합니다. 예를 들어, RedHat 이미지를 Microsoft 데이터베이스와 프로비저닝할 수 없습니다.
{:important}

| 필드     |세부사항 |
| --------- | ----------- |
| OS 추가 기능 | 월별 비용 청구를 선택하는 경우 다음 이미지 추가 기능을 선택할 수 있습니다. <br><br> **R1Soft Server Backup Manager**는 고성능 디스크 대 디스크 서버 백업 및 중앙 관리와 데이터 저장소를 제공합니다. R1Soft 추가 기능을 선택하는 경우 **서비스** 섹션의 CDP 추가 기능인 R1Soft Backup Agent 팩을 구입해야 합니다. 하나만 선택하면 주문 시 오류가 발생합니다. R1Soft 및 IBM Cloud에 대한 자세한 정보는 [R1Soft Server Backup Manager ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/cloud/backup-and-restore?mhq=R1Soft%20Server%20Backup%20Manager&mhsrc=ibmsearch_a){: new_window}를 참조하십시오.<br><br>**Veeam Backup and Replication**은 자동화된 백업을 복원 및 복제 기능과 결합합니다. Veeam은 또한 고급 모니터링, 보고 및 용량 계획을 제공합니다. Veeam Backup and Replication에 대한 자세한 정보는 [IBM 스토리지에서의 Veeam Backup and Replication ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www-356.ibm.com/partnerworld/gsd/solutiondetails.do?solution=54724&lc=en&stateCd=P&tab=2){: new_window}을 참조하십시오.<br><br>**VMware vCenter**는 유연하고 사용자 정의할 수 있는 VMware 솔루션에 필요한 기본 VMware vSphere 및 VMware vCenter Server 계층의 배치를 자동화합니다. vCenter on IBM Cloud에 대한 자세한 정보는 [vCenter Server on IBM Cloud 정보 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/downloads/cas/L7RKPZND?mhq=vmware%20vcenter&mhsrc=ibmsearch_a){: new_window}를 참조하십시오.|
| 제어판 소프트웨어 | 월별 비용 청구를 선택하는 경우 웹 호스팅을 위해 제어판을 추가할 수 있습니다. |
| 데이터베이스 소프트웨어 | 설치할 데이터베이스 소프트웨어를 선택할 수 있습니다. {{site.data.keyword.cloud_notm}}는 프로비저닝 프로세스 중에 배치되는 데이터베이스 소프트웨어를 지원합니다. 서버가 배치된 후 사용자가 자신의 데이터베이스 소프트웨어를 설치할 수도 있습니다.|
|서비스| 일부 서비스는 비용 청구 및 이미지 선택사항에 따라 사용자에 맞게 자동으로 선택됩니다. 사용자 인스턴스에 적합한 나머지 서비스 추가 기능에서 선택할 수 있습니다. |
| 스크립트 프로비저닝 |스크립트 프로비저닝은 일반적으로 서버에 고객 고유 구성을 적용하고 스케일링 전략의 자동화를 돕기 위해 사용됩니다. 스크립트 프로비저닝은 결합된 2진 파일 또는 OS 지원 언어를 포함하여 운영 체제(OS)가 실행할 수 있는 모든 파일일 수 있습니다. 프로비저닝 스크립트는 cloud-init 이미지에서 사용될 수 없습니다. 자세한 정보는 [스크립트 프로비저닝](/docs/vsi?topic=virtual-servers-provisioning-scripts)을 참조하십시오.|
| 사용자 데이터 | 자동으로 일반적인 구성 태스크를 수행하거나 스크립트를 실행하는 사용자 데이터를 추가할 수 있습니다. 사용자 데이터는 cloud-init 및 non-cloud-init 이미지에 사용될 수 있습니다. |
{: caption="표 2. 공용 인스턴스 추가 기능" caption-side="top"}

### 연결된 스토리지 디스크

추가 스토리지가 필요한 경우 스토리지 디스크를 인스턴스에 연결할 수 있습니다. 사용 가능한 스토리지 디스크 유형은 선택하는 프로파일에 따라 달라집니다. 예를 들어, 밸런스된 로컬 프로파일 및 일부 GPU 프로파일은 로컬 기반 디스크를 사용합니다. 월별 비용 청구를 선택하는 경우 {{site.data.keyword.backup_notm}}을 추가하고 요구사항에 가장 적합한 옵션을 선택할 수 있습니다. 자세한 정보는 [{{site.data.keyword.backup_notm}} 서비스](/docs/infrastructure/Backup?topic=Backup-getting-started)를 참조하십시오.

### 네트워크 인터페이스

| 필드    |세부사항 |
| -------- | ----------- |
| 업링크 포트 속도 |사용자 인스턴스에 맞게 최대 1GB/s까지 업링크 속도를 선택할 수 있습니다. 이러한 가상 업링크는 IBM 공용 및 전용 네트워크에 대한 중복 실제 업링크에 의해 지원됩니다. 공용 및 전용 속도는 주문 시에 항상 동일하며, 필요한 경우 링크를 업그레이드 또는 다운그레이드하는 옵션이 있습니다. |
|사설 및 공용 보안 그룹 |보안 그룹을 사용하여 인스턴스의 공용 및 사설 인터페이스에 대한 수신 및 발신 트래픽을 처리하는 방법을 정의하는 IP 필터 규칙 세트를 설정할 수 있습니다. 자세한 정보는 [IBM Security Groups 정보](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups)를 참조하십시오. |
|사설 및 공용 VLAN | 기본적으로 가상 서버 인스턴스는 지정된 VLAN에 자동으로 배치됩니다. 선택된 데이터 센터에 이미 VLAN이 있는 경우 다른 VLAN을 선택할 수 있습니다. 자세한 정보는 [VLAN 정보](/docs/infrastructure/vlans?topic=vlans-about-vlans)를 참조하십시오. |
|사설 및 공용 서브넷 |서브넷 선택은 선택사항이며 디바이스가 서브넷의 IP 주소를 사용해야 하는 경우에만 사용됩니다. 서브넷을 선택하는 경우, 요청 처리를 위한 충분한 IP 주소가 있는지 확인하십시오. 서브넷에 대해 충분한 IP 주소가 없는 경우에는 주문이 지연되거나 취소될 수 있습니다. 자세한 정보는 [서브넷 및 IP 정보](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips)를 참조하십시오. |
{: caption="표 3. 네트워크 인터페이스 옵션" caption-side="top"}

### 네트워크 인터페이스 추가 기능

| 필드    |세부사항 |
| -------- | ----------- |
|대역폭 | 250GB에는 공용 업링크가 있는 월별 인스턴스가 포함되어 있습니다. 초과 비용에 비해 저렴한 가격으로 더 큰 할당량을 구입할 수 있습니다. |
| 하드웨어 및 소프트웨어의 방화벽 |방화벽 서비스는 서버에서 원하지 않는 트래픽을 방지하고 공격의 가능성을 줄이고 서버 리소스가 원래 의도에 충실하게 작업할 수 있게 해 줍니다.|
| 기본 IP 주소 | 기본 IP 주소는 자동으로 인스턴스에 지정됩니다. |
| 공용 보조 IP 주소 | 이 서브넷은 가상 서버 인스턴스의 기간 동안 사용자가 소유합니다. 서브넷을 개별적으로 취소할 수 있으나 인스턴스를 취소하면 서브넷도 제거됩니다. 자세한 정보는 [서브넷 및 IP 정보](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips)를 참조하십시오. |
| IPv6 및 공용 정적 IPv6 주소 | 사용자 인스턴스에 맞게 IPv6 주소 또는 공용 정적 IPv6 주소를 선택할 수 있습니다. |
| VPN 관리 | 이 옵션은 무제한 SSL VPN 사용자를 포함하여 사용자 인스턴스에 맞게 자동으로 선택됩니다. 자세한 정보는 [VPN 정보](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn)를 참조하십시오. |
{: caption="표 4. 네트워크 인터페이스 추가 기능" caption-side="top"}


## 고객 포털을 통해 공용 인스턴스 프로비저닝
{{site.data.keyword.slportal}}을 통해 공용 가상 서버 인스턴스를 프로비저닝하려면 다음 단계를 완료하십시오.

  1. 고유 인증 정보를 사용하여 [{{site.data.keyword.slportal}} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}에 로그인하십시오.
  2. **주문** 섹션을 찾고 **디바이스**를 클릭하십시오.
  3. 디바이스 페이지에서, Virtual Server 오퍼링 중 하나에 대해 **시간별 SAN**, **시간별 로컬**, **월별** 또는 **임시**를 클릭하십시오.
  4. *클라우드 서버 구성* 페이지에서 모든 관련 정보를 입력하십시오.
  5. **주문에 추가**를 클릭하여 계속 진행하십시오.
  6. 서버의 도메인 정보를 확인하거나 편집하십시오.
  7. **클라우드 서비스 이용 약관** 및 **서드파티 서비스 계약** 선택란을 클릭하십시오.
  8. 지불 정보를 확인하거나 입력하고 **주문 제출**을 클릭하십시오. 사용자의 프로비저닝 주문 번호가 있는 화면으로 이동됩니다. 이는 프로비저닝 주문 영수증이기도 하므로 사용자는 이 화면을 인쇄할 수 있습니다.

## 다음 단계
일련의 이메일(프로비저닝 주문 확인, 프로비저닝 주문 승인 및 처리, 프로비저닝 완료)이 관리자에게 발송됩니다. 프로비저닝 완료 이메일은 {{site.data.keyword.Bluemix_notm}}에 로그인한 후 *디바이스 세부사항* 페이지로 이동하는 링크를 포함합니다. 

가상 서버가 프로비저닝되어 사용 가능한 상태가 되면 {{site.data.keyword.cloud_notm}} 콘솔 또는 {{site.data.keyword.slapi_short}}를 사용하여
가상 서버를 구성할 수 있습니다. 자세한 정보는 [가상 서버 구성](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers)을 참조하십시오.
