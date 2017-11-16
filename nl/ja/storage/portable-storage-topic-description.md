---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ポータブル・ストレージ・ボリュームの概要

ポータブル・ストレージ・ボリュームは、{{site.data.keyword.BluVirtServers_short}}上でのみ使用可能な補助ストレージ・ソリューションです。一度に 1 つの仮想サーバーに接続できます。また、これは {{site.data.keyword.cloud}} のネットワーク上のデータ・センターに存在する仮想サーバー間でデータを転送する場合の理想的なソリューションです。ポータブル・ストレージ・ボリュームは、未加工の不定形式ブロック・レベル・ストレージにアクセスする必要があるデータベース・アプリケーションや、{{site.data.keyword.BluVirtServers_short}}間で大容量のデータ・セットを移動する場合に便利です。

ポータブル・ストレージ・ボリュームが、元の仮想サーバーとは異なるデータ・センター内で仮想サーバーに接続された場合、{{site.data.keyword.cloud}} の内部システムは、ボリュームを新しいデータ・センター内の SAN にコピーします。次に、システムはコピーされたボリュームの整合性を検査し、元のデータ・センター SAN から元のポータブル・ボリュームを削除します。

## 次のステップ
ポータブル・ストレージ・ボリュームの使用方法について詳しくは、以下のタスクを参照してください。
* [ポータブル・ストレージへのアクセス](../storage/access-portable-storage-screen.html)
* [ポータブル・ストレージの説明の編集](../storage/edit-description-portable-storage-volume-psv.html)
