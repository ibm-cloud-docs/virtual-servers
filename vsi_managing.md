---

copyright:
  years: 2017, 2021
lastupdated: "2021-07-26"

keywords: manage virtual servers, power off, replicate, manage device, reload os, delete server, manage server, cancel virtual server, cancel device, cancel server, restart, reboot, rename

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
{:shortdesc}


## Before you begin
{: #before-you-begin-managing-virtual-servers}

First, go to the device menu and ensure you have the correct account permissions to complete the tasks.

* Go to your console's device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/account?topic=account-infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Device types
{: #device-types-and-actions}

The device details list shows you the following device types:

| Device  | Device type  |
| ------  | ------------ |
| Virtual servers | Virtual |
| Bare metal servers | Server |
| Dedicated hosts | Dedicated virtual host |
{: caption="Table 1. Device types" caption-side="top"}

The actions that you see depend on the device type, and the permissions that are granted to your user account.

Complete the following steps to perform management tasks for your servers.

1. From the **Devices** menu, select **Device List**.
2. Click **Actions** for the device you want to manage and select the relevant task. See [Device tasks](#device-tasks) for relevant tasks. 

* You can interact with servers in the {{site.data.keyword.cloud_notm}} console in both the snapshot view (a summary of your device) and on the device's details page (a fully detailed list). To view and interact with your server in the snapshot view, click the arrow next to the Device Name to expand the view. To view and interact with your server on the device's details page, click the Device Name of the server.

* You can add notes to a device at any time from the **Configuration** tab. Notes can help identify details about the device, its use, and actions that were taken on the device.
 {:tip}

## Device tasks
{: #device-tasks}

The following are relevant tasks that you can do from the **Actions** menu as described the previous steps.

### Rebooting a device
{: #reboot}

A reboot is one of the most basic device actions. Rebooting a device results in the immediate powering off and then back on of your device. Device reboots can take place from both the Device List and from the Device View of an individual device. Virtual Servers can be rebooted at any time.

A reboot is helpful when you experience an issue in which the server cannot boot to the operating system because of a configuration issue.  You can also boot into rescue mode. After it boots into rescue mode, you can mount the drives of your server, and then fix the configuration issue. When the issue is fixed, reboot the server from the command line, and the server reboots into the default kernel for your server.
{:tip}

### Powering a device On or Off
{: #power-on-off}

If the device is powered off, the device remains powered off and must be manually powered on by repeating the previous steps. Users can't interact with a powered off device. If the virtual server supports the suspend billing feature, billing is suspended for some compute resources. You can't complete all management actions on an instance until billing is resumed. For more information, see [Suspend billing](/docs/virtual-servers?topic=virtual-servers-requirements). To find out whether your virtual server instance supports the suspend billing feature, see [Viewing suspend billing feature](/docs/virtual-servers?topic=virtual-servers-viewing-suspend-billing-feature#viewing-suspend-billing-feature). If the device is powered on, normal interaction can take place. The device remains on until further action is taken.

### Renaming a device
{: #rename}

After you rename a device, the name is automatically updated in the {{site.data.keyword.cloud_notm}} console. When a search is done within the {{site.data.keyword.cloud_notm}} console, use the new device name when you attempt to locate content that is associated with it. Repeat the previous steps to rename the device at any time.

### Connecting to the KVM console
{: #kvm-console}

The KVM console is a Java applet. Java must be installed before you can access the console. If Java is installed, make sure that a connection is established through the VPN. If a connection isn't established, a warning displays saying that a VPN connection is required. If you have connection issues with your KVM console, see [Why can I not connect to the KVM console?](/docs/virtual-servers?topic=virtual-servers-faqs-servers-general-#why-can-i-not-connect-to-the-kvm-console-).

If you have issues with incompatible Java settings in your browser, you can alternatively use the TightVNC viewer. You must download and install TightVNC viewer for Windows 64-bit version. For more information, see [How to connect to KVM console of IBM Cloud Virtual Servers](https://www.ibm.com/support/pages/how-connect-kvm-console-ibm-cloud-virtual-servers){: external} from the Support Center.
{:tip}

### Canceling a device
{: #cancel}

If you cancel a device, you end use of that device. Devices can be canceled immediately or on a billing anniversary. After you confirm the cancellation of your device, the action cannot be undone. Refunds can't be given for immediate cancellations.

After you confirm the cancellation, the device cancellation process begins. If an immediate cancellation was requested, the device is canceled immediately. If a billing anniversary cancellation was requested, the device remains active until the next billing anniversary. Upon its cancellation, the device no longer appears in the **Device List** on the {{site.data.keyword.cloud_notm}} console. Billing items are also removed from invoices when all outstanding balances are paid on the device, if any. For questions about a bill for a canceled device, [open a case](https://cloud.ibm.com/unifiedsupport/cases/add){: external} and select **Billing and usage** as the type of support needed. Refunds can't be given for immediate cancellations.

## Next steps
{: #managing-virtual-servers-next-steps}

If you need to reconfigure an existing virtual server, see [Reconfiguring an existing virtual server](/docs/virtual-servers?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).
