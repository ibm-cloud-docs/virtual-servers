---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-28"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 請求一時停止フィーチャーの表示
{: #viewing-suspend-billing-feature}

## 始めに
まず、デバイス・メニューに移動して、タスクを実行するための適切なアカウント権限を持っていることを確認します。 

* コンソールのデバイス・メニューに移動します。詳しくは、[デバイスへのナビゲート](/docs/vsi?topic=virtual-servers-navigating-devices)を参照してください。
* 必要なアカウント権限とデバイス・アクセス権限を持っていることを確認します。アカウントの所有者、またはクラシック・インフラストラクチャーの**「ユーザーの管理」**権限を持つユーザーのみが、権限を調整できます。 

権限について詳しくは、[クラシック・インフラストラクチャー許可](/docs/iam?topic=iam-infrapermission#infrapermission)および[デバイス・アクセスの管理](/docs/vsi?topic=virtual-servers-managing-device-access)を参照してください。

## 請求一時停止フィーチャーの表示 
仮想サーバー・インスタンスが請求一時停止フィーチャーをサポートしているかどうかを確認するには、以下の手順を実行します。

1. **「デバイス」**メニューから**「デバイス・リスト」**を選択します。 
2. **「デバイス・リスト」**で、仮想サーバー・インスタンスの名前をクリックします。 
3. **「インスタンスの詳細」**セクションで、仮想サーバー・インスタンスが請求一時停止フィーチャーをサポートしているかどうかを確認できます。 

| フィールド                                 | 値                     |
| --------------------------------------| ------------------------- |
| 請求処理が中断されました: 電源オフで使用可能 | フィーチャーはサポートされています。     |
| 請求処理が中断されました: 使用不可          | フィーチャーはサポートされません。 |
{: caption="表 1. 請求一時停止の詳細" caption-side="top"}

## SoftLayer API を使用した請求一時停止フィーチャーの表示

次のコマンドは、仮想サーバー・インスタンスが請求一時停止フィーチャーをサポートしているかどうかを、{{site.data.keyword.slapi_short}} を使用して検証する要求の例です。

次の JSON 要求と応答は、一般的な例です。 
{:note}

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

要求に対する JSON 応答の例を次に示します。

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

詳しくは、[SLDN API 資料![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}を参照してください。

## 次のステップ

請求一時停止フィーチャーについて詳しくは、以下の情報を参照してください。
1. [請求一時停止](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [仮想サーバーの管理](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

