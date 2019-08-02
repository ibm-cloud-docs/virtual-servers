---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Launching rescue mode
{: #launching-rescue}

Rescue mode is a live rescue environment designed to provide you with the ability to bring a bare metal server or virtual server online in order to troubleshoot system issues that would normally only be resolved through OS Reload. Rescue mode must be initiated in the {{site.data.keyword.cloud}} console. Use the following steps to launch rescue mode for a device.
{:shortdesc}

## Before you begin
First, navigate to the device menu and ensure you have the correct account permissions to complete the tasks.

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/vsi?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Launching rescue mode

1. From the **Devices** menu, select **Device List**.
2. From the **Device List**, click the device name that you want to rescue.
3. In the *Actions* menu, select **Rescue mode**.
4. Click **Yes** to transition your device to rescue mode immediately.

## Launching rescue mode for a Windows instance

1. From the **Devices** menu, select **Device List**.
2. From the **Device List**, click the device name that you want to rescue.
3. In the *Actions* menu, select **Boot from image**.
4. Select **Boot from this image** next to the public image, *WindowsRescueStandalone.iso*.

## Next steps
After launching rescue mode, the device is powered down and rebooted into rescue mode for the device's operating system. This might take several minutes.

Remote access to the device is available from the device's IP address. You can access the device in rescue mode by using the root or admin credentials for the devices that are recorded in the {{site.data.keyword.cloud_notm}} console. When using rescue mode, you can troubleshoot, discover issues, and resolve issues as you would on a regularly booted device. If necessary, you can mount drives into the rescue mode OS. To exit rescue mode and return your device to its regular environment, reboot the device in the {{site.data.keyword.cloud_notm}} console or reboot from rescue mode OS.

For more information about rebooting a device, see [Managing virtual servers](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
