---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# サード・パーティー・イメージからの仮想サーバー・インスタンスのプロビジョニング
{: #ordering-3P}

サード・パーティー・ベンダーによって作成されたイメージから仮想サーバー・インスタンスをプロビジョンすることができます。サード・パーティーのイメージは {{site.data.keyword.cloud}} カタログの「クラウド・イメージ」リンクから利用できます。
{:shortdesc}

## 始めに
開始する前に、{{site.data.keyword.cloud_notm}} カタログの資格情報をセットアップしたことを確認します。

{{site.data.keyword.Bluemix_notm}} カタログの場合、仮想サーバーを注文するには、アップグレードされたアカウントを持っている必要があります。 アカウントのアップグレードについて詳しくは、[IBMid への切り替え](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)を参照してください。
{:note}

## 仮想サーバー・イメージの選択
1. ユーザー固有の資格情報を使用して [{{site.data.keyword.cloud_notm}} カタログ ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://console.bluemix.net/catalog/){: new_window} にログインします。
2. **「クラウド・イメージ」**セクションで、デプロイするサード・パーティーのイメージを見つけてクリックします。
3. カスタム・イメージの詳細を確認し、**「続行」**をクリックします。事前に選択したカスタム・イメージの**「仮想サーバー・インスタンス - カスタム・イメージ (Virtual server instance - custom image)」**ページが表示されます。

## デプロイメント・オプションの確認と選択
詳しくは、以下のトピックを参照してください。

|              デプロイメント・オプション                           |  説明                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[パブリック仮想サーバー](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)            | IBM が管理するマルチテナンシー仮想サーバー・デプロイメント|
|[一時仮想サーバー](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)| 割引コストで提供され、柔軟なワークロードに最適な、IBM が管理するマルチテナンシー仮想サーバー・デプロイメント |
|[予約済み仮想サーバー](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | 契約条件の保証容量を含む、IBM が管理するマルチテナンシー仮想サーバー・デプロイメント |
|[専用仮想サーバー](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)      | IBM が管理する単一テナンシー仮想サーバー・デプロイメント            |
{: caption="表 1. デプロイメント・オプション" caption-side="top"}

## 仮想サーバーのプロビジョニング
デプロイメント・オプションを決定したら、プロビジョニング・プロセスを開始します。 詳しくは、以下のトピックを参照してください。

カスタム・イメージを使用してプロビジョニング・プロセスを開始したため、このプロビジョニング・プロセス中にイメージ・タイプを変更することはできません。
{:note}

|              プロビジョニングの説明                                         |  説明                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[パブリック・インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                | さまざまなオプションによるパブリック・インスタンスのプロビジョン             |
|[一時インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                | さまざまなオプションによる一時インスタンスのプロビジョン            |
|[予約済み容量およびインスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | さまざまなオプションによる予約済み容量およびインスタンスのプロビジョン |
|[専用ホストおよび専用インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)| 専用ホスト上のプライベート・インスタンスまたは専用インスタンスのプロビジョン|
{: caption="表 2. プロビジョニング情報" caption-side="top"}


## 次のステップ
仮想サーバーがプロビジョンされて使用可能になったら、{{site.data.keyword.cloud_notm}} コンソールまたは {{site.data.keyword.slapi_short}} を使用して仮想サーバーを構成できます。 詳しくは、[仮想サーバーの構成](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers)を参照してください。
