---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 佈建公用實例
{: #ordering-vs-public}

## 開始之前
您有兩個選項可以佈建公用虛擬伺服器實例。第一個是透過 {{site.data.keyword.Bluemix}} 型錄，第二個則是透過 {{site.data.keyword.slportal}}。型錄及 {{site.data.keyword.slportal}} 需要唯一登入 ID。您的型錄使用者名稱及密碼將不適用於登入入口網站，反之亦然。
{:shortdesc}

開始之前，請檢閱下列必要條件。

  1. 確定您已設定 {{site.data.keyword.Bluemix_notm}} 型錄或 {{site.data.keyword.slportal}} 認證。

     **附註：**針對 {{site.data.keyword.Bluemix_notm}} 型錄，您必須具有已升級的帳戶，才能訂購虛擬伺服器。如需升級帳戶的相關資訊，請參閱[切換至 IBM ID](https://console.bluemix.net/docs/admin/softlayerlink.html)。

  2. 如果您還沒有這麼做，請檢閱您可使用的部署選項。如需相關資訊，請參閱[部署選項：公用虛擬伺服器](../vsi/vsi_public.html)。

  3. 檢閱虛擬伺服器實例容量考量。如需相關資訊，請參閱[容量考量](ts_capacity_bp.html)。

## 佈建公用虛擬伺服器實例
{: #ordering-public-instance}

在您完成必要條件之後，即可開始佈建公用虛擬伺服器實例。您可以透過 {{site.data.keyword.cloud_notm}} 型錄或 {{site.data.keyword.slportal}} 佈建公用實例。

### 透過 IBM Cloud 型錄佈建公用虛擬伺服器實例
若要透過 {{site.data.keyword.cloud_notm}} 型錄佈建公用虛擬伺服器實例，請完成下列步驟：

  1. 使用唯一認證來登入 [{{site.data.keyword.cloud_notm}} 型錄 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/catalog/){: new_window}。 
  2. 在**運算基礎架構**區段中，按一下**虛擬伺服器**磚。
  3. 選取**公用虛擬伺服器**選項。
  4. 按一下**建立**。
  5. 完成虛擬伺服器實例的所有相關資訊。 
  6. 在您檢閱訂單摘要之後，請按一下**協力廠商服務合約**勾選框。 
  7. 按一下**佈建**。
  
### 透過客戶入口網站佈建公用虛擬伺服器實例
若要透過 {{site.data.keyword.slportal}} 佈建公用虛擬伺服器實例，請完成下列步驟：

  1. 使用唯一認證來登入 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window}。
  2. 找到**訂單**區段，然後按一下**裝置**。 
  3. 在「裝置」頁面上，針對其中一個「虛擬伺服器」供應項目，按一下**每小時 SAN**、**每小時本端**、**每月**或**暫時性**。
  4. 在*配置雲端伺服器* 頁面上，完成所有相關資訊。
  5. 按一下**新增至訂單**按鈕以繼續。
  6. 確認或編輯伺服器的網域資訊。
  7. 按一下**雲端服務條款**及**協力廠商服務合約**勾選框。
  8. 確認或輸入您的付款資訊，然後按一下**提交訂單**按鈕。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

 一系列的電子郵件會傳送給管理者：佈建訂單確認、佈建訂單核准和處理，以及佈建完成。登入 {{site.data.keyword.Bluemix_notm}} 之後，佈建完成電子郵件會包含*裝置詳細資料* 頁面的鏈結。您也可以直接登入 {{site.data.keyword.slportal}}。

## 後續步驟
佈建虛擬伺服器之後，即可開始進行管理。如需相關資訊，請參閱[管理虛擬伺服器](../vsi/vsi_managing.html)。
