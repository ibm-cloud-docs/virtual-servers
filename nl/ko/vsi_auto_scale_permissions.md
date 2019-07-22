---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-14"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 자동 스케일링에 대한 사용자 권한 설정
{: #user-permissions-required-to-use-auto-scale}

자동 스케일링 옵션에 액세스하려면 {{site.data.keyword.virtualmachinesshort}}를 주문하고 관리하는 기능 이상의 특수 사용자 권한이 필요합니다. 자동 스케일링 기능에 액세스하려면 추가된 향후 가상 디바이스 외에도 계정에 있는 모든 가상 서버를 관리할 수 있는 권한이 있어야 합니다. 

계정 관리자가 사용자에게 자동 스케일링 옵션을 볼 수 있는 권한을 부여하려면 다음 단계를 완료하십시오. 

1. {{site.data.keyword.cloud}} 콘솔의 [액세스(IAM) ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/iam#/users){: new_window} 페이지에 로그인하십시오.  
2. **사용자** 탭에서 **보기 기준: 내 클래식 인프라 사용자**를 선택하십시오.
3. 사용자를 선택한 후 **클래식 인프라** 탭을 클릭하십시오. 
4. **권한 탭**에서 **디바이스** 카테고리를 펼치고 **자동 스케일링 그룹 관리**를 선택하십시오.
5. **적용**을 클릭하십시오.

## 다음 단계

자동 스케일링 옵션에 대한 액세스 및 사용 권한을 갖게 되면 이제 이 기능을 사용할 준비가 된 것입니다. 시작하려면 다음 정보를 검토하십시오.

1. [스케줄 기반 자동 스케일링으로 트래픽 급증 관리](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling)
2. [리소스 기반 자동 스케일링으로 트래픽 급증 관리](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling)
3. [FAQ: 자동 스케일링](/docs/vsi?topic=virtual-servers-faqs-auto-scale)

