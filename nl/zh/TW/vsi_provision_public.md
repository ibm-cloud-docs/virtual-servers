---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-17"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 佈建公用實例
{: #ordering-vs-public}

## 開始之前
您有兩個選項可以佈建公用虛擬伺服器實例。第一個是透過 {{site.data.keyword.cloud}} 主控台，第二個則是透過 {{site.data.keyword.slportal}}。主控台及 {{site.data.keyword.slportal}} 需要唯一登入 ID。您無法使用主控台使用者名稱和密碼來登入入口網站，反之亦然。
{:shortdesc}

對於 {{site.data.keyword.cloud_notm}} 主控台，您必須具有已升級的帳戶，才能訂購虛擬伺服器。如需升級帳戶的相關資訊，請參閱[隨收隨付制帳戶](/docs/account?topic=account-accounts#paygo)。
{:note}

開始之前，請檢閱下列必要條件。

  1. 檢閱可供您使用的部署選項。如需相關資訊，請參閱[公用虛擬伺服器](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)。

  2. 檢閱虛擬伺服器實例容量考量。如需相關資訊，請參閱[虛擬伺服器實例的資源考量](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations)。
  
  3. 從 {{site.data.keyword.cloud_notm}} 主控台開啟[虛擬伺服器實例 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} 頁面。

## 佈建公用虛擬伺服器實例  
{: #ordering-public-instance}

若要佈建虛擬伺服器實例，您需要考量下列資訊。

您必須登入才能查看所有可用的選項。
{:tip}

### 公用實例

|欄位|詳細資料     |
| -------- | ----------- |
| 計費                      |根據您的虛擬伺服器實例，選取按小時或按月計費。主要差異（而非成本）在於每小時實例不包含頻寬配置。在計費週期結束時，會計算每一個實例作用於帳戶上的頻寬用量和小時數。例如，如果您在 10 天之後取消每小時實例，則只需支付那 10 天的時數費用。如果您在 10 天之後取消每月實例，則需支付整個月的費用。如果您對暫停計費特性有興趣（只能在每小時實例上使用），請參閱[關於暫停計費](/docs/vsi?topic=virtual-servers-about-suspend-billing)。|
|主機名稱|可以包含由英數字元和橫線所構成的標籤，並以句點區隔。標籤不能只含數字、以橫線為開頭或結尾，也不能有連續的橫線或句點。|
|網域|必須有兩個以上的標籤，標籤可以由英數字元和橫線所構成，並以句點區隔。標籤不能以橫線為開頭或結尾，也不能有連續的橫線或句點。最後一個標籤只能是字母。|
|放置群組|您可以選取實例的放置群組。如果您新增放置群組，則「分散」規則表示實例位於不同的實體硬體上。如需相關資訊，請參閱[放置群組](/docs/vsi?topic=virtual-servers-placement-groups)。|
|位置|位置是由地區（特定地理區域）和區域（地區內的容錯資料中心）所組成。選取要在其中建立虛擬伺服器實例的位置。|
|熱門設定檔|考慮從支援最常見之使用案例的熱門設定檔配置中選取。這些設定檔包含預先配置的實例，這些實例在幾分鐘內即可備妥使用。|
|所有設定檔|如需公用實例之可用設定檔選項的相關資訊，請參閱[公用虛擬伺服器](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)。|
|SSH 金鑰|SSH 金鑰容許您存取實例，而不需對實例上實作的每一個公開金鑰使用來自對應用戶端的密碼。如果您決定新增 SSH 金鑰，請提供 SSH 金鑰的公開金鑰，您可以在佈建金鑰之後，用它來登入實例。|
|映像檔|映像檔是實例的已部署作業系統。您可以選取一些免費選項（例如 CentOS 及 Ubuntu）。也可以使用付費選項（例如 Windows Server 及 Red Hat Enterprise Linux (RHEL)）。請務必注意，Windows 需要 100 GB 主要磁碟。|
{: caption="表 1. 公用實例選項" caption-side="top"}

### 公用實例附加程式 

如果您選擇任何 OS、控制台或軟體附加程式，則它們必須與您的映像檔相容，以避免在訂購實例時發生錯誤。例如，您無法使用 Microsoft 資料庫來佈建 RedHat 映像檔。
{:important}

|欄位|詳細資料     |
| --------- | ----------- |
|OS 附加程式|如果您選取按月計費，則可以選取下列映像檔附加程式：<br><br> **R1Soft Server Backup Manager** 提供高效能磁碟對磁碟伺服器備份，以及中央管理與資料儲存庫。如果您選取 R1Soft 附加程式，則必須購買 R1Soft Backup Agent 套件，這是**服務**區段中的 CDP 附加程式。選取一項而未選取另一項，會導致您的訂單發生錯誤。如需 R1Soft 和 IBM Cloud 的相關資訊，請參閱 [R1Soft Server Backup Manager ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/cloud/backup-and-restore?mhq=R1Soft%20Server%20Backup%20Manager&mhsrc=ibmsearch_a){: new_window}。<br><br>**Veeam Backup and Replication** 可結合自動化備份，以及還原與抄寫功能。Veeam 也提供進階監視、報告及產能規劃。如需 Veeam Backup and Replication 的相關資訊，請參閱 [Veeam Backup and Replication 與 IBM 儲存空間 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www-356.ibm.com/partnerworld/gsd/solutiondetails.do?solution=54724&lc=en&stateCd=P&tab=2){: new_window}。<br><br>**VMware vCenter** 可自動部署您需要的基礎 VMware vSphere 和 VMware vCenter Server 層，以取得彈性且可自訂的 VMware 解決方案。如需 vCenter on IBM Cloud 的相關資訊，請參閱[關於 vCenter Server on IBM Cloud ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/downloads/cas/L7RKPZND?mhq=vmware%20vcenter&mhsrc=ibmsearch_a){: new_window}。|
|控制台軟體|如果您選取按月計費，則可以新增控制台，以進行 Web 管理。|
|資料庫軟體|您可以選取要安裝的資料庫軟體。{{site.data.keyword.cloud_notm}} 支援任何在佈建過程中部署的資料庫軟體。您也可以在部署伺服器之後安裝自己的資料庫軟體。|
|服務|系統會自動為您選取部分服務，取決於您的計費和映像檔選項。您可以從實例的任何其餘服務附加程式中選擇。|
|佈建 Script|佈建 Script 一般用來將客戶特定配置套用至伺服器，以及協助調整策略的自動化。佈建 Script 可以是作業系統 (OS) 可執行的任何檔案，包括結合的二進位檔或任何 OS 支援的語言。佈建 Script 無法用於 cloud-init 映像檔。如需相關資訊，請參閱[佈建 Script](/docs/vsi?topic=virtual-servers-provisioning-scripts)。|
|使用者資料|您可以新增使用者資料，以自動執行一般配置作業或執行 Script。使用者資料可以用於 cloud-init 和 non-cloud-init 映像檔。|
{: caption="表 2. 公用實例附加程式" caption-side="top"}

### 附加的儲存空間磁碟

如果您需要額外儲存體，則可以將儲存空間磁碟連接至實例。可供您使用的儲存空間磁碟類型取決於您選取的設定檔。例如，平衡的本端設定檔和少數 GPU 設定檔會使用本端支援的磁碟。如果您選取按月計費，則可以新增 {{site.data.keyword.backup_notm}}，並選擇最適合您需求的選項。如需相關資訊，請參閱 [{{site.data.keyword.backup_notm}} 服務](/docs/infrastructure/Backup?topic=Backup-getting-started)。

### 網路介面

|欄位|詳細資料     |
| -------- | ----------- |
|上行鏈路埠速度|您可以選取實例的上行鏈路速度，最多 1 GB/秒。這些虛擬上行鏈路是透過 IBM 公用及專用網路的備援實體上行鏈路所支援。在訂購時，公用及專用速度一律會相同，而且可以視需要選擇升級或降級鏈結。|
|專用和公用安全群組|您可以使用安全群組來制定一組 IP 過濾器規則，以定義如何處理實例的公用和專用介面的送入及送出資料流量。如需相關資訊，請參閱[關於 IBM 安全群組](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups)。|
|專用和公用 VLAN|依預設，您的虛擬伺服器實例會放置在自動指派的 VLAN 上。如果您在選取的資料中心已有一個 VLAN，則可以選擇不同的 VLAN。如需相關資訊，請參閱[關於 VLAN](/docs/infrastructure/vlans?topic=vlans-about-vlans)。|
|專用和公用子網路|選取子網路是選用的，而且只有在您需要裝置使用子網路中的 IP 位址時才能使用。如果您選取子網路，請驗證您有足夠的 IP 位址可滿足要求。如果您的子網路沒有足夠的 IP 位址，則可能會延遲或取消訂單。
如需相關資訊，請參閱[關於子網路和 IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips)。|
{: caption="表 3. 網路介面選項" caption-side="top"}

### 網路介面附加程式

|欄位|詳細資料     |
| -------- | ----------- |
|頻寬|具有公用上行鏈路的每月實例隨附 250 GB。與超額使用費率相較之下，您可以使用較少的成本來購買較大的配置。|
|軟硬體防火牆|防火牆服務可防止伺服器上不需要的資料流量、減少攻擊可能性，以及容許伺服器資源專用於其預期用途。|
|主要 IP 位址|主要 IP 位址會自動指派給您的實例。|
|公用次要 IP 位址|這些子網路在虛擬伺服器實例的持續時間由您所擁有。您可以單獨取消子網路，但是如果您取消實例，則也會移除子網路。如需相關資訊，請參閱[關於子網路及 IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips)。|
|IPv6 和公用靜態 IPv6 位址|您可以為實例選取 IPv6 位址或公用靜態 IPv6 位址。|
|VPN 管理|對於具有無限 SSL VPN 使用者的實例，會自動為其選取此選項。如需相關資訊，請參閱[關於 VPN](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn)。|
{: caption="表 4. 網路介面附加程式" caption-side="top"}


## 透過客戶入口網站佈建公用實例
若要透過 {{site.data.keyword.slportal}} 佈建公用虛擬伺服器實例，請完成下列步驟：

  1. 使用唯一認證來登入 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window}。
  2. 找到**訂單**區段，然後按一下**裝置**。
  3. 在「裝置」頁面上，針對其中一個「虛擬伺服器」供應項目，按一下**每小時 SAN**、**每小時本端**、**每月**或**暫時性**。
  4. 在*配置雲端伺服器* 頁面上，完成所有相關資訊。
  5. 按一下**新增至訂單**以繼續。
  6. 確認或編輯伺服器的網域資訊。
  7. 按一下**雲端服務條款**及**協力廠商服務合約**勾選框。
  8. 確認或輸入您的付款資訊，然後按一下**提交訂單**。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

## 後續步驟
將一系列的電子郵件傳送給管理者：佈建訂單確認、佈建訂單核准和處理，以及佈建完成。在您登入 {{site.data.keyword.Bluemix_notm}} 之後，佈建完成電子郵件會包含*裝置詳細資料* 頁面的鏈結。

虛擬伺服器在佈建且可供使用之後，即可使用 {{site.data.keyword.cloud_notm}} 主控台或 {{site.data.keyword.slapi_short}} 來配置虛擬伺服器。如需相關資訊，請參閱[配置虛擬伺服器](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers)。
