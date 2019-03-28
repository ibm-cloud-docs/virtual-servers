---
copyright:
  years: 2014, 2018
lastupdated: "2018-10-23"
---

{:new_window: target="_blank"}

# ストレージのオプション
{: #storage-options}

仮想サーバーごとに SAN (ポータブル SAN) またはローカル・ストレージを選択できます。 必要に応じて、SAN またはローカル・ストレージを他のストレージ製品で補足することができます。

## ローカル・ストレージ

ローカル・ストレージは、仮想サーバー・ホストにとってローカルとなるディスクに構築されます。 ローカル・ストレージでは、ディスクの読み取り/書き込みのパフォーマンスが向上します。 ディスクは、冗長、ディスク交換、および正常性のモニタリングのために、{{site.data.keyword.cloud}} によって完全に管理されている RAID (Redundant Array of Independent Disks) 構成内に構築されます。 新しいデータ・センターでは、最良のパフォーマンスを提供するために、このストレージはすべてソリッド・ステート・ドライブ (SSD) になっています。

## ポータブル SAN ストレージ

ポータブル・ストレージ・ボリュームは、{{site.data.keyword.BluVirtServers_short}}上でのみ使用可能な補助ストレージ・ソリューションです。  ポータブル SAN は、ローカル・ホスト・ストレージではなく、{{site.data.keyword.cloud_notm}} のすべてのフラッシュ・ストレージ・クラスター上に構築されます。 このインフラストラクチャーにより、ホスト障害の際の回復力が向上し、また、より大きいボリュームのサポートが可能になります。 ホストで障害が発生した場合、SAN ベースのストレージを使用している仮想サーバー・インスタンスは、自動的に他のホストにマイグレーションされ、再始動されます。

ポータブル・ストレージは {{site.data.keyword.cloud_notm}} のネットワーク上のデータ・センターに存在する仮想サーバー間でデータを転送する場合の理想的なソリューションです。 ポータブル・ストレージ・ボリュームは、未加工の不定形式ブロック・レベル・ストレージにアクセスする必要があるデータベース・アプリケーションや、{{site.data.keyword.BluVirtServers_short}}間で大容量のデータ・セットを移動する場合に便利です。

2 次ディスクはすべてポータブル・ストレージとして接続されます。 多くの場合、これらの 2 次ディスクは、他の仮想サーバーに移動できるように、いつでも切り離すことができます。

**例外:** 平衡型ローカル・ストレージを使用するパブリック仮想サーバーでは、1 次ディスクも 2 次ディスクも切り離すことができません。

変更によってターゲット仮想サーバーのディスク割り当て量または最大ボリューム・サイズの制限を超えない限り、ディスクは別のサーバーに再接続できます。

**注:** 移動されたディスクは、ターゲット・サーバーのストレージ・タイプに変換されます。

ポータブル・ストレージ・ボリュームが、元の仮想サーバーとは異なるデータ・センター内で仮想サーバーに接続された場合、{{site.data.keyword.cloud_notm}} の内部システムは、ボリュームを新しいデータ・センター内の SAN にコピーします。 次に、システムはコピーされたボリュームの整合性を検査し、元のデータ・センター SAN から元のポータブル・ボリュームを削除します。

## LVM の制限

LVM (Logical Volume Management) は、ブート可能パーティショニング・スキームとしてサポートされていません。 適切なオペレーティング・システムのサポートおよび構成により、2 次仮想サーバー・ディスクを LVM パーティションに使用できます。 しかし、LVM は、Image Template のサポート対象ファイル・システムでも Flex Image のサポート対象ファイル・システムでもありません。

## 補足ストレージ

仮想サーバーは、{{site.data.keyword.filestorage_short}} および {{site.data.keyword.blockstorageshort}}、および {{site.data.keyword.cos_full}} とも完全に互換性があります。 これらのストレージ・タイプは、クラスター・ドライブ、共有ファイル・ストレージ、アーカイブ・ストレージ、大きいストレージ要件、または特定のパフォーマンス要件に推奨されます。

補足ストレージ・オプションについて詳しくは、以下のリソースを参照してください。

* [Getting Started with Block Storage](/docs/infrastructure/BlockStorage?topic=BlockStorage-GettingStarted)
* [Getting Started with File Storage](/docs/infrastructure/FileStorage?topic=FileStorage-GettingStarted)
* [Object Storage 概説](/docs/services/cloud-object-storage?topic=cloud-object-storage-about-ibm-cloud-object-storage#about-ibm-cloud-object-storage)

## 次のステップ
ポータブル・ストレージ・ボリュームの使用方法について詳しくは、以下のタスクを参照してください。
* [ポータブル・ストレージへのアクセス](/docs/vsi/storage?topic=virtual-servers-accessing-portable-storage)
* [ポータブル・ストレージの説明の編集](/docs/vsi/storage?topic=virtual-servers-editing-a-portable-storage-description)
