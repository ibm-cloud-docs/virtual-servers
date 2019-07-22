---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 配置虛擬伺服器
{: #configuring-virtual-servers}

當您存取虛擬伺服器時，請務必變更您的密碼，並考慮為更安全的鑑別解決方案設定 SSH。有許多其他選項可用來配置您的虛擬伺服器，以符合您環境的需求。
{:shortdesc}

## 登入
使用一開始建立帳戶時透過電子郵件收到的認證，登入 [{{site.data.keyword.cloud}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/classic?){: new_window}。或者，您也可以登入 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){:new_window}。

## 尋找虛擬伺服器
在 {{site.data.keyword.cloud_notm}} 主控台的「裝置清單」中，尋找虛擬伺服器。從「裝置清單」中，您可以管理裝置、升級裝置，或產生頻寬使用情形圖表。如需相關資訊，請參閱[管理虛擬伺服器](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)。

## 變更您的密碼
使用高保護性密碼準則來變更您的密碼。請參閱[檢視及管理裝置使用者名稱和密碼](/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device#view-update-user-name-password-for-device)。

## 配置 SSH
SSH 提供比密碼鑑別更好的安全解決方案。請參閱[開始使用 SSH 金鑰](/docs/infrastructure/ssh-keys?topic=ssh-keys-getting-started-tutorial#getting-started-tutorial)。

## 記錄 IP 位址及認證
將伺服器的 IP 位址及認證日誌保留在安全的位置，讓您可以快速存取它們，而不需要登入 {{site.data.keyword.cloud_notm}} 主控台。
- 從「裝置清單」中，可以檢視個別裝置 IP 位址。
- 在裝置的「Snapshot 視圖」中，可以檢視個別裝置 root 密碼。按一下裝置名稱旁邊的箭頭來展開視圖。
- 使用「裝置清單」內的「下載 CSV」動作，可以檢視多台裝置的 IP 位址。請從「設定」齒輪選取「下載 CSV」，以下載試算表格式的完整裝置和詳細資料清單。

## 更新軟體認證
所有已在佈建過程中載入裝置的軟體都會獲指派暫時認證。您可以在 {{site.data.keyword.cloud_notm}} 主控台中每一台裝置的「密碼」標籤上檢視及管理這些認證。第一次存取您的軟體時，請使用這些暫時認證。最好是在第一次存取軟體的密碼之後變更該密碼。請使用包含字母、數字及符號組合的高保護性密碼。

密碼更新可以選擇性地儲存在每一台裝置的「密碼」標籤上；不過，請瞭解，當您在 {{site.data.keyword.cloud_notm}} 主控台內儲存密碼時，任何具有帳戶存取權及適當許可權的人員都可以檢視「密碼」畫面上所儲存的密碼。

如需檢視及管理軟體認證的相關資訊，請參閱[管理標準基礎架構存取](/docs/vsi?topic=iam-mngclassicinfra)。

## 在專用網路上存取伺服器
專用網路是透過遠端桌面 (RDP) 使用 SSH 及 KVM over IP 與裝置互動的前導。「VPN 存取」工具容許與最接近 SSL VPN 端點或所選擇端點的專用網路連線。也需要有 VPN 存取，才能與數個提供的服務互動。如需相關資訊，請參閱[開始使用虛擬專用網路 (VPN)](/docs/infrastructure/iaas-vpn?topic=VPN-gettingstarted-with-virtual-private-networking)。

## 設定監視
監視主要是作為用來檢查伺服器執行時間的資源，但也適用於知道何時需要進行調整。提供「標準監視」及「Nimsoft 監視」服務以涵蓋各種監視需求。「標準監視」（有時稱為「基本監視」）一般用於「Ping 並回應」方法，該方法是使用透過 {{site.data.keyword.cloud_notm}} 主控台所起始的慢速或服務 Ping。「Nimsoft 監視」也稱為「進階監視」，提供三個層級：「基本」、「進階」和「高階」。此服務也可以透過 {{site.data.keyword.cloud_notm}} 主控台進行存取。如需相關資訊，請參閱[監視](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring#monitoring)。

## 配置安全群組
您可以使用安全群組來限制虛擬伺服器上的網路資料流量。請使用安全群組來制定一組 IP 過濾器規則，以定義如何處理虛擬伺服器實例的公用和專用介面的送入及送出資料流量。如需相關資訊，請參閱[開始使用安全群組](/docs/infrastructure/security-groups?topic=security-groups-getting-started)。

## 配置防火牆
硬體防火牆也可用於提供更多保護。硬體防火牆是在無需關閉的情況下依需求進行佈建。如果適當地建立規則，防火牆可以防止伺服器發生不想要的活動。在您訂購防火牆之後，必須啟用防火牆，而且必須設定規則。

如需相關資訊，請參閱下列資訊。

* [硬體防火牆（共用）](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [硬體防火牆（專用）](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)

## 排定備份
備份確保資料安全地儲存在裝置外部，並防止其遺失。如果您需要將資訊重新載入至裝置，則可以使用下列備份服務將資料儲存到安全位置：
- {{site.data.keyword.backup_notm}} 是自動化的代理程式型備份系統。這是用於管理您裝置的常用「設定後即忘記」解決方案。它可透過額外的外掛程式與 Microsoft 軟體（包括 Exchange 及 SQL）相容。{{site.data.keyword.backup_notm}} 使用者是透過 {{site.data.keyword.backup_notm}} 的 WebCC Web 型應用程式與此服務互動。如需相關資訊，請參閱[開始使用 {{site.data.keyword.backup_notm}} 服務](/docs/infrastructure/Backup?topic=Backup-getting-started)。
- 「R1Soft 持續資料保護」是可安裝於伺服器或自行管理虛擬機器上的備份軟體。如果您要使用單一介面來管理所有備份，則建議使用它。您可以透過專有管理系統與 R1Soft CDP 互動，而此管理系統容許將代理程式安裝在虛擬機器上，並提供額外功能的資料庫外掛程式。如需相關資訊，請參閱[開始使用 {{site.data.keyword.backup_notm}} 服務](/docs/infrastructure/Backup?topic=Backup-getting-started)。

## 後續步驟
配置虛擬伺服器之後，即可開始進行管理。如需相關資訊，請參閱[管理虛擬伺服器](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)。
