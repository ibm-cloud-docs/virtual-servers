---



copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 常見問題：伺服器（一般）

## 「從映像檔開機」與「從映像檔載入」的差異為何？
「從映像檔開機」及「從映像檔載入」都是利用現有映像檔範本，而這些映像檔範本會套用至裝置來取代現有作業系統或補充作業系統，以試圖補救現有問題。「開機」與「載入」處理程序的主要差異在於所使用的映像檔類型。執行「從映像檔開機」或「從映像檔載入」處理程序時，請確定您已備份要回復的所有資料。

   * 「從映像檔開機」是一種方法，使用下列 ISO 將裝置開機：{{site.data.keyword.BluSoftlayer_full}} 為進行系統回復所提供的 ISO，或利用 {{site.data.keyword.slportal_full}} 中的*匯入映像檔* 特性所上傳的 ISO。ISO 可能是全新版本的裝置作業系統或回復磁碟，可用於試圖補救裝置問題。
   * 「從映像檔載入」是一種「OS 重新載入」方法，其利用已從裝置所擷取或使用 {{site.data.keyword.slportal}} 中的*映像檔匯入* 特性所上傳的映像檔範本。*從映像檔載入* 選項會使用 VHD 執行重新載入，而抹除裝置的所有資料，並將現有的作業系統和檔案取代為「類似新版」的所選取映像檔。

## 為何無法連接至 KVM 主控台？
如果您無法連接至 KVM 主控台，請檢閱下列疑難排解提示來協助解決此問題。發生其他問題時，請與支援中心聯絡。如需與支援中心聯絡的相關資訊，請參閱[取得協助及支援](../vsi/vsi_ts_index.html)。

   * KVM 主控台是一種 Java Applet。必須先安裝 Java，才能存取主控台。如需安裝 Java 的相關資訊，請參閱[免費 Java 下載 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.java.com/en/download/){: new_window}。  
   * 如果已安裝 Java，請確定已使用 VPN 來建立連線。如果未建立連線，則會在試圖連接至需要 VPN 連線的 KVM 主控台時顯示一則警告。
   * KVM 主控台可能會在連線處理程序期間產生一個以上的蹦現方框。請啟用來自 {{site.data.keyword.slportal}} 的蹦現畫面，以確保可以建立連線。
   * 您可能會收到「安全設定已封鎖 Java 應用程式」錯誤。若為裸機 iKVM 裝置，您必須針對 IPMI 裝置的「IP 位址」新增異常狀況。若為 VSI 裝置，請務必容許 "https://control.softlayer.com" 以及 KVM 的 IP 位址。如需相關資訊，請參閱[具有最新 Java 的安全設定為何封鎖 Java 應用程式？![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.java.com/en/download/help/java_blocked.xml){: new_window}。
   * 如果已符合上述條件，而且您收到的錯誤指出「main.jar 中遺漏必要的許可權資訊清單」，則表示「Java 控制台」中尚未啟用 Java Applet。在 Java SE 第 7 版中，已引進此設定作為 Oracle 的安全預防措施。在「控制台」中啟用 Applet 來解決此問題。

     **附註：**如果搭配使用 Mac OSX 與 Google Chrome，請參閱 Java 網站上的「安裝及使用 Mac Java 7 的資訊和系統需求」。

   * 如果您要嘗試透過標準 Java 連接至 VSI，而且除了錯誤之外並未取得任何項目，則也可以嘗試使用 VNC。

如果您已完成上述所有檢查，但仍然無法連接至 KVM 主控台，請與「支援中心」聯絡以取得疑難排解問題的其他協助。如果已建立主控台連線，但連接至裝置時發生問題，請確定所用來存取裝置的認證有效。必要的話，請與帳戶管理者聯絡來驗證認證。

## 我遺失了伺服器的密碼。如何才能進行回復？
如果伺服器的 root 或管理者密碼突然無法正常運作，則請檢查下列項目。必要的話，請使用啟動救援核心及重設密碼的指示。

   * 您要複製並貼上密碼嗎？如果不要，請嘗試這麼做。也請將密碼貼入記事本，以確保沒有空格意外與密碼一起複製。
   * 如果伺服器具有 cPanel，則 cPHulk 可能已因登入失敗而封鎖 IP 位址嗎？如果是這樣，可以使用 KVM 或 IPMI 存取伺服器，並在 "/scripts/cphulkdwhitelist" 後接 IP 位址的 cPHulk 中將 IP 位址設為白名單。
   * 最近是否有人嘗試在 {{site.data.keyword.slportal}} 中修改伺服器密碼來變更密碼？在 {{site.data.keyword.slportal}} 中變更密碼只會將您看到的內容變更為密碼。它並不會變更伺服器所使用的密碼。如果發生這種情況，您可以聯絡「支援中心」，他們通常可以回復原始有效密碼。
   * 您可能需要開機進入作業系統的救援模式，才能重設密碼。如需相關資訊，請參閱[啟動救援核心](/docs/vsi/vsi_launch_rescue.html)。

如果您已檢查上述所有項目，但仍然無法使用密碼連接至伺服器，請使用問題單聯絡支援中心，並要求密碼重設。「支援中心」需要將伺服器重新開機以重設密碼，因此，請確定您已準備好核准重新開機，以及（或）提供要在其間完成它的維護時間範圍。大部分密碼重設可以在 15 分鐘內完成。在 {{site.data.keyword.slportal}} 中，您可以移至**支援 > 新增問題單**來建立問題單，並使用*重新開機及主控台存取* 主旨。

## 支援將 LVM 分割區作為有效的檔案系統嗎？
LVM（邏輯磁區管理）提供 Linux 中檔案系統的邏輯管理。在 {{site.data.keyword.BluSoftlayer}} 環境中，不支援將 LVM 作為可開機分割方法。無法使用 LVM 訂購虛擬伺服器實例，而且匯入使用 LVM 作為開機分割區的映像檔將無法佈建。如果開機分割區上需要有 LVM，則裸機供應項目可以在特定作業系統開機時支援 LVM。藉由適當的 OS 支援及配置，可以將次要「VSI 磁碟」用於 LVM 分割區；不過，請務必注意，LVM 不是「Flex 映像檔」或「映像檔範本」支援的檔案系統。如果您還有其他問題，請向可協助您的支援團隊開立問題單。

## 客戶主機上預先配置的 161.26.0.0/16 路徑
{{site.data.keyword.BluSoftlayer}} 將會在所有新佈建的伺服器上啟用新路徑來支援未來產品。
   * 路徑會將 161.26.0.0/16 範圍 (161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255) 中的任何位址指向後端專用網路。
   * 此 IP 區塊是由 IANA 指派給 {{site.data.keyword.BluSoftlayer_notm}}，而且不會在公用網際網路上進行通告。
   * 只有 {{site.data.keyword.BluSoftlayer_notm}} 系統才會定址到此空間外部。
   * 需要更新客戶伺服器、虛擬伺服器及 Vyatta 閘道上的 ACL，以容許客戶主機使用已配置不在此範圍內之 IP 位址的「基礎架構」服務。

## 如何新增各種 OS 的新路徑

   <table>
   <CAPTION>表 1. 依 OS 新增路徑</CAPTION>
   <THEAD>
   <TR>
   <th>作業系統</th>
   <th>步驟</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Windows 2003 Standard 及 Enterprise</td>
   <td>
   從指令行新增持續性路徑，方法是鍵入：
   <blockquote>route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p</blockquote>
   <b>附註：</b>請將 10.0.0.1 取代為您的專用閘道 IP 位址。
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Server Core
   </td>
   <td>
   從指令行新增持續性路徑，方法是鍵入：
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>附註：</b>請將 10.0.0.1 取代為您的專用閘道 IP 位址。
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Web、Standard、Enterprise 及 Datacenter</td>
   <td>
   從指令行新增持續性路徑，方法是鍵入：
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>附註：</b>請將 10.0.0.1 取代為您的專用閘道 IP 位址。
   </td>
   </tr>
    <tr>
   <td>RedHat、Fedora 及 CentOS</td>
   <td>
   編輯/建立下列檔案來建立新路徑：<i>/etc/sysconfig/network-scripts/route-eth0</i>
   <p>在您建立該檔案之後，必須在其中新增下列資訊：<i>161.26.0.0/16 via 10.0.0.1</i>
   </p>
   <b>附註：</b>請將 10.0.0.1 取代為您的專用閘道 IP 位址。
   </td>
   </tr>
   <tr>
   <td>Ubuntu 及 Debian</td>
   <td>
   在 <i>/etc/network/interfaces</i> 檔案中，於檔案結尾新增下行：
   <blockquote>
   up route add -net 161.26.0.0/16 gw 10.0.0.1
   </blockquote>
   <b>附註：</b>請將 10.0.0.1 取代為您的專用閘道 IP 位址。
   </td>
   </tr>
   <tr>
   <td>Vyatta</td>
   <td><i>set protocols static route 161.26.0.0/16 next-hop 172.16.0.26</i>
   <p>
   <b>附註：</b>請將 172.16.0.26 取代為機器所在子網路的閘道，而此閘道應該與針對 10.0.0./8 路徑所定義的閘道相同。</p>
   </td>
   </tr>
   <tr>
   <td>ESXi</td>
   <td>使用下列指令，以將路徑新增至 ESXi 主機：
   <blockquote>
   esxcfg-route -a 161.26.0.0/16 10.0.0.1
   </blockquote>
   <b>附註：</b>請將 10.0.0.1 取代為您的專用閘道 IP 位址。
   </td>
   </tr>
   <tr>
   <td>CoreOS</td>
   <td>在 /etc/systemd/network 中建立名為 10-static.network 的靜態路徑檔，如下所示：
   <blockquote>
   [Route]
   Gateway=10.0.0.1
   Destination=161.26.0.0/16
   </blockquote>
   <b>附註：</b>請將 10.0.0.1 取代為您的專用閘道 IP 位址。
   </td>
   </tr>
   </TBODY>
   </table>
   
   <a name="top"></a>

## 我可以讓監視系統發出自動重新開機，並在伺服器停止回應時警告支援技術人員嗎？

可以，只要訂購**因監視失敗而自動重新開機**服務，您就可以設定監視系統自動將伺服器重新開機，並在發出監視警示時為支援技術人員發出問題單。我們提供 **NOC 監視**作為額外的服務，而在此服務中，您會在發生監視問題時收到個人通知。若要進一步瞭解這兩個供應項目，請參閱[伺服器監視 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://www.softlayer.com/services/monitoring/){:new_window}。

## 何謂 cvsup 鏡映？

您可以對已針對您執行的本端 cvsup 鏡映進行更新。請確定 supfile 具有下列項目：

```
*default host=cvsup.service.softlayer.com
```
{:pre }

distfiles 也可以從 freebsd.org 中進行鏡映及取得。您可以將下行新增至 */etc/make.conf* 檔案，以嘗試先從本端儲存庫進行下載：

```
MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"
```
{:screen }

如果在這裡找不到檔案，則會遵循個別埠 Makefile，並移至下一個鏡映。



