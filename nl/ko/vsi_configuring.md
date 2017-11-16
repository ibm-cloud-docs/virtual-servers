---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 가상 서버 구성
{: #configuring-virtual-servers}

가상 서버에 대한 액세스 권한을 확보한 후에는 이를 사용자 환경의 요구사항에 맞게 구성해야 합니다.
{:shortdesc}

## 로그인 
계정이 처음 작성될 때 이메일에서 수신한 신임 정보를 사용하여 [{{site.data.keyword.slportal_full}} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}에 로그인하십시오.

## 가상 서버 찾기
{{site.data.keyword.slportal}}의 디바이스 목록에서 가상 서버를 찾으십시오. 디바이스 목록에서는 디바이스를 관리하거나, 업그레이드하거나 대역폭 사용량 차트를 생성할 수 있습니다. 자세한 정보는 [가상 서버 관리](../vsi/vsi_managing.html)를 참조하십시오. 

## IP 주소 및 신임 정보 기록
{{site.data.keyword.slportal}}에 로그인할 필요 없이 빠르게 액세스할 수 있도록 안전한 위치에 서버의 IP 주소 및 신임 정보에 대한 로그를 보관하십시오. 
- 개별 디바이스의 IP 주소는 디바이스 목록에서 볼 수 있습니다. 
- 개별 디바이스의 루트 비밀번호는 디바이스의 스냅샷 보기에서 볼 수 있습니다. 이 보기를 펼치려면 디바이스 이름 옆에 있는 화살표를 클릭하십시오. 
- 여러 디바이스의 IP 주소는 디바이스 목록 내의 CSV 다운로드 조치를 사용하여 볼 수 있습니다. 디바이스 및 상세 정보의 전체 목록을 스프레드시트 형식으로 다운로드하려면 설정 섹션에서 CSV 다운로드를 선택하십시오. 

## 소프트웨어 신임 정보 업데이트
프로비저닝 프로세스 중에 사용자의 디바이스에 로드된 모든 소프트웨어에는 임시 신임 정보가 지정되어 있습니다. 이러한 신임 정보는 {{site.data.keyword.slportal}}에 있는 각 디바이스의 비밀번호 탭에서 보고 관리할 수 있습니다. 소프트웨어에 처음 액세스할 때는 이러한 임시 신임 정보를 사용하십시오. 우수 사례로써, 소프트웨어에 처음 액세스한 후에는 이 비밀번호를 변경하십시오. 문자, 숫자 및 기호 조합으로 구성된 보안성 높은 비밀번호를 사용하십시오. 

선택적으로, 각 디바이스의 비밀번호 탭에 비밀번호 업데이트를 저장할 수 있습니다. 그러나 {{site.data.keyword.slportal}}에 비밀번호를 저장하면 계정에 대한 액세스 권한 및 적절한 권한을 가진 모든 사용자가 비밀번호 화면에서 저장된 비밀번호를 볼 수 있다는 점을 참고하십시오.

소프트웨어 신임 정보를 보고 관리하는 데 대한 자세한 정보는 [소프트웨어 사용자 및 비밀번호 추가, 삭제 및 업데이트 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://knowledgelayer.softlayer.com/procedure/add-delete-and-update-software-users-and-passwords){: new_window}를 참조하십시오. 

## 사설 네트워크의 서버에 액세스
사설 네트워크는 SSH 및 KVM over IP를 사용하여 원격 데스크탑(RDP)을 통해 디바이스와 상호작용하기 위한 전제입니다. VPN 액세스 도구는 가장 가까운 SSL VPN 엔드포인트 또는 원하는 엔드포인트에 대해 사설 네트워크 연결을 설정할 수 있게 해 줍니다. VPN 액세스는 제공되는 여러 서비스와 상호작용하기 위해서도 필요합니다. 자세한 정보는 [{{site.data.keyword.cloud}} VPN 시작하기 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://knowledgelayer.softlayer.com/procedure/getting-started-softlayer-vpn){: new_window}를 참조하십시오.

## 모니터링 설정
모니터링은 대개 서버 가동시간을 확인하기 위한 자원으로 사용되지만, 스케일 시점을 파악하는 데도 유용할 수 있습니다. 표준 모니터링 및 Nimsoft Monitoring 서비스는 모두 다양한 모니터링 요구사항을 만족시키는 데 사용할 수 있습니다. "기본 모니터링"이라고도 하는 표준 모니터링은 주로 {{site.data.keyword.slportal}}을 사용하여 시작되는 느린 ping 또는 서비스 ping을 사용하는 ping 실행 및 응답 방법에서 사용됩니다. "고급 모니터링"이라고도 하는 Nimsoft Monitoring은 기본, 고급, 프리미엄의 3개 계층으로 사용 가능합니다. 이 서비스는 {{site.data.keyword.slportal}}을 통해서도 액세스할 수 있습니다. 모니터링을 통해 시스템 상태를 계속해서 확인하는 방법을 알아보려면 [모니터링 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://knowledgelayer.softlayer.com/topic/monitoring){: new_window}을 참조하십시오. 

## 시스템 보안
하드웨어 방화벽을 사용하여 디바이스를 항상 안전한 상태로 보호할 수 있습니다. 하드웨어 방화벽은 요청 시 작동 중지 시간 없이 프로비저닝됩니다. 방화벽은 규칙이 적절히 설정되면 사용자가 원치 않는 활동으로부터 서버를 보호할 수 있습니다. 방화벽을 주문하고 나면 이를 사용으로 설정하고 규칙을 설정해야 합니다. 방화벽을 최대한 활용하는 방법에 대한 자세한 정보는 [Firewall ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://knowledgelayer.softlayer.com/topic/firewall){: new_window}을 참조하십시오. 

보안 그룹은 가상 서버의 네트워크 트래픽을 제한하는 데 사용할 수 있는 또 다른 옵션입니다. 보안 그룹을 사용하여 가상 서버 인스턴스의 공용 및 개인용 인터페이스에 대한 수신 및 발신 트래픽을 처리하는 방법을 정의하는 IP 필터 규칙 세트를 설정할 수 있습니다. 자세한 정보는 [보안 그룹 시작하기](/docs/infrastructure/security-groups/sg_index.html)를 참조하십시오-.

## 백업 스케줄 
백업은 데이터를 외부에 안전하게 저장하고 데이터가 유실되는 경우 이를 보호할 수 있게 해 줍니다. 정보를 디바이스에 다시 로드해야 하는 경우를 위해 데이터를 안전한 위치에 저장하는 데 다음 백업 서비스를 사용할 수 있습니다. 
- EVault 백업은 자동화된 에이전트 기반 백업 시스템입니다. 이는 "한 번만 설정하면 되는" 인기 디바이스 관리 솔루션입니다. 이는 추가 플러그인을 통해 Exchange 및 SQL과 같은 Microsoft 소프트웨어와 호환 가능합니다. EVault 사용자는 EVault의 WebCC 웹 기반 애플리케이션을 통해 이 서비스와 상호작용합니다. 자세한 정보는 [EVault ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://knowledgelayer.softlayer.com/topic/evault-backup){: new_window}를 참조하십시오. 
- [R1Soft Continuous Data Protection(CDP) ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://knowledgelayer.softlayer.com/topic/r1soft-cdp){: new_window}은 서버 또는 자체 관리 가상 머신에 설치할 수 있는 백업 소프트웨어입니다. 이는 하나의 인터페이스에서 모든 백업을 관리하려는 경우 권장됩니다. 사용자는 가상 머신에 에이전트를 설치할 수 있게 해 주며 추가 기능을 위한 데이터베이스 플러그인을 제공하는 독점 관리 시스템을 통해 R1Soft CDP와 상호작용합니다. 

## 다음 단계
가상 서버가 구성된 후에는 이 서버의 관리를 시작할 수 있습니다. 자세한 정보는 [가상 서버 관리](../vsi/vsi_managing.html)를 참조하십시오. 



