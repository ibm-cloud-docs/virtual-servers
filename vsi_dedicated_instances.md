---



copyright:
  years: 2017
lastupdated: "2017-08-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Dedicated instances

You have two options on how to provision your dedicated instances. The first is through the IBM® Bluemix® Catalog and the second is through the Customer Portal. Note that the catalog and portal require unique log-in IDs, in other words, your catalog username and password won’t work for logging in to the portal and vice versa. See [https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window}  to set up either your Bluemix Catalog or Customer Portal credentials.
{:shortdesc}

## Log into the Bluemix Catalog
Use the following steps to log in to the Bluemix Catalog to begin provisioning your dedicated instances. 

1. Open a new browser window and enter [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/){: new_window}.
2.	Click the **Log In** link (upper-right corner). 
3.	Enter your email or IBMid and click **Continue**.
4.	Enter your Password and click **Log in**.
5.	Select **Infrastructure > Compute**.
6.	Click the **Dedicated Virtual Servers (Hourly)** or **Dedicated Virtual Servers (Monthly)** tile.
7.  Click the **Create** button.

You will be on the main page of the Customer Portal.

## Log in to the Customer Portal
Use the following steps to log in to the Customer Portal to begin the order for your dedicated instances.

1.	Open a new browser window and enter [https://control.softlayer.com](https://control.softlayer.com){: new_window}. 
2.	Enter your Username and Password, and click **Log In** OR click **Log in with IBMid**.
3.	Enter your email or IBMid and click **Continue**.
4.	Enter your Password and click **Log In**.

You will be on the main page of the Customer Portal.

## Provision your dedicated instances
{: #provision-dedicated-instances}
You can provision your dedicated instances two ways—through the **Devices** icon or the **Devices** menu.

### Provisioning your dedicated host instances through the Devices icon
{: #ordering-dedicated-devices-menu}
The first option to provision dedicated host instances is to use the **Device** icon on the Customer Portal home page. The following steps take you through this process.

1.	Click the **Devices** icon. The **Order SoftLayer Product and Services** window displays. 
2.  Select **Hourly** or **Monthly** under Dedicated Virtual Servers. You’re redirected to the *Configure your Cloud Server* page. 

3.	Enter the following information:
       
    <table>
    <CAPTION>Table 1. Dedicated host instances selections</CAPTION>
    <THEAD>
    <TR>
    <th>Field</th>
    <th>Value</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantity</td>
    <td>The number of dedicated instances to be deployed.</td>
    </tr>
    <tr>
    <td>Placement</td>
    <td>
    <ul>
    <li>Auto Assign – Bluemix automatically assigns your instance to a host in your selected data center.</li>
    <li>Specify Host – Ussed with dedicated host instances. See [Dedicated virtual server](../vsi/vsi_dedicated.html) for more information on dedicated hosts and dedicated host instances.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Data Center</td>
    <td>Select the data center where the instances are to be provisioned.</td>
    </tr>
    <tr>
    <td>Computing Instance</td>
    <td> Select memory and CPU for each instance in a provisioning order.</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> Select the RAM for each instance in a provisioning order.</td>
    </tr>
    <tr>
    <td>Operating System</td>
    <td>Select the operating system for the instance. Note that an error message is issued if there is a conflict between the server and operating system. For example, selecting Linux on a Microsoft SQL server.</td>
    </tr>
    <tr>
    <td>First Disk</td>
    <td>Select either SAN or Local for each instance in an order.</td>
    </tr>
    <tr>
    <td>Additional Disks</td>
    <td>You can provision up to four additional boot disks—SAN or Local—per dedicated instance.</td>
    </tr>
    <td>Network Options</td>
    <td> Select the appropriate options or use the default values.</td>
    </tr>
    <tr>
    <td>Addons</td>
    <td> Select the appropriate options or use the default values.</td>
    </tr>
    <tr>
    </TBODY>
    </table> 

4.	Click the **Add to Order** button. You'll be redireted to the Checkout page.
5.  Enter the following information on the *Checkout* page under *Advanced System Configuration*:

<table>
    <CAPTION>Table 2. Dedicated instance Advanced System Configuration</CAPTION>
    <THEAD>
    <TR>
    <th>Field</th>
    <th>Value</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>VLAN Selection</td>
    <td>Add the new server to a VLAN under your account if you already ordered at least one server.</td>
    </tr>
    <tr>
    <td>Provision Scripts</td>
    <td>Provide a script that allows you to automate certain steps after provisioning.</td>
    </tr>
    <tr>
    <td>SSH Keys</td>
    <td>Provide a public key of your SSH key, which will allow you to log in to your server after it is provisioned.</td>
    </tr>
    <tr>
    <td>User Metadata</td>
    <td>Optional metadata for custom provisioning scripts.</td>
    </tr>
    <tr>
    <td>Hostname</td>
    <td>Enter a permanent or temporary name for your server, for example, server1.</td>
    </tr>
    <tr>
    <td>Domain</td>
    <td>Enter a sub-domain name that will not collide with an Internet domain name, for example, test.acme.com.</td>
    </tr>
    </TBODY>
    </table>

6.  Click the **Cloud Service terms** and **Third-Party Services Agreement** checkboxes.
7. Confirm or enter your payment information and click the **Submit Order** button. You will be redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

    A series of emails are sent to your administrator—acknowledgement of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email will include a link that will take you directly to your **Device Details** page after logging in to Bluemix. Another option would be to log directly in to the Customer Portal.

### Provisioning your dedicated instances through the Devices menu

Your second option is to provision your dedicated instances through the **Devices** menu from the main Customer Portal page. The following steps take you through this process.

1.	Click **Devices > Device List**. 
 
    The *Devices* page displays all device types—virtual servers, bare metal servers, dedicated hosts and NetScaler application delivery controllers—within your account. 

2.	Click the **Ordering Devices** link on the right side of the page.
    The **Order SoftLayer Product and Services** window displays.
3.	Follow the steps under [Provisioning your dedicated instances through the Devices](#ordering-dedicated-devices-menu) menu, beginning with Step 2.

### What's Next?
After your virtual server is provisioned, you can start managing it. For more information, see [Managing virtual servers](../vsi/vsi_managing.html).
