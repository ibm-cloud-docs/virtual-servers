---

copyright:
  years: 2014, 2019
lastupdated: "2019-02-06"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 利用 Apache Brooklyn 進行自動調整
{: #auto-scale-with-apache-brooklyn}

## 簡介

這是一家每日將重要消費者資料提供給超過十億位行動使用者的公司，已要求我們提供可針對位於專用網路的伺服器建立其自動調整群組的功能。關鍵需求是彈性；在其中，根據工作量需求及使用者體驗回應時間，系統會基於預先決定的原則自動擴增及縮減。

自動調整是以 CPU 使用率為基礎。如果群組中伺服器的平均 CPU 使用率高於最高臨界值或觸發事件，則需要佈建或擴增更多資源。如果群組中伺服器的平均 CPU 使用率低於最低臨界值或觸發事件，則需要縮減資源。客戶具有下列需求：

1. 指定下列參數的能力：
  * 群組中伺服器的起始數目
  * 群組中的伺服器數目下限及上限
  * 高及低 CPU 臨界值
  * 要在觸發事件時擴增及縮減的額外伺服器數目
2. 整合網域名稱系統 (DNS)
  * 在群組中的伺服器完成佈建或擴增並可供使用之後，就會為其建立適當的 DNS 記錄。
  * 當縮減伺服器時，會移除其 DNS 記錄。
3. 整合負載平衡器
  * 在群組中的伺服器完成佈建或擴增並可供使用之後，伺服器記錄會新增至適當的 NetScaler 負載平衡器，並連結至適當的負載平衡群組。
  * 當縮減伺服器時，必須從負載平衡群組中取消其連結，並且會從 NetScaler 中移除伺服器記錄。
4. 整合 Chef
  * 在群組中的伺服器完成佈建或擴增並可供使用之後，Chef 用戶端就會執行，並在 Chef 伺服器上登錄節點。
  * 當縮減伺服器時，會從 Chef 伺服器中移除伺服器的節點及用戶端記錄。
5. 伺服器佈建需求
  * 群組中的所有伺服器都會佈建為虛擬機器 (VM)，其中具有僅限專用的上行鏈路、1,000 Mbps 埠速度，以及指定的專用 VLAN。
  * VM 是從多重磁碟標準範本佈建的，而這些範本是由 {{site.data.keyword.cloud}} 中的客戶所建立的。
6. 作業系統
  * CentOS 7。

根據客戶的需求，已選取 Apache Brooklying 作為自動調整工具來實作解決方案。

## Apache Brooklyn 概觀

Apache Brooklying 是一種透過自主藍圖建模、監視及管理應用程式的架構。如需相關資訊，請參閱 [Apache Brooklyn ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://brooklyn.incubator.apache.org/){: new_window} 網站。

### Apache Brooklyn 概念

Apache Brookas 文件提供 Apache Brooklyn 概念的定義，例如

* 實體
* 應用程式
* 母項及成員資格配置
* 感應器及反應器
* 生命週期及管理環境定義
* 相依配置
* 位置、原則
* 執行
* 實作

### 整合 DNS、NetScaler 和 Chef

Apache Brooklyn 提供自訂位置的基礎類別 (`brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`)，其中包含容許在佈建機器時建立其他參數的方法。可在佈建機器之後，以及在取消時釋放它前後執行動作。

我們建立了自己的位置自訂程式類別，其已延伸 Brooklyn 所提供的 `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`。在此範例中，將它稱之為 `brooklyn.location.jclouds.ProjectJcloudsLocationCustomizer`。

已置換下列三個方法：

1. `public void customize(JcloudsLocation location, ComputeService computeService, TemplateOptions templateOptions)` - 在呼叫雲端 API 來佈建伺服器之前，會先啟動此方法。我們已啟用提供佈建內容（例如 `privateNetworkOnly、primaryBackendNetworkComponentVlanId、portSpeed`，以及其他項目）的能力。

* `public void customize(JcloudsLocation location, ComputeService computeService, JcloudsSshMachineLocation machine)` - 在佈建並啟動機器之後，會啟動此方法，因此可以使用所有伺服器參數，例如伺服器 IP 位址。將伺服器新增至 DNS 及負載平衡器的程式碼必須置於此方法中。DNS 及 NetScaler REST API 用來建立 DNS 記錄，並將伺服器連結至 NetScaler。我們已使用 `Brooklyn，brooklyn.util.http` 所提供的套件，將 REST 呼叫提交給 DNS 及 NetScaler API。

* `public void preRelease(JcloudsSshMachineLocation machine)` - 在停止伺服器之前，會在取消機器時啟動此方法。我們已在這裡將 REST 呼叫新增至 DNS 及 NetScaler，以移除 DNS 及 NetScaler 記錄，並從 NetScaler 的群組取消連結伺服器。

我們並未執行特定的動作，將新伺服器連接至 Chef。用來佈建伺服器的映像檔已安裝 Chef 用戶端，並具有啟動 Script（此 Script 會執行 Chef 用戶端，並將它連接至 Chef 伺服器）。如果喜好的話，您可以使用 Brooklyn 與 Chef 的整合來建立藍圖。

我們也已將 REST 呼叫新增至 Chef 伺服器，以移除適當的用戶端及節點記錄。

### 應用程式藍圖

在應用程式藍圖內，我們已自訂位置、度量收集參數，以及伺服器的自動調整內容。下列指令用來自訂每一個元件。

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

在藍圖的 location 區段中，我們已指定佈建內容，例如

* 將佈建伺服器的位置（資料中心及 VLAN）
* 是否將搭配 privateNetworkOnly 佈建伺服器
* {{site.data.keyword.cloud_notm}} 標準範本或彈性映像檔的映像檔 ID
* 埠速度

我們也已指定 DNS 區域 ID，其是由 `ProjectJcloudLocationCustomizer` 用來新增及刪除 DNS 區域中的記錄，以及用於從 NetScaler 連結及取消連結伺服器的 NetScaler資訊。

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

### 服務

在藍圖的 services 區段中，我們已指定

* 我們正在部署伺服器群組
* 每一部伺服器上要安裝哪個 Brooklyn
* 要如何收集及使用 CPU 度量
* 自動調整原則的參數

#### 應用程式規格

    services:
    - type: brooklyn.entity.group.DynamicCluster #group of servers
      id: cluster
      name: dynamic cluster
      initialSize: 1 #number of servers initially created in the group

#### 成員規格

已使用 `brooklyn.entity.basic.EmptySoftwareProcess` 呼叫，因為 Apache Brooklyn 只需要從映像檔佈建伺服器，而不需要任何其他安裝或配置。此區段也已指定感應器 (server.cpucd)，其會定期從伺服器收集 CPU 使用率。

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

### 度量

在藍圖的 metrics 區段中，會收集個別伺服器中的度量，並將平均值指派給叢集層次感應器。

    brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $me0$brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average

### 自動調整原則

在此區段中，會定義自動調整原則內容：

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

一旦部署了解決方案，使用者就能夠以及時的方式無縫地自動擴增及縮減其應用程式，同時利用負載平衡、DNS 及 Chef 伺服器登錄及取消登錄系統記錄。
