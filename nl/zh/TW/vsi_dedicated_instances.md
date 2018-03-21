---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 佈建專用實例

您有兩個關於如何佈建專用實例的選項。第一個是透過 {{site.data.keyword.Bluemix}} 型錄，第二個則是透過 {{site.data.keyword.slportal_full}}。型錄及 {{site.data.keyword.slportal}} 需要唯一登入 ID。您的型錄使用者名稱及密碼將不適用於登入入口網站，反之亦然。請參閱[註冊 {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} 以設定 {{site.data.keyword.Bluemix_notm}} 型錄或 {{site.data.keyword.slportal}} 認證。
{:shortdesc}

## 登入 IBM Cloud 型錄
請使用下列步驟登入 {{site.data.keyword.Bluemix_notm}}，以開始佈建專用實例。 

1. 開啟新的瀏覽器視窗，然後輸入 [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/){: new_window}。
2.	按一下**登入**鏈結（右上角）。 
3.	輸入您的電子郵件或 IBM ID，然後按一下**繼續**。
4.	輸入您的「密碼」，然後按一下**登入**。
5.	選取**基礎架構 > 計算**。
6.  按一下**虛擬伺服器**磚。
7.	選取**專用虛擬伺服器**選項。
8.  按一下**建立**。 

您將會位於 {{site.data.keyword.slportal}} 的主頁面上。

## 登入客戶入口網站
請使用下列步驟登入 {{site.data.keyword.slportal}}，以開始專用實例的訂購。

1.	開啟新的瀏覽器視窗，然後輸入 [https://control.softlayer.com](https://control.softlayer.com){: new_window}。 
2.	輸入您的「使用者名稱」及「密碼」，然後按一下**登入**，或按一下**使用 IBM ID 登入**。
3.	輸入您的電子郵件或 IBM ID，然後按一下**繼續**。
4.	輸入您的「密碼」，然後按一下**登入**。

您將會位於 {{site.data.keyword.slportal}} 的主頁面上。

## 佈建專用實例
{: #provision-dedicated-instances}
您可以透過兩種方式來佈建專用實例：透過**裝置**圖示或**裝置**功能表。

### 透過裝置圖示佈建專用主機實例
{: #ordering-dedicated-devices-menu}
佈建專用主機實例的第一個選項是使用 {{site.data.keyword.slportal}} 首頁上的**裝置**圖示。下列步驟會引導您完成此處理程序。

1.	按一下**裝置**圖示。即會顯示**訂購 SoftLayer 產品及服務**視窗。 
2.  在「專用虛擬伺服器」下，選取**每小時**或**每月**。即會將您重新導向至*配置雲端伺服器* 頁面。 

3.	輸入下列資訊：
       
    <table>
    <CAPTION>表 1. 專用主機實例選項</CAPTION>
    <THEAD>
    <TR>
    <th>欄位</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>數量</td>
    <td>要部署的專用實例數目。</td>
    </tr>
    <tr>
    <td>放置</td>
    <td>
    <ul>
    <li>自動指派 - {{site.data.keyword.Bluemix_notm}} 會自動將實例指派給所選取資料中心內的主機。</li>
    <li>指定主機 - 與專用主機實例搭配使用。如需專用主機及專用主機實例的相關資訊，請參閱[專用虛擬伺服器](../vsi/vsi_dedicated.html)。</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>資料中心</td>
    <td>選取要在其中佈建實例的資料中心。</td>
    </tr>
    <tr>
    <td>運算實例</td>
    <td> 選取佈建訂單中每一個實例的記憶體及 CPU。</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> 選取佈建訂單中每一個實例的 RAM。</td>
    </tr>
    <tr>
    <td>作業系統</td>
    <td>選取實例的作業系統。請注意，如果伺服器與作業系統之間發生衝突，則會發出錯誤訊息。例如，在 Microsoft SQL Server 上選取 Linux。</td>
    </tr>
    <tr>
    <td>第一個硬碟</td>
    <td>選取訂單中每一個實例的 SAN 或「本端」。</td>
    </tr>
    <tr>
    <td>其他磁碟</td>
    <td>每個專用實例最多可以佈建四個其他開機磁碟（SAN 或「本端」）。</td>
    </tr>
    <td>網路選項</td>
    <td> 選取適當的選項，或使用預設值。</td>
    </tr>
    <tr>
    <td>附加程式</td>
    <td> 選取適當的選項，或使用預設值。</td>
    </tr>
    <tr>
    </TBODY>
    </table> 

4.	按一下**新增至訂單**按鈕。即會將您重新導向至「結帳」頁面。
5.  在*結帳* 頁面的*進階系統配置* 下方，輸入下列資訊：

<table>
    <CAPTION>表 2. 專用實例進階系統配置</CAPTION>
    <THEAD>
    <TR>
    <th>欄位</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>VLAN 選項</td>
    <td>如果您已訂購至少一部伺服器，請將新的伺服器新增至您帳戶下的 VLAN。</td>
    </tr>
    <tr>
    <td>佈建 Script</td>
    <td>提供可讓您在佈建之後自動化特定步驟的 Script。</td>
    </tr>
    <tr>
    <td>SSH 金鑰</td>
    <td>提供 SSH 金鑰的公開金鑰，以讓您在佈建伺服器之後登入該伺服器。</td>
    </tr>
    <tr>
    <td>使用者 meta 資料</td>
    <td>自訂佈建 Script 的選用 meta 資料。</td>
    </tr>
    <tr>
    <td>主機名稱</td>
    <td>輸入伺服器的永久或暫時名稱（例如，server1）。</td>
    </tr>
    <tr>
    <td>網域</td>
    <td>輸入不會與網際網路網域名稱衝突的子網域名稱（例如，test.acme.com）。</td>
    </tr>
    </TBODY>
    </table>

6.  按一下**雲端服務條款**及**協力廠商服務合約**勾選框。
7. 確認或輸入您的付款資訊，然後按一下**提交訂單**按鈕。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

    一系列的電子郵件會傳送給管理者：佈建訂單確認、佈建訂單核准和處理，以及佈建完成。登入 {{site.data.keyword.Bluemix_notm}} 之後，佈建完成電子郵件所包含的鏈結會直接將您帶到**裝置詳細資料**頁面。另一個選項則是直接登入 {{site.data.keyword.slportal}}。

### 透過裝置功能表佈建專用實例

您的第二個選項是透過主要 {{site.data.keyword.slportal}} 頁面中的**裝置**功能表來佈建專用實例。下列步驟會引導您完成此處理程序。

1.	按一下**裝置 > 裝置清單**。 
 
    *裝置* 頁面會顯示您帳戶內的所有裝置類型：虛擬伺服器、裸機伺服器、專用主機，以及 NetScaler 應用程式交付控制器。 

2.	按一下頁面右側的**訂購裝置**鏈結。即會顯示**訂購 SoftLayer 產品及服務**視窗。
3.	遵循[透過裝置功能表佈建專用實例](#ordering-dedicated-devices-menu)下從步驟 2 開始的步驟。

### 後續步驟
佈建虛擬伺服器之後，即可開始進行管理。如需相關資訊，請參閱[管理虛擬伺服器](../vsi/vsi_managing.html)。
