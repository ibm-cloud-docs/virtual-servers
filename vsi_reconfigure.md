---

copyright:
  years: 2017, 2024
lastupdated: "2023-10-23"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Reconfiguring an existing virtual server
{: #reconfiguring-virtual-servers}

After you provision {{site.data.keyword.BluVirtServers}}, you can upgrade or downgrade your server configurations at any time.
{: shortdesc}

Various public virtual servers are available in pre-set profiles. For a limited time, you can modify any virtual servers that were available before pre-set profiles. Then, you are required to migrate or cancel the existing instances and reorder.
{: important}

You cannot modify the individual core, RAM, or disk size of a virtual server that uses profiles. You must pick a different profile that has the pre-set cores, RAM, and disk size you need. The virtual server profile that you select determines the valid cores, RAM, and disk sizes.

Dedicated virtual servers are more customizable than public virtual servers. Therefore, you can modify the individual cores, RAM, and disk sizes.

## Before you begin
{: #before-you-begin-reconfiguring-virtual-server}

First, go to the device menu, and make sure that you have the correct account permissions to complete the tasks.

* Go to your console device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions. For more information about permissions, see [Classic infrastructure permissions](/docs/account?topic=account-infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

Resizing or reconfiguring a virtual server initiates a system restart.
{: important}

## Resizing an existing virtual server
{: #resizing-an-existing-virtual-server}

Complete the following steps to resize an existing virtual server that uses pre-set profiles.

1. From the **Devices** menu, select **Device List** and click the name of the virtual server that you want to resize.
2. Select **Resize**.
3. In the **Resize window** section, specify the window of time your system is down to perform the update. You can select **Immediately** for an immediate update, or schedule a time for the update to become active by choosing a date and time for the update. You can also specify any applicable notes for your device.
4. In the **Profiles** section, select a new profile configuration for your device.

   When you modify a profile that uses local storage, you cannot switch to a profile that uses nonlocal storage. Likewise, when you modify a profile that uses nonlocal storage, you cannot switch to a profile that uses local storage.
   {: note}

5. If you need extra storage, you can attach storage disks to your device.
6. Click **Resize** to confirm your order and apply the changes to your device.

## Resizing an existing virtual server (before pre-set profiles) or dedicated virtual server
{: #resizing-a-dedicated-virtual-server}

Complete the following steps to resize an existing virtual server (before pre-set profiles) or a dedicated virtual server.

1. From the **Device** menu, select **Device List** and click the name of the virtual server that you want to resize.
2. Select **Resize**.
3. In the **Resize window** section, specify the window of time your system is down to perform the update. You can select **Immediately** for an immediate update, or schedule a time for the update to become active by choosing a date and time for the update. You can also specify any applicable notes for your device.
4. In the **Computing instance** section, you can select a new vCPU and RAM for your device.
5. If you need extra storage, you can attach storage disks to your device. The type of storage disks that are available to you depend on the profile that you select.

   For public virtual servers, if you are upgrading local storage and require more vCPU or RAM, you might lose your secondary disk. When you modify a virtual server profile that uses local storage, the profile is preset for you. You can't select profiles that aren't comparable.
   {: note}

6. Click **Resize** to confirm your order and apply the changes to your device.

## Mounting and configuring disks on Windows
{: #mount-configure-disks-windows}

If you added storage disks when you resized a virtual server, the disks aren't usable until they are configured. Use the following steps to configure new storage disks.

1. From the Windows search bar, enter `Disk management` and click **Create and format hard disk partitions** to open the Disk Management tool.
2. In the **Initialize Disk** prompt, select the disks that you want to initialize and click **OK**. Your new disks are ready to initialize and appear in the last section of the tool.
3. Right-click the disk that you want to initialize and select **New simple volume**. The **New Simple Volume Wizard** opens.
4. Follow the steps in the volume wizard and select all the appropriate information for the disk.
5. After you click **Finish**, repeat steps 2-4 for each disk that you want to initialize.
6. You can now access your new disks from the file explorer.
