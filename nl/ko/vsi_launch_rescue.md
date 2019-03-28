---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

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

복구 커널(Rescue Kernel)은 실시간 복구 환경으로, 보통 OS 다시 로드로 해결되는 시스템 문제를 해결하기 위해 베어메탈 서버 또는 가상 서버를 온라인 상태로 전환할 수 있는 기능을 고객에게 제공할 수 있도록 디자인되었습니다. 복구 커널은 {{site.data.keyword.slportal_full}}에서 시작해야 합니다. 특정 디바이스에 대해 복구 커널을 시작하려면 다음 단계를 사용하십시오.
{:shortdesc}

## 복구 커널 시작

1. 고유 인증 정보를 사용하여 [{{site.data.keyword.slportal}} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/)에 액세스하십시오.
2. 디바이스 목록에서 복구할 디바이스 이름을 클릭하십시오.
3. 오른쪽 상단에 있는 *조치* 드롭 다운 목록을 클릭하고 **복구**를 선택하십시오. (또는 *원격 관리* 탭을 클릭하고 **복구**를 선택할 수 있습니다.)
4. **예** 단추를 클릭하여 디바이스를 복구 커널로 즉시 상태 전이하십시오. 조치를 취소하려면 **아니오** 단추를 클릭하십시오.

## Windows VSI에서

1. 고유 인증 정보를 사용하여 [{{site.data.keyword.slportal}} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/)에 액세스하십시오.
2. 디바이스 목록에서 복구할 디바이스 이름을 클릭하십시오.
3. 오른쪽 상단에 있는 *조치* 드롭 다운 목록을 클릭하고 **이미지에서 부팅**을 선택하십시오.
4. 공용 이미지 *WindowsRescueStandalone.iso* 옆에 있는 **이 이미지에서 부팅**을 선택하십시오.


## 다음 단계
복구 커널을 시작하면 디바이스의 전원이 꺼진 후 디바이스 운영 체제의 복구 커널로 다시 부팅됩니다. 여기에는 몇 분 정도 소요될 수 있습니다.

디바이스의 IP 주소로부터 디바이스에 대한 원격 액세스가 사용 가능합니다. {{site.data.keyword.slportal}}에 기록된 디바이스의 루트 또는 관리자 인증 정보를 사용하여 복구 커널에서 디바이스에 액세스할 수 있습니다. 복구 커널을 사용할 때는 정상 부팅한 디바이스에서와 마찬가지로 문제를 검색하고 해결할 수 있습니다. 필요한 경우에는 복구 커널 OS에 드라이브를 마운트할 수 있습니다. 복구 커널을 종료하고 디바이스를 일반 환경으로 되돌리려면 디바이스를 {{site.data.keyword.slportal}} 또는 복구 커널 OS에서 다시 부팅하십시오.

디바이스를 다시 부팅하는 방법은 [가상 서버 관리](/docs/vsi?topic=virtual-servers-managing-virtual-servers)를 참조하십시오.
