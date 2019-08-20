---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Managing device access
{: #managing-device-access}

To access and manage the details for a specific device, you must have the correct permissions granted to your user account.  After the account administrator grants your user account access to a device, you can view the device details by using the {{site.data.keyword.cloud}} console or by using the {{site.data.keyword.slapi_short}}. The information or actions that you see depend on the device type, as well as the permissions that are granted to your user account.
{:shortdesc}

If your account has devices to which you have not been granted access, you will see an "Unknown Device" name when you try to access those devices.
{:note}

You can assign device access to any users on your account, but not to yourself. Only an account's administrator has access to all devices on their customer account and can set access for all other users on their account. 

You must have the following permissions to access the device details for public virtual servers or dedicated virtual servers.

* **View Virtual Servers Details** - Allows you to view the IP addresses, operating system type, passwords, and more for a given virtual server.  It also allows you to update virtual server passwords in the portal. You must have this access to view public instances, dedicated instances, and dedicated host instances.

* **View Virtual Dedicated Host Details** - Allows you to view the IP addresses, operating system type, passwords, and more for a given dedicated host.  It also allows you to migrate dedicated instances to a different dedicated host. You must have this access to view dedicated hosts.


## Adding permissions for your users
{: #adding-permissions-for-your-users}

If you are the account administrator and you want to grant users permission to view virtual server details and dedicated host details, complete the following steps.

1. Log in to the [Access (IAM) ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/iam#/users){: new_window} page in the {{site.data.keyword.cloud}} console. 
2. In the **Users** tab, select **View by: My classic infrastructure users**.
3. Select a user, then click the **Classic infrastructure** tab.
4. Expand the **Devices** category in the **Permissions tab** and select **View Virtual Server Details** and **View Virtual Dedicated Host Details**.
5. Click **Apply**.

### Adding specific device-level permissions
{: #adding-specific-device-level-permissions}

If you want to provide users access at a specific device level, complete the following steps.

1. In the **Users** tab, select **View by: My classic infrastructure users**. 
2. Select a user, then click the **Classic infrastructure** tab.
3. In the **Select type** section in the **Devices** tab, select the appropriate permission: **All bare metal servers**, **All dedicated hosts**, or **All virtual servers**. 
4. In the **Enable future access** section in the **Devices** tab, select the appropriate permission: **Auto bare metal server access**, **Auto dedicated host access**, or **Auto virtual server access**. This permission allows your users to always have access to the device type when new devices are added.
5. Click **Set** to apply the new permissions.

## Adding permissions for your users in the customer portal
{: #adding-permissions-for-your-users-in-the-customer-portal}

If you are the account administrator and you want to grant users permission to view virtual server details and dedicated host details, complete the following steps.

1. Access the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
2. Select **Account > Users** from the Navigation Bar to access the Users screen.
3. Click the relevant user name to access the User Profile.
4. Click the **Portal Permissions** icon to access the Portal Permissions screen.
5. On the **Device** tab, select **View Virtual Server Details** and **View Virtual Dedicated Host Details** to add these permissions to the user’s profile.

### Adding specific device-level permissions in the customer portal
{: #adding-specific-device-level-permissions-in-the-customer-portal}

To provide access at a specific device level, continue to the following steps.

1. Click the **Device Access** icon to access the Device Access screen.
2. Click the **Quick Access** tab. 
3. From the **Device Type** drop down list, select **All virtual servers** and **All dedicated hosts**.
4. Select the **Automatically grant access when new devices are added** check box if the associated user should always have access to this device type.
5. Verify the correct devices are selected.
6. Click **Update device access**.

You can also use the SoftLayer_User_Customer::addBulkDedicatedHostAccess API service to give a user access to one or more dedicated hosts. For more information, see [Adding Bulk Dedicated Host Access ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/reference/services/SoftLayer_User_Customer/addBulkDedicatedHostAccess/){: new_window}.  
{:note}

## Next steps
{: #next-steps-device-access}

User permissions are updated immediately after the changes are submitted. If permissions have been granted, the user can view or interact with the selected features. If permissions have been removed, the user can no longer view or interact with the selected features. Permissions can be updated again at any time.

