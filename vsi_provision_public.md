---

copyright:
  years: 2017, 2019
lastupdated: "2019-09-16"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning public instances
{: #ordering-vs-public}

## Before you begin
{: #before-you-begin-provisioning-public}

You have two options to provision your public virtual server instances. The first is through the {{site.data.keyword.cloud}} console and the second is through the {{site.data.keyword.slportal}}. The console and {{site.data.keyword.slportal}} require unique log-in IDs. You can't use your console user name and password to log in to the portal and vice versa.
{:shortdesc}

For the {{site.data.keyword.cloud_notm}} console, you must have an upgraded account to order virtual servers. For more information about upgrading your account, see [Pay-As-You-Go account](/docs/account?topic=account-accounts#paygo).
{:note}

Before you begin, review the following prerequisites.

  1. Review the deployment options available to you. For more information, see [Public virtual servers](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers).

  2. Review virtual server instance capacity considerations.  For more information, see [Resource considerations for virtual server instances](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).
  
  3. Open the [virtual server instance ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} page from the {{site.data.keyword.cloud_notm}} console.

## Provisioning a public virtual server instance  
{: #ordering-public-instance}

To provision a virtual server instance, you need to consider the following information.

You must be logged in to see all available options. 
{:tip}

### Public instance
{: #public-instance}

| Field    | Details     |
| -------- | ----------- |
| Billing  | Depending on your virtual server instance, you can select either hourly or monthly billing. The primary difference, other than cost, is that hourly instances don't have an included bandwidth allocation. At the end of a billing period, the bandwidth usage and the number of hours that each instance was active on the account are calculated. For example, if you cancel an hourly instance after 10 days, you pay for only the hours for those 10 days. If you cancel a monthly instance after 10 days, you pay for the whole month. If you're interested in the suspend billing feature, which is only available on hourly instances, see [About suspend billing](/docs/vsi?topic=virtual-servers-requirements). |
| Hostname | Can contain labels that are made of alphanumeric characters and dashes, separated by periods. Labels cannot be numeric only, begin or end with a dash, nor have consecutive dashes or periods. |
| Domain | Must have two or more labels that can be made of alphanumeric characters and dashes, separated by periods. Labels can't begin or end with a dash, or have consecutive dashes or periods. The last label must be letters only. |
| Placement group | You can select a placement group for your instance. If you add a placement group, the "spread" rule means that the instances are on different physical hardware. For more information, see [Placement groups](/docs/vsi?topic=virtual-servers-placement-groups). |
| Location  | Locations are composed of regions (specific geographic areas) and zones (fault tolerant data centers within a region). Select the location where you want your virtual server instance to be created. |
| Popular profiles | Consider selecting from popular profile configurations that support most common use cases. Profiles contain preconfigured instances that are ready to use in a matter of minutes. |
| All profiles | For more information about available profile options for public instances, see [Public virtual servers](/docs/vsi?topic=virtual-servers-about-public-virtual-servers). |
| SSH keys     | SSH keys allow access to an instance without using a password from corresponding clients for each public key that is implemented on the instance. If you decide to add an SSH key, provide a public key of your SSH key, which you can use to log in to your instance after it is provisioned. |
| Image        |  An image is the deployed operating system for your instance. You can select a number of free options such as CentOS and Ubuntu. Paid options such as Windows Server and Red Hat Enterprise Linux (RHEL) are also available. It's important to note that Windows requires a 100 GB primary disk. |
{: caption="Table 1. Public instance options" caption-side="top"}

### Public instance add-ons
{: #public-instance-add-ons}

If you choose any OS, control panel, or software add-ons, they must be compatible with your image to avoid an error when you are ordering your instance. For example, you can’t provision a Red Hat image with a Microsoft database.
{:important}

Depending on your instance billing type (hourly or monthly), some add-ons might not be available.
{:tip}

| Field     | Details     |
| --------- | ----------- |
| OS add-ons | If you select monthly billing, you can select the following image add-ons:<br><br> **R1Soft Server Backup Manager** provides high-performance disk-to-disk server backup and a central management and data repository. If you select the R1Soft add-on, you must purchase an R1Soft Backup Agent pack, which is a CDP add-on in the **Services** section. Selecting one without the other causes an error with your order. For more information about R1Soft and IBM Cloud, see [R1Soft Server Backup Manager ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud/backup-and-restore?mhq=R1Soft%20Server%20Backup%20Manager&mhsrc=ibmsearch_a){: new_window}.<br><br>**Veeam Backup and Replication** combines automated backup along with restore and replication capabilities. Veeam also provides advanced monitoring, reporting, and capacity planning. For more information about Veeam Backup and Replication, see [Veeam Backup and Replication with IBM storage ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www-356.ibm.com/partnerworld/gsd/solutiondetails.do?solution=54724&lc=en&stateCd=P&tab=2){: new_window}.<br><br>**VMware vCenter** automates deployment of the underlying VMware vSphere and VMware vCenter Server layers that you need for a flexible and customizable VMware solution. For more information about vCenter on IBM Cloud, see [About vCenter Server on IBM Cloud ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/downloads/cas/L7RKPZND?mhq=vmware%20vcenter&mhsrc=ibmsearch_a){: new_window}.|
| Control panel software | If you select monthly billing, you can add a control panel for web hosting. |
| Database software      | You can select a database software to install. {{site.data.keyword.cloud_notm}} supports any database software that is deployed during the provisioning process. You can also install your own database software after the server is deployed. |
| Services | Some services are automatically selected for you, depending on your billing and image selections. You can choose from any of the remaining service add-ons for your instance. |
| Provision script | Provisioning scripts are commonly used to apply a customer-specific configuration to a server and to aid in automation of your scaling strategy. Provisioning scripts can be any file that the operating system (OS) can run, including combined binary files or any OS-supported language. Provisioning scripts can't be used on cloud-init images. For more information, see [Provisioning scripts](/docs/vsi?topic=virtual-servers-provisioning-scripts). |
| User data        | You can add user data that automatically performs common configuration tasks or runs scripts. User data can be used on cloud-init and non-cloud-init images.  |
{: caption="Table 2. Public instance add-ons" caption-side="top"}

### Attached storage disks
{: #attached-storage-disks-public}

If you need extra storage, you can attach storage disks to your instance. The type of storage disks that are available to you depend on the profile that you select. For example, balanced local profiles and a few of the GPU profiles use local storage disks. If you select monthly billing, you can add {{site.data.keyword.backup_notm}} and choose the option that best fits your needs. For more information, see [{{site.data.keyword.backup_notm}} services](/docs/infrastructure/Backup?topic=Backup-getting-started).

### Network interface
{: #network-interface-public}

| Field    | Details     |
| -------- | ----------- |
| Uplink port speeds | You can select the uplink speed for your instance, up to 1 Gbps. These virtual uplinks are backed by redundant physical uplinks to the IBM public and dedicated networks. The public and dedicated speed is always the same at the time of order, with the option to upgrade or downgrade a link if needed. If you select the 100 Mbps rate-limited option, the maximum instance throughput is limited only by the physical bandwidth available to the virtual server host. If you select the 1 Gbps non rate-limited option, you can achieve higher network performance through additional configuration. For more information, see [Configuring virtual server settings for improved network performance](/docs/vsi?topic=virtual-servers-configuring-network-performance). |
| Private and public security group  | You can use security groups to enact a set of IP filter rules that define how to handle incoming and outgoing traffic to both the public and private interfaces your instance. For more information, see [About IBM Security Groups](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups). |
| Private and public VLAN | Your virtual server instance is placed on an automatically assigned VLAN by default. You can choose a different VLAN if you already have one in your selected data center. For more information, see [About VLANs](/docs/infrastructure/vlans?topic=vlans-about-vlans). |
| Private and public subnet | Selecting a subnet is optional and to be used only when you require your device to use an IP address from the subnet. If you select a subnet, verify that you have enough IP addresses to fulfill the request. If you do not have enough IP addresses for your subnet, your order can be delayed or canceled. For more information, see [About subnets and IPs](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
{: caption="Table 3. Network interface options" caption-side="top"}

### Network interface add-ons
{: #network-interface-add-ons-public}

| Field    | Details     |
| -------- | ----------- |
| Bandwidth | 250 GB are included with monthly instances that have a public uplink. You can purchase larger allocations at a reduced cost compared to the overage rate. |
| Hardware and software firewalls  | Firewall services prevent unwanted traffic on your servers, reduce the likelihood of an attack, and allow your server resources to be dedicated for their intended use. |
| Primary IP address | A primary IP address is automatically assigned to your instance. |
| Public secondary IP addresses | These subnets are owned by you for the duration of your virtual server instance. You can cancel the subnet separately, but if you cancel your instance, the subnet is also removed. For more information, see [About subnets and IPs](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
| IPv6 and public static IPv6 addresses | You can select an IPv6 address or public static IPv6 addresses for your instance. |
| VPN management | This option is automatically selected for your instance with unlimited SSL VPN users. For more information, see [About VPN](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn). |
{: caption="Table 4. Network interface add-ons" caption-side="top"}


## Provisioning a public instance through the customer portal
{: #provisioning-a-public-instance-through-the-customer-portal}

To provision your public virtual server instance through the {{site.data.keyword.slportal}}, complete the following steps:

  1. Log in to the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
  2. Locate the **Order** section and click **Devices**.
  3. On the Devices page, click **Hourly SAN**, **Hourly local**, **Monthly**, or **Transient** for one of the Virtual Server offerings.
  4. On the *Configure your Cloud Server* page, complete all the relevant information.
  5. Click **Add to Order** to continue.
  6. Confirm or edit the domain information for the server.
  7. Click the **Cloud Service terms** and the **Third-Party Service Agreement** check box.
  8. Confirm or enter your payment information and click **Submit Order**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

## Next steps
{: #next-steps-provisioning-public}

A series of emails is sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page after you log in to {{site.data.keyword.Bluemix_notm}}.

After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.cloud_notm}} console or {{site.data.keyword.slapi_short}}. For more information, see [Configuring virtual servers](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
