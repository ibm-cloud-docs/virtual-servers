---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-22"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 專用主機定價
{: #dedicated-virtual-server-pricing}

專用主機定價是以每小時及每月模型提供。
{:shortdesc}

當實例佈建至專用主機時，專用主機定價包括所有 vCPU、RAM、本端儲存空間，以及上行鏈路埠速度元件。如需定價的相關資訊，請參閱[虛擬伺服器佈建計算機 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}。

使用專用主機，會在第一個、第二個、第三個、第四個和第五個磁碟上提供其他本端儲存空間磁碟。每一個次要磁碟最多也會有 400 GB 的額外容量。

每小時實例可以佈建於每小時及每月主機。每月實例只能佈建於每月主機。

|主機配置           |vCPU	|RAM (GB) |本端儲存空間 (TB SSD)  |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |56 	|242    |        	1.2	          |
| 56x484x1.2         |56 	|   484    |          1.2           |
{: caption="表 1. 專用主機配置" caption-side="top"}

定價會隨著地區而改變。
{:note}

SAN（網路連接）、超值 OS 及軟體附加程式將會依實例按小時或按月收費（視專用主機上佈建的實例而定）。這些元件的定價與公用實例及專用實例上的現有供應項目一致。 

例如，具有下列配置的專用主機上所佈建的專用實例不會依實例收費。專用主機費用包含 vCPU、RAM、本端儲存空間及上行鏈路埠速度。 

* 8 vCPU
* 16 GB RAM
* 100 GB 本端 SSD 第一個磁碟
* 400 GB 本端 SSD 第二個磁碟
* 400 GB 本端 SSD 第三個磁碟
* 1 Gbps 公用及專用網路上行鏈路（專用主機） 

