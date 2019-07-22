---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-09"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# FAQ: 가상 서버  
{: #faqs-virtual-servers}

## 사용 가능한 가상 서버 유형에는 어떤 것이 있습니까?
{: faq}
{{site.data.keyword.BluSoftlayer_full}}에서는 클래식 인프라 내에 있는 여러 유형의 가상 서버를 제공합니다. 표준 오퍼링은 공용 기반 가상 서버로, 이는 다양한 요구사항에 적합한 멀티 테넌트 환경입니다. 싱글 테넌트 환경을 찾고 있는 경우에는 전용 Virtual Server 오퍼링을 고려하십시오. 전용 가상 서버 옵션은 리소스 요구사항이 더 엄격한 애플리케이션에 적합합니다. 현재 가상 서버 오퍼링에 대한 자세한 정보는 [가상 서버 시작하기](/docs/vsi?topic=virtual-servers-getting-started-with-virtual-servers#getting-started-with-virtual-servers)를 참조하십시오.

IBM Cloud는 차세대 클라우드 플랫폼인 VPC(Virtual Private Cloud) 인프라를 제공합니다. VPC를 사용하여 퍼블릭 클라우드 내에 격리된 환경을 실행하도록 {{site.data.keyword.cloud_notm}}에서 자체 공간을 작성합니다. VPC는 퍼블릭 클라우드의 보안에 민첩성과 용이성을 제공합니다. 자세한 정보는 [가상 프라이빗 클라우드 정보](https://cloud.ibm.com/docs/vpc-on-classic?topic=vpc-on-classic-about)를 참조하십시오.

## 공용 인스턴스 유형에 대한 가격 정보는 어디에서 찾을 수 있습니까?
{: faq}

가격 정보는 [가상 서버 빌드 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/cloud/virtual-servers){: new_window}를 참조하십시오.

## 가상 공용 인스턴스에 대한 가격 정보는 어디에서 찾을 수 있습니까?
{: faq}

워크로드 지원을 위한 {{site.data.keyword.cloud_notm}} 서버 비용 예상은 [{{site.data.keyword.cloud_notm}} 카탈로그](https://cloud.ibm.com/catalog)에서 시작됩니다. 카탈로그에서 **계산**을 선택하고 베어메탈 서버, 가상 서버 또는 VPC(Virtual Private Cloud)의 가상 서버 중에서 서버 유형을 선택하십시오. 가격 정보는 [가상 서버 프로비저닝 계산기 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}를 참조하십시오.

## 내 시간별 또는 월별 가상 서버에 디스크 스토리지를 추가할 수 있습니까?
{: faq}

업데이트할 디바이스의 *구성* 화면에서 *첫 번째 디스크*부터 *다섯 번째 디스크* 필드까지 스토리지 옵션을 업데이트하여 가상 서버의 디스크 스토리지를 업그레이드하거나 다운그레이드할 수 있습니다. 자세한 정보는 [기존 가상 서버 다시 구성](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers)을 참조하십시오.

## 시작할 수 있는 시간별 가상 서버의 최대 수는 몇 개입니까?
{: #concurrent}
{: faq}

실행할 수 있는 인스턴스 수는 계정의 성숙도에 따라 달라집니다. 기본적으로 45일이 지난 계정은 언제든지 공용 가상 서버, 전용 가상 서버 및 베어메탈 서버에서 최대 20개의 인스턴스를 보유할 수 있습니다. 새 계정일수록 한계 값이 작아집니다. 한계를 증가시키려는 경우에는 지원에 문의하여 지금 수행하고 있는 작업과 필요한 동시 인스턴스 수를 알려주십시오.

## 내 시간별 virtual Server의 대역폭은 어떻게 비용 청구됩니까?
{: faq}

시간별 가상 서버 비용 청구는 인바운드 트래픽과 아웃바운드 트래픽으로 구분됩니다. 가상 서버에 대한 모든 인바운드 트래픽은 무료입니다. 아웃바운드 트래픽은 측정되어 GB 단위로 비용 청구되며, 총계는 비용 청구 기간의 끝에 계산됩니다.

## 어떤 경우에 내 가상 서버가 다른 호스트로 마이그레이션됩니까?
{: faq}

제한된 경우에 가상 서버가 다른 호스트로 마이그레이션되어야 합니다. 마이그레이션이 필수인 경우, 가상 서버가 시스템 종료되고 마이그레이션된 다음 다시 시작됩니다. 다음 경우에 가상 서버가 마이그레이션될 수 있습니다.

* 하이퍼바이저가 업데이트되어야 하며 호스트가 사용 중지되거나 호스트가 새 인스턴스를 채택하도록 허용되지 않습니다. 호스트에 이러한 변경사항 중 하나가 있는 것으로 표시되는 경우 가상 서버 중 하나가 {{site.data.keyword.cloud_notm}} 콘솔에서 다시 부팅되며 이렇게 다시 부팅되는 것으로 인해 자동으로 가상 서버가 다른 호스트로 마이그레이션되도록 트리거됩니다.
* 인프라 유지보수. 가상 서버를 호스팅하는 시스템에 유지보수가 필요함을 표시하는 이메일을 수신합니다. 가상 서버가 인프라 유지보수의 일부로 마이그레이션되어야 할 필요가 있을 수 있습니다.
* 기존 인스턴스에 대한 업그레이드. 일관된 성능을 유지하기 위해 인스턴스를 업그레이드하는 경우, 적절한 전용 CPU 및 메모리를 수신할 수 있도록 다른 호스트에 마이그레이션될 수 있습니다.
* 전용 호스트가 실패합니다. 전용 인스턴스는 보유하고 있는 기존 용량을 사용하지 않고 비어 있는 다른 호스트로 마이그레이션됩니다. 

유지보수 창에서 {{site.data.keyword.cloud_notm}} 콘솔 내의 디바이스의 **조치** 메뉴에 **호스트 마이그레이션** 옵션이 표시되는 것을 볼 수 있습니다. **호스트 마이그레이션**을 사용하면 지정된 유지보수 기간 동안 편리한 시간에 새 호스트로 가상 서버를 마이그레이션할 수 있습니다. 유지보수 기간 동안 마이그레이션을 시작하지 않은 경우, 필수 유지보수를 완료하기 위해 가상 서버가 자동으로 마이그레이션됩니다. **호스트 마이그레이션** 옵션은 지속되지 않으며 유지보수 알림을 통해 통신되는 유지보수 기간 동안만 사용 가능합니다.

가상 서버 중 하나에 현재 호스트에서 사용할 수 없는 특정 레벨의 하이퍼바이저가 있어야 하는 경우에도 **호스트 마이그레이션** 옵션을 볼 수 있습니다.

## 휴대용 스토리지 삭제 시에 데이터는 어떻게 됩니까?
{: faq}

스토리지가 삭제되면 해당 볼륨에서 데이터에 대한 모든 포인터가 제거되기 때문에 데이터는 액세스 불가능합니다. 물리적 스토리지가 다른 계정으로 다시 프로비저닝되는 경우, 새 포인터 세트가 지정됩니다. 새 계정이 물리적 스토리지에 있었을 수도 있는 임의 데이터에 액세스할 수 있는 방법은 없습니다. 새 포인터 세트는 모두 0으로 표시합니다. 새 데이터가 볼륨/LUN에 작성되면 여전히 존재하던 모든 액세스 불가능하던 데이터는 겹쳐쓰기됩니다.

## Red Hat Cloud Access 구독을 사용하여 가상 서버를 작성할 수 있습니까?
{: faq}

예. 이미지를 가져올 때 운영 체제 라이센스를 제공하도록 지정할 수 있습니다. 자세한 정보는 [Red Hat Cloud Access 사용](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription#using-your-own-os-license-or-subscription)을 참조하십시오. 그런 다음 해당 이미지 템플리트로부터 가상 서버를 주문하고 기존 [Red Hat Cloud Access ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} 구독을 사용할 수 있습니다.

## 가상 서버와 가상 사설 서버(VPS) 간의 차이점은 무엇입니까?
{: faq}

가상 서버는 널리 사용되고 있는 가상 사설 서버(VPS) 또는 가상 전용 서버(VDS) 플랫폼과 유사합니다. 이러한 "가상 서버" 환경은 특정 환경을 비공개로 안전하게 하나의 하드웨어 노드에 프로비저닝할 수 있게 해 주지만, VDS 및 VPS의 기능은 좀 더 제한되어 있습니다. VPS 및 VDS 옵션은 일반적으로 단일 서버 아키텍처로 한정됩니다. VDS 또는 VPS의 각 가상 서버에 추가하거나 이들 간에 분배할 수 있는 리소스는 단일 서버에 실제 설치된 리소스뿐입니다. 

가상 서버는 개별 인스턴스가 사용 가능한 모든 하드웨어 리소스를 포함하는 멀티 서버 클라우드 아키텍처에서 프로비저닝됩니다. 가상 서버는 공유 고용량 SAN 기반 기본 스토리지 플랫폼 또는 고성능 로컬 디스크 스토리지를 사용할 수 있습니다. 각 인스턴스는 더 큰 클라우드 환경의 일부이므로, 모든 가상 서버 간의 통신은 즉시 이뤄집니다.

## 가상 서버를 프로비저닝할 때 용량 오류가 수신되는 이유는 무엇입니까?
{: faq}

가상 서버를 프로비저닝할 때 요청을 완료하기에 용량이 충분하지 않다는 오류 메시지를 받을 수 있습니다. 프로비저닝이 실패하는 경우, 해당하는 특정 요청 내의 모든 가상 서버 인스턴스가 실패합니다. 용량 오류는 라우터 또는 데이터 센터에 서비스 요청을 처리하는 데 필요한 리소스가 충분하지 않은 경우에 발생합니다. 몇 가지 이유로 인해 이런 오류가 수신될 수 있습니다. 리소스 가용성은 자주 변경되기 때문에 잠시 대기한 후에 다시 시도해 볼 수도 있습니다. 이 오류를 방지하는 전략에 대한 자세한 정보는 [가상 서버 인스턴스에 대한 리소스 고려사항](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations)을 참조하십시오.

## 내 서버에 어떻게 로그인할 수 있습니까?
{: faq}

콘솔에 로그인하고 **디바이스** 메뉴로 이동하십시오. 자세한 정보는 [디바이스로 이동](/docs/vsi?topic=virtual-servers-navigating-devices)을 참조하십시오.**디바이스 목록**에서 인스턴스를 선택하십시오. 로그인하는 데 사용할 디바이스 사용자 이름 및 비밀번호를 보고 관리할 수 있습니다. 자세한 정보는 [디바이스 사용자 이름과 비밀번호 보기 및 관리](https://test.cloud.ibm.com/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device)를 참조하십시오. 

## IBM Cloud 사설 네트워크에 액세스하려면 어떻게 VPN을 사용할 수 있습니까?
{: faq}

[웹 인터페이스](https://www.softlayer.com/VPN-Access){: external}를 통해 VPN에 로그인하거나 Linux, macOS 또는 Windows용 [독립형 VPN 클라이언트](/docs/infrastructure/iaas-vpn?topic=VPN-standalone-vpn-clients)를 사용할 수 있습니다.VPN에 연결된 후 수행할 작업에 대한 자세한 정보는 [SSL VPN 사용](/docs/infrastructure/iaas-vpn?topic=VPN-use-ssl-vpn)을 참조하십시오.

## 내 가상 서버를 어떻게 다시 부팅할 수 있습니까?
{: faq}

디바이스 다시 부팅은 **디바이스 목록** 또는 개별 인스턴스의 스냅샷 보기에서 발생할 수 있습니다. 콘솔의 **디바이스 목록**에서 가상 서버 인스턴스로 이동하십시오. 자세한 정보는 [디바이스로 이동](/docs/vsi?topic=virtual-servers-navigating-devices)을 참조하십시오. 관리할 디바이스에 대해 **조치**를 선택하고 **다시 부팅**을 선택하십시오. 

## 복구 커널을 어떻게 사용할 수 있습니까?
{: faq}

서버에 문제가 발생하는 경우 복구 커널로 부팅하면 도움이 됩니다. 복구 커널을 실행하려면 콘솔의 **디바이스 목록**에서 디바이스 이름을 선택하십시오. Windows 인스턴스의 경우 **조치** 메뉴에서 **복구 모드**를 선택하거나 **이미지에서 부팅**을 선택하십시오. 자세한 정보는 [복구 커널 실행](/docs/vsi?topic=virtual-servers-launching-rescue)을 참조하십시오.

## 네트워크 상태를 어디서 찾을 수 있습니까?
{: faq}

[{{site.data.keyword.cloud_notm}} - 상태](https://cloud.ibm.com/status){: external}에서 직접 **상태** 페이지에 액세스하여 모든 {{site.data.keyword.cloud_notm}} 위치에서 리소스의 현재 상태를 볼 수 있습니다. 특정 컴포넌트 및 위치를 선택하여 목록을 필터링할 수 있습니다(예를 들어, 가상 서버를 선택하고 네트워크 연결을 볼 수 있음). 

## 규제 준수 보고서를 어떻게 요청할 수 있습니까?
{: faq}

SOC 보고서를 포함하여 규제 준수 정보 보기 또는 요청에 대한 자세한 정보는 [내 데이터의 안전성을 어떻게 알 수 있습니까?](/docs/overview?topic=overview-security)를 참조하십시오. 

