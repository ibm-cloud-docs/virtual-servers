---

copyright:
  years: 2017, 2024
lastupdated: "2021-04-20"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:important: .important}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Launching rescue mode
{: #launching-rescue}

Rescue mode is a live rescue environment that is designed to provide you with the ability to bring a bare metal server or virtual server online to troubleshoot system issues that would normally be resolved only through OS Reload. Rescue mode must be initiated in the {{site.data.keyword.cloud}} console. Use the following steps to start rescue mode for a device.
{: shortdesc}

## Before you begin
{: #before-you-begin-launching-rescue-mode}

First, go to the device menu and make sure that you have the correct account permissions to complete the tasks.

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/account?topic=account-infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Launching rescue mode
{: #launching-rescue-mode}

To launch rescue mode, use the following steps.

CentOS version 7 and higher requires a minimum of 6 GB of RAM for any Linux&reg; virtual server configuration. For a Linux&reg; virtual server configuration with less than 6 GB of RAM, CentOS version 5 is used.
{: important}

1. From the **Devices** menu, select **Device List**.
2. From the **Device List**, click the device name that you want to rescue.
3. In the *Actions* menu, select **Rescue mode**.
4. Click **Yes** to change your device to rescue mode immediately.

## Launching rescue mode for a Windows instance
{: #launching-rescue-mode-for-a-Windows-instance}

1. From the **Devices** menu, select **Device List**.
2. From the **Device List**, click the device name that you want to rescue.
3. In the *Actions* menu, select **Boot from image**.
4. Select **Boot from this image** next to the public image, *WindowsRescueStandalone.iso*.

## Next steps
{: #next-steps-launching-rescue-mode}

After you start rescue mode, the device is powered down and restarted into rescue mode for the device's operating system. This process might take several minutes.

Remote access to the device is available from the device's IP address. You can access the device in rescue mode by using the root or admin credentials for the devices that are recorded in the {{site.data.keyword.cloud_notm}} console. When you use rescue mode, you can troubleshoot, discover issues, and resolve issues as you would on a regularly started device. If necessary, you can mount drives into the rescue mode OS. To exit rescue mode and return your device to its regular environment, restart the device in the {{site.data.keyword.cloud_notm}} console or restart from rescue mode OS.

For more information about restarting a device, see [Managing virtual servers](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
