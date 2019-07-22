---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# 프로비저닝 스크립트
{: #provisioning-scripts}

프로비저닝 스크립트는 프로비저닝 프로세스 중에 디바이스에 다운로드하거나 다운로드하여 실행할 수 있습니다. 기존 계정의 경우 프로비저닝 스크립트는 {{site.data.keyword.cloud_notm}} 콘솔 내에서 관리됩니다. 주문 프로세스 중에는 새 계정의 스크립트 또는 아직 추적되지 않은 스크립트를 수동으로 입력할 수 있습니다.

또는 cloud-init 사용 이미지를 사용하고 사용자 데이터를 제공하여 자동으로 구성 태스크를 수행하거나 스크립트를 실행할 수 있습니다. 자세한 정보는 [cloud-init 사용 이미지로 프로비저닝](/docs/infrastructure/image-templates?topic=image-templates-provisioning-with-a-cloud-init-enabled-image)을 참조하십시오.
{: tip}

프로비저닝 프로세스 중에, HTTP URL과 연관된 스크립트가 디바이스에 다운로드됩니다. 프로비저닝 후에는 관리자가 디바이스에서 스크립트를 수동으로 실행해야 합니다. HTTPS URL과 연관된 스크립트는 자동으로 다운로드되고 실행됩니다. 프로비저닝 스크립트는 현재 표준 Linux 운영 체제(Cent, RHEL, Fedora, Debian 또는 Ubuntu), Windows 및 FreeBSD에서 사용 가능합니다. Vyatta, Netscaler, XenServer, VMware와 같은 기타 시스템은 지원되지 않습니다. 프로비저닝 스크립트는 결합된 바이너리 파일 또는 임의의 OS 지원 언어를 포함, 운영 체제에서 실행되는 임의의 유형의 파일일 수 있습니다.

자세한 정보는 [프로비저닝 스크립트 관리](/docs/vsi?topic=virtual-servers-managing-a-provisioning-script#managing-a-provisioning-script)를 참조하십시오.
