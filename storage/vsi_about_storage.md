---

copyright:
  years: 2014, 2019
lastupdated: "2019-07-16"

subcollection: virtual-servers

---

{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Storage options
{: #storage-options}

You have the option of local storage or SAN (portable SAN) for each virtual server. You can supplement local storage or SAN with other storage products as needed.

## Local storage
{: #local-storage}

Local storage is built on disks that are local to the virtual server host. Local storage provides improved disk read/write performance. The disks are built in a redundant array of independent disks (RAID) configuration for redundancy, disk replacement, and health monitoring which is fully managed by {{site.data.keyword.cloud}}. In newer data centers, this storage is all solid state drive (SSD) to provide the best performance. For more information about available data centers for local SSD storage, see [Balanced local storage](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage).

## Portable SAN storage
{: #portable-san-storage}

Portable storage volumes are auxiliary storage solutions that are exclusively available on {{site.data.keyword.BluVirtServers_short}}.  The portable SAN is built on {{site.data.keyword.cloud_notm}}'s all flash storage clusters rather than the local host storage. This infrastructure provides greater resiliency in the event of a host failure and can also support much larger volumes. If there is a host failure, virtual server instances using SAN-based storage are automatically migrated to other hosts and restarted.

Portable storage is an ideal solution if you want to transfer data between virtual servers that exist in any data center on {{site.data.keyword.cloud_notm}}'s network. Portable storage volumes are useful for database applications that require access to raw, unformatted block-level storage and for moving large data sets between {{site.data.keyword.BluVirtServers_short}}.

All secondary disks are attached as portable storage. In most cases, these secondary disks can be detached at any time to allow them to be moved to other virtual servers.

With public virtual servers that use balanced local storage, you cannot detach primary or secondary disks.
{:important}

The disks can be re-attached to another server, as long as the change does not exceed the disk quota or the maximum volume size limit of the target virtual server.

The moved disk is converted to the storage type of the target server.
{:note}

When a portable storage volume is attached to a virtual server in a different data center than the original virtual server, {{site.data.keyword.cloud_notm}}'s internal system copies the volume to the SAN in the new data center. The system then verifies the integrity of the copied volume and removes the original portable volume from the original data center SAN.

## LVM limitations
{: #lvm-limitations}

Logical volume management (LVM) is not supported as a bootable partitioning scheme. With proper operating system support and configuration, secondary virtual server disks can be used for LVM partitions. However, LVM is not a supported file system for Image Templates or Flex Images.

## Supplemental storage
{: #supplemental-storage}

Virtual servers are fully compatible with {{site.data.keyword.filestorage_short}} and {{site.data.keyword.blockstorageshort}}, as well as, {{site.data.keyword.cos_full}}. These storage types are recommended for cluster drives, shared file storage, archival storage, large storage requirements, or specific performance requirements.

For more information about supplemental storage options, see the following resources:

* [Getting Started with Block Storage](/docs/BlockStorage?topic=BlockStorage-getting-started)
* [Getting Started with File Storage](/docs/FileStorage?topic=FileStorage-getting-started)
* [Getting Started with Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started)

## Next steps
{: #next-steps-storage}

For more information about how to use portable storage volumes, see the following tasks:
* [Managing portable storage](/docs/vsi?topic=virtual-servers-accessing-portable-storage#accessing-portable-storage)
* [Editing a portable storage description](/docs/vsi?topic=virtual-servers-editing-a-portable-storage-description#editing-a-portable-storage-description)
