---

copyright:
  years: 2018
lastupdated: "2018-10-31"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 放置组
{: #placement-groups}

利用 {{site.data.keyword.BluVirtServers}} 的放置组，您可以使用公共实例在数据中心内实现高可用性构建，也可以在规模更大的部署中提供另一级别的故障容错。
{:shortdesc}

创建自己的放置组，然后最多分配 5 个新的虚拟服务器实例。利用分布规则，可以在不同的物理主机上供应每个虚拟服务器。

要开始操作，请执行下列步骤：

1. 在浏览器中，打开 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){:new_window} 并登录您的帐户。
2. 在“放置组”页面上，单击**添加放置组**。
3. 输入放置组的名称、描述和数据中心，然后单击**添加**。
4. 找到**订购**部分，然后单击**设备**。
5. 在“设备”页面上，对其中一个虚拟服务器产品，单击**每小时**或**每月**。
6. 填写其他必填信息，然后单击**添加到订单**。这将打开“检出”页面。
7. 您可以选择任何现有放置组。**分布**意味着实例位于不同的物理硬件上。
8. 最后，单击**提交订单**。

##限制
无法将现有实例添加到放置组；在供应时，只能将虚拟服务器实例添加到放置组中。

要除去放置组中的实例，必须删除或回收该实例。

## 后续步骤

要创建和管理新的放置组，请参阅[管理放置组](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup)。
