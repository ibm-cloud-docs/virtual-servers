---
copyright:
  years: 2014, 2018
lastupdated: "2018-02-26"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Storage options

You have the option for SAN or local storage for each virtual server. You can supplement SAN or local storage with other storage products as needed. 

## Local storage

Local storage is built on disks that are local to the virtual server host. Local storage provides improved disk read/write performance. The disks are built in a redundant array of independent disks (RAID) configuration for redundancy, disk replacement, and health monitoring which is fully managed by {{site.data.keyword.cloud}}. In newer data centers, this storage is all solid state drive (SSD) to provide the best performance. 

## SAN storage
 
SAN storage is built on {{site.data.keyword.cloud_notm}}'s SAN infrastructure rather than the local host storage. This provides greater resiliency in the event of a host failure and can also support much larger volumes. In the event of a host failure, virtual server instances using SAN-based storage are automatically migrated to other hosts and restarted. 

All secondary disks are attached as portable storage. In most cases, the disks can be detached at any time to allow them to be moved to other virtual servers. 

**Exception:** With public virtual servers that use balanced local storage, you cannot detach primary or secondary disks.

The disks can be re-attached to another server, as long as the change does not exceed the disk quota or the maximum volume size limit of the target virtual server.

**Note:** The moved disk is converted to the storage type of the target server.

## Portable storage volumes

Portable storage volumes are auxiliary storage solutions that are exclusively available on {{site.data.keyword.BluVirtServers_short}}. They can be connected to one virtual server at a time. They are also an ideal solution if you want to transfer data between virtual servers that exist in any data center on {{site.data.keyword.cloud_notm}}'s network. Portable storage volumes are useful for database applications that require access to raw, unformatted block-level storage and for moving large data sets between {{site.data.keyword.BluVirtServers_short}}.

When a portable storage volume is attached to a virtual server in a different data center than the original virtual server, {{site.data.keyword.cloud_notm}}'s internal system copies the volume to the SAN in the new data center. The system then verifies the integrity of the copied volume and removes the original portable volume from the original data center SAN.

## LVM limitations

Logical volume management (LVM) is not supported as a bootable partitioning scheme. With proper operating system support and configuration, secondary virtual server disks can be used for LVM partitions. However, LVM is not a supported file system for Image Templates or Flex Images.

## Supplemental storage

Virtual servers are fully compatible with file and block SAN storage, as well as, object storage. These storage types are recommended for cluster drives, shared file storage, archival storage, large storage requirements, or specific performance requirements.

For more information about supplemental storage options, see the following resources:

* [Getting Started with Block Storage](/docs/infrastructure/BlockStorage/index.html)
* [Getting Started with File Storage](/docs/infrastructure/FileStorage/index.html)
* [Getting Started with Object Storage](/docs/services/ObjectStorage/index.html)

## Next steps
For more information about how to use portable storage volumes, see the following tasks:
* [Accessing portable storage](../storage/access-portable-storage-screen.html)
* [Editing the portable storage description](../storage/edit-description-portable-storage-volume-psv.html)


