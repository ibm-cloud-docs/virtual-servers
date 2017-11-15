---



copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 映像檔範本
使用 {{site.data.keyword.BluVirtServers}} 映像檔範本，即可擷取裝置的映像檔來快速抄寫其配置，而且訂購處理程序中的變更最少。
{:shortdesc}

不論作業系統為何，標準映像檔範本都會提供所有 {{site.data.keyword.BluVirtServers_short}} 的映像選項。標準映像檔範本可讓您擷取現有虛擬伺服器的映像檔，以及根據所擷取的映像檔來建立新的映像檔。標準映像檔範本與裸機伺服器不相容。

## 映像檔範本運作方式
任何映像檔範本的兩個主要動作都是建立及部署。當您要求建立映像檔時，{{site.data.keyword.BluSoftlayer_full}} 的自動化系統會讓您的伺服器離線。伺服器離線時，就會建立資料的壓縮備份，並記錄配置資訊，然後將映像檔範本儲存至 {{site.data.keyword.BluSoftlayer_notm}} SAN。在映像檔範本的部署階段期間，自動化系統會根據從所選映像檔收集的資料，建構新的伺服器。部署程序會對磁區進行調整、還原複製的資料，然後對新主機進行最終配置變更（例如，網路配置）。

## 專用映像檔

專用映像檔是帳戶上的使用者所建立的映像檔，或是在另一個帳戶上建立並共用的映像檔。依預設，建立的所有映像檔都是專用映像檔。 

## 公用映像檔

公用映像檔是預先配置的機器，這些機器由 {{site.data.keyword.BluSoftlayer_notm}} 張貼，或由客戶公開，並且可供所有 {{site.data.keyword.BluSoftlayer_notm}} 客戶使用。透過公用映像檔範本佈建的虛擬伺服器一般會針對最佳效能而配置，並且會有各種配置規格的特定組合。

如需映像檔範本的相關資訊，請參閱[開始使用映像檔範本](/docs/infrastructure/image-templates/image_index.html)。
