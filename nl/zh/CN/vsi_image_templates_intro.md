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

# 映像模板
通过 {{site.data.keyword.BluVirtServers}} 映像模板，可以捕获设备的映像，以迅速复制其配置，而只需在订购过程中进行极少的更改。
{:shortdesc}

标准映像模板为所有 {{site.data.keyword.BluVirtServers_short}}（与操作系统无关）提供映像选项。通过标准映像模板，可以捕获现有虚拟服务器的映像，并基于捕获的映像来创建新映像。但是，标准映像模板与裸机服务器不兼容。

## 映像模板的工作方式
对于任何映像模板，两个主要操作是创建和部署。请求创建映像时，{{site.data.keyword.BluSoftlayer_full}} 的自动化系统会使服务器脱机。服务器处于脱机状态期间，将创建数据的压缩备份，记录配置信息，并将映像模板存储在 {{site.data.keyword.BluSoftlayer_notm}} SAN 上。在映像模板的部署阶段，自动化系统会根据从所选映像收集的数据来构造新服务器。部署过程会对卷进行调整，复原复制的数据，然后对新主机进行最终配置更改（例如，网络配置）。

## 专用映像

专用映像是用户在自己帐户上创建的映像，或是在其他帐户上创建并共享的映像。缺省情况下，创建的所有映像都是专用映像。 

## 公共映像

公共映像是由 {{site.data.keyword.BluSoftlayer_notm}} 发布或由客户公开且可供所有 {{site.data.keyword.BluSoftlayer_notm}} 客户使用的预先配置的机器。通过公用映像模板供应的虚拟服务器通常配置为使用各种配置规范的特定组合，以实现最佳性能。

有关映像模板的更多信息，请参阅[映像模板入门](/docs/infrastructure/image-templates/image_index.html)。
