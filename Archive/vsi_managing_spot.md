---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Archived 6/3/19 - Managing virtual servers
{: #managing-virtual-servers}

From the Device List, you can manage virtual servers and other devices such as bare metal servers and VLAN firewalls.
{: shortdesc}

In the device list, virtual servers have a device type of *Virtual*. Bare metal servers are indicated with the device type of *Server*. Dedicated hosts have a device type of *Dedicated Virtual Host*. Many interactions available for the devices are similar, but each type of device also has device-specific interactions.

The following virtual server management tasks are available to you from the device list:
* Reboot -  immediately power off a device and then power it back on again.
* Power On / Off - remotely turn a device on or off.

    When some virtual server instances are powered off, billing is also suspended. For more information, see [About suspend billing](/docs/virtual-servers?topic=virtual-servers-requirements).
    {: tip}

* Rename - change or update a device name.
* Cancel - end use of a device. Devices can be canceled immediately or on a billing anniversary. After you confirm the cancellation of your device, the action cannot be undone. Refunds cannot be given for immediate cancellations.

Complete the following steps to perform management tasks for your virtual servers from the Device List in the Customer Portal:  
1. Log in to the [{{site.data.keyword.slportal_full}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
2. From the **Devices** menu, select **Device List**.
3. Click **Actions** for the device you want to manage and select the wanted management task.

* You can interact with servers in the {{site.data.keyword.slportal}} in both the Snapshot view (a summary of your device) and on the Device Details screen (a fully detailed list). To view and interact with your server in the Snapshot View, click the arrow next to the Device Name to expand the view. To view and interact with your server on the Device Details screen, click the Device Name of the server.
* You can add notes to a device at any time from the **Configuration** tab. Notes can help identify details about the device, its use, and actions that have been taken on the device.
{: tip}

## What happens next
* **Power On/Off**

    If the device has been powered off, the device remains in the power off state and must be manually powered on by repeating the steps above. Users may not interact with a device when a device is powered off. If the device has been powered on, normal interaction may take place. It will remain on until further action is taken.

    If the virtual server supports suspend billing and has been powered off, billing is suspended for some compute resources until the virtual server is powered on again. For more information, see [About suspend billing](/docs/virtual-servers?topic=virtual-servers-requirements). When the device is powered on, billing resumes and you can manage the instance again.

* **Rename**

    After renaming the device, the name will automatically be updated in the {{site.data.keyword.slportal}}. When performing a search within the {{site.data.keyword.slportal}}, use the new device name when attempting to locate content associated with it. Repeat the previous steps to rename the device again at any time.

* **Cancel**

    After confirming the cancellation, the device cancellation process will begin. If an immediate cancellation was requested, the device will be canceled immediately. If a billing anniversary cancellation was requested, the device will remain active until the next billing anniversary. Upon its cancellation, the device will no longer appear in the Device List on the {{site.data.keyword.slportal}}. Billing items will also be removed from invoices when all outstanding balances have been paid on the device, if any. For questions about a bill for a canceled device, please open a ticket and select Accounting Request as the ticket subject. Refunds cannot be given for immediate cancellations.

* **Reboot**

    A reboot is very helpful when experiencing an issue in which the server cannot boot to the operating system because of a configuration issue.  You can also boot into the Rescue Kernel. After booting to the Rescue Kernel, you can mount the drive/drives of your server, and then fix the configuration issue. Once the issue has been fixed, just reboot the server from the command line, and the server will reboot into the default kernel for your server.

    After you have issued the reboot, you will see an estimated time of completion.

## Next Steps
If you need to reconfigure an existing virtual server, see [Reconfiguring an existing virtual server](/docs/virtual-servers?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).
