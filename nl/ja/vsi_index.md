---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-29"

keywords: virtual servers, provisioning process, IBM Cloud Virtual Servers

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 入門チュートリアル
{: #getting-started-tutorial}

{{site.data.keyword.BluVirtServers}} のデプロイは、ほんの数分で行うことができます。 仮想サーバーは、ユーザーが選択した仮想サーバー・イメージから、ワークロードに適した地理的地域にデプロイされます。
{:shortdesc}

仮想プライベート・クラウドで仮想サーバーを試してみてください。 詳しくは、[
仮想プライベート・クラウド用の IBM Cloud Virtual Servers](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started)を参照してください。
{:tip}

クラシック・インフラストラクチャーで仮想サーバーを作成するときに、パブリック (マルチテナンシー) 環境か専用 (単一テナンシー) 環境を選択することができます。 その後、選択した環境に応じて、時間単位の仮想サーバー、月単位の仮想サーバー、または一時仮想サーバーを選択する必要もあります。 パブリック仮想サーバーの場合、さらに SAN ベースのストレージかローカル・ストレージのいずれかを使用するように選択します。

## 始めに

始めに、以下の前提条件を確認してください。

  1. 仮想サーバーをオーダーするには、アップグレードされたアカウントを持っている必要があります。 このプロセスにはある程度時間がかかり、続行する前にユーザーの要求が承認される必要があります。 アカウントのアップグレードについて詳しくは、[IBMid への切り替え](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)を参照してください。
  2. デプロイメント・オプションを確認および選択します。 詳しくは、以下のトピックを参照してください。

|              デプロイメント・オプション                           |  説明                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[パブリック仮想サーバー](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)            | IBM が管理するマルチテナンシー仮想サーバー・デプロイメント|
|[一時仮想サーバー](/docs/vsi?topic=virtual-servers-about-vs-transient)| 割引コストで提供され、柔軟なワークロードに最適な、IBM が管理するマルチテナンシー仮想サーバー・デプロイメント |
|[予約済み仮想サーバー](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers)  | 契約条件の保証容量を含む、IBM が管理するマルチテナンシー仮想サーバー・デプロイメント |
|[専用仮想サーバー](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers)      | IBM が管理する単一テナンシー仮想サーバー・デプロイメント            |
{: caption="表 1. デプロイメント・オプション" caption-side="top"}   

## 仮想サーバーのプロビジョニング

デプロイメント・オプションを決定したら、プロビジョニング・プロセスを開始します。

|              プロビジョニングの説明                                         |  説明                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[パブリック・インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-public)                | さまざまなオプションによるパブリック・インスタンスのプロビジョン             |
|[一時インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-transient)                | さまざまなオプションによる一時インスタンスのプロビジョン            |
|[予約済み容量およびインスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances)            | さまざまなオプションによる予約済み容量およびインスタンスのプロビジョン |
|[専用ホストおよび専用インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)| 専用ホスト上のプライベート・インスタンスまたは専用インスタンスのプロビジョン|
{: caption="表 2. プロビジョニング情報" caption-side="top"}

## 次のステップ

仮想サーバーがプロビジョンされて使用可能になったら、{{site.data.keyword.cloud_notm}} コンソールまたは {{site.data.keyword.slapi_short}} を使用して仮想サーバーを構成できます。 詳しくは、[仮想サーバーの構成](/docs/vsi?topic=virtual-servers-configuring-virtual-servers)を参照してください。
