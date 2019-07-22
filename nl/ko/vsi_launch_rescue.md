---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 복구 커널 시작
{: #launching-rescue}

복구 커널(Rescue Kernel)은 실시간 복구 환경으로, 보통 OS 다시 로드로 해결되는 시스템 문제를 해결하기 위해 베어메탈 서버 또는 가상 서버를 온라인 상태로 전환할 수 있는 기능을 사용자에게 제공할 수 있도록 디자인되었습니다. 복구 커널은 {{site.data.keyword.cloud}} 콘솔에서 시작해야 합니다. 특정 디바이스에 대해 복구 커널을 시작하려면 다음 단계를 사용하십시오.
{:shortdesc}

## 시작하기 전에
먼저 디바이스 메뉴로 이동하여 태스크를 완료할 수 있는 올바른 계정 권한이 있는지 확인하십시오. 

* 콘솔의 디바이스 메뉴로 이동하십시오. 자세한 정보는 [디바이스로 이동](/docs/vsi?topic=virtual-servers-navigating-devices)을 참조하십시오.
* 필요한 계정 권한 및 디바이스 액세스 권한이 있는지 확인하십시오. 계정 소유자 또는 **사용자 관리** 클래식 인프라 권한이 있는 사용자만 권한을 조정할 수 있습니다. 

권한에 대한 자세한 정보는 [클래식 인프라 권한](/docs/iam?topic=iam-infrapermission#infrapermission) 및 [디바이스 액세스 관리](/docs/vsi?topic=virtual-servers-managing-device-access)를 참조하십시오.

## 복구 커널 시작

1. **디바이스** 메뉴에서 **디바이스 목록**을 선택하십시오.
2. **디바이스 목록**에서 복구할 디바이스 이름을 클릭하십시오.
3. *조치* 메뉴에서 **복구 모드**를 선택하십시오.
4. **예**를 클릭하여 디바이스를 복구 커널로 즉시 상태 전이하십시오. 

## Windows 인스턴스용 복구 커널 시작

1. **디바이스** 메뉴에서 **디바이스 목록**을 선택하십시오.
2. **디바이스 목록**에서 복구할 디바이스 이름을 클릭하십시오.
3. *조치* 메뉴에서 **이미지에서 부팅**을 선택하십시오.
4. 공용 이미지 *WindowsRescueStandalone.iso* 옆에 있는 **이 이미지에서 부팅**을 선택하십시오.

## 다음 단계
복구 커널을 시작하면 디바이스의 전원이 꺼진 후 디바이스 운영 체제의 복구 커널로 다시 부팅됩니다. 여기에는 몇 분 정도 소요될 수 있습니다.

디바이스의 IP 주소로부터 디바이스에 대한 원격 액세스가 사용 가능합니다. {{site.data.keyword.cloud_notm}} 콘솔에 기록된 디바이스의 루트 또는 관리자 인증  정보를 사용하여 복구 커널에서 디바이스에 액세스할 수 있습니다. 복구 커널을 사용할 때는 정상 부팅한 디바이스에서와 마찬가지로 문제를 검색하고 해결할 수 있습니다. 필요한 경우에는 복구 커널 OS에 드라이브를 마운트할 수 있습니다. 복구 커널을 종료하고 디바이스를 일반 환경으로 되돌리려면 디바이스를 {{site.data.keyword.cloud_notm}} 콘솔 또는 복구 커널 OS에서 다시 부팅하십시오.

디바이스를 다시 부팅하는 방법은 [가상 서버 관리](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)를 참조하십시오.
