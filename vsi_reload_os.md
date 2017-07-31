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

#  Reloading the OS
You can reload the operating system (OS) on a device at any time to restore a device to its original working order, or to reconfigure a device with different software. An OS reload removes all data from the device and applies a "like new" configuration, as specified during the configuration process of the OS Reload setup. Because OS reloads clear all data from the device, if the data has not been backed up prior to the reload, it is permanently deleted and cannot be retrieved.
{:shortdesc}

**Important:** If you want to retain your data, back up all data prior to performing a reload.

## Performing the reload
1. From the **Device List**, click the server that needs an OS Reload.
2. From the **Actions** menu on the top left of the page, select **OS Reload**.
3. Determine if you want to reload the existing configuration or reload the device with with a new configuration.

   <table>
   <CAPTION>Table 1. OS reload options</CAPTION>
   <THEAD>
   <TR>
   <th>Reload type</th>
   <th>Steps</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>If you want to reload using a new configuration...</td>
   <td>
   <ol>
   <li>Click <b>Edit</b> for the Category that requires an update.</li>
   <li>Select the new software to apply to the device from the <i>Select Software</i> drop down list.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>If you want to reload using the existing configuration...</td>
   <td>Proceed to the next step.</td>
   </tr>
   </TBODY>
   </table>

4. Determine if a Post Install script should be applied after the device is provisioned.

   If you want to apply a post installation script, select the script from the Existing Script drop down list or enter the qualified URL for the new script.  Otherwise, proceed to the next step.

5. For physical devices, determine if installed partitions should be added, removed, or remain unchanged.
   
   <table>
   <CAPTION>Table 2. Partition action options</CAPTION>
   <THEAD>
   <TR>
   <th>Partition action</th>
   <th>Steps</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>To add installed partitions...</td>
   <td>
   <ul>
   <li>Click the <b>Add Another Partition</b> link.</li>
   <li>Enter the exact name of the partition.</li>
   <li>Enter the parition size (in GBs). If you want, you can select Grow to grow the partition to fill the remaining disk space.
   <p><b>Note:</b> Only one partition can be selected to grow at any time. This partition is larger than the specified size, and fills all available capacity. The capacity of the Grow partition is calculated by subtracting the combined size of all other partitions from the Total Capacity number that is provided in the Installed Partitions section.</p>
   </li>
   </ul>
   </td>
   </tr>
   <tr>
   <td>To delete installed partitions...</td>
   <td>Click the <b>Delete</b> icon to delete the partition.</td>
   </tr>
   <tr>
   <td>To remain unchanged...</td>
   <td>Proceed to the next step.</td>
   </tr>
   </TBODY>
   </table>
    
6. Determine whether to apply one or more SSH Keys to the device.

7. Select the applicable checkboxes for the desired options that you want to be applied to the device during or after the OS Reload.

   **Note:** Options vary based on device. Not all options are available for every device.

8. Click the **Reload Above Configuration** button to proceed to the Review pop-up. Click the **Cancel** button to cancel the changes to the device and exit the screen.

9. Verify that all details in the New Configuration section are correct.  

10. Click the **Confirm OS Reload** button to confirm and initiate the OS Reload. Click the **Cancel** button to cancel the action.

## What's Next?
After initiating the OS Reload process, the device is taken offline and the OS Reload process begins.
The time period in which an OS reload takes place varies based on the current and new configuration of the device.
Throughout the configuration process, the minimum time for the OS Reload is displayed on each screen.
The timeframe displayed is an estimate made by the system and is given as a courtesy. If the reload takes longer than 24 hours,
please contact our Support team. When the device returns online, it functions as specified in the New Configuration for the OS Reload. All data previously saved to the device is lost, but can be restored if a backup was made of the device prior to its reload.
If data was not backed up, it cannot be retrieved.
 
To re-register your device with eVault, see [Re-registering your device with eVault ![External link icon](../icons/launch-glyph.svg "External link icon")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
