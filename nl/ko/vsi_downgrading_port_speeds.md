---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-29"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 포트 속도 다운그레이드
{: #downgrading-port-speeds}

티켓을 열지 않고도 가상 서버 인스턴스의 포트 속도를 임시로 다운그레이드할 수 있습니다. 이미 지불한 최대값에서 다운그레이드, 연결 끊기 또는 다시 연결만 가능합니다. 이 옵션에서는 업그레이드할 수 없습니다. 다시 변경할 때까지 콘솔에서 변경이 유지됩니다. 이 상태에서는 비용 변경이 발생하지 않으며 서버를 다운그레이드해도 비용이 임시로 낮아지지는 않습니다. 포트 속도를 영구적으로 변경하려면 판매 티켓을 열어야 합니다.
{:shortdesc}

## 시작하기 전에
먼저 디바이스 메뉴로 이동하여 태스크를 완료할 수 있는 올바른 계정 권한이 있는지 확인하십시오.  

* 콘솔의 디바이스 메뉴로 이동하십시오. 자세한 정보는 [디바이스로 이동](/docs/vsi?topic=virtual-servers-navigating-devices)을 참조하십시오.
* 필요한 계정 권한 및 디바이스 액세스 권한이 있는지 확인하십시오. 계정 소유자 또는 **사용자 관리** 클래식 인프라 권한이 있는 사용자만 권한을 조정할 수 있습니다.  

권한에 대한 자세한 정보는 [클래식 인프라 권한](/docs/iam?topic=iam-infrapermission#infrapermission) 및 [디바이스 액세스 관리](/docs/vsi?topic=virtual-servers-managing-device-access)를 참조하십시오.

## 포트 속도 다운그레이드
다음 단계를 완료하여 포트 속도를 다운그레이드하십시오.

1. **디바이스** 메뉴에서 **디바이스 목록**을 선택하십시오.
2. 업데이트하려는 서버를 선택하십시오.
3. **개요** 탭에서 **네트워크 세부사항**으로 이동하십시오.
4. **속도**(공용 또는 사설 네트워크)의 드롭 다운 메뉴를 선택하여 포트 속도를 다운그레이드하거나 연결을 끊으십시오. 

어떤 이유로든 포트 속도를 변경하거나 포트 연결을 끊는 경우, 서버 자체를 수동으로 변경해야 합니다.
{:tip}
