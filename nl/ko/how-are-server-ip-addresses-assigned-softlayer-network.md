---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 서버 IP 주소 지정
{: #assigning-server-ip-addresses}

{{site.data.keyword.cloud}}에서는 사설 네트워크의 IPv4 주소를 사용하여 가상 서버 인스턴스를 구성합니다. 요청된 경우에는 공용(인터넷 연결) IPv4 주소를 사용합니다. 또한 공용 네트워크에서 IPv6 주소를 요청할 수 있습니다. 이러한 모든 IP 주소는 통칭해서 _기본 IP 주소_라고 합니다.
{:shortdesc}

{{site.data.keyword.cloud_notm}} 콘솔을 통해 보조 서브넷을 구매하고 나면 추가 IP 주소를 가상 서버 인스턴스로 바인드할 수 있습니다. 이러한 방법으로 구매하고 사용자가 관리하는 IP 주소는 _보조 IP 주소_라고 합니다.

IP 주소 획득에 사용 가능한 옵션에 대한 자세한 정보는 [서브넷 및 IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips)를 참조하십시오.

## 보조 IP 주소 바인딩

보조 서브넷을 구매하여 라우팅한 후 새로 사용 가능한 IP 주소 중 하나 이상을 사용하도록 운영 체제를 구성해야 합니다. 새 IP 주소의 구성 단계는 각 운영 체제마다 다르지만, 일반적으로 이 설정을 "인터페이스 별명" 설정이라고 합니다. 추가 구성 세부사항에 대해서는 운영 체제 문서를 참조하십시오.
