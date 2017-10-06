---



copyright:
  years: 2017
lastupdated: "2017-08-23"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Managing device access
{: #managing-device-access}

To access and manage the details for a specific device, you must have the right permissions granted to your user account.  After the account administrator grants your user account access to a device, you can view the device details by using the customer portal or by using the API.  The information or action that you see depends on the device type, as well as the permissions that are granted to your user account.
{:shortdesc}

**Note:** If your account has devices to which you have not been granted access, you will see an "Unknown Device" name when you try to access those devices.

You can assign device access to any users on your account, but not to yourself. Only an account's administrator has access to all devices on their customer account and can set access for all other users on their account. 

You must have the following permissions to access the device details for public virtual servers or dedicated virtual servers.

**View Virtual Servers details**

Allows you to view the IP addresses, operating system type, passwords, and more for a given virtual server.  It also allows you to update virtual server passwords in the portal. A user must have this access to view public instances, dedicated instances, and dedicated host instances.

**View Virtual Dedicated Host Details**

Allows you to view the IP addresses, operating system type, passwords, and more for a given dedicated host.  It also allows you to migrate dedicated instances to a different dedicated host. A user must have this access to view dedicated hosts.

## Adding permission to view virtual server instances
Use the following steps to add *View Virtual Server Details* permissions for any of your child users. Only an account's administrator can grant permissions to other users on their account.  

1. Access the [Customer Portal ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
2. Select **Account > Users** from the Navigation Bar to access the Users screen.
3. Click the relevant user name to access the User Profile.
4. Click the **Portal Permissions** icon to access the Portal Permissions screen.
5. On the *Device* tab, select **View Virtual Server Details** to add this permission to the user’s profile.

To provide access at a specific device level, continue to the following steps.

1. Click the **Device Access** icon to access the Device Access screen.
2. Click the **Quick Access** tab. 
   Note: Another option is to select an individual device instead.
3. From the *Device Type* drop down list, select **All virtual servers**.
4. Select the **Automatically grant access when new devices are added** check box if the associated user should always have access to this device type.
5. Verify the correct devices are selected.
6. Click **Update device access**.

## Adding permission to view dedicated hosts
Use the following steps to add *View Virtual Dedicated Host Details* permissions for any of your child users. Only an account's administrator can grant permissions to other users on their account.

1. Access the [Customer Portal ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
2. Select **Account > Users** from the Navigation Bar to access the Users screen.
3. Click the relevant user name to access the User Profile.
4. Click the **Portal Permissions** icon to access the Portal Permissions screen.
5. On the *Device* tab, select **View Virtual Dedicated Host Details** to add this permission to the user’s profile.

To provide access at a specific device level, continue to the following steps.

1. Click the **Device Access** icon to access the Device Access screen.
2. Click the **Quick Access** tab. 
   Note: Another option is to select individual devices instead.
3. From the *Device Type* drop down list, select **All dedicated hosts**.
4. Select the **Automatically grant access when new devices are added** check box if the associated user should always have access to this device type.
5. Verify the correct devices are selected.
6. Click **Update device access**.

**Note:** You can also use the SoftLayer_User_Customer::addBulkDedicatedHostAccess API service to give a user access to one or more dedicated hosts. For more information, see [Adding Bulk Dedicated Host Access ![External link icon](../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/reference/services/softlayer_user_customer/addbulkdedicatedhostaccess){: new_window}.  

## Next Steps
User permissions are updated immediately after the changes are submitted. If permissions have been granted, the user can view or interact with the selected features. If permissions have been removed, the user can no longer view or interact with the selected features. Permissions can be updated again at any time.
