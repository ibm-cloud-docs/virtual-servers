---

copyright:
  years: 2024
lastupdated: "2024-12-03"

keywords: virtual servers, bare metal servers, classic

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}



# Understanding data portability for classic infrastructure compute services
{: #data-portability}





Data portability involves a set of tools and procedures that enable you to export the digital artifacts that are needed to implement similar workload and data processing on different service providers or on-premises software. It includes procedures for copying and storing the service customer content, including the related configuration that is used by the service to store and process the data, in your location.
{: shortdesc}

## Responsibilities
{: #data-portability-responsibilities}

{{site.data.keyword.cloud_notm}} services provide interfaces and instructions to guide you through the process of copying and storing service customer content, including the related configuration, in your selected location.

You're responsible for the use of the exported data and configuration for data portability to other infrastructures, which includes:

- The planning and execution for setting up alternative infrastructure on different cloud providers or on-premises software that provide similar capabilities to the {{site.data.keyword.IBM_notm}} services.
- The planning and execution for the porting of the required application code on the alternative infrastructure, including the adaptation of your application code, deployment automation, and so on.
- The conversion of the exported data and configuration to the format that's required by the alternative infrastructure and adapted applications.


To find out more about responsibility ownership for using {{site.data.keyword.cloud}} products between {{site.data.keyword.IBM_notm}} and the customer, see [Shared responsibilities for {{site.data.keyword.cloud_notm}} products](/docs/overview?topic=overview-shared-responsibilities).



## Data export procedures
{: #data-portability-procedures}

### Exporting customer data for virtual servers
{: #data-portability-virtual-servers}

Classic infrastructure Virtual Servers provides the mechanisms to export your content that's uploaded, stored, and processed when you use the service.

Complete the following steps to export customer data for your virtual server to {{site.data.keyword.cos_full_notm}}. From {{site.data.keyword.cos_full_notm}} you can download the image for your use. This procedure applies to virtual servers that are provisioned on both public hosts and dedicated hosts.

1. For the virtual server that contains data that you want to export, complete the steps in [Creating an image template](/docs/image-templates?topic=image-templates-creating-an-image-template).
1. Make sure that you have an {{site.data.keyword.cos_full_notm}} instance configured. For more information, see [Getting started with IBM Cloud Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage).
1. Complete the steps in [Exporting an image to IBM Cloud Object Storage](/docs/image-templates?topic=image-templates-exporting-an-image-to-ibm-cloud-object-storage).
1. Download the custom image from {{site.data.keyword.cos_full_notm}} for your use. For more information, see [Using Aspera high-speed transfer](/docs/cloud-object-storage?topic=cloud-object-storage-aspera).

You can find additional details about your virtual server configuration with the following resources.

| Service | {{site.data.keyword.cloud_notm}} console | CLI | SoftLayer_Virtual_Guest API |
|----------------|-------------------------|-------------------------|---------------|
| Virtual servers | View details for the virtual server | [ibmcloud sl vs detail](/docs/cli?topic=cli-cli-virtual-servers#sl_vs_detail) | [getBlockDevices](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/getBlockDevices/) \n [getAttachedNetworkStorages](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/getAttachedNetworkStorages/) \n [getAttributes](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/getAttributes/) |
{: caption="How to view details of a virtual server" caption-side="bottom"}

### Exporting customer data for bare metal servers
{: #data-portability-bare-metal-servers}

Bare metal servers are positioned as a fully customer-managed service. You are responsible to determine your own data export solution.

## Exported data formats
{: #data-portability-data-formats}



### Exported data formats for virtual servers and image templates
{: #data-portability-data-formats-virtual-servers}

Classic infrastructure virtual servers support the following data format and schema of the exported data, configuration, and application: 

When you export an image template that is created from a virtual server configuration, the image template is exported in the format that you specify:

* VHD
* VMDK 

## Data ownership
{: #data-portability-ownership}

All exported data is classified as customer content. Apply the full customer ownership and licensing rights, as stated in the [IBM Cloud Service Agreement](https://www.ibm.com/support/customer/csol/terms/?id=Z126-6304_WS){: external}.


