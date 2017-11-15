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


# 啟動救援核心 
{: #launching-rescue}

「救援核心」是一種即時救援環境，設計目的是要讓客戶可以將裸機伺服器或虛擬伺服器上線，以疑難排解一般只能透過「OS 重新載入」解決的系統問題。您必須在 {{site.data.keyword.slportal_full}} 上起始「救援核心」。請使用下列步驟，以啟動裝置的「救援核心」。
{:shortdesc}

## 啟動救援核心

1. 使用唯一認證來存取 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/)。
2. 從「裝置清單」中，按一下您要救援的裝置名稱。
3. 按一下右上角的*動作* 下拉清單，然後選取**救援**。
4. 按一下**是**按鈕，以立即將裝置轉移至「救援核心」。按一下**否**按鈕，以取消動作。

## 後續步驟
啟動「救援核心」之後，會關閉裝置電源，並將其重新開機到裝置作業系統的救援核心。這可能需要幾分鐘的時間。

您可以從裝置的 IP 位址遠端存取裝置。使用 {{site.data.keyword.slportal}} 上所記錄裝置的 root 或管理者認證，即可在「救援核心」中存取裝置。使用「救援核心」時，您可以疑難排解、探索問題以及解決問題，就像一般開機裝置一樣。必要的話，您可以將磁碟機裝載至「救援核心 OS」。若要結束「救援核心」，並將裝置還原成其一般環境，請在 {{site.data.keyword.slportal}} 中將裝置重新開機，或從「救援核心 OS」重新開機。

如需將裝置重新開機的相關資訊，請參閱[管理虛擬伺服器](../vsi/vsi_managing.html)。

