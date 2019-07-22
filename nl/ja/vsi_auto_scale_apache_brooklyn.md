---

copyright:
  years: 2014, 2019
lastupdated: "2019-02-06"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Apache Brooklyn によるオート・スケール
{: #auto-scale-with-apache-brooklyn}

## 概要

重要な利用者データを無数のモバイル・ユーザーに毎日提供する企業が、プライベート・ネットワーク上にあるサーバーのオート・スケール・グループを作成する機能を提供することを要請しました。 鍵となる要件は伸縮自在であることでした。伸縮自在とは、ワークロードの需要とユーザー・エクスペリエンスの応答時間に応じて、システムが事前定義されたポリシーに従って自動的にスケールアップおよびスケールダウンすることです。

オート・スケールは CPU 使用量に基づきます。 グループ内のサーバーの平均 CPU 使用量が上限しきい値を超えたら (つまりトリガー・イベントが発生したら)、追加リソースをプロビジョン、つまりスケールアップする必要があります。 グループ内のサーバーの平均 CPU 使用量が下限しきい値より低くなったら (つまりトリガー・イベントが発生したら)、リソースをスケールダウンする必要があります。 お客様の要件は以下のとおりでした。

1. 以下のパラメーターを指定できること
  * グループ内のサーバーの初期数
  * グループ内のサーバーの最大数と最小数
  * CPU の上限および下限のしきい値
  * トリガー・イベント時にスケールアップ/スケールダウンする追加サーバーの数
2. ドメイン・ネーム・システム (DNS) との統合
  * グループでサーバーがプロビジョン、つまりスケールアップされて使用可能になったら、そのサーバーの適切な DNS レコードを作成する。
  * サーバーがスケールダウンされたら、その DNS レコードを削除する。
3. ロード・バランサーと統合する
  * グループでサーバーがプロビジョン、つまりスケールアップされて使用可能になったら、サーバー・レコードが適切な NetScaler ロード・バランサーに追加され、適切なロード・バランシング・グループにバインドされる。
  * サーバーがスケールダウンされたら、そのサーバーをロード・バランシング・グループからアンバインドし、サーバー・レコードを NetScaler から削除する。
4. Chef と統合する
  * グループでサーバーがプロビジョン、つまりスケールアップされ、使用可能になったら、Chef クライアントを実行し、Chef サーバーにノードを登録する。
  * サーバーがスケールダウンされたら、サーバーのノードとクライアント・レコードを Chef サーバーから削除する。
5. サーバーのプロビジョニングに関する要件
  * グループ内のすべてのサーバーを、プライベート専用アップリンク、1,000 Mbps ポート速度、指定したプライベート VLAN を備えた仮想マシン (VM) としてプロビジョンする。
  * {{site.data.keyword.cloud}} でお客様が作成したマルチディスク標準テンプレートから、VM をプロビジョンする。
6. オペレーティング・システム
  * CentOS 7。

お客様のこれらの要件に基づき、ソリューションを実装するオート・スケール・ツールとして Apache Brooklyn が選択されました。

## Apache Brooklyn の概要

Apache Brooklyn は、オートノミック・ブループリントを使用してアプリケーションのモデル化、モニター、管理を行うためのフレームワークです。 詳細については、[Apache Brooklyn ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://brooklyn.incubator.apache.org/){: new_window} サイトを参照してください。

### Apache Brooklyn の概念

Apache Brooklyn の資料には、以下のような Apache Brooklyn の概念が定義されています。

* エンティティー
* アプリケーション
* 親およびメンバーシップ構成
* センサーとエフェクター
* ライフサイクルおよび管理コンテキスト
* 依存構成
* ロケーション、ポリシー
* 実行
* 実装

### DNS、NetScaler、Chef の統合

Apache Brooklyn は、ロケーションをカスタマイズするための基本クラス `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer` を提供しています。このクラスには、マシンをプロビジョンする場合に追加パラメーターを作成できるようにするメソッドが含まれています。 アクションは、マシンがプロビジョンされた後に実行できます。また、マシンのキャンセル時に、マシンが解放される前と後にも実行できます。

私たちは、Brooklyn 提供の `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer` を拡張した独自のロケーション・カスタマイザー・クラスを作成しました。 この例では、これを `brooklyn.location.jclouds.ProjectJcloudsLocationCustomizer` と表します。

以下の 3 つのメソッドがオーバーライドされました。

1. `public void customize(JcloudsLocation location, ComputeService computeService, TemplateOptions templateOptions)` - このメソッドは、サーバーをプロビジョンするクラウド API が呼び出される前に開始されます。 `privateNetworkOnly、primaryBackendNetworkComponentVlanId、portSpeed` などのプロビジョニング・プロパティーを設定できるようにしました。

* `public void customize(JcloudsLocation location, ComputeService computeService, JcloudsSshMachineLocation machine)` - このメソッドは、マシンがプロビジョンされて起動した後に開始されます。つまり、すべてのサーバー・パラメーター (サーバー IP アドレスなど) が使用可能になった後です。 サーバーを DNS とロード・バランサーに追加するためのコードは、このメソッドに中に置く必要があります。 DNS レコードを作成してサーバーを NetScaler にバインドするためには、DNS および NetScaler の REST API を使用します。 DNS および NetScaler API の REST 呼び出しを実行するために、`Brooklyn、brooklyn.util.http` で提供されているパッケージを使用しました。

* `public void preRelease(JcloudsSshMachineLocation machine)` - このメソッドは、マシンのキャンセル時に、サーバーが停止される前に開始されます。 これには、DNS および NetScaler のレコードを削除し、サーバーを NetScaler のグループからアンバインドする DNS および NetScaler への REST 呼び出しを追加しました。

新規サーバーを Chef に接続するための特別な操作はありませんでした。 サーバーをプロビジョンするために使用するイメージに、Chef クライアントをインストールしておき、開始スクリプトも入れておきました (このスクリプトが Chef クライアントを実行し、Chef サーバーに接続します)。 必要に応じて、Chef との Brooklyn 統合を使用して、ブループリントを作成できます。

該当するクライアント・レコードとノード・レコードを削除するための Chef サーバーへの REST 呼び出しも追加しました。

### アプリケーション・ブループリント

アプリケーション・ブループリント内では、サーバーのロケーション、メトリック収集パラメーター、オート・スケール・プロパティーをカスタマイズしました。 各コンポーネントのカスタマイズに使用するコマンドは以下のとおりです。

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

### 場所

ブループリントの location セクションには、以下のようなプロビジョニング・プロパティーを指定しました。

* サーバーをプロビジョンする場所 (データ・センターと VLAN)
* privateNetworkOnly を指定してサーバーをプロビジョンするかどうか
* {{site.data.keyword.cloud_notm}} 標準テンプレートまたは flex イメージのイメージ ID
* ポート速度

DNS ゾーン ID も指定しました。これを `ProjectJcloudLocationCustomizer` で使用して、DNS ゾーン内のレコードと、NetScaler にサーバーをバインド/アンバインドするための NetScaler 情報を追加および削除します。

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

### サービス

ブループリントの services セクションには、以下を指定しました。

* サーバーのグループをデプロイすること
* 各サーバーにインストールする Brooklyn
* CPU メトリックを収集して使用する方法
* オート・スケール・ポリシーのパラメーター

#### アプリケーションの仕様

    services:
    - type: brooklyn.entity.group.DynamicCluster #group of servers
      id: cluster
      name: dynamic cluster
      initialSize: 1 #number of servers initially created in the group

#### メンバーの仕様

Apache Brooklyn ではサーバーをイメージからプロビジョンするだけでよく、追加のインストールや構成は不要であったため、`brooklyn.entity.basic.EmptySoftwareProcess` 呼び出しを使用しました。 このセクションにはセンサー server.cpucount も指定しました。これにより、サーバーから CPU 使用率を定期的に収集します。

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

### メトリック

ブループリントのメトリック・セクションでは、個々のサーバーのメトリックを収集し、その平均をクラスター・レベル・センサーに割り当てます。

    brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $me0$brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average

### オート・スケール・ポリシー

このセクションでは、オート・スケール・ポリシー・プロパティーを定義します。

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

ソリューションがデプロイされると、ユーザーはアプリケーションを適切なタイミングでシームレスかつ自動的にスケールアップ/ダウンし、同時にロード・バランシング、DNS、Chef サーバーへのシステム・レコードの登録/登録解除を実行できるようになりました。
