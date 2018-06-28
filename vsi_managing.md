---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Managing virtual servers
{: #managing-virtual-servers}

From the Device List, you can manage virtual servers and other devices such as bare metal servers and VLAN firewalls.
{:shortdesc}

In the device list, virtual servers have a device type of *Virtual*. Bare metal servers are indicated with the device type of *Server*. Dedicated hosts have a device type of *Dedicated Virtual Host*. Many interactions available for the devices are similar, but each type of device also has device-specific interactions.

The following virtual server management tasks are available to you from the device list:
* Reboot -  immediately power off a device and then power it back on again.
* Power On / Off - remotely turn a device on or off.
* Rename - change or update a device name.
* Cancel - end use of a device. Devices can be canceled immediately or on a billing anniversary. After you confirm the cancellation of your device, the action cannot be undone. Refunds cannot be given for immediate cancellations.

Complete the following steps to perform management tasks for your virtual servers from the Device List in the Customer Portal:  
1. Log in to the [{{site.data.keyword.slportal_full}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials. 
2. From the **Devices** menu, select **Device List**.
3. Click **Actions** for the device you want to manage and select the wanted management task.

**Tips:** 
* You can interact with servers in the {{site.data.keyword.slportal}} in both the Snapshot view (a summary of your device) and on the Device Details screen (a fully detailed list). To view and interact with your server in the Snapshot View, click the arrow next to the Device Name to expand the view. To view and interact with your server on the Device Details screen, click the Device Name of the server.
* You can add notes to a device at any time from the **Configuration** tab. Notes can help identify details about the device, its use, and actions that have been taken on the device.

## What happens next
* **Reboot**

    A reboot is one of the most basic device actions. Rebooting a device results in the immediate powering off and then back on of your device and is done for many reasons, often specific to the device or business needs of the individual user. Device reboots can take place from both the Device List and from the Device View of an individual device. Virtual Servers can be rebooted at any time.  

* **Power On/Off**

    If the device has been powered off, the device remains in the power off state and must be manually powered on by repeating the steps above. Users may not interact with a device when a device is powered off. If the device has been powered on, normal interaction may take place. It will remain on until further action is taken. If the virtual server supports the suspend billing feature, billing is suspended for some compute resources. You cannot complete all management actions on an instance until billing is resumed. Suspend billing is only supported on new provisions, not existing instances. For more information, see [About suspend billing](vsi_about_suspend.html).

* **Rename**

  After renaming the device, the name will automatically be updated in the {{site.data.keyword.slportal}}. When performing a search within the {{site.data.keyword.slportal}}, use the new device name when attempting to locate content associated with it. Repeat the previous steps to rename the device again at any time.

* **Cancel**

  After confirming the cancellation, the device cancellation process will begin. If an immediate cancellation was requested, the device will be canceled immediately. If a billing anniversary cancellation was requested, the device will remain active until the next billing anniversary. Upon its cancellation, the device will no longer appear in the Device List on the {{site.data.keyword.slportal}}. Billing items will also be removed from invoices when all outstanding balances have been paid on the device, if any. For questions about a bill for a canceled device, please open a ticket and select Accounting Request as the ticket subject. Refunds cannot be given for immediate cancellations.
  
## Next Steps
If you need to reconfigure an existing virtual server, see [Reconfiguring an existing virtual server](../vsi/vsi_reconfigure.html).

