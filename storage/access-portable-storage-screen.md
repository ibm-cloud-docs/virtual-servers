---

copyright:
  years: 2014, {CURRENT_YEAR}]
lastupdated: "2024-07-25"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Managing portable storage
{: #accessing-portable-storage}

Portable storage volumes (PSVs) are an auxiliary storage solution exclusively for {{site.data.keyword.virtualmachinesshort}}. Within the {{site.data.keyword.cloud}} console, you can access portable storage volumes and display all PSVs. You can also attach, detach, swap, and edit volumes. Portable Storage Volumes (PSV) on virtual server instances are encrypted at rest.
{: shortdesc}

You can't attach or swap portable storage volumes to a virtual server instance that is provisioned from an encrypted image template because these PSVs are encrypted at rest.
{: note}

## Before you begin
{: #before-you-begin-managing-portable-storage}

First, go to the storage or devices menu and make sure that you have the correct account permissions to complete the tasks.

* Go to your console's storage or device menu. For more information, see [Going to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the `Manage users` classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Attaching portable storage
{: #attaching-portable-storage}

When you attach portable storage, the virtual server restarts while portable storage is attached or swapped.
{: important}

1. From the **Storage** menu, select **Block Storage.**
2. In the **Portable storage** section, select the attach option for the portable storage you want to use.
3. On the next screen, choose the device that needs the storage, and select **Attach.**

## Managing portable storage that is attached to a server
{: #managing-portable-storage-attached-to-a-server}

Portable storage attached to a server is listed on the server's *Device Details* page.

1. From the **Devices** menu, select **Device List.**
2. From the **Device List**, select a virtual server instance to view its details.
3. Click the **Storage** tab to view the portable storage that is attached to the instance.
4. In the **Actions** menu, you can select either **Swap** or **Detach** the storage.
