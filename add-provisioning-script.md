---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Managing provisioning scripts
{: #managing-a-provisioning-script}

You can use provisioning scripts to specify a URL to a script that runs on a newly provisioned device. Provisioning scripts can be any file that the operating system (OS) can run, including combined binary files or any OS-supported language. You have no restrictions for the script name; however, using a similar naming convention for each script makes it easier to identify. Provisioning scripts must be associated with a fully qualified domain name and accessible using the HTTP or HTTPS protocols. The type of protocol that is used impacts the system's automated response when the provisioning script is downloaded to the device.  
{:shortdesc}

* Using **HTTP protocol** requires an administrator to run the script manually after it is downloaded.
* Using **HTTPS protocol** downloads and runs the script automatically, if possible. If the URL is not associated to a valid script, the script is downloaded and no further action must be taken.

## Before you begin
{: #before-you-begin-managing-provisioning-scripts}

First, navigate to the device menu and ensure you have the correct account permissions to complete the tasks. 

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/vsi?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions. 

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Adding a provisioning script
{: #add-provisioning-script}

1. From the **Devices** menu, select **Manage > Provisioning Scripts**.
2. Select **Add Provisioning Script**. 
3. Enter an identifying name for the provisioning script in the **Name** field.
4. Enter the fully qualified domain name that is associated with the script in the **URL** field.
5. Click **Add** to add the provisioning script to the account. 

## Editing provisioning script details
{: #edit-provisioning-script-details}

1. From the **Devices** menu, select **Manage > Provisioning Scripts**.
2. Click anywhere in the **Name** or **URL** column for the provisioning script to open the script for edits.
3. Update the name or URL.
   When you update a URL, you must use a fully qualified domain name or the change is not saved.
   {:note}
4. Click anywhere on the screen to save the edit.

## Next steps
{: #next-steps-provisioning-scripts}

Provisioning scripts that are associated with an account can be modified or removed at any time. Provisioning scripts are saved in the {{site.data.keyword.cloud_notm}} console until they are removed and can be associated to any new device ordered through the {{site.data.keyword.cloud_notm}} console. If the script is associated with an HTTP URL, it is downloaded to the new device during provisioning and the administrator must log in to the device and run the script manually. Scripts that are associated with HTTPS URLs are downloaded and, when applicable, run on the new device without additional interaction required. 

If you edit a script, valid updates are displayed on the screen immediately. Changes made to existing provisioning scripts do not impact devices already provisioned.

