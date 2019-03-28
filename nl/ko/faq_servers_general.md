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
{:faq: data-hd-content-type='faq'}


# FAQ: 서버(일반)
{: #faqs-servers-general-}

## "이미지에서 부팅"과 "이미지에서 로드"의 차이점은 무엇입니까?
{:faq}

이미지에서 부팅과 이미지에서 로드는 모두 기존 문제를 해결하기 위해 기존 운영 체제를 대체하거나 운영 체제를 보강하려는 목적으로 디바이스에 적용되는 기존 이미지 템플리트를 이용합니다. 부팅과 로드 프로세스의 주된 차이점은 사용하는 이미지의 유형입니다. 이미지에서 부팅 또는 로드 프로세스를 수행할 때는 나중에 문제가 발생한 경우 복구할 모든 데이터를 백업했는지 확인하십시오.

   * 이미지에서 부팅은 시스템 복구를 위해 {{site.data.keyword.BluSoftlayer_full}}에서 제공한 ISO 또는 {{site.data.keyword.slportal_full}}의 *이미지 내보내기* 기능을 사용하여 업로드된 ISO를 사용하여 디바이스를 부팅하는 방법입니다. 이 ISO는 디바이스에 문제가 발생한 경우 이를 해결하기 위해 사용할 수 있는 디바이스 운영 체제의 클린 버전이거나 복구 디스크일 수 있습니다.
   * 이미지에서 로드는 디바이스에서 캡처되거나 {{site.data.keyword.slportal}}의 *이미지 가져오기* 기능을 사용하여 업로드된 이미지 템플리트를 이용하는 OS 다시 로드 방법입니다. *이미지에서 로드* 옵션은 디바이스에서 모든 데이터를 제거하고 기존 운영 체제와 파일을 선택한 이미지의 "새 것과 같은" 버전으로 대체하는 VHD를 사용하여 다시 로드를 수행합니다.

## KVM 콘솔에 연결할 수 없는 이유는 무엇입니까?
{:faq}

KVM 콘솔에 연결할 수 없는 경우에는 아래 문제점 해결 팁을 검토하여 문제를 해결하는 데 도움을 받으십시오. 추가 문제가 발생하는 경우에는 지원에 문의하십시오. 지원 문의에 대한 자세한 정보는 [도움 및 지원 받기](/docs/vsi?topic=virtual-servers-gettinghelp)를 참조하십시오.

   * KVM 콘솔은 Java 애플릿입니다. 이 콘솔에 액세스하려면 먼저 Java가 설치되어 있어야 합니다. Java를 설치하는 데 대한 자세한 정보는 [무료 Java 다운로드 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.java.com/en/download/){: new_window}를 참조하십시오.  
   * Java가 설치된 경우에는 VPN을 사용하여 연결이 설정되었는지 확인하십시오. 연결이 설정되지 않은 경우에는 VPN 연결이 필요한 KVM 콘솔에 연결하려 할 때 경고가 표시됩니다.
   * KVM 콘솔은 연결 프로세스 중에 하나 이상의 팝업을 생성할 수 있습니다. {{site.data.keyword.slportal}}에서 팝업을 사용하여 연결이 설정될 수 있는지 확인하십시오.
   * "Java applications are blocked by your security settings."라는 오류가 수신될 수 있습니다. 베어메탈 iKVM 디바이스의 경우에는 IPMI 디바이스의 IP 주소에 대한 예외를 추가해야 합니다. VSI 디바이스의 경우에는 "https: //control.softlayer.com", 그리고 KVM의 IP 주소를 허용하도록 하십시오. 자세한 정보는 [최신 Java를 사용 중인 상태에서 보안 설정이 Java 애플리케이션을 차단하는 이유는 무엇입니까? ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.java.com/en/download/help/java_blocked.xml){: new_window}를 참조하십시오.
   * 위 조건을 만족하는 상태에서 "Missing required Permissions manifest in main.jar"라는 오류를 수신하는 경우에는 Java 제어판에서 Java 애플릿이 사용으로 설정되지 않은 것입니다. 이 설정은 Oracle에 의해 Java SE v7에서 보안 예방조치로 도입되었습니다. 이 문제를 해결하려면 제어판에서 애플릿을 사용으로 설정하십시오.

     **참고:** Mac OSX를 Google Chrome과 함께 사용하고 있는 경우에는 Java 웹 사이트에 있는 Mac Java 7 설치 및 사용에 대한 정보 및 시스템 요구사항을 참조하십시오.

   * 표준 Java를 통해 VSI에 연결하려 시도했으나 오류만 수신하는 경우에는 VNC를 사용해 볼 수도 있습니다.

위 확인을 완료했으나 여전히 KVM 콘솔에 연결할 수 없는 경우에는 추가 지원을 받고 문제를 해결하기 위해 지원에 문의하십시오. 콘솔에 대한 연결이 설정되었으나 디바이스에 연결하는 중에 문제가 발생하는 경우에는 디바이스에 액세스하는 데 사용되는 인증 정보가 유효한지 확인하십시오. 필요한 경우에는 계정 관리자에 문의하여 인증 정보를 확인하십시오.

## 서버에 대한 비밀번호를 잃어버렸습니다. 어떻게 하면 복구할 수 있습니까?
{:faq}

서버에 대한 루트 또는 관리자 비밀번호가 갑자기 작동하지 않는 경우 다음 항목을 확인하십시오. 필요한 경우 지시사항에 따라 복구 커널을 시작하고 비밀번호를 재설정하십시오.

   * 비밀번호를 복사하여 붙여넣고 있습니까? 그렇지 않은 경우에는 이를 시도해 보십시오. 비밀번호를 메모장에 복사하여 공백이 실수로 비밀번호와 함께 복사되지 않았는지 확인하십시오.
   * 서버에 cPanel이 있는 경우에는 실패한 로그인으로 인해 cPHulk에서 사용자의 IP 주소를 차단했을 가능성이 있습니다. 이러한 경우에는 KVM 또는 IPMI를 사용하여 서버에 액세스한 후 cPHulk에서 "/scripts/cphulkdwhitelist"를 입력하고 그 뒤에 사용자의 IP 주소를 붙여 해당 주소를 화이트리스트에 추가할 수 있습니다.
   * 누군가 최근에 {{site.data.keyword.slportal}}?에서 비밀번호를 수정하여 서버에 대한 비밀번호를 변경하려 시도했습니까? {{site.data.keyword.slportal}}에서 비밀번호를 변경하면 비밀번호로 표시되는 것만 변경됩니다. 서버가 사용하고 있는 비밀번호는 변경되지 않습니다. 이 상황이 발생한 경우에는 지원에 문의하면 작동하는 원래 비밀번호를 복구할 수 있습니다.
   * 비밀번호를 재설정하기 위해서는 운영 체제의 복구 모드로 부팅해야 할 수 있습니다. 자세한 정보는 [복구 커널 실행](/docs/vsi?topic=virtual-servers-launching-rescue)을 참조하십시오.

이러한 항목을 모두 확인했으나 여전히 비밀번호를 사용하여 서버에 연결할 수 없는 경우에는 티켓을 사용해 지원에 문의하여 비밀번호 재설정을 요청하십시오. 지원에서 비밀번호를 재설정하려면 서버를 다시 부팅해야 하므로, 다시 부팅을 승인할 수 있도록 준비하고 다시 부팅을 수행했으면 하는 유지보수 시간 범위를 제공하십시오. 대부분의 비밀번호 재설정은 15분 내에 완료됩니다. {{site.data.keyword.slportal}}에서는 **지원 > 티켓 추가**로 이동해 주제 *"다시 부팅 및 콘솔 액세스"*를 사용하여 티켓을 작성할 수 있습니다.

## LVM 파티션은 유효한 파일 시스템으로 지원됩니까?
{:faq}

LVM(Logical Volume Management)은 Linux에서 파일 시스템의 논리적 볼륨 관리를 제공합니다. {{site.data.keyword.BluSoftlayer}} 환경에서는 LVM이 부트 가능한 파티셔닝 스킴으로 지원되지 않습니다. 가상 서버 인스턴스는 LVM과 함께 주문할 수 없으며, LVM을 부트 파티션으로 사용하는 이미지 가져오기는 프로비저닝에 실패합니다. 부트 파티션에서 LVM을 필요로 하는 경우에는 베어메탈 오퍼링이 특정 운영 체제에 대해 부트에서 LVM을 지원할 수 있습니다. 적절한 OS 지원 및 구성을 갖춘 경우에는 2차 VSI 디스크를 LVM 파티션으로 사용할 수 있으나, LVM은 Flex 이미지 또는 이미지 템플리트에 대해 지원되는 파일 시스템이 아니라는 점을 명심해야 합니다. 추가 질문이 있는 경우에는 도움을 줄 수 있는 지원 팀에게 티켓을 작성하십시오.

## 고객 호스트에 사전 구성된 161.26.0.0/16 라우트
{:faq}

{{site.data.keyword.BluSoftlayer}}에서는 향후 제품을 지원하기 위해 새로 프로비저닝된 모든 서버에서 새 라우트를 사용으로 설정합니다.
   * 이 라우트는 161.26.0.0/16 범위(161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255)에서 백엔드 사설 네트워크로 연결된 모든 주소를 가리킵니다.
   * 이 IP 블록은 IANA에 의해 {{site.data.keyword.BluSoftlayer_notm}}에 지정되었으며 공용 인터넷에 공표되지 않습니다.
   * 이 영역에서는 {{site.data.keyword.BluSoftlayer_notm}} 시스템만 주소 지정됩니다.
   * 고객 서버, 가상 서버 및 Vyatta 게이트웨이의 ACL은 고객 호스트가 이 범위 외의 IP 주소로 구성된 인프라 서비스를 사용할 수 있도록 업데이트되어야 합니다.

## 다양한 OS에서 새 라우팅을 추가하는 방법
{:faq}

   <table>
   <CAPTION>표 1. OS별 라우트 추가 방법</CAPTION>
   <THEAD>
   <TR>
   <th>운영 체제</th>
   <th>단계</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Windows 2003 Standard 및 Enterprise</td>
   <td>
   다음 내용을 명령행에서 입력하여 지속적 라우트를 추가하십시오.
   <blockquote>route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p</blockquote>
   <b>참고:</b> 10.0.0.1을 사용자의 개인용 게이트웨이 IP 주소로 대체하십시오.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Server Core
   </td>
   <td>
   다음 내용을 명령행에서 입력하여 지속적 라우트를 추가하십시오.
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>참고:</b> 10.0.0.1을 사용자의 개인용 게이트웨이 IP 주소로 대체하십시오.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Web, Standard, Enterprise 및 Datacenter</td>
   <td>
   다음 내용을 명령행에서 입력하여 지속적 라우트를 추가하십시오.
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>참고:</b> 10.0.0.1을 사용자의 개인용 게이트웨이 IP 주소로 대체하십시오.
   </td>
   </tr>
    <tr>
   <td>RedHat, Fedora 및 CentOS</td>
   <td>
   파일 <i>/etc/sysconfig/network-scripts/route-eth0</i>을 편집/작성하여 새 라우트를 작성하십시오.
   <p>이 파일은 작성한 후에는 여기에 <i>161.26.0.0/16 via 10.0.0.1</i>을 추가하십시오.
   </p>
   <b>참고:</b> 10.0.0.1을 사용자의 개인용 게이트웨이 IP 주소로 대체하십시오.
   </td>
   </tr>
   <tr>
   <td>Ubuntu 및 Debian</td>
   <td>
   <i>/etc/network/interfaces</i> 파일의 끝에 다음 행을 추가하십시오.
   <blockquote>
   up route add -net 161.26.0.0/16 gw 10.0.0.1
   </blockquote>
   <b>참고:</b> 10.0.0.1을 사용자의 개인용 게이트웨이 IP 주소로 대체하십시오.
   </td>
   </tr>
   <tr>
   <td>Vyatta</td>
   <td><i>set protocols static route 161.26.0.0/16 next-hop 172.16.0.26</i>
   <p>
   <b>참고:</b> 172.16.0.26을 시스템이 속한 서브넷의 게이트웨이(이는 10.0.0./8 라우트에 대해 정의된 게이트웨이와 동일해야 함)로 대체하십시오.</p>
   </td>
   </tr>
   <tr>
   <td>ESXi</td>
   <td>다음 명령을 사용하여 ESXi 호스트에 대한 라우트를 추가하십시오.
   <blockquote>
   esxcfg-route -a 161.26.0.0/16 10.0.0.1
   </blockquote>
   <b>참고:</b> 10.0.0.1을 사용자의 개인용 게이트웨이 IP 주소로 대체하십시오.</td>
   </tr>
   <tr>
   <td>CoreOS</td>
   <td>/etc/systemd/network에 10-static.network로 이름 지정된, 다음과 같은 정적 라우트 파일을 작성하십시오.
   <blockquote>
   [Route]
   Gateway=10.0.0.1
   Destination=161.26.0.0/16
   </blockquote>
   <b>참고:</b> 10.0.0.1을 사용자의 개인용 게이트웨이 IP 주소로 대체하십시오.</td>
   </tr>
   </TBODY>
   </table>

   <a name="top"></a>

## 서버가 응답을 중지하는 경우 자동 다시 부팅을 실행하면서 지원 기술자에게 이를 알리는 모니터링 시스템을 구축할 수 있습니까?
{:faq}

**모니터링 중 실패 발생 시 자동 다시 부팅** 서비스를 주문하면 모니터링 경보가 발생하는 경우 서버를 자동으로 다시 부팅하고 지원 기술자에게 티켓을 발행하는 모니터링 시스템을 설정할 수 있습니다. 또한 추가 서비스로서, 모니터링 문제가 발생하는 경우 개별 알림을 수신할 수 있는 **NOC 모니터링** 또한 제공하고 있습니다. 이러한 오퍼링에 대해 자세히 알아보려면 [서버 모니터링 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://www.softlayer.com/services/monitoring/){:new_window}을 참조하십시오.

## cvsup 미러 개념
{:faq}

사용자를 위해 실행된 로컬 cvsup 미러에 대해 업데이트할 수 있습니다. supfile 파일에 다음 항목이 있어야 합니다.

```
*default host=cvsup.service.softlayer.com
```
{:pre }

distfile 파일로 미러링되며 freebsd.org에서 사용 가능합니다. 다음 행을 */etc/make.conf* 파일에 추가하여 로컬 저장소에서 먼저 다운로드를 시도할 수 있습니다.

```
MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"
```
{:screen }

파일이 해당 위치에 없는 경우에는 개별 포트 Makefile에 따라 수행하고 다음 미러로 이동합니다.
