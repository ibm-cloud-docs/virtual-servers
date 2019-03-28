---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 이미지 템플리트
{: #image-templates}

{{site.data.keyword.BluVirtServers}} 이미지 템플리트를 사용하면 특정 디바이스의 이미지를 캡처하여 주문 프로세스에서 해당 구성을 변경을 최소화하여 빠르게 복제할 수 있습니다.
{:shortdesc}

이미지 템플리트는 운영 체제에 상관없이 모든 {{site.data.keyword.BluVirtServers_short}}에 대한 이미징 옵션을 제공합니다. 이미지 템플리트를 통해 기존 가상 서버의 이미지를 캡처하고 캡처된 이미지를 기반으로 새 이미지를 작성할 수 있습니다. 이미지 템플리트는 베어메탈 서버와 호환되지 않습니다.

## 이미지 템플리트의 작동 방식
이미지 템플리트의 두 가지 주요 조치는 작성과 배치입니다. 이미지 작성 요청을 하면 {{site.data.keyword.BluSoftlayer_full}}의 자동화된 시스템이 서버를 오프라인으로 전환합니다. 서버가 오프라인이 된 상태에서 사용자 데이터의 압축된 백업이 작성되고, 구성 정보가 기록되며 이미지 템플리트가 {{site.data.keyword.BluSoftlayer_notm}} SAN에 저장됩니다. 이미지 템플리트의 배치 단계 동안 자동화된 시스템은 선택된 이미지에서 수집된 데이터를 기반으로 새 서버를 구축합니다. 그런 다음, 배치 프로세스가 볼륨에 대한 조정을 수행하고, 복사된 데이터를 복원한 후 새 호스트를 위한 최종 구성 변경(예: 네트워크 구성)을 수행합니다.

이미지 템플리트에 대한 자세한 정보는 [이미지 템플리트 시작하기](/docs/infrastructure/image-templates?topic=image-templates-getting-started-with-image-templates)를 참조하십시오.
