---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# API 参考概述
{: #api-reference}

{{site.data.keyword.slapi_full}}是供开发者和系统管理员与 {{site.data.keyword.cloud_notm}} 后端系统进行直接交互的开发接口。{{site.data.keyword.slapi_short}} 支持 {{site.data.keyword.cloud_notm}} 控制台中的许多功能，这通常意味着如果某个交互可以在 {{site.data.keyword.cloud_notm}} 控制台中执行，那么也可以在此 API 中运行。由于在 API 中可以通过编程方式与 {{site.data.keyword.cloud_notm}} 环境的所有部分进行交互，所以 {{site.data.keyword.slapi_short}} 支持自动执行任务。例如，可以使用 *SoftLayer_Virtual_Guest/createObject* API 来部署虚拟服务器实例。
{:shortdesc}

{{site.data.keyword.slapi_short}} 是一种远程过程调用系统。每个调用都涉及向 API 端点发送数据以及接收所返回的结构化数据。通过 {{site.data.keyword.slapi_short}} 发送和接收数据时所使用的格式将取决于您所选择的 API 实现。{{site.data.keyword.slapi_short}} 当前使用 SOAP、XML-RPC 或 REST 进行数据传输。

有关 {{site.data.keyword.slapi_short}} 和虚拟服务器 API 的更多信息，请参阅 {{site.data.keyword.sldn_full}}中的以下资源：
* [{{site.data.keyword.slapi_short}} 概述 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/reference/softlayerapi/){: new_window}
* [ {{site.data.keyword.slapi_short}} 入门 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/article/getting-started/){: new_window}
* [API 参考：SoftLayer_Virtual_Guest::createObject ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/){: new_window}
* [API 参考：SoftLayer_Product_Order::placeOrder ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/){: new_window}

有关 API 用法示例，请参阅以下资源：
* [通过使用 {{site.data.keyword.slapi_short}} 订单 CLI 了解和构建订单 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/article/understanding-ordering/){: new_window}
* [{{site.data.keyword.slapi_short}} Python 客户机：使用虚拟服务器 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [{{site.data.keyword.slapi_short}} 示例 - 发行说明 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/){: new_window}
* [Python 示例 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/python/){: new_window}

## 专用虚拟服务器用法示例
* [获取专用主机分配 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/python/getDediHostAllocation/){: new_window}
* [获取专用主机访客 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/python/getDedicatedHostGuests/){: new_window}
* [在专用主机之间迁移虚拟服务器实例 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/python/migrateDedicatedHost.py/){: new_window}

## 公共虚拟服务器用法示例
* [softlayer_virtual_guest API 示例 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
