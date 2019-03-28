---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

keywords: public virtual servers, network traffic, virtual server deployment

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 关于公共虚拟服务器
{: #about-public-virtual-servers}

公共 {{site.data.keyword.BluVirtServers}} 产品是 IBM 管理的多租户虚拟服务器部署。通过这些产品，您可以利用满足所有业务需求的预定义大小来迅速进行扩展，并获得更高的成本效益，从而快速入门并熟练运用。  
{:shortdesc}

公共虚拟服务器有许多优点，包括：

* **全球可用性**

    公共虚拟服务器产品在全球各个数据中心内可用。

* **配置选项、快速部署和可扩展性**

    公用虚拟服务器产品为您提供了大大小小的虚拟服务器选项，可满足各种工作负载需求。

无法保证公共虚拟服务器（包括 VSI SAN 和其他网络连接存储器）的网络流量。如果某个虚拟服务器实例的网络流量开始对其他虚拟服务器产生严重的负面影响，那么可以在新主机上重新启动该实例，或者在极端情况下，可完全禁用该实例。在流量级别接近 20,000 到 30,000 个包/秒 (PPS) 时，通常会观察到这种负面影响。要获得有保证的网络连接，建议使用专用虚拟服务器产品。有关更多信息，请参阅单租户环境的[专用虚拟服务器](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers)产品。

公共实例位于与其他客户机共享的系统管理程序上；但是，处理器和内存为虚拟服务器专用，从而使服务器性能可靠。

提供了以下公共虚拟服务器。

|公共虚拟服务器|描述|
| ----------------------- | -------------------------------------------------------------------------------------------------------- |
|[均衡](/docs/vsi?topic=virtual-servers-balanced#balanced)|最适用于需要均衡性能和可扩展性的常用云工作负载。使用网络连接存储器。|
|[均衡本地存储器](/docs/vsi?topic=virtual-servers-balanced-local-storage#balanced-local-storage)|最适用于需要高流量、低延迟 I/O 性能的大型数据库集群。|
|[计算](/docs/vsi?topic=virtual-servers-compute#compute)|最适用于中到高 Web 流量工作负载。|
|[内存](/docs/vsi?topic=virtual-servers-memory#memory)|最适用于内存高速缓存和实时分析工作负载。
|
|[GPU](/docs/vsi?topic=virtual-servers-gpu#gpu)|最适用于高性能工作负载。
{: caption="表 1. 支持的公共虚拟服务器" caption-side="top"}

上述某些系列也可用于 IBM Cloud Virtual Server for VPC。有关更多信息，请参阅 [IBM Cloud Virtual Server for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen)。
{:tip}

## 后续步骤

复查并确定虚拟服务器类型模板之后，即可以供应公共虚拟服务器。首先，请查看以下信息：
1. [供应选择内容](/docs/vsi?topic=virtual-servers-provisioning-selections)
2. [供应公共实例](/docs/vsi?topic=virtual-servers-ordering-vs-public)
