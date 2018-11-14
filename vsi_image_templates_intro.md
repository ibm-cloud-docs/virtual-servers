---



copyright:
  years: 2015, 2018
lastupdated: "2018-11-14"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Image templates
With {{site.data.keyword.BluVirtServers}} image templates, you can capture a device's image to quickly replicate its configuration with minimal changes in the order process. 
{:shortdesc}

Image templates provide an imaging option for all {{site.data.keyword.BluVirtServers_short}}, regardless of operating system. Image templates allow you to capture an image of an existing virtual server and create a new one based on the captured image. Image templates are not compatible with bare metal servers.

## How Image Templates Work
The two main actions for any image template are create and deploy. When you request to create an image, the automated system of {{site.data.keyword.BluSoftlayer_full}} takes your server offline. While the server is offline, a compressed backup of your data is created, the configuration information is recorded, and the image template is stored on the {{site.data.keyword.BluSoftlayer_notm}} SAN. During the deployment stage of the image template, the automated system constructs a new server that is based on the data that is gathered from the selected image. The deployment process makes adjustments for volume, restores the copied data, and then makes final configuration changes (for example, network configurations) for the new host.

For more information about image templates, see [Getting started with image templates](/docs/infrastructure/image-templates/image_index.html).
