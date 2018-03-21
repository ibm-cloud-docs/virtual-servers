---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 关于可移植存储卷

可移植存储卷是仅在 {{site.data.keyword.BluVirtServers_short}} 上提供的辅助存储器解决方案。可移植存储卷一次只能连接到一个虚拟服务器。如果您希望在 {{site.data.keyword.cloud}} 网络上的任何数据中心内存在的虚拟服务器之间传输数据，那么可移植存储卷也是理想的解决方案。可移植存储卷适用于需要访问原始未格式化块级别存储器的数据库应用程序，还适用于在 {{site.data.keyword.BluVirtServers_short}} 之间移动大型数据集。

可移植存储卷连接到不同于原始虚拟服务器的其他数据中心内的虚拟服务器时，{{site.data.keyword.cloud}} 的内部系统会将该卷复制到新数据中心内的 SAN。然后，系统会验证所复制卷的完整性，并从原始数据中心 SAN 中除去原始可移植卷。

## 后续步骤
有关如何使用可移植存储卷的更多信息，请参阅以下任务：
* [访问可移植存储器](../storage/access-portable-storage-screen.html)
* [编辑可移植存储器描述](../storage/edit-description-portable-storage-volume-psv.html)
