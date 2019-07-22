---

copyright:
  years: 2014, 2019
lastupdated: "2019-02-06"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Apache Brooklyn을 사용한 자동 스케일링
{: #auto-scale-with-apache-brooklyn}

## 소개

10억명 이상의 모바일 사용자에게 매일 중요 이용자 데이터를 제공하는 한 회사는 IBM에게 사설 네트워크에 있는 서버의 자동 스케일링 그룹을 작성하는 기능을 제공해 줄 것을 요청했습니다. 주요 요구사항은 탄력성이었습니다. 즉, 워크로드 요구사항 및 사용자 경험 응답 시간을 기반으로 하여 시스템은 사전에 결정된 정책에 따라 자동으로 확장되고 축소됩니다. 

자동 스케일링은 CPU 사용량을 기반으로 합니다. 그룹에서 서버의 평균 CPU 사용량이 가장 높은 임계값 또는 트리거 이벤트를 초과하는 경우 추가 리소스가 프로비저닝되거나 확장되어야 합니다. 그룹에서 서버의 평균 CPU 사용량이 가장 낮은 임계값 또는 트리거 이벤트보다 적은 경우 리소스가 축소되어야 합니다. 고객의 요구사항은 다음과 같습니다. 

1. 다음 매개변수를 지정하는 기능:
  * 그룹에 있는 초기 서버 수
  * 그룹에 있는 최대 및 최소 서버 수
  * 높고 낮은 CPU 임계값
  * 트리거 이벤트에서 확장하고 추가할 추가 서버 수
2. 도메인 이름 시스템(DNS) 통합
  * 그룹에 있는 서버가 프로비저닝되거나 확장되며 사용 가능하게 되면 적절한 DNS 레코드가 작성되어야 합니다. 
  * 서버가 축소되면 서버에 대한 DNS 레코드가 제거됩니다. 
3. 로드 밸런서 통합
  * 그룹에 있는 서버가 프로비저닝되거나 확장되며 사용 가능하게 되면 서버 레코드가 적절한 DNS NetScaler 로드 밸런서에 추가되고 적절한 로드 밸런싱 그룹으로 바인드됩니다. 
  * 서버가 축소되면 로드 밸런싱 그룹에서 바인드 해제되어야 하고 서버 레코드가 NetScaler에서 제거됩니다. 
4. Chef 통합
  * 그룹에 있는 서버가 프로비저닝되거나 확장되며 사용 가능하게 되면 Chef 서버에서 Chef 클라이언트가 실행되어 노드를 등록합니다. 
  * 서버가 축소되면 서버의 노드와 클라이언트 레코드가 Chef 서버에서 제거됩니다. 
5. 서버 프로비저닝 요구사항
  * 그룹에 있는 모든 서버가 사설 전용 업링크, 1,000Mbps 포트 속도 및 지정된 사설 VLAN과 함께 가상 머신(VM)으로 프로비저닝됩니다. 
  * VM은 {{site.data.keyword.cloud}}에서 고객이 작성한 다중 디스크 표준 템플리트에서 프로비저닝됩니다. 
6. 운영 체제
  * CentOS 7

고객의 요구사항에 따라 Apache Brooklyn은 솔루션 구현을 위한 자동 스케일링 도구로 선택되었습니다. 

## Apache Brooklyn 개요

Apache Brooklyn은 자율 블루프린트를 통해 애플리케이션을 모델링하고, 모니터하고, 관리하기 위한 프레임워크입니다. 자세한 정보는 [Apache Brooklyn ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://brooklyn.incubator.apache.org/){: new_window} 사이트를 참조하십시오. 

### Apache Brooklyn 개념

Apache Brooklyn 문서에는 다음과 같은 Apache Brooklyn 개념의 정의가 제공됩니다. 

* 엔티티
* 애플리케이션
* 상위 및 멤버십 구성
* 센서 및 이펙터
* 라이프사이클 및 관리 컨텍스트
* 종속자 구성
* 위치, 정책
* 실행
* 구현

### DNS, NetScaler 및 Chef 통합

Apache Brooklyn은 사용자 정의 위치의 기본 클래스인 `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`를 제공합니다. 여기에는 머신이 프로비저닝될 때 추가 매개변수를 작성할 수 있는 메소드가 포함되어 있습니다. 조치는 머신이 프로비저닝된 후와 취소될 때 머신이 릴리스되기 전후에 실행될 수 있습니다. 

Brooklyn에서 제공된 `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`를 확장하여 고유한 위치 사용자 정의자 클래스를 작성했습니다. 이 예에서는 `brooklyn.location.jclouds.ProjectJcloudsLocationCustomizer`로 간주하십시오. 

대체된 세 가지 메소드는 다음과 같습니다. 

1. `public void customize(JcloudsLocation location, ComputeService computeService, TemplateOptions templateOptions)` - 이 메소드는 서버를 프로비저닝하기 위해 클라우드 API를 호출하기 전에 시작됩니다. 이 기능을 사용하여 프로비저닝 특성(예: `privateNetworkOnly, primaryBackendNetworkComponentVlanId, portSpeed,` 등)을 제공했습니다. 

* `public void customize(JcloudsLocation location, ComputeService computeService, JcloudsSshMachineLocation machine)` - 이 메소드는 머신이 프로비저닝되고 시작된 후에 시작됩니다. 그러므로 모든 서버 매개변수(예: 서버 IP 주소)가 사용 가능합니다. 서버를 DNS 및 로드 밸런서에 추가하는 코드는 이 메소드에 배치되어야 합니다. DNS 및 NetScaler REST API는 DNS 레코드를 작성하고 서버를 NetScaler에 바인드하는 데 사용됩니다. REST 호출을 DNS 및 NetScaler API에 제출하기 위해 `Brooklyn, brooklyn.util.http`에서 제공된 패키지를 사용했습니다. 

* `public void preRelease(JcloudsSshMachineLocation machine)` - 이 메소드는 서버가 중지되기 전에 머신 취소 시 시작됩니다. REST 호출을 DNS 및 NetScaler에 추가하여 DNS 및 NetScaler 레코드를 제거하고 NetScaler의 그룹에서 서버를 바인드 해제했습니다. 

새 서버를 Chef에 연결하기 위한 어떠한 조치도 취하지 않았습니다. 서버를 프로비저닝하는 데 사용한 이미지에는 Chef 클라이언트가 설치되어 있으며 시작 스크립트(Chef 클라이언트를 실행하고 Chef 서버에 연결하는 스크립트)가 있습니다. 원하는 경우 Chef와의 Brooklyn 확장을 사용하여 블루프린트를 작성할 수 있습니다. 

또한 REST 호출을 Chef 서버에 추가하여 적절한 클라이언트와 노드 레코드를 제거했습니다. 

### 애플리케이션 블루프린트

애플리케이션 블루프린트 내에서 서버의 위치, 매개변수를 수집하는 메트릭 및 자동 스케일링 특성을 사용자 정의했습니다. 다음 명령은 각 컴포넌트를 사용자 정의하는 데 사용됩니다. 

    name: Group1
    location:

      jclouds:softlayer:tor01:
      customizerType: brooklyn.location.jclouds.ProjectJcloudLocationCustomizer
      privateNetworkOnly: true
      primaryBackendNetworkComponentVlanId: 12345
      portSpeed: 1000
      imageId: 123456
      dnsZoneId: 12345
      netscalerGroup: app1
      netscalerGroupPort: 8080
      netscalerUrl: http://user:password@10.10.10.10/nitro/v1/

    services:
    - type: brooklyn.entity.group.DynamicCluster
      id: cluster
      name: dynamic cluster
      initialSize: 1
      memberSpec:
        $brooklyn:entitySpec:
        name: VMinSL
        type: brooklyn.entity.basic.EmptySoftwareProcess
        brooklyn.initializers:
        - type: brooklyn.entity.software.ssh.SshCommandSensor
          brooklyn.config:
            name: server.cpucount
            command: "LANG=en_US.UTF-8 sar -u 1 1|grep Average | awk '{print 100 - $8}'"
            targetType: java.lang.Double
            period: 10s
          brooklyn.config:
            post.launch.command: "sudo apt-get install -y sysstat"

      brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $brooklyn:sensor("server.cpucount")
          enricher.targetSensor: $brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average
        brooklyn.policies:
        - policyType: brooklyn.policy.autoscaling.AutoScalerPolicy
        brooklyn.config:
          metric: $brooklyn:sensor("server.cpucount.averaged")
          metricLowerBound: 10
          metricUpperBound: 60
          minPoolSize: 1
          maxPoolSize: 5

### 위치

블루프린트의 위치 섹션에서 다음과 같은 프로비저닝 특성을 지정했습니다. 

* 서버가 프로비저닝되는 위치(데이터 센터 및 VLAN)
* 서버가 privateNetworkOnly로 프로비저닝되는지 여부
* {{site.data.keyword.cloud_notm}} 표준 템플리트 또는 플렉스 이미지의 이미지 ID
* 포트 속도

또한 `ProjectJcloudLocationCustomizer`에서 사용되는 DNS 구역 ID를 지정하여 DNS 구역의 레코드와 NetScaler에서 서버를 바인드 및 바인드 해제하기 위한 NetScaler 정보를 추가하고 삭제했습니다. 

    location:

      jclouds:softlayer:tor01:
        customizerType: brooklyn.location.jclouds.ProjectJcloudLocationCustomizer
        privateNetworkOnly: true
        primaryBackendNetworkComponentVlanId: 12345
        portSpeed: 1000
        dnsZoneId: 12345
        netscalerGroup: app1
        netscalerGroupPort: 8080
        netscalerUrl: http://user:password@10.10.10.10/nitro/v1/

### 서비스

블루프린트의 서비스 섹션에서 다음을 지정했습니다. 

* 서버의 그룹을 배치함
* 각 서버에 설치할 Brooklyn 항목
* CPU 메트릭이 수집되고 사용된 방법
* 자동 스케일링 정책의 매개변수

#### 애플리케이션 스펙

    services:
    - type: brooklyn.entity.group.DynamicCluster #group of servers
      id: cluster
      name: dynamic cluster
      initialSize: 1 #number of servers initially created in the group

#### 멤버 스펙

Apache Brooklyn은 이미지에서 서버를 프로비저닝하는 목적으로만 필요하고 추가 설치 또는 구성이 필요하지 않음에 따라 `brooklyn.entity.basic.EmptySoftwareProcess` 호출이 사용되었습니다. 이 섹션에서는 서버에서 CPU 활용률을 주기적으로 수집하는 server.cpucount 센서도 지정했습니다. 

    memberSpec:
      $brooklyn:entitySpec:
      name: VMinSL
      type: brooklyn.entity.basic.EmptySoftwareProcess
      brooklyn.initializers:
      - type: brooklyn.entity.software.ssh.SshCommandSensor
        brooklyn.config:
          name: server.cpucount
          command: "LANG=en_US.UTF-8 sar -u 1 1|grep Average | awk '{print 100 - $8}'"
          targetType: java.lang.Double
          period: 10s
      brooklyn.config:
        post.launch.command: "sudo apt-get install -y sysstat"

### 메트릭

블루프린트의 메트릭 섹션에서 개별 서버의 메트릭이 수집되며 평균 값이 클러스터 레벨 센서에 지정됩니다. 

    brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $me0$brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average

### 자동 스케일링 정책

이 섹션에서는 자동 스케일링 정책 특성이 정의됩니다. 

    brooklyn.policies:
    - policyType: brooklyn.policy.autoscaling.AutoScalerPolicy
      brooklyn.config:
        metric: $brooklyn:sensor("server.cpucount.averaged")
        metricLowerBound: 10
        metricUpperBound: 60
        minPoolSize: 1
        maxPoolSize: 5
        minPeriodBetweenExecs: 10m
        resizeUpIterationIncrement: 2
        resizeUpIterationMax: 2
        resizeDownIterationIncrement: 2
        resizeDownIterationMax: 2

솔루션이 배치되면 사용자는 로드 밸런싱, DNS 및 Chef 서버가 포함된 시스템 레코드를 등록 및 등록 해제하여 적절한 방식으로 완벽하게 애플리케이션을 자동 스케일링(확장 및 축소)할 수 있었습니다. 
