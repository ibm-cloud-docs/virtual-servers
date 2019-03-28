---

copyright:
  years: 2014, 2018
lastupdated: "2018-10-18"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# 佈建 Script
{: #provisioning-scripts}

佈建 Script 是一種可在佈建處理程序期間下載至裝置或在裝置上下載並執行的 Script。針對現有帳戶，佈建 Script 是在 {{site.data.keyword.slportal_full}} 內管理。在訂購處理程序期間，您可以手動輸入新帳戶的 Script，或尚未追蹤的 Script。

或者，您可以使用啟用 cloud-init 的映像檔，並提供使用者資料以自動執行配置作業或執行 Script。如需相關資訊，請參閱[使用啟用 cloud-init 的映像檔進行佈建](/docs/infrastructure/image-templates?topic=image-templates-provisioning-with-a-cloud-init-enabled-image#provisioning-with-a-cloud-init-enabled-image)。
{: tip}

在佈建處理程序期間，會將與 HTTP URL 相關聯的佈建 Script 下載至裝置。佈建之後，管理者必須在裝置上手動執行 Script。會自動下載及執行與 HTTPS URL 相關聯的 Script。標準 Linux 作業系統（Cent、RHEL、Fedora、Debian 或 Ubuntu）以及 Windows 和 FreeBSD 目前都提供佈建 Script。不支援其他系統（例如 Vyatta、Netscaler、XenServer、VMware）。佈建 Script 可以是作業系統所執行之任何類型的檔案（包括結合的二進位檔或任何 OS 支援的語言）。

如需相關資訊，請參閱[管理佈建 Script](/docs/vsi?topic=virtual-servers-managing-a-provisioning-script)。
