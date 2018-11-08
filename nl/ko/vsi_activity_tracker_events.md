---

copyright:
  years: 2016, 2018

lastupdated: "2018-09-12"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Activity Tracker 이벤트 
{: #at_events}

보안 담당자, 감사자 또는 관리자는 {{site.data.keyword.cloudaccesstrailfull}} 서비스를 사용하여 사용자와 애플리케이션이
{{site.data.keyword.Bluemix}}의 VSI(Virtual Server Instance)와 상호 작용하는 방법을 추적할 수 있습니다. 계정에 연결되어 있는
계정 소유자 및 사용자는 가상 서버 이벤트를 트리거할 수 있으며 이러한 이벤트는 {{site.data.keyword.cloudaccesstrailshort}}에 로깅됩니다.
{:shortdesc}

{{site.data.keyword.cloudaccesstrailshort}} 서비스는 {{site.data.keyword.Bluemix_notm}}에서 서비스의 상태를 변경하는
사용자 개시 활동을 기록합니다. 자세한 정보는
[{{site.data.keyword.cloudaccesstrailshort}} 정보](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov )를 참조하십시오.

사용자 조치 모니터링을 시작하려면,
[{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla)의 내용을 참조하십시오. 

개시자는 사용자, 서비스 또는 애플리케이션일 수 있습니다. 사용자가 이벤트를 생성하는 경우, 해당 사용자에게는 {{site.data.keyword.Bluemix}} 콘솔의 **인프라** 리소스에 대한 액세스 권한이 있어야 합니다. 
{: tip}

## 로그인 이벤트
{: #login}

다음 표에는 로그인 이벤트를 생성하는 조치가 나열되어 있습니다.

| 조치 |설명 |
|----------|---------|
| `audit-log.user.login`  | 개시자가 {{site.data.keyword.Bluemix}} UI 또는 {{site.data.keyword.slportal}}을 통해 {{site.data.keyword.Bluemix}}에 로그인할 때 이벤트가 생성됩니다. | 
{: caption="표 1. 로그인 조치" caption-side="top"} 


## 가상 서버 인스턴스 이벤트
{: #vsi}

{{site.data.keyword.cloudaccesstrailshort}} 서비스를 사용함으로써 VSI(Virtual Server Instance)를 해당 라이프사이클을 통해 편집할 수 있습니다.

다음 표에는 이벤트를 생성하는 조치가 나열되어 있습니다.

| 조치 |설명 |
|----------|---------|
| `audit-log.vsi.provision`             | 개시자가 VSI를 프로비저닝할 때 이벤트가 생성됩니다.  | 
| `audit-log.vsi-port.disable`          | 개시자가 VSI의 포트를 사용 안함으로 설정할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi-port.enable`           | 개시자가 VSI의 포트를 사용으로 설정할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi-port-speed.update`     | 개시자가 VSI의 포트 속도를 업데이트할 때 이벤트가 생성됩니다. |
| `audit-log.vsi-image-template.create` | 개시자가 VSI에 대한 이미지 템플리트를 작성할 때 이벤트가 생성됩니다.  |
| `audit-log.vsi.power-off`             | 개시자가 VSI의 전원을 끌 때 이벤트가 생성됩니다.  |
| `audit-log.vsi.soft-power-off`        | 개시자가 VSI에서 소프트 전원 끄기를 수행할 때 이벤트가 생성됩니다. |
| `audit-log.vsi.force-power-off`       | 개시자가 VSI에서 전원 끄기를 강제 실행할 때 이벤트가 생성됩니다. |
| `audit-log.vsi.reboot`                | 개시자가 VSI를 다시 부팅할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi.soft-reboot`           | 개시자가 VSI에서 소프트 다시 부팅을 수행할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi.hard-reboot`           | 개시자가 VSI에서 하드 다시 부팅을 수행할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi.power-on`              | 개시자가 VSI에서 전원을 켤 때 이벤트가 생성됩니다. | 
| `audit-log.vsi.rename`                | 개시자가 VSI의 이름을 바꿀 때 이벤트가 생성됩니다. | 
| `audit-log.vsi.rescue`                | 개시자가 VSI를 복구할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi-security-group.add`    | 개시자가 VSI에 보안 그룹을 추가할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi-security-group.remove` | 개시자가 VSI에서 보안 그룹을 제거할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi.reload`                | 개시자가 VSI에 대해 운영 체제(OS) 다시 로드를 수행할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi.boot`                  | 개시자가 이미지에서 VSI를 부팅할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi.reclaim`               | 개시자가 VSI를 취소할 때 이벤트가 생성됩니다. | 
| `audit-log.vsi.pause`                 | 개시자가 VSI를 일시정지할 때 이벤트가 생성됩니다. | 
{: caption="표 2. VSI 조치" caption-side="top"} 



## 이벤트 보기
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} 이벤트는 이벤트가 생성되는 {{site.data.keyword.Bluemix_notm}} 지역에서 사용 가능한
{{site.data.keyword.cloudaccesstrailshort}} **계정 도메인**에서 사용 가능합니다. 자세한 정보는 [계정 이벤트
보기](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events)를 참조하십시오.

{{site.data.keyword.cloudaccesstrailshort}} 이벤트는 조치가 발생하는 동일한 지역의 {{site.data.keyword.cloudaccesstrailshort}} 서비스에
자동으로 전달됩니다.
