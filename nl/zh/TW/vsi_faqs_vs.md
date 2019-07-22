---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-09"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# 常見問題：虛擬伺服器  
{: #faqs-virtual-servers}

## 哪些類型的虛擬伺服器可供使用？
{: faq}
{{site.data.keyword.BluSoftlayer_full}} 在其「標準基礎架構」內提供幾種類型的虛擬伺服器。標準供應項目是適用於各種需求的公用型虛擬伺服器（即多方承租戶環境）。如果您要尋找單一承租戶環境，請考慮使用「專用虛擬伺服器」供應項目。專用虛擬伺服器選項適用於具有更嚴格資源需求的應用程式。如需現行虛擬伺服器供應項目的相關資訊，請參閱[開始使用虛擬伺服器](/docs/vsi?topic=virtual-servers-getting-started-with-virtual-servers#getting-started-with-virtual-servers)。

IBM Cloud 提供「Virtual Private Cloud (VPC) 基礎架構」，它是新一代雲端平台。您可以在 {{site.data.keyword.cloud_notm}} 中建立自己的空間，以使用 VPC 在公用雲端內執行隔離的環境。VPC 提供專用雲端的安全，以及公用雲端的靈活性和易用性。如需相關資訊，請參閱[關於 Virtual Private Cloud](https://cloud.ibm.com/docs/vpc-on-classic?topic=vpc-on-classic-about)。

## 我可以在哪裏找到公用實例類型的定價資訊？
{: faq}

如需相關資訊，請參閱[建置虛擬伺服器 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/cloud/virtual-servers){: new_window}。

## 我可以在哪裏找到虛擬公用實例的定價資訊？
{: faq}

預估 {{site.data.keyword.cloud_notm}} 伺服器支援工作負載的成本開始於 [{{site.data.keyword.cloud_notm}} 型錄](https://cloud.ibm.com/catalog)。從型錄中，選取**計算**，然後選擇伺服器類型 - Bare Metal Server、「虛擬伺服器」或 Virtual Server for VPC (Virtual Private Cloud)。如需定價資訊，請參閱[虛擬伺服器佈建計算機 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}。

## 是否可以將磁碟儲存空間新增至我的每小時或每月虛擬伺服器？
{: faq}

您可以升級或降級任何虛擬伺服器的磁碟儲存空間，方法是在您要更新之裝置的*配置* 畫面的*第一個硬碟* 到*第五個硬碟* 欄位中更新儲存空間選項。如需相關資訊，請參閱[重新配置現有虛擬伺服器](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers)。

## 我可以啟動多少部每小時虛擬伺服器？
{: #concurrent}
{: faq}

您可以執行的實例數目取決於帳戶的成熟度層次。依預設，超過 45 天的帳戶在任何時間都有 20 個實例的限制，而這些實例可以在公用虛擬伺服器、專用虛擬伺服器及裸機伺服器上執行。較新的帳戶具有較小的限制。如果您要增加限制，請與支援中心聯絡，進一步告訴我們您正在執行的作業以及您可能需要的並行實例數目。

## 如何計算我的每小時虛擬伺服器頻寬的費用？
{: faq}

每小時虛擬計費會細分為入埠及出埠資料流量。虛擬伺服器的所有入埠資料流量都是免費的。出埠資料流量是按 GB 進行計量及收費，並在計費期間結束時估算出總計。

## 我的虛擬伺服器在什麼情況下會移轉至不同主機？
{: faq}

在有限的情況下，虛擬伺服器可能需要移轉至不同的主機。如果需要移轉，虛擬伺服器會先關閉、移轉，然後再重新啟動。在下列情況下，可能會移轉虛擬伺服器：

* 需要更新 Hypervisor、主機正在解除任務，或不容許主機承擔新的實例。如果主機標示要進行任何上述變更，當其中一部虛擬伺服器從 {{site.data.keyword.cloud_notm}} 主控台重新啟動時，重新開機會自動觸發，讓虛擬伺服器移轉至不同的主機。
* 基礎架構維護。您可能收到電子郵件，指出需要在管理您的虛擬伺服器的系統上進行維護。在基礎架構維護時，您的虛擬伺服器可能需要移轉。
* 現有實例升級。為了讓效能一致，如果您升級實例，它可能會移轉至不同的主機，以確保它收到適當的專用 CPU 及記憶體。
* 專用主機失敗。專用實例會移轉至另一個空的主機，而不使用您可能具有的任何現有容量。

在維護時間範圍內，您可能會看到**移轉主機**選項顯示在 {{site.data.keyword.cloud_notm}} 主控台中您裝置的**動作**功能表中。**移轉主機**可讓您在指定的維護期間，在您方便時將虛擬伺服器移轉至新的主機。如果在維護期間未起始移轉，則會自動移轉虛擬伺服器，以完成所需的維護。**移轉主機**選項不會持續保存，並且只能在透過維護通知傳達的維護期間使用。

如果您的其中一個虛擬伺服器需要的特定 Hypervisor 層次無法在現行主機上使用，您也可能看到**移轉主機**選項。

## 刪除我的可攜式儲存空間時，我的資料會發生什麼情況？
{: faq}

刪除儲存空間時，會移除該磁區上資料的任何指標，因此，資料會變成無法存取。如果將實體儲存空間重新佈建至另一個帳戶，則會指派一組新的指標。新的帳戶沒有方法可以存取任何可能已在實體儲存空間上的資料。這組新的指標全部顯示 0。將新的資料寫入至磁區/LUN 時，會改寫仍然存在的任何無法存取資料。

## 我可以使用 Red Hat Cloud Access 訂閱來建立虛擬伺服器嗎？
{: faq}

可以。匯入映像檔時，您可以指定將提供作業系統授權。如需相關資訊，請參閱[使用 Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription#using-your-own-os-license-or-subscription)。接下來您可以從該映像檔範本訂購虛擬伺服器，並使用現有的 [Red Hat Cloud Access ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} 訂閱。

## 虛擬伺服器與虛擬專用伺服器 (VPS) 之間的差異為何？
{: faq}

虛擬伺服器與您可能已熟悉的虛擬專用伺服器 (virtual private server, VPS) 或虛擬專用伺服器 (virtual dedicated server, VDS) 平台類似。這些「虛擬伺服器」環境容許在單一硬體節點上以專用且安全地方式佈建不同的環境，但 VDS 及 VPS 的功能較為受限。VPS 及 VDS 選項一般侷限於單一伺服器架構。只有可在 VDS 或 VPS 的每一部虛擬伺服器之間新增或分配的資源，才是在該單一伺服器上實際安裝的資源。

虛擬伺服器是佈建於多部伺服器雲端架構上，而此架構儲存要使用之個別實例的所有可用硬體資源。虛擬伺服器可以使用共用的高容量 SAN 型主要儲存空間平台或高效能本端磁碟儲存空間。因為每一個實例都是較大型雲端環境的一部分，所以所有虛擬伺服器之間的通訊都是即時的。

## 我在佈建虛擬伺服器時為什麼收到容量錯誤？
{: faq}

當您佈建虛擬伺服器時，可能會收到錯誤訊息，指出容量不足，無法完成要求。佈建失敗時，特定要求內的所有虛擬伺服器實例都會失敗。路由器或資料中心內的可用資源不足而無法滿足服務要求時，發生容量錯誤。您可能會收到此錯誤的原因有很多。資源可用性會經常變更，因此您可能需要等待，然後再試一次。如需避免此錯誤的策略相關資訊，請參閱[虛擬伺服器實例的容量考量](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations)。

## 如何登入我的伺服器？
{: faq}

登入主控台，導覽至**裝置**功能表。如需相關資訊，請參閱[導覽至裝置](/docs/vsi?topic=virtual-servers-navigating-devices)。在**裝置清單**中，選取您的實例。您可以檢視及管理要用來登入的裝置使用者名稱和密碼。如需相關資訊，請參閱[檢視及管理裝置使用者名稱和密碼](https://test.cloud.ibm.com/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device)。 

## 如何使用 VPN 來存取 IBM Cloud 專用網路？
{: faq}

您可以透過 [Web 介面](https://www.softlayer.com/VPN-Access){: external}登入 VPN，或使用 Linux、macOS 或 Windows 的[獨立式 VPN 用戶端](/docs/infrastructure/iaas-vpn?topic=VPN-standalone-vpn-clients)。如需在連接至 VPN 之後要執行哪些動作的相關資訊，請參閱[使用 SSL VPN](/docs/infrastructure/iaas-vpn?topic=VPN-use-ssl-vpn)。

## 如何重新啟動我的虛擬伺服器？
{: faq}

裝置重新開機可以從**裝置清單**或從個別實例的 Snapshot 視圖中執行。在主控台的**裝置清單**中，導覽至您的虛擬伺服器實例。如需相關資訊，請參閱[導覽至裝置](/docs/vsi?topic=virtual-servers-navigating-devices)。針對您要管理的裝置選取**動作**，然後選取**重新開機**。

## 如何使用「救援核心」？
{: faq}

如果您遇到伺服器問題，則開機至「救援核心」很有用。若要啟動「救援核心」，請從主控台的**裝置清單**中選取裝置名稱。在**動作**功能表中，選取**救援模式**，或針對 Windows 實例選取**從映像檔開機**。如需相關資訊，請參閱[啟動救援核心](/docs/vsi?topic=virtual-servers-launching-rescue)。

## 在何處尋找網路狀態？
{: faq}

您可以直接在 [{{site.data.keyword.cloud_notm}} - 狀態](https://cloud.ibm.com/status){: external}中存取**狀態**頁面，以檢視所有 {{site.data.keyword.cloud_notm}} 位置中的資源現行狀態。您可以藉由選取特定元件和位置來過濾清單（例如，您可以選取「虛擬伺服器」並檢視網路連線功能）。

## 如何要求相符性報告？
{: faq}

如需檢視或要求相符性資訊（包括 SOC 報告）的相關資訊，請參閱[如何知道我的資料是否安全？](/docs/overview?topic=overview-security)

