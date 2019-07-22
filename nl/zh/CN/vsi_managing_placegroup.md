---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:note: .note}
{:new_window: target="_blank"}

# 管理放置组
{: #vsi_managing_placegroup}

可以使用 {{site.data.keyword.cloud}} 控制台中的“放置组”页面或“设备详细信息”页面来管理放置组。
{:shortdesc}

## 管理放置组

要从“放置组”页面添加放置组，请完成下列步骤：
{:shortdesc}

1. 打开[“放置”组 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window} 页面。
2. 在“放置组”页面上，单击**新建组**。
3. 输入放置组的名称、位置、pod 和规则，然后单击**创建**。

无法将现有实例添加到放置组；在供应时，只能将虚拟服务器实例添加到放置组中。
{:note}

## 管理放置组

要从“放置组”页面管理放置组，请完成下列步骤：
{:shortdesc}

1. 打开[“放置”组 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window} 页面。
2. 在“放置组”部分下，可以完成几项管理任务。
     * 查看放置组的列表和已分配实例的数量
     * 添加组
     * 重命名组
     * 供应实例
     * 删除组
     
必须先除去放置组中的已分配服务器，然后才能删除放置组。要除去放置组中的实例，必须删除或回收该实例。
{:note}
