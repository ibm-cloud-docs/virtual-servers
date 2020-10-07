---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# Managing portable storage
{: #accessing-portable-storage}

Portable storage volumes (PSVs) are an auxiliary storage solution exclusively for {{site.data.keyword.virtualmachinesshort}}. Within the {{site.data.keyword.cloud}} console, you can access portable storage volumes and display all PSVs. You can also attach, detach, swap, and edit volumes.
{:shortdesc}

You can't attach or swap portable storage volumes to a virtual server instance that is provisioned from an encrypted image template.
{:note}

## Before you begin
{: #before-you-begin-managing-portable-storage}

First, navigate to the storage or devices menu and ensure you have the correct account permissions to complete the tasks.

* Navigate to your console's storage or device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/account?topic=account-infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Attaching portable storage
{: #attaching-portable-storage}

1. From the **Storage** menu, select **Block Storage.**
2. In the **Portable storage** section, select the attach option for the portable storage you want to use.
3. On the next screen, choose the device that needs the storage, and select **Attach.**

## Managing portable storage attached to a server
{: #managing-portable-storage-attached-to-a-server}

Portable storage attached to a server is listed on the server's *Device Details* page.

1. From the **Devices** menu, select **Device List.**
2. From the **Device List**, select a virtual server instance to view its details.
3. Click the **Storage** tab to view the portable storage currently attached to the instance.
4. In the **Actions** menu, you can **Swap** or **Detach** the storage.
