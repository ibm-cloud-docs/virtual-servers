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


# Archived 6/3/19 - Managing virtual servers that support suspend billing
{: #managing-virtual-servers}

From the Device List, you can manage virtual servers and other devices such as bare metal servers and VLAN firewalls.
{: shortdesc}

## Before you begin

1. Ensure you have provisioned a virtual server instance that supports suspend billing.

   In the device list, virtual servers that support suspend billing have a device type of *Virtual* and must meet the requirements, as described in [About suspend billing](/docs/virtual-servers?topic=virtual-servers-requirements).
2. Ensure you have the required permissions assigned to your user account. For more information, see [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access#managing-device-access).

Complete the following steps to perform management tasks for your virtual servers from the Device List in the Customer Portal:  
1. Log in to the [{{site.data.keyword.slportal_full}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
2. From the **Devices** menu, select **Device List**.
3. Click **Actions** for the device you want to manage and select the wanted management task.

If the virtual server supports suspend billing and has been powered off, billing is suspended for some compute resources until the virtual server is powered on again. For more information, see [About suspend billing](/docs/virtual-servers?topic=virtual-servers-requirements). When the device is powered on, billing resumes and you can manage the instance again.

## Next Steps
For information about other management tasks you can perform, see [Managing virtual servers](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
