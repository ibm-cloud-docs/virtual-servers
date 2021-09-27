---

copyright:
  years: 2020, 2021
lastupdated: "2021-09-16"

content-type: tutorial
services: virtual-servers, loadbalancer-service
account-plan: paid
completion-time: 
subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}
{:step: data-tutorial-type='step'}


# Migrating a virtual server between classic data centers
{: #migrating-vsi-new-datacenter}
{: toc-content-type="tutorial"} 
{: toc-services="virtual-servers, loadbalancer-service"} 
{: toc-completion-time=" "}

You have two ways to move your virtual server instance between {{site.data.keyword.Bluemix}} classic infrastructure data centers:

* **Lift and Shift**

When you use this method, you create an image template, provision it, and cancel the old virtual server instance. This method is like lift and shift. The advantage of this method is that it is usually the easier and quicker method for moving a virtual server instance. However, while the image is being made, the virtual server instance is shut down.

*  **System Rebuild**

When you use this method, you order a new virtual server instance and copy the data from the old virtual server instance to the new virtual server instance. This method is more involved because you need to rebuild the OS specifics and redeploy the application, which might also involve making modifications. The advantage of this method is that it provides an opportunity to start fresh with a new system or to upgrade to a newer OS.

Both methods work; the method you choose depends on your business and timeline requirements.

## Lift and Shift method
{: #vsi-migrate-lift-shift-method}

### Before you begin
{: #vsi-migrate-before-lift-shift-method}

Before you create an image template: 
* **Plan for maintenance time** 

Creating an image template is an intrusive operation and shuts down the virtual server instance. After the template is complete, the virtual server instance powers back up. Powering down and up happens automatically and does not require user interaction.
* **Attached storage considerations**

Capturing the data on the attached storage is optional. You can select which attached storage disks are part of the image template. The Boot volume is always mandatory.

* **Network-attached storage considerations**

Block Endurance and Performance and File storage volumes are not captured as part of the imaging process. You migrate data for these volumes at the OS level by using data migration tools such as `scp`, `rsync`, `dd`, or another third-party tool of choice. These storage services are data center specific. If you are moving your virtual server instance to a different data center, order new storage volumes at the same location where the new virtual server instance is being deployed.

### Evaluate and create an image template
{: #vsi-migrate-evaluate-lift-shift-method}

1. Evaluate the virtual server that you want to migrate to see which services it is using, such as:
   * Auto scale group
   * Placement group
   * Security group 
1.  Log in to the [{{site.data.keyword.cloud}} console](https://cloud.ibm.com/classic?){: external} by using your unique credentials. 

1. From the dashboard, click **Menu icon ![Menu icon](../icons/icon_hamburger.svg) > Classic Infrastructure > Devices > Device List**.

1. Click the virtual server that you want to use to create an image template. 

1. From the **Actions** menu, select *Create Image Template*. Give the template a unique name that is easily recognized. For more information, see [Creating an image template](/docs/image-templates?topic=image-templates-creating-an-image-template).

### Provision the new virtual server instance
{: #vsi-migrate-provision-lift-shift-method}

1. From the [{{site.data.keyword.cloud}} console](https://cloud.ibm.com/classic?){: external}, click **Menu icon ![Menu icon](../icons/icon_hamburger.svg) > Classic Infrastructure > Devices > Device List > Manage > Images**.

1. Locate the image template that you created in *Evaluate and create an image template*. 

1. Click the **Actions** ![Menu icon](../../icons/action-menu-icon.svg) icon for the image template and select *Order < Type of > VSI*. < Type of > is the type of virtual server instance that you are creating.

1. Change the virtual server instance location to the new data center. The form defaults to the original virtual server properties. Other than selecting the new location, you can keep or modify the rest of the parameters to better suit the new environment, for example:
   * Enter hostname and domain
   * (Optional) Select or create a placement group
   * Select a virtual server profile
   * (Recommended) Select SSH key
   * Select Uplink port speeds

 The new virtual server is given a new IP address automatically on deployment.
 {: note}

### Verify and validate the virtual server instance, and update network resources
{: #vsi-migrate-verify-lift-shift-method}

1. After the new virtual server is deployed, verify the instance.

1. Make any OS level modifications that are needed to the virtual server. 

1. (Optional) If block or file storage volumes were part of the original virtual server, create the new volumes and update the iSCSI or NFS configuration on the new virtual server. After created and attached, copy the data over from the old to new virtual server by using your tool of choice. 

1. Update and add or modify any infrastructure resources, such as:
   * Security groups
   * Firewall rules
   * Load balancers
   * VPN
   * DNS

### Final check
{: #vsi-migrate-final-lift-shift-method}

1. After you complete the new virtual server verification and are ready to activate the new server, do one last sync of any data drift from the old to new virtual server. 

1. Shut down the old server.

1. Create one last image template as a backup. 

1. When ready, clean and cancel any unused resources at the old location. 

## System rebuild method
{: #vsi-migrate-system-rebuild-method}

For this method, you're ordering a new virtual server and copying the data from the old to the new virtual server. Copying the data is handled at the OS level, by using `scp`, `rsync`, `dd`, or another third-party tool. 

### Evaluate your virtual server
{: #vsi-migrate-evaluate-system-rebuild-method}

1. Evaluate the virtual server that you want to migrate so see which services it is using, such as (not an exhaustive list):
   * Auto scale group
   * Placement group
   * Security groups
   * Firewall rules
   * Load balancers

1. Make sure that similar services are created at the new data center. 

### Order, provision, and configure the new virtual server
{: #vsi-migrate-provision-system-rebuild-method}

1. Log in to the [{{site.data.keyword.cloud}} console](https://cloud.ibm.com/classic?){: external} by using your unique credentials.

1. Click the **Virtual Server for Classic** tile in the catalog. 

1. Provision the new virtual server:
   * Enter a hostname and domain
   * (Optional) Select or create a placement group
   * Select a location
   * Select a virtual server profile
   * (Recommended) Select an SSH key
   * Add an extra attached storage disk, if necessary
   * Select Uplink port speeds

1. (Optional) If block or file volumes were part of the original virtual server, create the new volumes and attach them to the new virtual server. 

1. Configure the OS on the new virtual server.

1. Install all of the appropriate packages applications.

1. Copy the data from the old server to the new server by using `scp`, `rsync`, `dd`, or another third-party tool. 

1. Update and add or modify any infrastructure resources, such as: 
   * Security groups
   * Firewall rules
   * Load balancers
   * VPN
   * DNS

### Verify and validate
{: #vsi-migrate-verify-system-rebuild-method}

1. Verify the new virtual server.

1. When you're ready to make the new virtual server active, power off the old server.

1. Create an image template of the old server as a backup. For more information, see [Creating an image template](/docs/image-templates?topic=image-templates-creating-an-image-template).

1. When you're ready, clean and cancel any unused resources at the old location. 
