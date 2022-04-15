---

copyright:
  years: 2017, 2022
lastupdated: "2022-04-15"

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
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/account?topic=account-infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Resizing an existing virtual server 
{: #resizing-an-existing-virtual-server}

Complete the following steps to resize an existing virtual server that uses pre-set profiles.

1. From the **Devices** menu, select **Device List**.
2. From the **Device List**, click the name of the virtual server that you want to resize.
3. Select **Resize**.
4. In the **Resize window** section, specify the window of time your system is down to perform the update. You can select **Immediately** for an immediate update, or schedule a time for the update to become active by choosing a date and time for the update. You can also specify any applicable notes for your device.
5. In the **Profiles** section, select a new profile configuration for your device. 

   When you modify a profile that uses local storage, you cannot switch to a profile that uses nonlocal storage. Likewise, when you modify a profile that uses nonlocal storage, you cannot switch to a profile that uses local storage.
   {: note}

6. If you need extra storage, you can attach storage disks to your device.
7. Click **Resize** to confirm your order and apply the changes to your device.

## Resizing an existing virtual server (before pre-set profiles) or dedicated virtual server
{: #resizing-a-dedicated-virtual-server}

Complete the following steps to resize an existing virtual server (before pre-set profiles) or a dedicated virtual server.

1. From the **Device** menu, select **Device List**.
2. From the **Device List**, click the name of the virtual server that you want to resize.
3. Select **Resize**.
4. In the **Resize window** section, specify the window of time your system is down to perform the update. You can select **Immediately** for an immediate update, or schedule a time for the update to become active by choosing a date and time for the update. You can also specify any applicable notes for your device.
5. In the **Computing instance** section, you can select new vCPU and RAM for your device. 
6. If you need extra storage, you can attach storage disks to your device. The type of storage disks that are available to you depend on the profile that you select.

   For public virtual servers, if you are upgrading local storage and require more vCPU or RAM, you might lose your secondary disk. When you modify a virtual server profile that uses local storage, the profile is preset for you. You can't select profiles that aren't comparable.
   {: note}

7. Click **Resize** to confirm your order and apply the changes to your device.

