---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# API reference
{: #api-reference} 

The {{site.data.keyword.slapi_full}} is the development interface that gives developers and system administrators direct interaction with {{site.data.keyword.cloud}} backend system. The {{site.data.keyword.slapi_short}} powers many of the features in the {{site.data.keyword.slportal_full}}, which typically means if an interaction is possible in the {{site.data.keyword.slportal}}, it can also be run in the API. Because you can programmatically interact with all portions of the {{site.data.keyword.BluSoftlayer_full}} environment within the API, {{site.data.keyword.slapi_short}} enables you to automate tasks. For example, you can use the *SoftLayer_Virtual_Guest/createObject* API to deploy a virtual server instance.
{:shortdesc}

The {{site.data.keyword.slapi_short}} is a Remote Procedure Call system. Each call involves sending data towards an API endpoint and receiving structured data in return. The format used to send and receive data with the {{site.data.keyword.slapi_short}} depends on which implementation of the API you choose. The {{site.data.keyword.slapi_short}} currently uses SOAP, XML-RPC or REST for data transmission.

For more information about the {{site.data.keyword.slapi_short}} and virtual server APIs, see the following resources in the {{site.data.keyword.sldn_full}}:
* [{{site.data.keyword.slapi_short}} Overview ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/reference/softlayerapi/){: new_window}
* [Getting Started with the {{site.data.keyword.slapi_short}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/article/getting-started/){: new_window}
* [API Reference: SoftLayer_Virtual_Guest::createObject ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/){: new_window}
* [API Reference: SoftLayer_Product_Order::placeOrder ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/){: new_window}

For API usage examples, see the following resources:
* [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/article/understanding-ordering/){: new_window}
* [{{site.data.keyword.slapi_short}} Python Client: Working with Virtual Servers ![External link icon](../icons/launch-glyph.svg "External link icon")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [{{site.data.keyword.slapi_short}} Examples - Release Notes ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/){: new_window}
* [Python examples ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/python/){: new_window}

## Dedicated virtual servers usage examples
* [Get Dedicated Host Allocation ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/python/getdedihostallocation/){: new_window}
* [Get Dedicated Host Guests ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/python/getdedicatedhostguests/){: new_window}
* [Migrate a virtual server instance between dedicated hosts ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/python/migratededicatedinstance/){: new_window}

## Public virtual servers usage examples
* [softlayer_virtual_guest API examples ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
