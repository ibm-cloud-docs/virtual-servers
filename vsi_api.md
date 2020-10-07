---

copyright:
  years: 2017, 2020
lastupdated: "2020-03-20"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# API reference overview
{: #api-reference}

The {{site.data.keyword.slapi_full}} is the development interface that gives developers and system administrators direct interaction with {{site.data.keyword.cloud_notm}} backend system. The {{site.data.keyword.slapi_short}} powers many of the features in the {{site.data.keyword.cloud_notm}} console, which typically means if an interaction is possible in the {{site.data.keyword.cloud_notm}} console, it can also be run in the API. Because you can programmatically interact with all portions of the {{site.data.keyword.cloud_notm}} environment within the API, {{site.data.keyword.slapi_short}} enables you to automate tasks. For example, you can use the *SoftLayer_Virtual_Guest/createObject* API to deploy a virtual server instance.
{:shortdesc}

The {{site.data.keyword.slapi_short}} is a Remote Procedure Call system. Each call involves sending data towards an API endpoint and receiving structured data in return. The format used to send and receive data with the {{site.data.keyword.slapi_short}} depends on which implementation of the API you choose. The {{site.data.keyword.slapi_short}} currently uses SOAP, XML-RPC or REST for data transmission.

For more information about the {{site.data.keyword.slapi_short}} and virtual server APIs, see the following resources in the {{site.data.keyword.sldn_full}}:
* [{{site.data.keyword.slapi_short}} Overview](https://softlayer.github.io/reference/softlayerapi/){: external}
* [Getting Started with the {{site.data.keyword.slapi_short}}](https://softlayer.github.io/article/getting-started/){: external}
* [API Reference: SoftLayer_Virtual_Guest::createObject](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/){: external}
* [API Reference: SoftLayer_Product_Order::placeOrder](https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/){: external}

For API usage examples, see the following resources:
* [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI](https://softlayer.github.io/article/understanding-ordering/){: external}
* [{{site.data.keyword.slapi_short}} Examples - Release Notes](https://softlayer.github.io/){: external}
* [Python examples](https://softlayer.github.io/python/){: external}

## Dedicated virtual servers usage examples
{: #dedicated-virtual-servers-usage-examples}

* [SoftLayer_Virtual_DedicatedHost API examples](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_DedicatedHost/){: external}

## Public virtual servers usage examples
{: #public-virtual-servers-usage-examples}

* [softlayer_virtual_guest API examples](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/){: external}