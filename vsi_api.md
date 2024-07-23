---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-23"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# API reference overview
{: #api-reference}

The {{site.data.keyword.slapi_full}} is the development interface that gives developers and system administrators direct interaction with {{site.data.keyword.cloud_notm}} backend system. The {{site.data.keyword.slapi_short}} powers many of the features in the {{site.data.keyword.cloud_notm}} console, which typically means if an interaction is possible in the {{site.data.keyword.cloud_notm}} console, it can also be run in the API. Because you can programmatically interact with all portions of the {{site.data.keyword.cloud_notm}} environment within the API, {{site.data.keyword.slapi_short}} can automate tasks. For example, you can use the `SoftLayer_Virtual_Guest/createObject` API to deploy a virtual server instance.
{: shortdesc}

The {{site.data.keyword.slapi_short}} is a Remote Procedure Call system. Each call involves sending data to an API endpoint and receiving structured data in return. The format that is used to send and receive data with the {{site.data.keyword.slapi_short}} depends on which implementation of the API you choose. The {{site.data.keyword.slapi_short}} currently uses SOAP, XML-RPC, or REST for data transmission.

For more information about the {{site.data.keyword.slapi_short}} and virtual server APIs, see the following resources in the {{site.data.keyword.sldn_full}}:

* [{{site.data.keyword.slapi_short}} Overview](https://sldn.softlayer.com/reference/softlayerapi/){: external}
* [Getting Started with the {{site.data.keyword.slapi_short}}](https://sldn.softlayer.com/article/getting-started/){: external}
* [API Reference: Virtual_Guest::createObject](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/createObject/){: external}
* [API Reference: Product_Order::placeOrder](https://sldn.softlayer.com/reference/services/SoftLayer_Product_Order/placeOrder/){: external}

For API usage examples, see the following resources:

* [Understanding and building an order by using the {{site.data.keyword.slapi_short}} order CLI](https://sldn.softlayer.com/article/understanding-ordering/){: external}
* [{{site.data.keyword.slapi_short}} Examples - Release Notes](https://sldn.softlayer.com/){: external}
* [Python examples](https://sldn.softlayer.com/python/){: external}

## Dedicated virtual servers usage examples
{: #dedicated-virtual-servers-usage-examples}

* [Virtual_DedicatedHost API examples](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_DedicatedHost/){: external}

## Public virtual servers usage examples
{: #public-virtual-servers-usage-examples}

* [Virtual_guest API examples](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/){: external}
