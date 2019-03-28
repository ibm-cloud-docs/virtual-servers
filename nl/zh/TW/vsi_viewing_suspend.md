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

# 檢視暫停計費特性
{: #viewing-suspend-billing-feature}

您可以在 {{site.data.keyword.slportal_full}} 中或透過 {{site.data.keyword.slapi_short}} 檢視您的虛擬伺服器實例是否支援暫停計費特性。

## 在客戶入口網站中檢視暫停計費特性
若要在 {{site.data.keyword.slportal}} 中判斷虛擬伺服器實例是否支援暫停計費特性，請使用下列步驟：

1. 使用唯一認證來登入 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window}。
2. 從**裝置**功能表中，選取**裝置清單**。
3. 從**裝置清單**中，按一下虛擬伺服器實例的名稱。
4. 在**一般**區段的**配置**標籤上，您可以檢視虛擬伺服器實例是否支援暫停計費特性。

|欄位|值|
| --------------------------------------| ------------------------- |
|暫停計費：關閉電源時啟用|支援該特性。|
|暫停計費：無法使用|不支援該特性。|
{: caption="表 1. 暫停計費詳細資料" caption-side="top"}

## 透過 SoftLayer API 檢視暫停計費特性

下列指令是在 {{site.data.keyword.slapi_short}} 中驗證您的虛擬伺服器實例是否支援暫停計費特性的範例要求。

**附註**：下列 JSON 要求及回應是一般的範例。

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

以下是要求的範例 JSON 回應：

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

如需相關資訊，請參閱 [SLDN API 文件 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}。

## 後續步驟

若要進一步瞭解暫停計費特性，請檢閱下列資訊：
1. [關於暫停計費](/docs/vsi?topic=virtual-servers-requirements)
2. [管理虛擬伺服器](/docs/vsi?topic=virtual-servers-managing-virtual-servers)
