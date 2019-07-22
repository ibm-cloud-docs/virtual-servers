---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-31"

keywords: apps, deploy, virtual server, App Service, vsi, virtual machine, delivery pipeline, virtual deployment

subcollection: virtual-servers

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:table: .aria-labeledby="caption"}

# 가상 서버에 배치
{: #deploying-to-a-virtual-server}

종량과금제 계정이 있는 경우 {{site.data.keyword.cloud}} [앱 서비스](https://{DomainName}/developer/appservice/starter-kits){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")를 사용하여 앱을 가상 서버 인스턴스를 포함한 여러 유형의 환경에 배치할 수 있습니다. 가상 서버 인스턴스는 베어메탈 머신을 에뮬레이트하고 온프레미스 워크로드를 클라우드로 배치하는 경우의 공통 배치 선택사항입니다.
{: shortdesc}

가상 서버 인스턴스는 다른 구성과 비교해서 모든 워크로드 유형에 적합한 향상된 투명성, 예측 가능성 및 자동화를 제공합니다. 가상 인스턴스를 베어메탈 서버와 결합하여 고유한 워크로드 결합을 작성합니다. 예를 들어, Debian Linux 기반 운영 체제를 실행하는 베어메탈 및 GPU 구성으로 고성능 데이터베이스 로직 또는 기계 학습을 작성할 수 있습니다. 

가상 서버 인스턴스 프로비저닝 및 배치는 복잡하고 시간이 걸리는 프로세스일 수 있으나 {{site.data.keyword.cloud_notm}} 앱 서비스를 사용하여 빠르게 시작하고 실행할 수 있습니다. 

서비스는 가상 서버 인스턴스에 바인드하지 않습니다. 가상 서버에서 서비스를 애플리케이션에 추가할 수 없습니다. 그러나 인증 정보가 가상 서버 인스턴스에서 실행되는 앱에 사용 가능하도록 설정한 경우 애플케이션에서 {{site.data.keyword.cloud_notm}} 서비스를 계속해서 사용할 수 있습니다.
{: important}

## 앱 배치
{: #create-deploy-vsi}

앱 서비스는 사용자를 위해 가상 서버 인스턴스를 프로비저닝하고, 앱이 포함된 이미지를 로드하고, Devops 도구 체인을 작성하고, 사용자를 위해 첫 번째 배치를 시작합니다. 

1. [앱을 작성](/docs/apps?topic=creating-apps-tutorial-scratch#tutorial-scratch)하십시오. 
2. 앱 세부사항 페이지에서 **지속적 딜리버리 구성**을 클릭하십시오.
3. 서버를 실행할 지역과 함께 **가상 서버에 배치**를 선택하십시오. 

## 배치 프로세스 작동 방법

가상 서버 배치 프로세스는 Terraform, 파이프라인 인에이블먼트, API 키 관리(Git 오퍼레이션) 및 도구 체인 프로세스의 이해가 포함된 여러 가지 키 기술로 구성되어 있습니다.  

### Terraform을 통한 배치

모든 앱 서비스 스타터 킷은 코드 프레임워크로서 오픈 소스 인프라인 [Terraform](https://ibm-cloud.github.io/tf-ibm-docs/v0.10.0/){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")을 통해 동적으로 작성된 가상 인스턴스에 배치될 수 있습니다.  

### 파이프라인 배치 사용

{{site.data.keyword.cloud_notm}} [앱 서비스](https://{DomainName}/developer/appservice/starter-kits){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")를 사용하는 스타터 킷을 작성하는 경우 가상 서버 인스턴스는 사용으로 설정됩니다. 앱이 작성되면 앱을 배치할 위치를 선택할 수 있습니다. 스타터 킷은 지속적 딜리버리 도구 체인을 사용하여 배치를 지원하도록 사용으로 설정됩니다. 스타터 킷은 Kubernetes, Cloud Foundry 및 가상 서버 인스턴스를 대상으로 지정할 수 있습니다. 도구 체인에는 소스 코드 저장소와 배치 파이프라인이 포함됩니다. 

가상 서버 옵션은 단계적으로 작동합니다. 먼저 앱 코드가 준비되어 GitLab Git 저장소에 저장되며 소스 코드는 파이프라인과 함께 도구 체인을 작성합니다. 파이프라인은 코드를 빌드하고 Debian Package 관리자 형식으로 패키징하도록 정의됩니다. 그런 다음 Terraform은 가상 인스턴스를 프로비저닝합니다. 마지막으로 앱이 실행 중인 가상 이미지 내부에 배치되고 설치된 후 시작되며 상태는 유효성 검증됩니다. 

파이프라인은 사용자 계정 특성 세트와 새 SSH 키 쌍을 사용하여 인프라에 배치합니다. 이 특성은 도구 체인으로 자동 전달되지만 보안상의 이유로 Git 소스 코드에 저장되지 않습니다. 

이 환경 특성을  보려면 다음 단계를 완료하십시오. 

1. 앱 세부사항 페이지에서 **도구 체인 보기**를 클릭하십시오.
2. **Delivery Pipeline** 타일을 클릭하십시오. 
3. **단계 구성** 아이콘을 클릭한 후 빌드 단계에서 **구성 단계**를 클릭하십시오. 
4. **환경 특성** 탭을 클릭하여 특성을 보십시오. 다음 표를 사용하여 사용 가능한 특성에 대해 알아보십시오. 

| 특성 |설명  |
|-----------|--------------|
| `TF_VAR_ibm_sl_api_key` |[인프라 API 키](/docs/apps?topic=creating-apps-vsi-deploy#iaas-key)는 클래식 인프라 콘솔에서 생성됩니다. |
| `TF_VAR_ibm_sl_username` | 클래식 인프라 계정을 식별하는 [인프라 사용자 이름](/docs/apps?topic=creating-apps-vsi-deploy#user-key)입니다. |
| `TF_VAR_ibm_cloud_api_key` | {{site.data.keyword.cloud_notm}} [API 키](/docs/apps?topic=creating-apps-vsi-deploy#platform-key)는 서비스 작성을 사용으로 설정하도록 사용됩니다. |
| `PUBLIC_KEY` | 가상 서버 인스턴스에 대한 액세스를 사용으로 설정하도록 정의된 [공개 키](/docs/apps?topic=creating-apps-vsi-deploy#public-key)입니다. |
| `PRIVATE_KEY` | 가상 서버 인스턴스에 대한 액세스를 사용으로 설정하도록 정의된 [개인 키](/docs/apps?topic=creating-apps-vsi-deploy#public-key)입니다. `\n` 줄 바꾸기 스타일 형식을 사용해야 합니다.|
| `VI_INSTANCE_NAME` | 가상 서버 인스턴스에 대해 자동으로 생성된 이름입니다. |
| `GIT_USER` | 적용 명령의 상태를 저장하도록 [Terraform 상태](/docs/apps?topic=creating-apps-vsi-deploy#tform-state)를 설정하는 경우 GitLab 사용자 이름이 필요합니다. |
| `GIT_PASSWORD` | 적용 명령의 상태를 저장하도록 [Terraform 상태](/docs/apps?topic=creating-apps-vsi-deploy#tform-state)를 설정하는 경우 GitLab 비밀번호가 필요합니다. |
{: caption="표 1. 인에이블먼트를 위해 변경하는 환경 변수" caption-side="top"}


#### 클래식 인프라 API 키
{: #iaas-key}

Terraform에는 인프라 리소스를 작성하기 위한 클래식 인프라 API 키가 필요합니다. API 키는 배치 중에 자동으로 가져옵니다. 키를 수동으로 검색하려면 다음 단계를 완료하십시오. 

1. [사용자 목록](https://{DomainName}/iam#/users){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")으로 이동하십시오. 또한 **관리** > **액세스(IAM)**를 클릭하고 **사용자**를 선택할 수 있습니다.
2. 사용자 이름을 클릭한 후 **사용자 세부사항**을 클릭하십시오.
3. API 키 섹션에서 **클래식 인프라 키 추가**를 클릭하십시오. 
4. API 키 `TF_VAR_ibm_sl_api_key`를 복사하거나 다운로드한 후 안전한 위치에 저장하십시오. **조치** ![조치 아이콘 목록](../icons/action-menu-icon.svg) 메뉴에서 **세부사항 보기** 옵션을 사용하여 API 키의 세부사항을 검색할 수 있습니다. 
5. 복사된 API 키 값을 도구 체인 구성에 붙여넣어 `TF_VAR_ibm_sl_api_key`를 대체하십시오.

자세한 정보는 [클래식 인프라 API 키 관리](/docs/iam?topic=iam-classic_keys#classic_keys) 및 [클래식 인프라 권한](/docs/iam?topic=iam-infrapermission#infrapermission)을 참조하십시오.

#### 클래식 인프라 사용자 이름
{: #user-key}

클래식 인프라 사용자 이름은 배치 중에 자동으로 가져와서 사용됩니다. 사용자 이름을 수동으로 가져오려면 다음 단계를 완료하십시오. 

1. [사용자 목록](https://{DomainName}/iam#/users){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")으로 이동하십시오. 또한 **관리** > **액세스(IAM)**를 클릭하고 **사용자**를 선택할 수 있습니다.
2. 사용자 이름을 클릭한 후 **사용자 세부사항**을 클릭하십시오.
3. **VPN 사용자 이름** 특성을 찾으십시오. 
4. 이 값을 잘라내어 붙여넣은 후 도구 체인 구성 `TF_VAR_ibm_sl_username`을 대체하십시오.

#### {{site.data.keyword.cloud_notm}} API 키
{: #platform-key}

Terraform에서 데이터베이스 및 구성 서비스와 같은 플랫폼 레벨 서비스를 작성하기 위해 파이프라인에서 환경 변수로 {{site.data.keyword.cloud_notm}} API 키를 자동으로 가져와서 저장합니다. {{site.data.keyword.cloud_notm}} API 키를 수동으로 검색하려면 다음 단계를 완료하십시오. 

1. [사용자 목록](https://{DomainName}/iam#/users){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")으로 이동하십시오. 또한 **관리** > **액세스(IAM)**를 클릭하고 **사용자**를 선택할 수 있습니다.
2. 사용자 이름을 클릭한 후 **사용자 세부사항**을 클릭하십시오.
3. API 키 섹션을 찾아 **IBM Cloud API 키 작성**을 클릭하십시오.
4. 이름 및 설명을 입력하고 **작성**을 클릭하십시오.
5. 창이 열리면 **표시**를 클릭하여 키를 검토하십시오.
6. 키를 클립보드에 복사하여 붙여넣거나 키를 다운로드하십시오.
7. 도구 체인 구성 `TF_VAR_ibm_cloud_api_key`의 값을 생성된 값으로 대체하십시오 

#### 공개 및 개인 키
{: #public-key}

Debian 패키징을 가상 서버 인스턴스에 설치하는 도구 체인의 경우, 배치 인프라가 자동으로 개인 및 공개 SSH 키 쌍을 생성하여 Git 컨텐츠를 인스턴스로 전송합니다. 

이를 수동으로 수행하려면 다음을 따르십시오.
1. 클라이언트에서 다음 지시사항을 사용하여 [공개 및 개인 키 쌍](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")을 작성하십시오.
2. [인프라 SSH 키 보기](https://{DomainName}/iam/#/users){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")로 이동하십시오. 또한 **메뉴** > **클래식 인프라** > **디바이스** > **관리** > **SSH 키**를 클릭할 수 있습니다. 
3. **추가**를 클릭하십시오.
4. 이전에 작성한 공개 키의 컨텐츠를 복사하여 키 컨텐츠에 붙여넣으십시오. 
5. 키 이름을 제공한 후 **추가**를 클릭하십시오.

개인 키는 단일 행에 있어야 합니다. 새 행을 `\n`으로 대체하십시오. 다음 예를 참조하십시오.
{: tip}

```
---------BEGIN RSA KEY----------\nasdfasdfeqwtqf13rf1eqwfwe\netq3efaewf23fa23f23f\n.....\n----------END RSA KEY-------------
```
{: screen}

#### Terraform 상태 사용
{: #tform-state}

Terraform은 Terraform `apply` 명령 상태의 저장을 지원합니다. 이 상태 파일에서는 `apply` 명령을 다시 한 번 실행하여 Terraform 구성 파일이 변경되었는지 여부를 판별합니다. 상태는 앱 및 구성이 자동으로 설정된 Git 저장소에 저장됩니다. 

상태 스토리지를 사용으로 설정하려면 `GIT_USER` 및 `GIT_PASSWORD`가 도구 체인 환경 변수에서 특성으로 자동 구성됩니다. 이 값에 액세스해야 하는 경우 다음 단계를 수행하십시오.

1. 도구 체인 보기의 코드 도구에서 Git 저장소에 액세스하십시오. 
2. GIT Lab에서 **프로파일 아이콘**을 클릭한 후 **설정**을 클릭하십시오.
3. **계정**을 클릭하여 사용자 이름을 복사하고 `GIT_USER` 값을 대체하십시오. 
4. **액세스 토큰**을 클릭하십시오.
5. 토큰의 이름을 지정하고 범위를 선택한 후 **개인 액세스 토큰 작성**을 클릭하십시오.
6. `Your New Personal Access Token` 필드에서 **복사**를 클릭하고 도구 체인 특성에서 `GIT_PASSWORD`의 값을 대체하십시오. 

Terraform 상태는 `terraform`이라고 하는 분기에 저장되며 Terraform 상태가 변경된 경우 실행할 파이프라인을 트리거하지 않습니다. 

### Git 오퍼레이션 사용
{: #git-repo-vsi}

앱이 {{site.data.keyword.cloud_notm}}에 배치되면 소스 코드 관리를 위해 호스팅하도록 GitLab 저장소가 작성됩니다. Git 오퍼레이션을 사용하여 팀이 작업을 수행하고 앱에 변경사항을 전달할 수 있습니다. 이 저장소에 포함된 폴더와 해당 컨텐츠에 대한 설명입니다.

#### Debian 폴더
{: #debian-folder}

`debian` 폴더에는 [Debian 패키지](https://www.debian.org/doc/manuals/debian-faq/ch-pkgtools.en.html){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에 대한 앱의 패키징을 사용으로 설정하는 데 필요한 구성이 있습니다.

#### Terraform 폴더
{: #terraform-folder}

`terraform` 폴더에는 인프라 리소스를 프로비저닝하는 데 사용할 수 있는 코드로서 인프라에 대한 구성이 있습니다. 파일 `main.tf`는 Terraform 구성에 대한 옵션을 변경하기 위한 기본 소스입니다. 

```json
resource "ibm_compute_vm_instance" "vm1" {
    hostname = "${var.vi_instance_name}"
    domain = "example.com"
    os_reference_code = "DEBIAN_8_64"
    datacenter = "${var.datacenter}"
    network_speed = 100
    hourly_billing = true
    private_network_only = false
    cores = 1
    memory = 1024
    disks = [25]
    local_disk = false
    ssh_key_ids = [
        "${ibm_compute_ssh_key.ssh_key_gip.id}"
    ]
}
```

Terraform을 사용하여 베어메탈 서버도 프로비저닝할 수 있습니다. 자세한 정보는 [IBM Terraform 제공자 문서](https://ibm-cloud.github.io/tf-ibm-docs/v0.10.0/){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘") 및 [IBM Terraform 제공자 GIT 저장소](https://github.com/IBM-Cloud/terraform-provider-ibm){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")를 참조하십시오.

`variables.tf`는 가상 인스턴스를 작성하도록 대상으로 지정할 데이터 센터를 변경하는 데 사용될 수 있습니다. 플랫폼에서 정의된 데이터 센터 목록을 보려면 [데이터 센터](https://www.ibm.com/cloud/data-centers/){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")를 참조하십시오.

기본적으로 Terraform 파일은 Washington 및 `wdc04`로 구성됩니다. 
```json
variable "datacenter" {
  description = "Washington"
  default = "wdc04"
}
```

### 도구 체인 단계 이해
{: #toolchain-stages-vsi}

도구 체인은 하나의 단순 파이프라인에서 인프라 및 앱 배치를 표시합니다. 코드 파트로서 인프라를 하나의 파이프라인으로 분할하고 앱 배치를 다른 파이프라인으로 분할하십시오. 

도구 체인 프로세스에는 다섯 개의 단계가 있습니다. 

1. 빌드 단계에서는 Git 저장소를 복제하고 코드를 Debian 패키지로 패키징합니다. 
2. Terraform 플랜 단계에서는 Terraform 플랜을 준비합니다. 
  ```console
  terraform init -input=false
  terraform validate
  terraform plan -var "ssh_public_key=$PUBLIC_KEY" -input=false -out tfplan
  ```

3. Terraform 적용 단계에서는 Terraform 구성을 적용하고 가상 서버의 IP 주소가 사용 가능할 때까지 기다립니다. 

  ```console
  terraform apply -auto-approve -input=false tfplan
  terraform output "host ip" > hostip.txt
  ```

4. 배치, 설치, 시작 단계에서는 첫 번째 단계에서 빌드된 Debian 패키지를 실행 중인 가상 서버로 이동하고, 설치한 후 시작합니다. 
5. 상태 검사 단계에서는 앱에서 사용 가능한 상태 엔드포인트를 유효성 검증하고 파이프라인을 완료합니다. 

앱이 시작된 후 앱에 액세스하려면 상태 검사 단계의 로그를 확인하십시오. 앱의 IP 주소와 포트를 표시하는 로그에 나열되어 있는 URL 링크를 클릭하십시오. 
