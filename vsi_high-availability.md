---

copyright:
  years: 2019, 2024
lastupdated: "2024-07-23"

keywords: high availability, ha

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Considerations for high availability
{: #ha-dr}

The default behavior for the IBM scheduler is to place virtual servers in available hypervisors first, which can result in virtual servers that share a hypervisor. This result can be catastrophic if any or all of the virtual servers are deployed on the same hypervisor. A hardware or software failure can cause a disruption.

IBM Cloud provides two solutions to help avoid virtual servers from deploying on the same hypervisor.

1. Use a dedicated virtual server. By using a dedicated virtual server, you to own the entire hypervisor and control the placement of the virtual servers. For more information, see [About dedicated virtual servers](/docs/virtual-servers?topic=virtual-servers-dedicated-virtual-servers)
2. Use Placement Groups. Placement Groups is an anti-affinity feature. If virtual servers are marked in the same placement group, then these virtual servers are instantiated across different hypervisors. By putting the virtual servers in placement groups, availability is improved. For more information, see [Placement groups](/docs/virtual-servers?topic=virtual-servers-placement-groups).
