---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:note: .note}
{:new_window: target="_blank"}

# 配置グループの管理
{: #vsi_managing_placegroup}

配置グループは、{{site.data.keyword.cloud}} コンソールの「配置グループ」ページまたは「デバイス詳細」ページを使用して管理できます。
{:shortdesc}

## 配置グループの追加

「配置グループ」ページから配置グループを追加するには、以下の手順を実行します。
{:shortdesc}

1. [「配置グループ」 ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window} ページを開きます。
2. 「配置グループ」ページで、**「新規グループ」**をクリックします。
3. 配置グループの名前、場所、ポッド、ルールを入力し、**「作成」**をクリックします。

既存のインスタンスを配置グループに追加することはできません。仮想サーバー・インスタンスは、プロビジョニング時のみ配置グループに追加できます。 
{:note}

## 配置グループの管理

「配置グループ」ページから配置グループを管理するには、以下の手順を実行します。
{:shortdesc}

1. [「配置グループ」 ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window} ページを開きます。
2. 「配置グループ」セクションの下で、いくつかの管理タスクを実行できます。
     * 配置グループのリストと、割り当てられたインスタンスの数を表示する
     * グループを追加する
     * グループを名前変更する
     * インスタンスをプロビジョンする
     * グループを削除する
     
配置グループを削除する前に、割り当てられたサーバーを配置グループから削除する必要があります。 配置グループからインスタンスを除去するには、インスタンスを削除または再利用する必要があります。
{:note}
