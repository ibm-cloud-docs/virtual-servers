---
copyright:
  years: 2014, 2018
lastupdated: "2018-10-23"
---

{:new_window: target="_blank"}

# 存储器选项
{: #storage-options}

可以为每个虚拟服务器选择 SAN（可移植 SAN）或本地存储器。您可以根据需要使用其他存储产品作为 SAN 或本地存储器的补充。

## 本地存储器

本地存储器基于虚拟服务器主机的本地磁盘而构建。本地存储器的磁盘读/写性能有所改进。磁盘采用独立磁盘冗余阵列 (RAID) 配置进行构建，可实现冗余、磁盘更换以及由 {{site.data.keyword.cloud}} 全面管理的运行状况监视。在较新的数据中心内，此存储器全部是固态驱动器 (SSD)，能提供最佳性能。

## 可移植 SAN 存储器

可移植存储卷是仅在 {{site.data.keyword.BluVirtServers_short}} 上提供的辅助存储器解决方案。可移植 SAN 基于 {{site.data.keyword.cloud_notm}} 的全闪存存储器集群构建，而不是基于本地主机存储器构建。在发生主机故障时，此基础架构能提供更大的弹性，而且支持的卷也要大得多。万一发生主机故障，使用基于 SAN 的存储器的虚拟服务器实例会自动迁移到其他主机并重新启动。

如果您希望在 {{site.data.keyword.cloud_notm}} 网络上的任何数据中心内存在的虚拟服务器之间传输数据，那么可移植存储器是理想的解决方案。可移植存储卷适用于需要访问原始未格式化块级别存储器的数据库应用程序，还适用于在 {{site.data.keyword.BluVirtServers_short}} 之间移动大型数据集。

所有辅助磁盘都作为可移植存储器连接。在大多数情况下，这些备用磁盘可以随时拆离，以便能移至其他虚拟服务器。

**例外：**对于使用均衡本地存储器的公用虚拟服务器，无法拆离主磁盘或辅助磁盘。

磁盘可以重新连接到其他服务器，只要更改不超过目标虚拟服务器的磁盘限额或最大卷大小限制即可。

**注**：已移动的磁盘将转换为目标服务器的存储器类型。

可移植存储卷连接到不同于原始虚拟服务器的其他数据中心内的虚拟服务器时，{{site.data.keyword.cloud_notm}} 的内部系统会将该卷复制到新数据中心内的 SAN。然后，系统会验证所复制卷的完整性，并从原始数据中心 SAN 中除去原始可移植卷。

## LVM 限制

不支持逻辑卷管理 (LVM) 作为可引导分区方案。使用正确的操作系统支持和配置，辅助虚拟服务器磁盘可用于 LVM 分区。但是，对于映像模板或 Flex 映像，LVM 不是支持的文件系统。

## 补充存储器

虚拟服务器与 {{site.data.keyword.filestorage_short}} 和 {{site.data.keyword.blockstorageshort}} 以及 {{site.data.keyword.cos_full}} 完全兼容。对于集群驱动器、共享文件存储器、归档存储器、大型存储器需求或特定性能需求，建议使用这些存储器类型。

有关补充存储器选项的更多信息，请参阅以下资源：

* [块存储器入门](/docs/infrastructure/BlockStorage?topic=BlockStorage-GettingStarted)
* [文件存储器入门](/docs/infrastructure/FileStorage?topic=FileStorage-GettingStarted)
* [对象存储器入门](/docs/services/cloud-object-storage?topic=cloud-object-storage-about-ibm-cloud-object-storage#about-ibm-cloud-object-storage)

## 后续步骤
有关如何使用可移植存储卷的更多信息，请参阅以下任务：
* [访问可移植存储器](/docs/vsi/storage?topic=virtual-servers-accessing-portable-storage)
* [编辑可移植存储器描述](/docs/vsi/storage?topic=virtual-servers-editing-a-portable-storage-description)
