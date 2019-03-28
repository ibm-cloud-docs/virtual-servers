---

copyright:
  years: 2018, 2019
lastupdated: "2019-03-01"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 請求一時停止フィーチャーの表示
{: #viewing-suspend-billing-feature}

仮想サーバー・インスタンスが、{{site.data.keyword.slportal_full}} で、または {{site.data.keyword.slapi_short}} を使用して、請求一時停止フィーチャーをサポートしているかどうかを表示できます。

## カスタマー・ポータルでの請求一時停止フィーチャーの表示
仮想サーバー・インスタンスが {{site.data.keyword.slportal}} で請求一時停止フィーチャーをサポートしているかどうかを確認するには、以下の手順を実行します。

1. ユーザー固有の資格情報を使用して、[{{site.data.keyword.slportal}} ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://control.softlayer.com/){: new_window} にログインします。
2. **「デバイス」**メニューから**「デバイス・リスト」**を選択します。
3. **「デバイス・リスト」**で、仮想サーバー・インスタンスの名前をクリックします。
4. **「構成」**タブの**「一般」**セクションで、仮想サーバー・インスタンスが請求一時停止フィーチャーをサポートしているかどうかを確認できます。

| フィールド                                 | 値                     |
| --------------------------------------| ------------------------- |
| 請求一時停止: 電源オフで使用可能 | フィーチャーはサポートされています。     |
| 請求一時停止: 使用不可          | フィーチャーはサポートされません。 |
{: caption="表 1. 請求一時停止の詳細" caption-side="top"}

## Softlayer API を使用した請求一時停止フィーチャーの表示

次のコマンドは、仮想サーバー・インスタンスが {{site.data.keyword.slapi_short}} の請求一時停止フィーチャーをサポートしているかどうかを検証する要求の例です。

**注**: 次の JSON 要求と応答は、一般的な例です。

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
1. [請求一時停止について](/docs/vsi?topic=virtual-servers-requirements)
2. [仮想サーバーの管理](/docs/vsi?topic=virtual-servers-managing-virtual-servers)
