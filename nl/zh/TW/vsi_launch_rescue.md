---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 啟動救援核心
{: #launching-rescue}

「救援核心」是一種即時救援環境，設計目的是要讓您可以將裸機伺服器或虛擬伺服器上線，以疑難排解一般只能透過「OS 重新載入」解決的系統問題。您必須在 {{site.data.keyword.cloud}} 主控台中起始「救援核心」。請使用下列步驟，以啟動裝置的「救援核心」。
{:shortdesc}

## 開始之前
首先，導覽至裝置功能表，並確定您具有完成作業所需的正確帳戶許可權。

* 導覽至主控台的裝置功能表。如需相關資訊，請參閱[導覽至裝置](/docs/vsi?topic=virtual-servers-navigating-devices)。
* 確保您具有任何必要的帳戶許可權及裝置存取權。只有帳戶擁有者或具有**管理使用者**標準基礎架構許可權的使用者才能調整許可權。

如需許可權的相關資訊，請參閱[傳統基礎架構許可權](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理裝置存取權](/docs/vsi?topic=virtual-servers-managing-device-access)。

## 啟動救援核心

1. 從**裝置**功能表，選取**裝置清單**。
2. 從**裝置清單**中，按一下您要救援的裝置名稱。
3. 在*動作*功能表中，選取**救援模式**。
4. 按一下**是**，立即將裝置轉移至「救援核心」。

## 啟動 Windows 實例的救援核心

1. 從**裝置**功能表，選取**裝置清單**。
2. 從**裝置清單**中，按一下您要救援的裝置名稱。
3. 在*動作*功能表中，選取**從映像檔開機**。
4. 選取公用映像檔 *WindowsRescueStandalone.iso* 旁的**從此映像檔開機**。

## 後續步驟
啟動「救援核心」之後，會關閉裝置電源，並將其重新開機到裝置作業系統的救援核心。這可能需要幾分鐘的時間。

您可以從裝置的 IP 位址遠端存取裝置。使用 {{site.data.keyword.cloud_notm}} 主控台中所記錄裝置的 root 或管理者認證，即可在「救援核心」中存取裝置。使用「救援核心」時，您可以疑難排解、探索問題以及解決問題，就像一般開機裝置一樣。必要的話，您可以將磁碟機裝載至「救援核心 OS」。若要結束「救援核心」，並將裝置還原成其一般環境，請在 {{site.data.keyword.cloud_notm}} 主控台中將裝置重新開機，或從「救援核心 OS」重新開機。

如需將裝置重新開機的相關資訊，請參閱[管理虛擬伺服器](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)。
