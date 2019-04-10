---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Reconfiguring an existing virtual server
{: #reconfiguring-virtual-servers}

After a virtual server is provisioned, you can upgrade or downgrade its configuration at any time.  

**Important note:** There are various public virtual servers available in pre-set profiles. For a limited time, you can modify any virtual servers that were available before pre-set profiles. Then, you will be required to migrate or cancel the existing instances and reorder.

You cannot modify the individual core, RAM, or disk size of a virtual server that uses profiles. You must pick a different profile that has the pre-set cores, RAM, and disk size you need. The virtual server profile you select determines the valid cores, RAM, and disk sizes.  

Dedicated virtual servers are more customizable; therefore, you can modify the individual cores, RAM, and disk sizes.

Use the following steps to reconfigure an existing virtual server.
{:shortdesc}

## Modifying an existing virtual server (that uses pre-set profiles)
1. Access the [console](https://cloud.ibm.com/classic?){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon") with the credentials that you received in an email when your account was initially created. Alternatively, you can log in to the [{{site.data.keyword.slportal}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){:new_window}. 
2. From the Device List, click the name of the virtual server that you want to reconfigure.
3. On the **Configuration** tab, you can click **Modify** or **Modify device configuration** to update the following items.
  <dl>
  <dt>Size</dt>
  <dd>Select a new size.</dd>
  <p><note>Note: When you modify a profile that uses local storage, you cannot switch to a profile that uses non-local storage. Likewise, when you modify a profile that uses non-local storage, you cannot switch to a profile that uses local storage.
  </note></p>
  </dl>
4. After you specify changes for the virtual server, complete the configuration update.
  <dl>

  <dt>Upgrade date</dt>
  <dd>You can click the Immediately check box for an immediate update, or schedule a time for the update to become active.</dd>

  <dt>Upgrade time</dt>
  <dd>Enter the date (YYYY-MM-DD) for the update to become active.</dd>

  <dt>Notes</dt>
  <dd>Enter any applicable notes for your device. </dd>
  </dl>

5. Click **Continue**.
6. Review your order confirmation for accuracy.  Click **Edit** to edit your upgrade.
7. Click **Confirm** to confirm your order and apply the changes to your device.

## Modifying an existing virtual server (before pre-set profiles) or a dedicated virtual server
1. From the Device List, click the name of the virtual server that you want to reconfigure.
2. On the **Configuration** tab, you can click **Core or RAM upgrade** link to update the following items.

|   Upgrade options       |  Description                                                                                                |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| Upgrade Date            | Enter the date (YYYY-MM-DD) for the update to become active.                                                |
| Upgrade Time            | Select the time from the drop down boxes for the time of the day for the update to become active, or click the **Immediate** checkbox for an immediate update.                                                                                        |
| Cores                   | Select the number of cores for the update, if applicable. |
| RAM                     | Select the amount of RAM to apply to your device for the update, if applicable.   |
| Uplink Port Speeds      | Select the new uplink port speeds for your device, if applicable. |
| Public Bandwidth        | Select the amount (in GB) of public bandwidth for your device, if applicable.   |
| First Disk – Fifth Disk | Select the disk space/storage option for your first disk, if applicable. See **Disk Notes** below for more information.                                                                                                                               |
| Notes                   | Enter any applicable notes for your device.                                                                 |
{: caption="Table 1. Deployment options" caption-side="top"}   

  **Disk Notes:**
  * Both Local and SAN storage is available.  Double check your selection to ensure your storage option is correct.
  * For public virtual servers, if you are upgrading local storage and require more core or RAM, you might lose your secondary disk. When you modify a virtual server profile that uses local storage, the profile is pre-set for you and profiles that are not comparable cannot be selected.
3. Click **Continue**.
4. Review your order confirmation for accuracy.  Click **Edit** to edit your upgrade.
5. Click **Confirm** to confirm your order and apply the changes to your device.
