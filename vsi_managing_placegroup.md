---

copyright:
  years: 2018, 2021
lastupdated: "2021-05-19"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:note: .note}
{:important: .important}

# Managing placement groups
{: #vsi_managing_placegroup}

You can manage placement groups by using the placement groups page or the device details page in the {{site.data.keyword.cloud}} console.
{: shortdesc}

## Adding placement groups
{: #adding-placement-groups}

To add placement groups from the placement groups page, complete the following steps:

1. Open [Placement groups](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: external}.
2. Click **New group**.
3. Enter a name, location, POD, and rule for the placement group, and click **Create**.

You can add existing instances to a placement group. You can add a virtual server instance only to a placement group at provisioning. 
{: note}

## Managing placement groups
{: #managing-placement-groups}

To manage placement groups from the placement groups page, complete the following steps:

1. Open [Placement groups](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: external}.
2. Under the placement group section, you can complete several management tasks.
   * View a list of placement groups and number of assigned instances
   * Add a group
   * Rename a group
   * Provision an instance
   * Delete a group
     
You must remove assigned servers from the placement group before the placement group can be deleted. To remove an instance from a placement group, you must delete or reclaim the instance.
{: note}
