---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-19"

keywords: manage virtual servers, power off, replicate, manage device reload os, delete server, manage server

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Managing virtual servers
{: #managing-virtual-servers}

You can manage virtual servers, along with other devices, from the device details list.
>>>>>>> origin/master
{:shortdesc}


## Before you begin
First, navigate to the device menu and ensure you have the correct account permissions to complete the tasks.

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/vsi?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Device types
The device details list shows you the following device types:

| Device  | Device type  |
| ------  | ------------ |
| Virtual servers | Virtual |
| Bare metal servers | Server |
| Dedicated hosts | Dedicated virtual host |
{: caption="Table 1. Device types" caption-side="top"}

The actions that you see depend on the device type, as well as the permissions that are granted to your user account.

Complete the following steps to perform management tasks for your servers.

1. From the **Devices** menu, select **Device List**.
2. Click **Actions** for the device you want to manage and select the relevant task.

* You can interact with servers in the {{site.data.keyword.cloud_notm}} console in both the snapshot view (a summary of your device) and on the device's details page (a fully detailed list). To view and interact with your server in the snapshot view, click the arrow next to the Device Name to expand the view. To view and interact with your server on the device's details page, click the Device Name of the server.

* You can add notes to a device at any time from the **Configuration** tab. Notes can help identify details about the device, its use, and actions that have been taken on the device.
 {:tip}

## Reboot
A reboot is one of the most basic device actions. Rebooting a device results in the immediate powering off and then back on of your device and is done for many reasons, often specific to the device or business needs of the individual user. Device reboots can take place from both the Device List and from the Device View of an individual device. Virtual Servers can be rebooted at any time.

A reboot is very helpful when experiencing an issue in which the server cannot boot to the operating system because of a configuration issue.  You can also boot into the Rescue Kernel. After booting to the Rescue Kernel, you can mount the drive/drives of your server, and then fix the configuration issue. Once the issue has been fixed, just reboot the server from the command line, and the server will reboot into the default kernel for your server.
{:tip}

## Power On/Off
If the device has been powered off, the device remains in the power off state and must be manually powered on by repeating the steps above. Users cannot interact with a device when a device is powered off. If the virtual server supports the suspend billing feature, billing is suspended for some compute resources. You cannot complete all management actions on an instance until billing is resumed. For more information, see [Suspend billing](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing). To find out if your virtual server instance supports the suspend billing feature, see [Viewing suspend billing feature](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature#viewing-suspend-billing-feature). If the device has been powered on, normal interaction can take place. It will remain on until further action is taken.

## Rename
After renaming the device, the name is automatically updated in the {{site.data.keyword.cloud_notm}} console. When performing a search within the {{site.data.keyword.cloud_notm}} console, use the new device name when attempting to locate content associated with it. Repeat the previous steps to rename the device again at any time.

## Cancel
If you cancel a device, you end use the of that device. Devices can be canceled immediately or on a billing anniversary. After you confirm the cancellation of your device, the action cannot be undone. Refunds cannot be given for immediate cancellations.

After confirming the cancellation, the device cancellation process will begin. If an immediate cancellation was requested, the device will be canceled immediately. If a billing anniversary cancellation was requested, the device will remain active until the next billing anniversary. Upon its cancellation, the device will no longer appear in the Device List on the {{site.data.keyword.cloud_notm}} console. Billing items will also be removed from invoices when all outstanding balances have been paid on the device, if any. For questions about a bill for a canceled device, please [open a case](/unifiedsupport/cases/add) and select **Billing & usage** as the type of support needed. Refunds cannot be given for immediate cancellations.

## Next steps
{: #managing-virtual-servers-next-steps}
If you need to reconfigure an existing virtual server, see [Reconfiguring an existing virtual server](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).
