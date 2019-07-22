---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 常见问题：自动缩放
{: #faqs-auto-scale}

## 自动缩放支持 Bare Metal Auto Scale 实例吗？
{: faq}

目前，自动缩放不支持 Bare Metal Auto Scale 实例。

## 自动缩放适用于负载均衡器吗？
{: faq}

是的，自动缩放目前适用于本地负载均衡器，并使用一部分负载均衡器 API。有关更多信息，请访问[缩放负载均衡器](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 有哪些不同的自动缩放终止策略？
{: faq}

有三种自动缩放终止策略：最新、最早和最接近下一次收费。这些策略描述了组在缩减时，如何选择要移除的成员。有关更多信息，请参阅[终止策略](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 什么是自动缩放策略？
{: faq}

策略包含一组操作和一组触发器。策略通常由以下元素组成：名称、冷却时间段、操作和触发器。有关更多信息，请参阅[策略](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 什么是自动缩放触发器？
{: faq}

触发器是有条件触发器，满足条件时触发（仅当组处于活动状态时）。有三种类型的触发器：一次性、重复性和基于资源使用量。有关更多信息，请参阅[触发器](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 什么是最大 VSI 成员计数？
{: faq}

这是指一个组中允许存在的最多成员数。有关更多信息，请参阅[最大 VSI 成员计数](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 什么是最小 VSI 成员计数？
{: faq}

这是指一个组中允许存在的最少成员数。有关更多信息，请参阅[最小 VSI 成员计数](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 什么是自动缩放资产？
{: faq}

资产是指组中的固定成员，它不影响成员计数，并且不会以任何方式进行自动控制。资产的存在是为了向策略触发器提供更多信息。例如，如果是将 CPU 百分比用作触发器，那么资产可以影响整个组的 CPU 百分比。目前，组只能有虚拟访客资产，其数量没有限制。此外，组不是必需的。

## 什么是自动缩放组？
{: faq}

组（缩放组）是指特定于组的资产、成员、缩放负载均衡器、VLAN 和策略的集合。组具有用于缩放的所有参数，包括成员计数边界以及缩放的虚拟服务器实例成员模板。

## 什么是自动缩放成员？
{: faq}

成员是组中的缩放单位。根据策略操作会自动供应或回收成员。当前，所有成员都是虚拟服务器实例。在活动组中，成员数绝不能少于最小成员数，也不能多于最大成员数。虽然成员通常是通过策略的操作添加的，但用户也可以手动进行添加。
