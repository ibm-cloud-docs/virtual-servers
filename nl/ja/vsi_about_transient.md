---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

keywords: transient virtual servers, transient instances, transient offering, cost savings

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 一時仮想サーバー
{: #about-vs-transient}
{{site.data.keyword.BluVirtServers}} の一時オファリングは、柔軟なワークロードがあり、コストを削減する必要がある場合に適したオプションです。 ワークロードを一時仮想サーバー上で実行することで、コストを節約できます。 一時インスタンスは、使用可能な未使用の容量がある場合にプロビジョンされます。 そのため、完全なオンデマンドのアカウントにデータ・センター・リソースが必要な場合は、これらのリソースを失う可能性もあります。 一時インスタンスは、これらのリソースを再利用する必要があるときに、最初にオンにしたものからプロビジョン解除されます。   

一時仮想サーバーには、以下の柔軟性があります。

* **グローバル・アベイラビリティー**

    一時仮想サーバー・オファリングは、世界中のデータ・センターで利用可能です。

* **コスト削減**

    一時仮想サーバーは、非実稼働ワークロードに理想的です。 例えば、一時インスタンスを使用して、アプリケーションのテストと開発や、常時のアップタイムを必要としない環境でのスケーラビリティーのテストを行うことができます。

一時インスタンスは、SAN バックアップ付きストレージを使用するパブリック・インスタンスです。

## 通知
{{site.data.keyword.slapi_short}} を使用して、一時インスタンスにリソースを使用できるときに通知を受信することができます。 API を使用して、リソースが使用可能になったときに一時仮想サーバーをプログラムでプロビジョンすることもできます。 同様に、API を使用して、リソースが使用不可になったときにインスタンスのプロビジョニングをプログラムで停止することができます。 詳しくは、[自動再利用通知の構成](/docs/vsi?topic=virtual-servers-configuring-notifications-for-reclaims-of-transient-virtual-servers)に関するセクションを参照してください。

## 制限
一時仮想サーバーをプロビジョンする前に、以下の制限を検討してください。

* サポートされる同時インスタンスの数は、アカウント全体のデバイス割り当て量の一部です。 同時インスタンスの制限について詳しくは、[FAQ: 仮想サーバー](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#concurrent)を参照してください。
* 一時インスタンスは、アップグレードしたりダウングレードすることはできません。
* リソースは、通知なしでいつでも再利用できます。
* 一時インスタンスは、ローカル・ストレージを使用できません。
* 一時インスタンスは、SAN バックアップ付きストレージ (平衡型、コンピュート、メモリー) のみを使用します。
* 一時インスタンスは、GPU ベースのプロファイルを使用できません。


## 次のステップ

仮想サーバー・フレーバーを検討して選択したら、一時仮想サーバーをプロビジョンします。 最初に、以下の情報を検討してください。
1. [プロビジョニングの選択](/docs/vsi?topic=virtual-servers-provisioning-selections)
2. [一時インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-transient)
