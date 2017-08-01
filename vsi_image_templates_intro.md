---



copyright:
  years: 2015, 2017
lastupdated: "2017-04-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# About image templates
{{site.data.keyword.BluVirtServers}} image templates allow you to capture a device's image to quickly replicate its configuration with minimal changes in the order process. {{site.data.keyword.BluVirtServers_short}} provide two options for creating image templates, each offers unique features based on your operating system and the type of image you want to use.
{:shortdesc}

Standard Image Templates provide an imaging option for all {{site.data.keyword.BluVirtServers_short}}, regardless of operating system. Standard image templates allow you to capture an image of an existing virtual server and create a new one based on the captured image. However, standard image templates are not compatible with bare metal servers.

Flex Image is IBM's platform-neutral imaging system that allows you to capture an image of both bare metal servers and virtual servers, and apply that image to either platform. Having the freedom to create images across platforms allows you to create bare metal servers from images of virtual servers and vice versa, expanding the options for how you use your devices.

## How Image Templates Work
The two main actions for any image template are create and deploy. When you request to create an image, IBM Bluemix Infrastructure's automated system takes your server offline. While the server is offline, a compressed backup of your data is created, the configuration information is recorded and the image template is stored on Bluemix infrastucture's SAN. During the deployment stage of the image template, IBM Bluemix Infrastructure's automated system constructs a new server based on the data gathered from the selected image, making adjustments for volume, restores the copied data and then makes final configuration changes (for example, network configurations) for the new host.

### Standard Image Templates
Standard Image Templates are available on all virtual servers and do not require a specific operating system for functionality. Standard Image Templates capture an image of your virtual server and allow you to replicate its configuration to another virtual instance.

### Flex Image Templates
Flex Image is available on machines running out of any Bluemix data center, worldwide. Flex Image is currently available for use on servers that run one of the following operating systems:

* CentOS 5 and 6 (7 is not supported yet)
* Red Hat Enterprise Linux 5 and 6 (7 is not supported yet)
* Microsoft Windows Server 2003
* Microsoft Windows Server 2008 R2

Similar to our Standard Image template, Flex Image captures an image of a server and gives you the ability to replicate that server on another instance. However, Flex Image goes a step further than our Standard Image template, in that, it is available for use and replication on both bare metal servers and virtual servers. Also, images captured using Flex Image may be used between platforms. Flex image gives you the flexibility of virtual, even when it's applied to a bare metal server.

For more information about image templates, see [Image Templates ![External link icon](../icons/launch-glyph.svg "External link icon")](https://knowledgelayer.softlayer.com/topic/image-templates){: new_window} in KnowledgeLayer.
