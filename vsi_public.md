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

# Public virtual servers

Public virtual instances are IBM-managed, multi-tenant virtual server deployments that allow for rapid scalability and higher cost effectiveness with configurations that meet all business requirements. If you're looking for a single-tenant environment, consider the [Dedicated Virtual Server](../vsi/vsi_dedicated.html) offering.
{:shortdesc}

Public nodes reside on a hypervisor that is shared with other clients. However, the processors and memory are dedicated to the virtual server, making server performance extremely reliable. Options are available for higher processor speeds and RAM when using public nodes. 

## Location
You can select the specific data center to which you want to deploy. For new deployments, Bluemix automatically identifies the best POD (based on availability) and creates the appropriate public and private VLANs. For additions to existing environments, you can select the specific POD, VLAN, and subnet that is required for your design.

## Processors / RAM
When you order, you have core processor options from which to select. The core processor options follow standards for virtual server deployments. Each physical core on the server is hyper-threaded and presented as two virtual CPUs (vCPUs) or cores. The virtual server offering provides 2.0GHz or better per core with up to 56 cores available on a single virtual server.

RAM is extremely straight-forward. The offering fully dedicates the amount of RAM that you select to your virtual server, with up to 242GB on a single virtual server.

**Note:** Public and dedicated nodes have slightly different configuration maximums. Very high allocations of either cores or memory limit the available options.

## Operating system

You also select the operating system to be deployed to the server. You can select a number of free options such as CentOS and Ubuntu. Paid  options such as Windows Server and Red Hat Enterprise Linux (RHEL) are also available. It is important to note that Windows requires a 100GB primary disk.

For existing customers, you can also deploy based on an Image Template through the Control Portal by navigating to **Devices -> Manage -> Images** and selecting **Order Virtual Server** from the *Actions* menu.  This automatically selects the appropriate operating system for the order.  Alternatively, you can order based on a standard image and then reload to an image template at any time.

## Storage

You have the option for SAN or local storage for each virtual server. You can supplement SAN or local storage with other storage products as needed. SAN and local storage are both exposed to the virtual server as local disks. Any changes to disks such as attach, detach, migrate, and so on, require a reboot of the virtual server. An entire virtual server can be migrated to SAN or to local storage at any time by using the Control Portal. Changes to storage configurations must stay within the disk quota and size maximums for that storage type.

### Local storage

Local storage is built on disks that are local to the virtual server host. Local storage provides improved disk read/write performance.  The disks are built in a redundant array of independent disks (RAID) configuration for redundancy, disk replacement, and health monitoring which is fully managed by Bluemix. In newer data centers, this storage is all solid state drive (SSD) to provide the best performance. Local storage virtual servers are limited to two disks. The primary disk can be 25GB or 100GB. The secondary disk can be up to 300GB.

### SAN storage

SAN storage is built on Bluemix's SAN infrastructure rather than the local host storage.  This provides greater resiliency in the event of a host failure and can also support much larger volumes.  In the event of a host failure, virtual server instances using SAN-based storage are automatically migrated to other hosts and restarted. The primary disk can be 25GB or 100GB. You can add up to four additional volumes, up to 2TB each.

### Portable storage

All secondary disks are attached as portable storage.  The disks can be detached at any time to allow them to be moved to other virtual servers. Detaching a local disk automatically migrates it to a SAN volume. The disks can be re-attached to another server at any time, as long as the change does not exceed the disk quota or the maximum volume size limit of the target virtual server. 

**Note:** The moved disk is converted to the storage type of the target server.

### LVM limitations

Logical volume management (LVM) is not supported as a bootable partitioning scheme. With proper operating system support and configuration, secondary virtual server disks can be used for LVM partitions. However, LVM is not a supported file system for Image Templates or Flex Images.

### Supplemental storage

Virtual servers are fully compatible with file and block SAN storage, as well as, object storage. These storage types are recommended for cluster drives, shared file storage, archival storage, large storage requirements, or specific performance requirements.

## Hourly and monthly billing

You can select hourly or monthly billing for a virtual server. The primary difference, other than cost, is that hourly servers do not have an included bandwidth allocation. At the end of a billing period, the bandwidth usage and the number of hours each server was active on the account are calculated. A running total is available in the Control Portal under the Virtual Server View page with a link to a Details page, showing each line item, number of hours, and running charges per item.

## Bandwidth

The offering includes 250GB with monthly virtual servers that have a public uplink. You can purchase larger allocations at a reduced cost compared to the overage rate.

## Port speed

You can select the uplink speed for the virtual server, up to 1GB/s. These virtual uplinks are backed by redundant physical uplinks to the IBM public and dedicated networks. The public and dedicated speed is always the same at the time of order, with the option to upgrade or downgrade a link if needed.

## Software

You can select software to be installed by Bluemix during the provisioning process. Bluemix provides support for any software deployed during the provisioning process. You can also install your own software after the server is deployed.

## Security

Before deployment, consider your security options. As part of the order process, you can select a device-specific hardware or software firewall to provide protection. Alternatively, you can deploy dedicated firewall appliances to the environment and deploy the virtual server to a protected VLAN. 

**Note:** A virtual server cannot be protected by two firewall appliances on the same interface. 

For more information, see [Security options](../vsi/vsi_security_options.html).

## Monitoring

You can select from a variety of monitoring options for the virtual server. Options include the standard monitoring, which monitors via Ping and transmission control protocol (TCP) service response, and has optional responses in the event of failures. You can also add Advanced Monitoring which uses the Nimsoft software agent to provide a larger feature set for monitoring of the virtual server and installed software.

For more information, see [Viewing and managing monitors](../vsi/vsi_viewing_monitors.html).

## Backup

During the order process, you can add Evault backups. You can also choose to purchase an R1soft license for your existing R1soft backup environment or utilize a third party backup solution.

For more information, see [Re-registering your device with eVault ![External link icon](../icons/launch-glyph.svg "External link icon")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.

## Post-provisioning scripts

Post-provisioning scripts can be associated with any virtual server order. This runs a customer-developed script after other provisioning tasks are completed. The scripts are commonly utilized to apply a customer-specific configuration to a server and to aid in automation of your scaling strategy.

For more information, see [Adding a custom provisioning script](../vsi/vsi_add_script.html).

## What's Next?

After you have reviewed and decided upon your deployment options, it's time to provision your virtual server. To get started, see [Provisioning public instances](../vsi/vsi_provision_public.html).
