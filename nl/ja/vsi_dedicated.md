---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# 専用仮想サーバーについて
{: #dedicated-virtual-servers}

{{site.data.keyword.Bluemix}} インフラストラクチャーの専用ホストのオファリングは、仮想化された単一テナントの専用サーバーです。 ワークロード配置を最大限に制御でき、プロビジョン後の柔軟なオプションが提供されます。 仮想サーバーを既定のどの {{site.data.keyword.cloud_notm}} データ・センターに配置するかを決定でき、ホストをアカウントに直接割り振ることで容量を確保できます。
{:shortdesc}

このオファリングには、以下の機能が含まれます。

* アフィニティーとアンチアフィニティー。 存続するホストと仮想サーバー、および仮想サーバーと仮想サーバーの関係を指定できます。これらは、アフィニティーおよびアンチアフィニティーのルールと呼ばれます。 これらのルールを利用して、ワークロード要件に基づいてワークロードを適切に配置することができます。
* デプロイ後の管理。 ワークロード要件に基づいて、専用ホスト間で仮想サーバーをマイグレーションすることができます。
* ワークロードの可視性。 各ホストのリソース使用量 (コア、RAM、ローカル・ストレージ) を表示して、ワークロード管理を最大限に制御することができます。

デプロイメント・モデルとして、専用ホストと専用インスタンスの 2 つから選択できます。 専用ホストでは、ワークロード配置を制御でき、専用インスタンスでは、単一テナントの独立性が提供されます。

専用インスタンスでは、専用ホストでの制御機能の一部が提供されません。  詳細については、以下の表を参照してください。
{:note}

| 専用仮想サーバー機能 | 専用ホスト・インスタンス | 専用インスタンス |
| ------- | ------- | ------- |
| 単一テナントの独立性 | ![チェック・マーク・アイコン](../../icons/checkmark-icon.svg) | ![チェック・マーク・アイコン](../../icons/checkmark-icon.svg) |
| 仮想サーバーの配置制御 | ![チェック・マーク・アイコン](../../icons/checkmark-icon.svg) |   |
| リソースの可視性 | ![チェック・マーク・アイコン](../../icons/checkmark-icon.svg) |   |
| インスタンスの請求 |   | ![チェック・マーク・アイコン](../../icons/checkmark-icon.svg) |
| ホストの請求<sup>(1)</sup> | ![チェック・マーク・アイコン](../../icons/checkmark-icon.svg) |   |
| デプロイ後の制御 | ![チェック・マーク・アイコン](../../icons/checkmark-icon.svg) |   |
| 容量の予約 | ![チェック・マーク・アイコン](../../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="表 1. 制御機能" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup>ホストの価格設定にはコア、RAM、ローカル SSD、およびネットワーク速度が含まれます。 プレミアムのオペレーティング・システム (OS)、ストレージ・エリア・ネットワーク (SAN) ストレージ、およびソフトウェアのアドオンは、時間単位または月単位モデルの既存の料金およびライセンスで、インスタンスごとに価格設定されます。

専用ホストおよび専用ホスト・インスタンスの注文時には、以下の点に留意してください。

* ホストのサイズは、そこで実行するワークロードによって決まります。 デフォルトは 56 コア X 242 GB RAM X 1.2 TB ですが、その他の構成から選択することもできます。
* 同時に注文できるホストは、2 台だけです。 例えば、6 台のホストが必要であれば、3 件の別個の発注が必要です。
* ホストごとに固有の名前が必要で、POD は自動的に割り当てることができます。

## 次のステップ

デプロイメント・オプションを検討して決定したら、仮想サーバーをプロビジョンします。 開始するには、[専用ホストおよびインスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)を参照してください。
