---



copyright:
  years: 2017
lastupdated: "2017-04-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# API reference
{: #api-reference} 

SoftLayer's Application Programming Interface (API) is the development interface that gives developers and system administrators direct interaction with SoftLayer's backend system. The Softlayer API (SLAPI) powers many of the features in the SoftLayer Customer Portal, which typically means if an interaction is possible in the Customer Portal, it can also be run in the API. Because you can programmatically interact with all portions of the SoftLayer environment within the API, SLAPI enables you to automate tasks. For example, you can use the *SoftLayer_Virtual_Guest/createObject* API to deploy a virtual server instance.
{:shortdesc}

Softlayer's API is a Remote Procedure Call system. Each call involves sending data towards an API endpoint and receiving structured data in return. The format used to send and receive data with the SLAPI depends on which implementation of the API you choose. The
SLAPI currently uses SOAP, XML-RPC or REST for data transmission.

For more information about the Softlayer API and virtual server APIs, see the following links in SoftLayer Development Network:
* [SoftLayer API Overview ![External link icon](../icons/launch-glyph.svg "External link icon")](https://sldn.softlayer.com/article/softlayer-api-overview){: new_window} 
* [Getting Started with the SoftLayer API ![External link icon](../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/article/getting-started){: new_window}
* [*SoftLayer_Virtual_Guest* API ![External link icon](../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest){: new_window}
* [Softlayer API Python Client: Working with Virtual Servers ![External link icon](../icons/launch-glyph.svg "External link icon")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}

