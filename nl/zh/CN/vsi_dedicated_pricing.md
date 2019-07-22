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

# 专用主机定价
{: #dedicated-virtual-server-pricing}

专用主机的定价将按每小时和每月模型提供。
{:shortdesc}

专用主机定价包括在专用主机上供应实例时的所有 vCPU、RAM、本地存储器和上行端口速度组成部分。有关定价的更多信息，请参阅[虚拟服务器供应计算器 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}。

对于专用主机，还将在第一个、第二个、第三个、第四个和第五个磁盘上提供附加本地存储器磁盘。此外，每个辅助磁盘上的额外容量最高达 400 GB。

每小时实例可在每小时和每月主机上供应。每月实例只能在每月主机上供应。

|主机配置|vCPU|RAM (GB)|本地存储器 (TB SSD)|
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |56|242|        	1.2|
| 56x484x1.2         |56|   484    |          1.2           |
{: caption="表 1. 专用主机配置" caption-side="top"}

价格因区域而异。
{:note}

根据在专用主机上供应的实例，SAN（网络连接）、高级操作系统和软件附加组件将根据实例按小时或按月收费。这些组件的定价与公共实例和专用实例上的现有产品一致。 

例如，对于在具有以下配置的专用主机上供应的专用实例，不会根据实例收费。vCPU、RAM、本地存储器和上行端口速度都包含在专用主机费用中。 

* 8 个 vCPU
* 16 GB RAM
* 100 GB 第一个本地 SSD 盘
* 400 GB 第二个本地 SSD 盘
* 400 GB 第三个本地 SSD 盘
* 1 Gbps 公用和专用网络上行链路（专用主机） 

