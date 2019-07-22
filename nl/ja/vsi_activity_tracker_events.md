---

copyright:
  years: 2016, 2018
lastupdated: "2018-11-06"

subcollection: virtual-servers

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Activity Tracker イベント
{: #at_events}

セキュリティー担当者、監査員、およびマネージャーは、{{site.data.keyword.cloudaccesstrailfull}} サービスを使用して、ユーザーおよびアプリケーションが {{site.data.keyword.Bluemix}} 内の仮想サーバー・インスタンス (VSI) とどのように対話しているかをトラッキングできます。 アカウント所有者およびアカウントにリンクされたユーザーは、{{site.data.keyword.cloudaccesstrailshort}}に記録される仮想サーバー・イベントをトリガーできます。
{:shortdesc}

{{site.data.keyword.cloudaccesstrailshort}} サービスは、{{site.data.keyword.Bluemix_notm}} 内のサービスの状態を変更するユーザー開始アクティビティーを記録します。 詳しくは、[{{site.data.keyword.cloudaccesstrailshort}} について](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov )を参照してください。

ユーザーのアクションのモニタリングを開始するには、[{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started-with-cla#getting-started-with-cla)を参照してください。

イニシエーターは、ユーザー、サービス、またはアプリケーションのいずれかです。 ユーザーがイベントを生成するには、 {{site.data.keyword.Bluemix}} コンソールの**「インフラストラクチャー」**リソースにアクセスできる必要があります。
{: tip}

## 仮想サーバー・インスタンス・イベント
{: #vsi}

{{site.data.keyword.cloudaccesstrailshort}} サービスを使用して、仮想サーバー・インスタンス (VSI) をそのライフサイクルを通じて監査できます。

以下の表に、イベントを生成するアクションをリストします。

| アクション | 説明 |
|----------|---------|
| `audit-log.vsi.provision`             | イニシエーターが VSI をプロビジョンするとイベントが生成されます。  |
| `audit-log.vsi-port.disable`          | イニシエーターが VSI でポートを無効化するとイベントが生成されます。 |
| `audit-log.vsi-port.enable`           | イニシエーターが VSI でポートを有効化するとイベントが生成されます。 |
| `audit-log.vsi-port-speed.update`     | イニシエーターが VSI でポート速度を更新するとイベントが生成されます。 |
| `audit-log.vsi-image-template.create` | イニシエーターが VSI のイメージ・テンプレートを作成するとイベントが生成されます。  |
| `audit-log.vsi.power-off`             | イニシエーターが VSI をパワーオフするとイベントが生成されます。  |
| `audit-log.vsi.soft-power-off`        | イニシエーターが VSI でソフト・パワーオフを実行するとイベントが生成されます。 |
| `audit-log.vsi.force-power-off`       | イニシエーターが VSI で強制パワーオフを実行するとイベントが生成されます。 |
| `audit-log.vsi.reboot`                | イニシエーターが VSI をリブートするとイベントが生成されます。 |
| `audit-log.vsi.soft-reboot`           | イニシエーターが VSI でソフト・リブートを実行するとイベントが生成されます。 |
| `audit-log.vsi.hard-reboot`           | イニシエーターが VSI でハード・リブートを実行するとイベントが生成されます。 |
| `audit-log.vsi.power-on`              | イニシエーターが VSI をパワーオンするとイベントか生成されます。 |
| `audit-log.vsi.rename`                | イニシエーターが VSI を名前変更するとイベントが生成されます。 |
| `audit-log.vsi.rescue`                | イニシエーターが VSI をレスキューするとイベントが生成されます。 |
| `audit-log.vsi-security-group.add`    | イニシエーターが VSI にセキュリティー・グループを追加するとイベントが生成されます。 |
| `audit-log.vsi-security-group.remove` | イニシエーターが VSI からセキュリティー・グループを削除するとイベントが生成されます。 |
| `audit-log.vsi.reload`                | イニシエーターが VSI に対してオペレーティング・システム (OS) 再ロードを実行するとイベントが生成されます。 |
| `audit-log.vsi.boot`                  | イニシエーターがイメージから VSI をブートするとイベントか生成されます。 |
| `audit-log.vsi.reclaim`               | イニシエーターが VSI をキャンセルするとイベントが生成されます。 |
| `audit-log.vsi.pause`                 | イニシエーターが VSI を一時停止するとイベントが生成されます。 |
{: caption="表 2. VSI アクション" caption-side="top"}



## イベントの表示
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} イベントは、イベントが生成された {{site.data.keyword.Bluemix_notm}} 地域で使用可能な {{site.data.keyword.cloudaccesstrailshort}} **アカウント・ドメイン**で確認できます。 詳しくは、[アカウント・イベントの表示](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events) を参照してください。

{{site.data.keyword.cloudaccesstrailshort}} イベントは、アクションが発生するのと同じ地域内の {{site.data.keyword.cloudaccesstrailshort}} サービスに自動的に転送されます。
