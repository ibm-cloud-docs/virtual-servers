---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# イメージ・テンプレート
{: #image-templates}

{{site.data.keyword.BluVirtServers}} のイメージ・テンプレートにより、デバイスのイメージを取り込み、オーダー・プロセスでの変更を最小限にして、素早く構成を複製することができます。
{:shortdesc}

イメージ・テンプレートは、オペレーティング・システムに関係なく、すべての{{site.data.keyword.BluVirtServers_short}}用のイメージ・オプションを提供します。 イメージ・テンプレートでは、既存の仮想サーバーのイメージを取り込み、取り込んだイメージに基づいて新しいイメージを作成することができます。 イメージ・テンプレートは、ベアメタル・サーバーとは互換性がありません。

## イメージ・テンプレートの仕組み
すべてのイメージ・テンプレートの 2 つの主要アクションは、作成とデプロイです。 イメージの作成を要求すると、{{site.data.keyword.BluSoftlayer_full}} の自動システムがサーバーをオフラインにします。 サーバーがオフラインの間に、データの圧縮バックアップが作成され、構成情報が記録され、イメージ・テンプレートが {{site.data.keyword.BluSoftlayer_notm}} SAN に保管されます。 イメージ・テンプレートのデプロイメント・ステージ中、自動システムは、選択したイメージから収集されたデータに基づいて新規サーバーを構成します。 デプロイメント・プロセスは、ボリュームの調整を行い、コピーされたデータをリストアし、新規ホスト用の最終的な構成変更 (ネットワーク構成など) を行います。

イメージ・テンプレートについて詳しくは、[イメージ・テンプレートの概説](/docs/infrastructure/image-templates?topic=image-templates-getting-started-with-image-templates)を参照してください。
