---



copyright:
  years: 2015, 2017
lastupdated: "2017-08-23"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# About image templates
With {{site.data.keyword.BluVirtServers}} image templates, you can capture a device's image to quickly replicate its configuration with minimal changes in the order process. {{site.data.keyword.BluVirtServers_short}} provide two options for creating image templates, each offers unique features based on your operating system and the type of image you want to use.
{:shortdesc}

Standard Image Templates provide an imaging option for all {{site.data.keyword.BluVirtServers_short}}, regardless of operating system. Standard image templates allow you to capture an image of an existing virtual server and create a new one based on the captured image. However, standard image templates are not compatible with bare metal servers.

## How Image Templates Work
The two main actions for any image template are create and deploy. When you request to create an image, IBM Bluemix Infrastructure's automated system takes your server offline. While the server is offline, a compressed backup of your data is created, the configuration information is recorded and the image template is stored on Bluemix infrastucture SAN. During the deployment stage of the image template, IBM Bluemix Infrastructure's automated system constructs a new server based on the data gathered from the selected image, making adjustments for volume, restores the copied data and then makes final configuration changes (for example, network configurations) for the new host.

### Standard Image Templates
Standard Image Templates are available on all virtual servers and do not require a specific operating system for functionality. Standard Image Templates capture an image of your virtual server and allow you to replicate its configuration to another virtual instance.

For more information about image templates, see [Image Templates ![External link icon](../icons/launch-glyph.svg "External link icon")](https://knowledgelayer.softlayer.com/topic/image-templates){: new_window} in KnowledgeLayer.
