---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:note: .note}
{:new_window: target="_blank"}

# Managing placement groups
{: #vsi_managing_placegroup}

You can manage placement groups by using the placement groups page or the device details page in the {{site.data.keyword.cloud}} console.
{:shortdesc}

## Adding placement groups

To add placement groups from the placement groups page, complete the following steps:
{:shortdesc}

1. Open the [Placement groups ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window} page.
2. On the placement groups page, click **New group**.
3. Enter a name, location, pod, and rule for the placement group, and click **Create**.

Existing instances cannot be added to a placement group; you can only add a virtual server instance to a placement group at provisioning. 
{:note}

## Managing placement groups

To manage placement groups from the placement groups page, complete the following steps:
{:shortdesc}

1. Open the [Placement groups ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window} page.
2. Under the placement group section, you can complete several management tasks.
     * View a list of placement groups and number of assigned instances
     * Add a group
     * Rename a group
     * Provision an instance
     * Delete a group
     
You must remove assigned servers from the placement group before the placement group can be deleted. To remove an instance from a placement group, you must delete or reclaim the instance.
{:note}
