---

copyright:
  years: 2019
lastupdated: "2019-09-16"

keywords: high availability, ha

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Considerations for high availability
{: #ha-dr}

The default behavior for the IBM scheduler is to place the VSIs in available hypervisors first, which can result in VSIs being placed within the same hypervisor. This can be catastrophic if any or all of the VSIs are deployed on the same hypervisor. A hardware (HW) or software (SW) failure can cause a disruption.

IBM Cloud provides two solutions to help avoid the VSIs being deployed on the same hypervisor.

1. Use a dedicated VSI. This option allows you to own the entire hypervisor and control the placement of the VSIs. For more information, see [About dedicated virtual servers](/docs/virtual-servers?topic=virtual-servers-dedicated-virtual-servers)
2. Use Placement Groups. Placement Groups is an anti-affinity feature. If VSIs are marked in the same placement group, then these VSIs is instantiated across different hypervisors. By putting the VSIs in placement groups, availability is improved. For more information see [Placement groups](/docs/virtual-servers?topic=virtual-servers-placement-groups).
