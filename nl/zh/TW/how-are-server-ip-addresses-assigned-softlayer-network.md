---

copyright:
  years: 2018
lastupdated: "2018-08-01"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 指派伺服器 IP 位址
{: #assigning-server-ip-addresses}

{{site.data.keyword.cloud}} 會使用在專用網路上的 IPv4 位址，以及在要求時使用公用（面對網際網路）IPv4 位址，來配置虛擬伺服器實例。此外，您可以在公用網路上要求 IPv6 位址。所有這些 IP 位址統稱為_主要 IP 位址_。
{:shortdesc}

透過 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com) 購買次要子網路之後，可以將其他 IP 位址連結至虛擬伺服器實例。使用此方式購買且由您管理的 IP 位址稱為_次要 IP 位址_。

如需獲得 IP 位址之可用選項的相關資訊，請參閱[子網路及 IP](https://console.bluemix.net/docs/infrastructure/subnets/)。

## 連結次要 IP 位址

購買及遞送次要子網路之後，您必須配置作業系統使用一個以上剛剛可用的 IP 位址。每個作業系統的新 IP 位址配置步驟都不同，但這項設定一般稱為是在設定「介面別名」。如需其他配置詳細資料，請參閱作業系統文件。
