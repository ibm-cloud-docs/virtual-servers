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

# Reloading the OS using an image template
Similar to the standard OS Reload, reloading a device from an Image Template allows users to restore or reconfigure a device based off of a pre-existing image template that is associated with the Customer Portal account in use. During the standard OS Reload process, configuration options for the device can be selected individually, while the Load From Image feature loads the configuration exactly as it appears in the image template. You can still add optional features prior to performing the reload.
Use the following steps to perform an OS reload from an image template by using the Load From Image feature in the Customer Portal.
{:shortdesc}

## Performing the reload using an image template
1. Back up all data on the device.
  
   **Note:** OS Reloads results in all data being wiped from the hard drive. If data is not backed up prior to the initiation of the OS Reload, it cannot be retrieved. Bluemix (Softlayer) does not back up any data stored on customer devices and is not responsible for any loss of data associated with the OS Reload process.
  
2. From the Device List page, select **Load from Image** from the **Actions** menu for the desired device.

3. Select the desired image template check box to select the image template that will be loaded to the device.

   **Note:** Prior to completing the reload, the image template is copied to the data center that contains the device, if it is not already located in the same data center. If the image template must be copied to the appropriate data center, an additional fee might be charged if the template is not deleted from the location after the OS Reload occurs.
  
4. Determine if you want to add any optional features. Any optional features you select are added to the device as part of the reload process.
   
   <table>
   <CAPTION>Table 1. Optional features</CAPTION>
   <THEAD>
   <TR>
   <th>Optional Features</th>
   <th>Steps</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   </tr>
   <tr>
   <td>Yes, I want to add optional features.</td>
   <td>
   <ol>
   <li>Click <b>Load Selected Image</b>.</li>
   <li>Review the Image Configuration and proceed or cancel.</li>
   <li>Click <b>Confirm OS Reload</b> to confirm the action and begin the OS reload process.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>No, I do not want to add optional features.</td>
   <td>Click <b>View Optional Features</b>.</td>
   </tr>
   </TBODY>
   </table>

5. Configure additional options, as relevant. Refer to the following information for more details.
   
   <dl>
   <dt>Post Install script</dt>
   <dd>Adds an existing or new post installation script.</dd>
   <dt>SSH key</dt>
   <dd>Adds an SSH key to the device upon the reload action. </dd>
   <dt>Reset IPMI Password</dt>
   <dd> This option is only available for physical devices. </dd>
   <dt>Apply motherboard BIOS upgrades</dt>
   <dd>This option is only available for physical devices. </dd>
   <dt>Apply firmware updates for all hard drives</dt>
   <dd>This option is only available for physical devices.</dd>
   <dt>Add to Spare Pool after OS Reload</dt>
   <dd>This option is available only on physical devices and requires internal approval prior to being available on an account.</dd>
   <dt>Erase all hard drives</dt>
   <dd> This option is available only on physical devices and requires special user permissions set by the Account's administrator.</dd>
   <dt>OS Reload with Disk Preservation</dt>
   <dd>Retains all data on the current primary disk during the OS Reload process. Disk preservation results in the primary drive being converted to a Portable Storage device. This option is available only on virtual devices and incurs additional charges based on the billing patterns (hourly or monthly) of the device. Charges may be canceled by canceling the Portable Storage device any time after it has been created.</dd>
   </dl>

6. Click **Load Selected Image**.

7. Review the image configuration and click **Next** to proceed to the next screen or **Cancel** to cancel the action.

   **Note:** After clicking **Next**, all network ports for the device are systematically shut down and the device is unavailable for up to 15 minutes. During this time, the action can be canceled at any time by clicking **Cancel**. The next step must be completed within 15 minutes of clicking **Next** or the previous steps must be completed again. This process is in place as a safeguard to ensure no additional data is added to a device between the configuration confirmation and the OS Reload initiation.

8. Click **Confirm OS Reload** to confirm the action and begin the OS reload process. Click **Cancel** to cancel the action.

## What's Next?
After initiating the OS Reload process, the device is taken offline and the OS Reload process begins.
The time period in which an OS reload takes place varies based on the current and new configuration of the device.
If the reload takes longer than 24 hours, please contact our Support team. When the device returns online,
it functions as specified in the New Configuration for the OS Reload. All data previously saved to the device is lost,
but can be restored if a backup was made of the device prior to its reload. If data was not backed up, it cannot be retrieved.

 To re-register your device with eValut, see [Re-registering your device with eVault ![External link icon](../icons/launch-glyph.svg "External link icon")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
