---

copyright:
  years: 2018, 2024
lastupdated: "2024-08-22"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

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

You can add a virtual server instance to a placement group only at provisioning. 
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
     
You must remove assigned servers from the placement group before you can delete a placement group. To remove an instance from a placement group, you must delete or reclaim the instance.
{: note}
