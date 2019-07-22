---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-16"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 佈建專用主機及實例
{: #ordering-vs-dedicated}

您有兩個關於如何佈建專用實例的選項。第一個是透過 {{site.data.keyword.Bluemix}} 型錄，第二個則是透過 {{site.data.keyword.slportal_full}}。型錄及 {{site.data.keyword.slportal}} 需要唯一登入 ID。您的型錄使用者名稱及密碼將不適用於登入入口網站，反之亦然。請參閱[註冊 {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-signup#signup) 以設定 {{site.data.keyword.Bluemix_notm}} 型錄或 {{site.data.keyword.slportal}} 認證。
{:shortdesc}

## 佈建專用主機及實例
您可以透過 {{site.data.keyword.cloud_notm}} 或 {{site.data.keyword.slportal}} 佈建專用主機及實例。

### 透過 IBM Cloud 型錄佈建專用主機及實例
若要透過 {{site.data.keyword.cloud_notm}} 型錄佈建專用主機及專用主機實例，請完成下列步驟：

1. 使用唯一認證來登入 [{{site.data.keyword.cloud_notm}} 型錄 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/catalog/){: new_window}。
2. 在**運算基礎架構**區段中，按一下**虛擬伺服器**磚。
3. 選取**專用虛擬伺服器**選項。
4. 按一下**建立**。
5. 在**專用主機**區段中，您可以選取**建立主機**以建立新的專用主機，或是選取**指定主機**以選取現有的專用主機。
6. 完成專用主機及專用虛擬伺服器實例的所有相關資訊。
7. 在您檢閱訂單摘要之後，請按一下**協力廠商服務合約**勾選框。
8. 按一下**佈建**。

### 透過客戶入口網站佈建專用主機及實例
若要透過 {{site.data.keyword.slportal}} 佈建專用主機及專用主機實例，請完成下列步驟：

1. 使用唯一認證來登入 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window}。

#### 佈建專用主機
請使用下列步驟，以佈建專用主機。

1.	按一下**裝置**圖示。
2.  按一下**每小時專用虛擬伺服器**或**每月專用虛擬伺服器**鏈結。

   **附註：**專用伺服器 (dedicated server) 是專用伺服器 (private server)。

即會將您帶到*配置雲端伺服器* 頁面。您可以從此頁面訂購與專用主機相關聯或無關的專用實例。如需訂購實例的相關資訊，請參閱[佈建專用主機實例](#provision-dedicated-instances)。

4.	按一下表單右側的**建立主機**按鈕。
5.	輸入下列資訊：

    <table>
    <CAPTION>表 1. 專用主機佈建選項</CAPTION>
    <THEAD>
    <TR>
    <th>欄位</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>數量</td>
    <td>輸入要訂購的專用主機數目。請注意，一個佈建訂單只能部署兩個專用主機。</td>
    </tr>
    <tr>
    <td>位置</td>
    <td>選取您要放置主機的 {{site.data.keyword.cloud}} 資料中心。如需適用資料中心的清單，請參閱「關於」。</td>
    </tr>
    <td>專用主機</td>
    <td>預設為 56 核心 X 242 GB RAM X 1.2 TB，但您可以從其他配置中選取。</td>
    </tr>
    </TBODY>
    </table>

    「訂單摘要」會顯示在*配置* 頁面右側。

6.  按一下**新增至訂單**按鈕。
7.  確認*結帳* 頁面上的選項，然後向下捲動至*專用主機進階系統配置*。
8.  輸入下列資訊：

    <table>
    <CAPTION>表 2. 專用主機進階系統配置</CAPTION>
    <THEAD>
    <TR>
    <th>欄位</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>POD 選項</td>
    <td>按一下下拉方框，然後選取您要放置專用主機的 POD。</td>
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

9.  按一下**雲端服務條款**勾選框。
10. 確認或輸入您的付款資訊，然後按一下**提交**按鈕。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

    一系列的電子郵件會傳送給管理者：佈建訂單確認、佈建訂單核准和處理，以及佈建完成。登入 {{site.data.keyword.Bluemix_notm}} 之後，佈建完成電子郵件所包含的鏈結會直接將您帶到**裝置詳細資料**頁面。另一個選項則是直接登入 {{site.data.keyword.slportal}}。

#### 佈建專用主機實例
{: #provision-dedicated-instances}

若要透過 {{site.data.keyword.slportal}} 佈建專用主機實例，請完成下列步驟：

1.	按一下**裝置 > 裝置清單**。

    *裝置* 頁面會顯示您帳戶內的所有裝置類型：專用主機、虛擬伺服器、裸機伺服器，以及 NetScaler 應用程式交付控制器。

2.	選取專用主機實例的主機，方法是按一下其在**裝置名稱**下的鏈結。

    您是位在*裝置詳細資料* 頁面的**配置**標籤。**問題單**標籤會列出作用中支援問題單，**配置**標籤則會顯示所選取計費期間的記憶體用量。如需這些標籤的相關資訊，請參閱「使用裝置詳細資料來管理專用主機及實例」。

3.	向下捲動至**實例**頁框。

    專用主機的計費方式（每月或每小時）可決定專用主機實例的計費。請注意，如果您有每月計費的主機，則可以同時佈建每小時及每月計費的專用主機實例。佈建實例時，提供兩個鏈結：**每小時新增**及**每月新增**。每小時計費的專用主機只能佈建每小時計費的專用主機實例，而且只會看到**每小時新增**鏈結。

4.	如果您的主機是每小時或每月計費，請按一下**每小時新增**鏈結；如果您的主機是每月付費，請按一下**每月新增**鏈結。即會將您重新導向至*配置雲端伺服器* 頁面。

5.	輸入下列資訊：

    <table>
    <CAPTION>表 3. 專用主機實例選項</CAPTION>
    <THEAD>
    <TR>
    <th>欄位</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>數量</td>
    <td>要部署在單一主機上的專用主機實例數目。</td>
    </tr>
    <tr>
    <td>放置</td>
    <td>
    <ul>
    <li>自動指派 - {{site.data.keyword.Bluemix_notm}} 會自動將實例指派給主機（相對於指定實例）。您的實例將會放在具有容量的資料中心內。如果您自動指派實例，將不會使用任何專用主機的容量。</li>
    <li>指定主機 - 與帳戶相關聯的專用主機將會顯示在「專用主機」下。</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>專用主機</td>
    <td>從清單中，選取要佈建實例的專用主機。</td>
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
    <td>每個專用主機實例最多可以佈建四個其他開機磁碟（SAN 或「本端」）。</td>
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

6.	按一下**新增至訂單**按鈕。
7.  在*結帳* 頁面的*進階系統配置* 下方，輸入下列資訊：

<table>
    <CAPTION>表 4. 專用主機實例進階系統配置</CAPTION>
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

8.  按一下**雲端服務條款**及**協力廠商服務合約**勾選框。
9. 確認或輸入您的付款資訊，然後按一下**提交**按鈕。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。


已佈建專用主機實例之後，您會收到一封電子郵件。

## 後續步驟
虛擬伺服器在佈建且可供使用之後，即可使用 {{site.data.keyword.slportal_full}} 或 {{site.data.keyword.slapi_full}} 來配置虛擬伺服器。如需相關資訊，請參閱[配置虛擬伺服器](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers)。
