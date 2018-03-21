---



copyright:
  years: 2017
lastupdated: "2017-10-24"


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
您有兩個選項可以佈建公用虛擬伺服器實例。第一個是透過 {{site.data.keyword.Bluemix}} 型錄，第二個則是透過 {{site.data.keyword.slportal_full}}。型錄及 {{site.data.keyword.slportal}} 需要唯一登入 ID。您的型錄使用者名稱及密碼將不適用於登入入口網站，反之亦然。
{:shortdesc}

開始之前，請檢閱下列必要條件。

  1. 確定您已設定 {{site.data.keyword.Bluemix_notm}} 型錄或 {{site.data.keyword.slportal}} 認證。 
  
     **附註：**針對 {{site.data.keyword.Bluemix_notm}} 型錄，您必須具有已升級的帳戶，才能訂購虛擬伺服器。如需升級帳戶的相關資訊，請參閱[切換至 IBM ID](https://console.bluemix.net/docs/admin/softlayerlink.html)。
  
  2. 如果您還沒有這麼做，請檢閱您可使用的部署選項。如需相關資訊，請參閱[部署選項：公用虛擬伺服器](../vsi/vsi_public.html)。

## 登入 
確定您已透過 {{site.data.keyword.Bluemix_notm}} 型錄或 {{site.data.keyword.slportal}} 登入： 

  <table>
   <CAPTION>表 1. 選擇登入位置</CAPTION>
   <THEAD>
   <TR>
   <th>如果您要使用下列項目登入...</th>
   <th>則...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud 型錄</td>
   <td>
   <ol>
   <li>開啟新的瀏覽器視窗，然後輸入 <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>。</li>
   <li>按一下<b>登入</b>鏈結（右下角）。</li>
   <li>輸入電子郵件或 IBM ID，然後按一下<b>繼續</b>。</li>
   <li>輸入您的「密碼」，然後按一下<b>登入</b>。</li>
   <li>選取<b>基礎架構</b> > <b>計算</b>。</li>
   <li>按一下<b>虛擬伺服器</b>磚。</li>
   <li>選取<b>公用虛擬伺服器</b>選項。</li>
   <li>按一下<b>建立</b>。即會開啟 {{site.data.keyword.slportal}} 的主頁面。</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>客戶入口網站</td>
   <td>
   <ol>
   <li>開啟新的瀏覽器視窗，然後輸入 <a href="https://control.softlayer.com">https://control.softlayer.com</a>。</li>
   <li>輸入您的「使用者名稱」及「密碼」，然後按一下<b>登入</b>。或者，按一下<b>使用 IBM ID 登入</b>。接著，輸入您的電子郵件或 IBM ID，然後按一下<b>繼續</b>。輸入您的密碼，然後按一下<b>登入</b>。即會開啟 {{site.data.keyword.slportal}} 的主頁面。</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## 佈建公用虛擬伺服器實例
{: #ordering-public-instance}
在您完成必要條件之後，即可開始佈建公用虛擬伺服器實例。您可以透過兩種方式來佈建公用實例：透過**裝置**功能表或**裝置**圖示。

### 透過裝置圖示佈建公用虛擬伺服器實例
若要透過*裝置* 圖示佈建公用虛擬伺服器實例，請完成下列步驟：

1.  從 {{site.data.keyword.slportal}} 中，找到**訂單**區段，然後按一下**裝置**。
2.  在「裝置」頁面上，針對其中一個「虛擬伺服器」供應項目，按一下**每小時**或**每月**。
3.  在*配置雲端伺服器* 頁面上，完成所有相關資訊。
4.  按一下**新增至訂單**按鈕以繼續。
5.  確認或編輯伺服器的網域資訊。
5.  按一下**雲端服務條款**及**協力廠商服務合約**勾選框。
6.  確認或輸入您的付款資訊，然後按一下**提交訂單**按鈕。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

 一系列的電子郵件會傳送給管理者：佈建訂單確認、佈建訂單核准和處理，以及佈建完成。登入 {{site.data.keyword.Bluemix_notm}} 之後，佈建完成電子郵件會包含*裝置詳細資料* 頁面的鏈結。您也可以直接登入 {{site.data.keyword.slportal}}。

### 透過裝置功能表佈建公用虛擬伺服器實例
{: #ordering-public-devices-menu}

您也可以透過主要 {{site.data.keyword.slportal}} 頁面上的*裝置* 功能表來佈建公用虛擬伺服器實例。 

1. 按一下**裝置 > 裝置清單**。

   「裝置」頁面會顯示您帳戶內的所有裝置類型：專用主機、虛擬伺服器、裸機伺服器，以及 NetScaler 應用程式交付控制器。
2. 按一下右上角的**訂購裝置**鏈結。
3. 在「裝置」頁面上，針對其中一個「虛擬伺服器」供應項目，按一下**每小時**或**每月**。
4. 在*配置雲端伺服器* 頁面上，完成所有相關資訊。
5. 按一下**新增至訂單**按鈕以繼續。
6. 確認或編輯伺服器的網域資訊。
7. 按一下**雲端服務條款**及**協力廠商服務合約**勾選框。
8. 確認或輸入您的付款資訊，然後按一下**提交訂單**按鈕。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

一系列的電子郵件會傳送給管理者：佈建訂單確認、佈建訂單核准和處理，以及佈建完成。登入 {{site.data.keyword.Bluemix_notm}} 之後，佈建完成電子郵件會包含*裝置詳細資料* 頁面的鏈結。您也可以直接登入 {{site.data.keyword.slportal}}。

### 後續步驟
佈建虛擬伺服器之後，即可開始進行管理。如需相關資訊，請參閱[管理虛擬伺服器](../vsi/vsi_managing.html)。
