---



copyright:
  years: 2017
lastupdated: "2017-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Launching a rescue kernel 
{: #launching-rescue}

Rescue Kernel is a live rescue environment, designed to provide customers with the ability to bring a bare metal server or virtual server online in order to troubleshoot system issues that would normally only be resolved through OS Reload. Rescue Kernel must be initiated on the Customer Portal. Use the following steps to launch Rescue Kernel for a device.
{:shortdesc}

## Launch rescue kernel

1. From the Device List, click the device name that you want to rescue.
2. Click the *Actions* drop down list at the upper right corner, and select **Rescue**.
3. Click the **Yes** button to transition your device to Rescue Kernel immediately. Click the **No** button to cancel the action.

## What's Next?
After launching Rescue Kernel, the device is powered down and rebooted into the rescue kernel for the device's operating system. This may take several minutes.

Remote access to the device is available from the device's IP address. You can access the device in Rescue Kernel by using the root or admin credentials for the devices that are recorded on the Customer Portal. When using Rescue Kernel, you can troubleshoot, discover issues, and resolve issues as you would on a regularly booted device. If necessary, you can mount drives into the Rescue Kernel OS. To exit Rescue Kernel and return your device to its regular environment, reboot the device in the Customer Portal or reboot from Rescue Kernel OS.

For more information about rebooting a device or about the rescue kernel, see the following resources:
* How to reboot a device, see [Managing virtual servers](../vsi/vsi_managing.html).
* About the rescue kernel, see [Rescue Kernel for Windows ![External link icon](../icons/launch-glyph.svg "External link icon")](http://knowledgelayer.softlayer.com/procedure/rescue-kernel-windows){: new_window}.
