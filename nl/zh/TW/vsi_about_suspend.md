---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-08"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 關於暫停計費（測試版）
{: #requirements}

當您關閉支援暫停計費特性之虛擬伺服器的電源時，並不會增加特定運算資源的成本。關閉伺服器電源時，就會自動停止計費。暫停計費特性可協助您降低成本，並且讓您於再次需要虛擬伺服器的資源時，不需要重新佈建虛擬伺服器。只有新的佈建才支援暫停計費，現有實例並不予支援。
{:shortdesc}

全球各資料中心都提供此特性。若要存取暫停計費特性，您必須使用 {{site.data.keyword.slapi_short}} 指定暫停計費套件，來佈建新的虛擬伺服器實例。必須使用下列設定來配置新的虛擬伺服器實例：

* 每小時 SAN
* 下列其中一個系列的公用特性：
  * 平衡
  * 運算
  * 記憶體

您可以使用暫停計費特性作為更快速的替代方案，來佈建及取消佈建虛擬伺服器實例。
{:tip}

**附註：**只有在您透過 {{site.data.keyword.slportal_full}}、CLI 或 {{site.data.keyword.slapi_short}} 關閉虛擬伺服器實例的電源時，才會暫停計費。如果您直接透過 OS 關閉虛擬伺服器實例的電源，並不會暫停該實例的計費。

## 佈建

在測試版中，若要佈建支援暫停計費特性的虛擬伺服器實例，您必須使用 {{site.data.keyword.slapi_short}}。針對 API 範例，請參閱[使用下訂單物件佈建公用實例](../vsi/vsi_provision_api.html#provisioning-a-public-instance-using-place-order-object)。 

您也必須在佈建處理程序期間指定特定暫停計費套件 ID。您可以使用 keyName `SUSPEND_CLOUD_SERVER` 在 {{site.data.keyword.slapi_short}} 中查詢暫停計費套件 ID。如需搜尋伺服器套件的範例，請參閱[瞭解及使用 {{site.data.keyword.slapi_short}} 訂單 CLI 建置訂單 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://softlayer.github.io/article/understanding-ordering/){: new_window}。

## 計費詳細資料

請務必瞭解成本停止增加的項目，以及關閉虛擬伺服器實例電源時成本持續保存的項目。

| 資源                          | 計費停止          | 計費持續保存     |
| ----------------------------- | ----------------- | ---------------- |
|vCPU|X|                  |
|RAM|X|                  |
|埠速度|X|                  |
| 作業系統授權                  |X|                  |
| 監視附加程式                  |X|                  |
| 次要公用 IP 位址              |                   |X|
|儲存空間|                   |X|
{: caption="表 1. 資源計費詳細資料" caption-side="top"}   

**附註：**當您佈建支援暫停計費特性的虛擬伺服器實例時，會針對虛擬伺服器實例的使用中時間及暫停時間，計算每分鐘的使用時間。即使您從未透過關閉實例電源來起始暫停計費特性，還是會計算實例生命週期每分鐘的計費。 

### 使用費用下限
支援暫停計費特性的虛擬伺服器實例每個月都會有使用費用下限。如果用量大於 25%，則會向您收取該用量的費用。如果用量小於 25%，則會向您收取現行計費週期內現有實例之 25% 的小時的費用。 

### 帳單發票
當您暫停虛擬伺服器上的計費時，會在帳單發票中看到一些變更。相關費用現在顯示為用量型詳細資料。例如，您可能會看到下列反映可用小時、已使用小時及已收費總時數的新增項目：

```
Computing instance usage...
RAM usage...
Operating system usage...
```
{:screen}

## 資源詳細資料

### 儲存空間

當您暫停虛擬伺服器實例上的計費時，會持續保存相關聯的儲存空間，但無法在關閉虛擬伺服器實例電源時存取資料。當您繼續實例上的計費時，即可接著存取您的資料，也會再次開始正常的計費。

### IP 位址

暫停您虛擬伺服器實例的計費時，會為您保留所有公用 IP 位址。

您可以透過 {{site.data.keyword.slapi_short}} 或存取 {{site.data.keyword.slportal_full}} 中的「裝置詳細資料」頁面，來檢視是否已停止裝置，以及變更狀態的相關日期。

### 限制

支援的並行實例數目是您帳戶層面裝置配額的一部分。如需並行實例限制的相關資訊，請參閱[常見問題：虛擬伺服器](vsi_faqs_vs.html#concurrent)。

## 後續步驟
在您佈建支援暫停計費的虛擬伺服器之後，即可開始暫停及繼續裝置上的計費。
暫停虛擬伺服器實例上的計費時，除非繼續裝置的計費，否則無法完成實例上的所有相同動作。

若要暫停虛擬伺服器實例上的計費，請關閉虛擬伺服器電源。如需相關資訊，請參閱[管理虛擬伺服器](vsi_managing.html)。
