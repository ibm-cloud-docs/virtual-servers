---

copyright:
  years: 2014, 2019
lastupdated: "2019-02-06"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 使用 Apache Brooklyn 自动缩放
{: #auto-scale-with-apache-brooklyn}

## 简介

一家公司每天向超过 10 亿的移动用户提供关键消费者数据。该公司要求我们提供用于创建位于专用网络上的自动缩放服务器组的功能。一个关键的需求是弹性；即根据工作负载需求和用户体验响应时间，系统可基于预先确定的策略自动扩展和缩减。

自动缩放基于 CPU 使用率。如果组中服务器的平均 CPU 使用率高于最高阈值或发生相应触发器事件，那么需要供应更多资源或对资源进行扩展。如果组中服务器的平均 CPU 使用率低于最低阈值或发生相应触发器事件，那么需要对资源进行缩减。客户的需求如下：

1. 能够指定以下参数：
  * 组中的初始服务器数
  * 组中最大服务器数和最小服务器数
  * CPU 阈值的上限和下限
  * 要在发生触发器事件时扩展和缩减的额外服务器数
2. 集成域名系统 (DNS)
  * 在供应或扩展了组中的服务器并且服务器可用后，将为其创建相应的 DNS 记录。
  * 缩减服务器后，将除去其 DNS 记录。
3. 集成负载均衡器
  * 在供应或扩展了组中的服务器并且服务器可用后，将向相应的 NetScaler 负载均衡器添加服务器记录，并将该服务器绑定到相应的负载均衡组。
  * 缩减服务器后，必须取消其与负载均衡组的绑定，并且将从 NetScaler 中除去相应的服务器记录。
4. 集成 Chef
  * 在供应或扩展了组中的服务器并且服务器可用后，Chef 客户机将在 Chef 服务器上运行并注册相应节点。
  * 缩减服务器后，将从 Chef 服务器中除去该服务器的节点和客户机记录。
5. 服务器供应需求
  * 组中的所有服务器都将作为虚拟机 (VM) 供应，并具有仅专用上行链路、1,000 Mbps 端口速度和指定的专用 VLAN。
  * VM 将通过客户在 {{site.data.keyword.cloud}} 中创建的多磁盘标准模板进行供应。
6. 操作系统
  * CentOS 7。

根据客户的需求，我们选择了将 Apache Brooklyn 作为实现解决方案的自动缩放工具。

## Apache Brooklyn 概述

Apache Brooklyn 是一个框架，用于通过自主蓝图对应用程序进行建模、监视和管理。有关更多信息，请参阅 [Apache Brooklyn ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://brooklyn.incubator.apache.org/){: new_window} 站点。

### Apache Brooklyn 概念

Apache Brooklyn 文档提供了 Apache Brooklyn 概念的定义，例如：

* 实体
* 应用程序
* 父配置和成员资格配置
* 传感器和受动器
* 生命周期和管理上下文
* 从属配置
* 位置和策略
* 执行
* 实施

### 集成 DNS、Netscaler 和 Chef

Apache Brooklyn 提供了用于定制位置 `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer` 的基类，该类包含允许在供应机器时创建其他参数的方法。操作可以在供应机器后运行，也可以在机器取消并释放之前和之后运行。

我们创建了自己的位置定制程序类，该类扩展了 Brooklyn 提供的 `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`。对于此示例，将其称为 `brooklyn.location.jclouds.ProjectJcloudsLocationCustomizer`。

覆盖了以下三个方法：

1. `public void customize(JcloudsLocation location, ComputeService computeService, TemplateOptions templateOptions)` - 此方法在调用云 API 来供应服务器之前启动。我们已启用提供供应属性（例如，`privateNetworkOnly、primaryBackendNetworkComponentVlanId、portSpeed` 等）的功能。

* `public void customize(JcloudsLocation location, ComputeService computeService, JcloudsSshMachineLocation machine)` - 此方法在供应并启动机器之后启动，这样所有服务器参数（如服务器 IP 地址）都可用。用于将服务器添加到 DNS 和负载均衡器的代码必须放置在此方法中。DNS 和 NetScaler REST API 用于创建 DNS 记录，并将服务器绑定到 NetScaler。我们使用了 `Brooklyn, brooklyn.util.http` 提供的包来提交对 DNS 和 NetScaler API 的 REST 调用。

* `public void preRelease(JcloudsSshMachineLocation machine)` - 此方法在取消机器后但停止服务器之前启动。我们在此添加了对 DNS 和 NetScaler 的 REST 调用，以除去 DNS 和 NetScaler 记录，并取消服务器与 NetScaler 组的绑定。

我们并未执行任何特定操作来将新服务器连接到 Chef。用于供应服务器的映像上已安装 Chef 客户机以及启动脚本（该脚本运行 Chef 客户机并将其连接到 Chef 服务器）。如果您愿意，可以使用 Brooklyn 与 Chef 的集成来创建蓝图。

我们还添加了对 Chef 服务器的 REST 调用，以除去相应的客户机和节点记录。

### 应用程序蓝图

在应用程序蓝图中，我们定制了服务器的位置、度量值收集参数和自动缩放属性。以下命令用于定制每个组成部分。

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

### 位置

在蓝图的 location 部分中，我们指定了供应属性，例如：

* 要供应服务器的位置（数据中心和 VLAN）
* 是否将使用 privateNetworkOnly 来供应服务器
* {{site.data.keyword.cloud_notm}} 标准模板或 flex 镜像的映像标识
* 端口速度

我们还指定了 DNS 区域标识（`ProjectJcloudLocationCustomizer` 将使用该标识来添加和删除 DNS 区域中的记录）以及 Netscaler 信息（用于将服务器绑定到 Netscaler 和取消服务器与 Netscaler 的绑定）。

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

### 服务

在蓝图的 services 部分中，我们指定了：

* 要部署一组服务器
* Brooklyn 要在每个服务器上安装的内容
* 如何收集和使用 CPU 度量值
* 自动缩放策略的参数

#### 应用程序规范

    services:
    - type: brooklyn.entity.group.DynamicCluster #group of servers
      id: cluster
      name: dynamic cluster
      initialSize: 1 #number of servers initially created in the group

#### 成员规范

使用了 `brooklyn.entity.basic.EmptySoftwareProcess` 调用，因为 Apache Brooklyn 只需要通过映像供应服务器，而无需其他安装或配置。此部分还指定了传感器 server.cpucount，用于定期从服务器收集 CPU 利用率。

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

### 度量值

在蓝图的 metrics 部分中，将收集各个服务器中的度量值，并将平均值分配给集群级别的传感器。

    brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $me0$brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average

### 自动缩放策略

在此部分中，定义了自动缩放策略属性：

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

一旦部署了该解决方案，用户就能够及时、无缝地自动扩展和缩减应用程序，注册和注销负载均衡、DNS 和 Chef 服务器的系统记录。
