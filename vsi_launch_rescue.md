---



copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Launching a rescue kernel 
{: #launching-rescue}

Rescue Kernel is a live rescue environment, designed to provide customers with the ability to bring a bare metal server or virtual server online in order to troubleshoot system issues that would normally only be resolved through OS Reload. Rescue Kernel must be initiated on the {{site.data.keyword.slportal_full}}. Use the following steps to launch Rescue Kernel for a device.
{:shortdesc}

## Launch Rescue Kernel

1. Access the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) by using your unique credentials.
2. From the Device List, click the device name that you want to rescue.
3. Click the *Actions* drop down list at the upper right corner, and select **Rescue**. (Alternatively, you can click the *Remote Mgmt* tab and select **Rescue**.)
4. Click the **Yes** button to transition your device to Rescue Kernel immediately. Click the **No** button to cancel the action.

## On Windows VSI

1. Access the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) by using your unique credentials.
2. From the Device List, click the device name that you want to rescue.
3. Click the *Actions* drop down list at the upper right corner, and select **Boot from Image**.
4. Select **Boot From This Image** next to the public image, *WindowsRescueStandalone.iso*.


## Next Steps
After launching Rescue Kernel, the device is powered down and rebooted into the rescue kernel for the device's operating system. This may take several minutes.

Remote access to the device is available from the device's IP address. You can access the device in Rescue Kernel by using the root or admin credentials for the devices that are recorded on the {{site.data.keyword.slportal}}. When using Rescue Kernel, you can troubleshoot, discover issues, and resolve issues as you would on a regularly booted device. If necessary, you can mount drives into the Rescue Kernel OS. To exit Rescue Kernel and return your device to its regular environment, reboot the device in the {{site.data.keyword.slportal}} or reboot from Rescue Kernel OS.

For more information about rebooting a device, see [Managing virtual servers](/docs/vsi/vsi_managing.html).

