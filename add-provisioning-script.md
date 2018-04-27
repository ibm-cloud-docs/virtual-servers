---
copyright:
  years: 2014, 2017
lastupdated: "2017-12-21"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Managing a provisioning script

Use provisioning scripts to specify a URL to a script to be run on a newly provisioned device. You have no restrictions for the script name; however, using a similar naming convention for each script makes it easier to identify. Provisioning scripts must be associated with a fully qualified domain name and accessible using the HTTP or HTTPS protocols. The type of protocol that is used impacts the system's automated response when the provisioning script is downloaded to the device.

* Using **HTTP protocol** requires an administrator to run the script manually after it is downloaded.
* Using **HTTPS protocol** downloads and runs the script automatically, if possible. If the URL is not associated to an executable script, the script is downloaded and no further action must be taken.

## Accessing the provisions scripts screen
1. Enter the [{{site.data.keyword.slportal_full}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} with your unique credentials.
2. Select **Devices > Manage > Provisioning Scripts** from navigation to access the provisioning scripts screen.


## Adding a provisioning script

1. From the **Provisioning Scripts** screen in the {{site.data.keyword.slportal}}, click **Add Provisioning Script** at the top of the screen.
* Enter an **identifying name** for the provisioning script in the **Name** field.
* Enter the **fully qualified domain name** that is associated with the script in the **URL** field.
* Click **Add** to add the provisioning script to the account. Click **Cancel** to cancel the action.

## Editing provisioning script details

1. From the **Provisioning Scripts** screen in the {{site.data.keyword.slportal}}, click anywhere in the **Name** or **URL** column for the provisioning script to open the script for edits.
3. Update the name or URL.
  * **Note:** When you update a URL, you must use a fully qualified domain name or the change is not saved.
4. Click anywhere on the screen to save the edit.

## Next steps

Provisioning scripts that are associated with an account can be modified or removed at any time. Provisioning scripts are saved in the {{site.data.keyword.slportal}} until they are removed and can be associated to any new device ordered through the {{site.data.keyword.slportal}}. If the script is associated with an HTTP URL, it is downloaded to the new device during provisioning. Scripts that are associated with HTTPS URLs are downloaded and, when applicable, run on the new device.

After you edit a script, valid updates are displayed on the screen immediately. Changes made to existing provisioning scripts do not impact devices already provisioned.
