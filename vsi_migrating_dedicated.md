---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Migrating a dedicated host instance to another host
{: #migrating-dedicated-host}

You can migrate your dedicated host instances from one host to another within the same POD. Select the instance to be migrated from either the host’s device details page or the instance’s device details page. Note that only two instances can be migrated at a time and the time needed to migrate depends on the disk. SAN disks are migrated quicker because local disks require copying the disk. The migrating instances are offline while being migrated; the host does remain up for any of its other dedicated host instances.
{:shortdesc}

## Before you begin
First, navigate to the device menu and ensure you have the correct account permissions to complete the tasks.

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/vsi?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Migrating from the dedicated host
Use the following steps to migrate dedicated host instances to another dedicated host within the same POD from the device details page of the *original dedicated host*. 

1. From the **Devices** menu, select **Device List**.
2. Select either the host or the hosted instance from the list.
3. Click the **Actions** drop-down list next to the dedicated instance to be migrated.
4. Select **Migrate** and enter the host where the instance is migrating to; remember, the target host must be within the same POD as the original host.
5. Click **Migrate** to begin the migration. 

The migration begins immediately. During the migration, the dedicated instance is offline until on its new host. You can view the target host’s Device Details page to make sure the instance migrated correctly.

## Migrating from the dedicated instance
Use the following steps to migrate dedicated host instances to another dedicated host within the same POD from the details page of the *dedicated host instance*.

1. From the **Devices** menu, select **Device List**.
2. Select the hosted instance to be migrated from the list.
3. Click **Migrate**.
4. Select the target host to migrate the instance to; remember, the target host must be within the same POD as the original host.
5. Click **Migrate** to begin the migration.

The migration begins immediately. During the migration, the dedicated instance is offline until on its new host. You can view the target host’s device details page to make sure the instance migrated correctly.

## Next steps
After you migrate a dedicated host instance, confirm the migration worked by verifying that its status is green on the new dedicated host's device details page.

