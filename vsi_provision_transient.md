---

copyright:
  years: 2017, 2019
lastupdated: "2019-09-16"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:note: .note}
{:important: .important}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Provisioning transient instances
{: #ordering-vs-transient}

## Before you begin
{: #before-you-begin-provisioning-transient}

You can provision your transient virtual server instances through the {{site.data.keyword.cloud}} console.
{:shortdesc}

For the {{site.data.keyword.cloud_notm}} console, you must have an upgraded account to order virtual servers. For more information about upgrading your account, see [Pay-As-You-Go account](/docs/account?topic=account-accounts#paygo).
{:note}

Before you begin, review the following prerequisites.

  1. Review the deployment options available to you. For more information, see [Transient virtual servers](/docs/vsi?topic=virtual-servers-about-vs-transient).

  2. Review virtual server instance capacity considerations.  For more information, see [Resource considerations for virtual server instances](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).
  
  3. Open the [virtual server instance ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?guestType=transient&cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} page from the {{site.data.keyword.cloud_notm}} console.

## Provisioning a transient virtual server instance
{: #ordering-transient-instance}

To provision a transient virtual server instance, you need to consider the following information.

You must be logged in to see all available options. 
{:tip}

### Transient instance
{: #transient-instance}

| Field    | Details     |
| -------- | ----------- |
| Billing  | Transient instances are only available as hourly instances. If you cancel your hourly instance after 10 days, you pay for only the hours for those 10 days. |
| Hostname | Can contain labels that are made of alphanumeric characters and dashes, separated by periods. Labels cannot be numeric only, begin or end with a dash, nor have consecutive dashes or periods. |
| Domain | Must have two or more labels that can be made of alphanumeric characters and dashes, separated by periods. Labels can't begin or end with a dash, or have consecutive dashes or periods. The last label must be letters only. |
| Placement group | You can select a placement group for your instance. If you add a placement group, the "spread" rule means that the instances are on different physical hardware. For more information, see [Placement groups](/docs/vsi?topic=virtual-servers-placement-groups). |
| Location  | Locations are composed of regions (specific geographic areas) and zones (fault tolerant data centers within a region). Select the location where you want your instance to be created. |
| Popular profiles | Consider selecting from popular profile configurations that support most common use cases. Profiles contain preconfigured instances that are ready to use in a matter of minutes. |
| All profiles | For more information about available profile options for transient instances, see [Transient virtual servers](/docs/vsi?topic=virtual-servers-about-vs-transient). |
| SSH keys     | SSH keys allow access to an instance without using a password from corresponding clients for each public key that is implemented on the instance. If you decide to add an SSH key, provide a public key of your SSH key, which you can use to log in to your instance after it is provisioned. |
| Image        |  An image is the deployed operating system for your instance. You can select a number of free options such as CentOS and Ubuntu. Paid options such as Windows Server and Red Hat Enterprise Linux (RHEL) are also available. It's important to note that Windows requires a 100 GB primary disk. |
{: caption="Table 1. Transient instance options" caption-side="top"}

### Transient instance add-ons
{: #transient-instance-add-ons}

If you choose any software add-ons, they must be compatible with your image to avoid an error when you are ordering your instance. For example, you can’t provision a RedHat image with a Microsoft database.
{:important}

| Field     | Details     |
| --------- | ----------- |
| Database software      | You can select a database software to install. {{site.data.keyword.cloud_notm}} supports any database software that is deployed during the provisioning process. You can also install your own database software after the server is deployed. |
| Services | Some services are automatically selected for you, depending on image selection. You can choose from any of the remaining service add-ons for your instance. |
| Provision script | Provisioning scripts are commonly used to apply a customer-specific configuration to a server and to aid in automation of your scaling strategy. Provisioning scripts can be any file that the operating system (OS) can run, including combined binary files or any OS-supported language. Provisioning scripts can't be used on cloud-init images. For more information, see [Provisioning scripts](/docs/vsi?topic=virtual-servers-provisioning-scripts). |
| User data        | You can add user data that automatically performs common configuration tasks or runs scripts. User data can be used on cloud-init and non-cloud-init images.  |
{: caption="Table 2. Transient instance add-ons" caption-side="top"}

### Attached storage disks
{: #attached-storage-disks-transient}

If you need extra storage, you can attach storage disks to your instance. The type of storage disks that are available to you depend on the profile that you select. 

### Network interface
{: #network-interface-transient}

| Field    | Details     |
| -------- | ----------- |
| Uplink port speeds | You can select the uplink speed for your instance, up to 1 Gbps. These virtual uplinks are backed by redundant physical uplinks to the IBM public and dedicated networks. The public and dedicated speed is always the same at the time of order, with the option to upgrade or downgrade a link if needed. If you select the 100 Mbps rate-limited option, the maximum instance throughput is limited only by the physical bandwidth available to the virtual server host. If you select the 1 Gbps non rate-limited option, you can achieve higher network performance through additional configuration. For more information, see [Configuring virtual server settings for improved network performance](/docs/vsi?topic=virtual-servers-configuring-network-performance). |
| Private and public security group  | You can use security groups to enact a set of IP filter rules that define how to handle incoming and outgoing traffic to both the public and private interfaces your instance. For more information, see [About IBM Security Groups](/docs/security-groups?topic=security-groups-about-ibm-security-groups). |
| Private and public VLAN | Your virtual server instance is placed on an automatically assigned VLAN by default. You can choose a different VLAN if you already have one in your selected data center. For more information, see [About VLANs](/docs/vlans?topic=vlans-about-vlans). |
| Private and public subnet | Selecting a subnet is optional and to be used only when you require your device to use an IP address from the subnet. If you select a subnet, verify that you have enough IP addresses to fulfill the request. If you do not have enough IP addresses for your subnet, your order can be delayed or canceled. For more information, see [About subnets and IPs](/docs/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
{: caption="Table 3. Network interface options" caption-side="top"}

### Network interface add-ons
{: #network-interface-add-ons-transient}

| Field    | Details     |
| -------- | ----------- |
| Bandwidth | Bandwidth allocation is not included with transient virtual server instances. |
| Hardware and software firewalls  | Firewall services prevent unwanted traffic on your servers, reduce the likelihood of an attack, and allow your server resources to be dedicated for their intended use. |
| Primary IP address | A primary IP address is automatically assigned to your instance. |
| Public secondary IP addresses | These subnets are owned by you for the duration of your virtual server instance. You can cancel the subnet separately, but if you cancel your instance, the subnet is also removed. For more information, see [About subnets and IPs](/docs/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
| IPv6 and public static IPv6 addresses | You can select an IPv6 address or public static IPv6 addresses for your instance. |
| VPN management | This option is automatically selected for your instance with unlimited SSL VPN users. For more information, see [About VPN](/docs/iaas-vpn?topic=VPN-about-iaas-vpn). |
{: caption="Table 4. Network interface add-ons" caption-side="top"}

You can also provision a transient virtual server by using the {{site.data.keyword.slapi_short}}. For an example, see [Provisioning a transient instance using Create Object](/docs/vsi?topic=virtual-servers-api-rest-public#api-rest-transient).
{:tip}

## Next steps
{: #next-steps-provisioning-transient}

A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page.
 
After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.cloud_notm}} console or {{site.data.keyword.slapi_short}}. For more information, see [Configuring virtual servers](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
