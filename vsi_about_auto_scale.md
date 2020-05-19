---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords: auto scale, virtual servers

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Auto scale
{: #about-auto-scale}

Auto scale for {{site.data.keyword.BluVirtServers}} provides you with the ability to automate the manual scaling process that's associated with adding or removing instances to support your business applications. This allows you to set up new instances automatically as more resources are needed and then those instances are shut down and removed when the extra load subsides. Auto scale uses groups to contain the policies that change how your environment expands or shrinks. These policies use actions to add or remove virtual server based on your business and application needs. 
{:shortdesc}

Auto scaling enables the following features:

* Seamless and automatic scaling up of instances when more resources are required due to demand
* Seamless and automatic scaling down of instances by removing unnecessary resources when demand goes down (saving you money)
* Flexible scaling triggers: CPU percentage, outgoing public and private bandwidth, and incoming public and private bandwidth
* Near-real-time status updates for scaling activity in groups
* Optional integration of virtual LAN (VLAN) and local load balancers

There are two common business solutions to which auto scaling can be applied:

| Solution | Description |
| -------- | ----------- |
| [Schedule-based scaling](/docs/virtual-servers?topic=virtual-servers-managing-schedule-based-auto-scaling) | Schedule-based scaling can be used to set up policies for time-based usage spikes, like over weekends or holidays. Schedule-based scaling can be used when a company is expecting traffic to spike, for example, a social networking site that requires more resources based on a schedule. |
| [Resource-based scaling](/docs/virtual-servers?topic=virtual-servers-managing-resourced-based-auto-scaling) | Resource-based scheduling can be used to set up policies for irregular spikes, based on resource usage. Irregular spikes in traffic can occur when there is a push to get a product to market or an e-commerce site is having a sale and resources are needed to sustain response times. |
{: caption="Table 1. Auto scaling solutions" caption-side="top"}

If you are not the account administrator, your user account must include permission to use auto scale. The account administrator can grant user's permission from the {{site.data.keyword.cloud_notm}} console. For more information about updating permissions, see [Setting up user permissions for auto scale](/docs/virtual-servers?topic=virtual-servers-user-permissions-required-to-use-auto-scale).
{:note}


