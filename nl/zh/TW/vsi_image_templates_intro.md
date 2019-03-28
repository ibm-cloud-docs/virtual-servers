---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 映像檔範本
{: #image-templates}

使用 {{site.data.keyword.BluVirtServers}} 映像檔範本，即可擷取裝置的映像檔來快速抄寫其配置，而且訂購處理程序中的變更最少。
{:shortdesc}

不論作業系統為何，映像檔範本都會提供所有 {{site.data.keyword.BluVirtServers_short}} 的映像選項。映像檔範本可讓您擷取現有虛擬伺服器的映像檔，並根據所擷取的映像檔來建立新的虛擬伺服器。映像檔範本與裸機伺服器不相容。

## 映像檔範本運作方式
任何映像檔範本的兩個主要動作都是建立及部署。當您要求建立映像檔時，{{site.data.keyword.BluSoftlayer_full}} 的自動化系統會讓您的伺服器離線。伺服器離線時，就會建立資料的壓縮備份，並記錄配置資訊，然後將映像檔範本儲存至 {{site.data.keyword.BluSoftlayer_notm}} SAN。在映像檔範本的部署階段期間，自動化系統會根據從所選映像檔收集的資料，建構新的伺服器。部署程序會對磁區進行調整、還原複製的資料，然後對新主機進行最終配置變更（例如，網路配置）。

如需映像檔範本的相關資訊，請參閱[開始使用映像檔範本](/docs/infrastructure/image-templates?topic=image-templates-getting-started-with-image-templates)。
