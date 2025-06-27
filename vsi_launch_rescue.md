---

copyright:
  years: 2017, 2025
lastupdated: "2025-06-27"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Starting rescue mode
{: #launching-rescue}

Rescue mode is a live rescue environment that is designed to provide you with the ability to bring a server online to troubleshoot system issues that are resolved only through OS Reload. Rescue mode must be initiated in the {{site.data.keyword.cloud}} console. Use the following steps to start rescue mode for a device.
{: shortdesc}

## Before you begin
{: #before-you-begin-launching-rescue-mode}

First, go to the device menu and make sure that you have the correct account permissions to complete the tasks.

* Go to your console's device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Starting rescue mode
{: #launching-rescue-mode}

To start rescue mode, use the following steps.

CentOS version 7 and higher requires a minimum of 6 GB of RAM for any Linux&reg; virtual server configuration. For a Linux&reg; virtual server configuration with less than 6 GB of RAM, CentOS version 5 is used.
{: important}

1. From the **Devices** menu, select **Device List**.
2. From the **Device List**, click the device name that you want to rescue.
3. In the *Actions* menu, select **Rescue mode**.
4. Click **Yes** to change your device to rescue mode immediately.

## Starting rescue mode for a Windows instance
{: #launching-rescue-mode-for-a-Windows-instance}

1. From the **Devices** menu, select **Device List**.
2. From the **Device List**, click the device name that you want to rescue.
3. In the *Actions* menu, select **Boot from image**.
4. Select **Boot from this image** next to the public image, *WindowsRescueStandalone.iso*.

## Next steps
{: #next-steps-launching-rescue-mode}

After you start rescue mode, the device is powered down and restarted into rescue mode for the device's operating system. This process might take several minutes.

Remote access to the device is available from the device's IP address. You can access the device in rescue mode by using the root or admin credentials for the devices that are recorded in the {{site.data.keyword.cloud_notm}} console. When you use rescue mode, you can troubleshoot, discover issues, and resolve issues as you would on a regularly started device. If necessary, you can mount drives into the rescue mode. 

To exit rescue mode and return your device to its regular environment, restart the device in the {{site.data.keyword.cloud_notm}} console or restart from rescue mode OS. To restart from the console, go to the *Actions* menu then select **Boot from image**. If prompted for your device type, select **Continue** to unload the current image and return to normal booting.
