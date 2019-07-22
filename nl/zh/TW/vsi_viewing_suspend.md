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

# 檢視暫停計費特性
{: #viewing-suspend-billing-feature}

## 開始之前
首先，導覽至裝置功能表，並確定您具有完成作業所需的正確帳戶許可權。 

* 導覽至主控台的裝置功能表。如需相關資訊，請參閱[導覽至裝置](/docs/vsi?topic=virtual-servers-navigating-devices)。
* 確保您具有任何必要的帳戶許可權及裝置存取權。只有帳戶擁有者或具有**管理使用者**標準基礎架構許可權的使用者才能調整許可權。 

如需許可權的相關資訊，請參閱[傳統基礎架構許可權](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理裝置存取權](/docs/vsi?topic=virtual-servers-managing-device-access)。

## 檢視暫停計費特性 
若要判斷虛擬伺服器實例是否支援暫停計費特性，請使用下列步驟：

1. 從**裝置**功能表，選取**裝置清單**。 
2. 從**裝置清單**中，按一下虛擬伺服器實例的名稱。 
3. 在**實例詳細資料**區段中，您可以檢視虛擬伺服器實例是否支援暫停計費特性。 

|欄位|值|
| --------------------------------------| ------------------------- |
|暫停計費：關閉電源時啟用|支援該特性。|
|暫停計費：無法使用|不支援該特性。|
{: caption="表 1. 暫停計費詳細資料" caption-side="top"}

## 透過 SoftLayer API 檢視暫停計費特性

下列指令是透過 {{site.data.keyword.slapi_short}} 驗證您的虛擬伺服器實例是否支援暫停計費特性的範例要求。

下列 JSON 要求及回應是一般範例。
{:note}

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
1. [暫停計費](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [管理虛擬伺服器](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

