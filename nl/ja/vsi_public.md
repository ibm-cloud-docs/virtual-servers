---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

keywords: public virtual servers, network traffic, virtual server deployment

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# パブリック仮想サーバー
{: #about-public-virtual-servers}

パブリック {{site.data.keyword.BluVirtServers}} オファリングは、IBM が管理するマルチテナント仮想サーバー・デプロイメントです。 これらのオファリングは、素早くビジネスを立ち上げて稼働させるためのあらゆるビジネス要件を満たす事前定義サイズにより、迅速なスケーラビリティーと高いコスト効率をお客様に提供します。
{:shortdesc}

パブリック仮想サーバーには、以下を含めて多くの利点があります。

* **グローバル・アベイラビリティー** 

    パブリック仮想サーバー・オファリングは、世界中のデータ・センターで利用可能です。

* **構成の選択、素早いデプロイメント、およびスケーラビリティー** 

    パブリック仮想サーバー・オファリングでは、さまざまなワークロード要件を満たすための、大小の仮想サーバー・オプションが提供されています。

VSI SAN およびその他の Network Attached Storage を含むパブリック仮想サーバーのネットワーク・トラフィックは保証されていません。 仮想サーバー・インスタンスのネットワーク・トラフィックが他の仮想サーバーに大きな悪影響を及ぼし始めた場合は、そのインスタンスを新しいホストで再始動するか、極端な場合は完全に無効にすることができます。 トラフィック・レベルが毎秒 20,000 から 30,000 パケット (PPS) に近づくと、このマイナスの影響がよく見られます。  保証されたネットワーキングを実現するには、専用仮想サーバー・オファリングを使用することをお勧めします。 詳しくは、単一テナント環境の[専用仮想サーバー](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)のオファリングを参照してください。

このオファリングでは、次のパブリック・インスタンス・ファミリーを利用できます。 

| ファミリー  | 説明                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [平衡型](/docs/vsi?topic=virtual-servers-balanced#balanced) | パフォーマンスとスケーラビリティーのバランスを必要とする、一般的なクラウド・ワークロードに最適です。 Network Attached Storage を使用します。 |
| [平衡型ローカル・ストレージ](/docs/vsi?topic=virtual-servers-balanced-local-storage#balanced-local-storage) | 非常に低遅延で高い入出力性能を必要とする大きなデータベース・ワークロードに最適です。|
| [コンピュート](/docs/vsi?topic=virtual-servers-compute#compute) | 中型から大型の Web トラフィック・ワークロードに最適です。|
| [メモリー](/docs/vsi?topic=virtual-servers-memory#memory)  | メモリー・キャッシュおよびリアルタイム分析ワークロードに最適です。 |
| [GPU](/docs/vsi?topic=virtual-servers-gpu#gpu)  | 高パフォーマンスのワークロードに最適です。
{: caption="表 1. パブリック仮想サーバー・ファミリーの選択" caption-side="top"}

これらのファミリーの中には、VPC 用の IBM Cloud Virtual Servers でも使用可能なものがあります。 詳しくは、[
仮想プライベート・クラウド用の IBM Cloud Virtual Servers](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started)を参照してください。
{:tip}

## 次のステップ

仮想サーバー・プロファイルを検討して決定したら、パブリック仮想サーバーをプロビジョンします。 開始するには、[パブリック・インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)を参照してください。
