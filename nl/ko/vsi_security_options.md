---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 방화벽
{: #virtual-server-security-options}

{{site.data.keyword.BluVirtServers}}에는 필수적인 보안 계층을 제공하는 몇 가지 방화벽 옵션이 있습니다.  방화벽 옵션은 요청 시 서비스 중단 없이 프로비저닝됩니다. 방화벽 서비스는 원치 않는 트래픽이 서버에 도달하는 것을 방지하여 공격의 가능성을 줄이고 서버 리소스가 원래 의도에 충실하게 작업할 수 있게 해 줍니다.
{:shortdesc}

방화벽은 인프라 공용 네트워크의 모든 서버에서 추가 기능으로 사용 가능합니다.

주문 프로세스의 일부로서, 사용자는 보호 기능을 제공하기 위해 디바이스 고유 하드웨어 또는 소프트웨어 방화벽을 선택할 수 있습니다. 또는, 환경에 전용 방화벽 어플라이언스를 배치하고 보호된 VLAN에 가상 서버를 배치할 수 있습니다.  

가상 서버는 동일 인터페이스의 두 방화벽 어플라이언스로 보호될 수 없습니다.
{:note}

자세한 정보는 다음 보안 주제 콜렉션을 참조하십시오.

* [Hardware Firewall (공유)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Hardware Firewalls (Dedicated)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)
