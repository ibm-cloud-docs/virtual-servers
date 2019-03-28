---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-25"

keywords: virtual server, suspend billing feature, virtual server instances, suspend billing

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:table: .aria-labeledby="caption"}

# 請求一時停止について
{: #requirements}

請求一時停止フィーチャーがサポートされている仮想サーバーの電源を切ると、一定のコンピュート・リソースについてはコストが発生しません。 サーバーの電源が切られると請求は自動的に停止します。 請求一時停止フィーチャーは、コスト削減に役立ち、仮想サーバーのリソースが再び必要になったときに仮想サーバーを再プロビジョンする必要がなくなります。
{:shortdesc}

2018 年 11 月 1 日より前に作成された仮想サーバー・インスタンスのほとんどは、請求一時停止フィーチャーをサポートしません。 仮想サーバー・インスタンスが請求一時停止フィーチャーをサポートしているかどうかを確認するには、[請求一時停止フィーチャーの表示](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature)を参照してください。

このフィーチャーは、世界中のデータ・センターで使用できます。 請求一時停止フィーチャーをサポートする仮想サーバー・インスタンスをプロビジョンするには、以下の設定を使用して仮想サーバー・インスタンスを構成する必要があります。

* 毎時 SAN
* 以下のいずれかのファミリーのパブリック・プロファイル:
  * 平衡型
  * コンピュート
  * メモリー

請求一時停止フィーチャーを、仮想サーバー・インスタンスのプロビジョニングおよび再利用をより素早く行うための代替方法として使用できます。
{:tip}

請求処理が中断されるのは、{{site.data.keyword.slportal_full}}、CLI、または {{site.data.keyword.slapi_short}} を介して仮想サーバー・インスタンスの電源をオフにした場合のみです。 OS を介して仮想サーバー・インスタンスの電源を直接オフにした場合、そのインスタンスの請求処理は中断されません。
{:note}

## プロビジョニングの詳細

{{site.data.keyword.cloud_notm}} カタログ (cloud.ibm.com)、CLI、または {{site.data.keyword.slapi_short}} を使用して、請求一時停止フィーチャーをサポートする仮想サーバー・インスタンスをプロビジョンできます。{{site.data.keyword.slportal}} (control.softlayer.com) を使用して請求一時停止フィーチャーをサポートする仮想サーバー・インスタンスをプロビジョンすることはできません。パブリック仮想サーバー・インスタンスのプロビジョニングについて詳しくは、[パブリック・インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)を参照してください。

{{site.data.keyword.cloud_notm}} カタログの場合、仮想サーバーを注文するには、アップグレードされたアカウントを持っている必要があります。 アカウントのアップグレードについて詳しくは、[IBM ID への切り替え](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)を参照してください。
{:note}

### Softlayer API を使用したプロビジョニング
{{site.data.keyword.slapi_short}} を使用して、請求一時停止フィーチャーをサポートする仮想サーバー・インスタンスをプロビジョンできます。 API サンプルについては、[Place Order Object を使用したパブリック・インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-api-rest-public#provisioning-a-public-instance-using-place-order-object)を参照してください。

プロビジョニング処理中に、特定の請求一時停止パッケージ ID を指定する必要があります。 {{site.data.keyword.slapi_short}} で、キー名 `SUSPEND_CLOUD_SERVER` を使用して請求一時停止パッケージ ID を照会できます。 サーバー・パッケージの検索例については、[Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/article/understanding-ordering/){: new_window} を参照してください。

## 請求の詳細

仮想サーバー・インスタンスの電源が切れているときに、どのコストの発生が停止するのか、どのコストが持続するのかを把握しておくことは重要です。

| リソース                      | 請求が停止する   | 請求が持続する |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          |          X        |                  |
| RAM                           |          X        |                  |
| ポート速度                    |          X        |                  |
| OS のライセンス     |          X        |                  |
| モニタリング・アドオン          |          X        |                  |
| 2 次パブリック IP アドレス |                   |         X        |
| ストレージ                       |                   |         X        |
{: caption="表 1. リソース請求の詳細" caption-side="top"}   

請求一時停止フィーチャーがサポートされている仮想サーバー・インスタンスをプロビジョンすると、仮想サーバー・インスタンスの使用時および使用停止時の両方で、分ごとに使用時間が計算されます。 インスタンスの電源を切ることによって請求一時停止フィーチャーを開始することがまったくなくても、インスタンスのライフサイクルにわたって分ごとに請求の計算が行われます。
{:note}

### 最小使用料金
請求一時停止フィーチャーをサポートする仮想サーバー・インスタンスは、場合によっては最小使用料金を適用できます。 使用量が 25 % より大きい場合、その使用量に対して請求されます。 使用量が 25 % より小さい場合、現行請求サイクル内でインスタンスが存在した時間の 25 % に対して課金されます。

### 請求書
仮想サーバーの請求を一時停止した場合、請求書にいくつか変更が見られます。 使用量ベースの詳細として、関連料金が示されるようになります。 例えば、利用可能時間、使用された時間、および課金される合計時間数を反映する、次のような項目が追加されることがあります。

```
Computing instance usage...
RAM usage...
Operating system usage...
```
{:screen}

## リソース詳細

### ストレージ

仮想サーバー・インスタンスの請求処理を一時停止すると、関連付けられたストレージの請求処理は持続しますが、仮想サーバー・インスタンスの電源が切れている間は保管データにアクセスできません。 インスタンスの請求処理を再開すると、データに再びアクセスできます。

### IP アドレス

仮想サーバー・インスタンスで請求が一時停止されている間、すべてのパブリック IP アドレスは保持されます。

### 制限

中断状態の仮想サーバー・インスタンスは、引き続きアカウント全体のデバイス割り当て量に加算されます。 インスタンスの制限について詳しくは、[FAQ: 仮想サーバー](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#concurrent)を参照してください。

## 次のステップ
請求一時停止がサポートされる仮想サーバーをプロビジョンした後、デバイスの請求処理の一時停止および再開を行うことができます。

仮想サーバー・インスタンスに対する請求が一時停止されると、デバイスに対する請求を再開するまで、そのインスタンスでは同じアクションの一部を実行できません。 {{site.data.keyword.slapi_short}} を介して、または、{{site.data.keyword.slportal}} の「デバイス詳細」ページにアクセスすることによって、デバイスが停止しているかどうかと、状況が変化した関連日付を確認できます。

仮想サーバー・インスタンスに対する請求を一時停止するには、仮想サーバーの電源を切ります。 詳しくは、[仮想サーバーの管理](/docs/vsi?topic=virtual-servers-managing-virtual-servers)を参照してください。
