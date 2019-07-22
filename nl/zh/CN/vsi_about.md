---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-29"

keywords: scalable virtual servers, virtual servers, key features

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 关于虚拟服务器
{: #about-virtual-servers}

{{site.data.keyword.BluVirtServers}} 是可缩放的虚拟服务器，随核心和内存分配一起购买。如果您在寻找的是能在几分钟内完成添加且有权访问映像模板等功能的计算资源，那么这是不错的选择。系统管理程序完全由 {{site.data.keyword.cloud_notm}} 管理，您可以使用 {{site.data.keyword.cloud_notm}} 控制台和 {{site.data.keyword.slapi_short}} 来执行配置和管理任务。虚拟服务器部署到与物理服务器相同的 VLAN，从而支持您跨虚拟服务器和裸机服务器分布工作负载，同时保持互操作性。虚拟服务器在您订购时可完全定制，并且随着您的计算需求增长，有多种选项可供扩展。
{:shortdesc}

创建虚拟服务器时，可以选择是公共（多租户）环境还是专用（单租户）环境。您可以选择是按小时还是按月计费，是高性能本地磁盘还是企业 SAN 存储器。

## 主要功能
以下信息列出了虚拟服务器随附的主要功能。

### 无缝集成
虚拟服务器会部署到裸机服务器和网络设备所在的 Pod 和网络。这让您能够灵活地将最佳技术用于每个工作负载。通常会在负载均衡器后面部署多个虚拟服务器以提供 Web 流量。这些服务器可以具有对裸机数据库服务器和其他更密集的工作负载的第 2 层专用网络直接访问权。

### 完全可定制
您可以使用若干选项来定制构建任何虚拟服务器。由于没有预定义的程序包需求，因此您可以调整每个服务器以适应其支持的工作负载。

### 快速供应
虚拟服务器在短短 5 分钟内就能完成供应，从而最大限度降低订购和供应之间的等待时间。

### 远程管理
与我们所有的服务和解决方案一样，您也能够远程管理虚拟服务器。使用 {{site.data.keyword.cloud_notm}} 控制台或 {{site.data.keyword.slapi_short}} 可查看和管理所有设备详细信息。还可以通过提供的 KVM 功能与服务器进行交互，或者通过公共或专用接口以完全管理控制权登录到服务器。

### 可轻松扩展
供应虚拟服务器后，可以快速、轻松地缩放或缩减您的实例，也可以根据需要添加或除去额外的实例。配置和调整服务器后，即可生成该服务器的映像模板，然后基于该原始映像来创建更多虚拟服务器。
