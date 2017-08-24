---



copyright:
  years: 2017
lastupdated: "2017-07-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning dedicated hosts and instances
{: #ordering-vs-dedicated}

You have two options on how to provision your dedicated host server and instances. The first is through the IBM® Bluemix® Catalog and the second is through the Customer Portal. Note that the catalog and portal require unique log-in IDs, in other words, your catalog username and password won’t work for logging in to the portal and vice versa. See [https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window}  to set up either your Bluemix Catalog or Customer Portal credentials.
{:shortdesc}

## Log into the Bluemix Catalog
Use the following steps to log in to the Bluemix Catalog to begin provisioning your dedicated hosts and dedicated host instances. 

1. Open a new browser window and enter [https://console.ng.bluemix.net/catalog/](https://console.ng.bluemix.net/catalog/){: new_window}.
2.	Click the **Log in** link (upper-right corner). 
3.	Enter your email or IBMid and click **Continue**.
4.	Enter your Password and click **Log in**.
5.	Select **Infrastructure > Compute**.
6.  Click the **Virtual Servers** tile.
7.	Select the **Dedicated Virtual Servers** option.
8.  Click **Create**.  

You will be on the main page of the Customer Portal.

## Log in to the Customer Portal
Use the following steps to log in to the Customer Portal to begin the order for your dedicated hosts and dedicated host instances.

1.	Open a new browser window and enter [https://control.softlayer.com](https://control.softlayer.com){: new_window}. 
2.	Enter your Username and Password, and click **Log In** OR click **Log in with IBMid**.
3.	Enter your email or IBMid and click **Continue**.
4.	Enter your Password and click **Log In**.

You will be on the main page of the Customer Portal.

## Provision your dedicated host 
Use the following steps to provision your dedicated hosts.

1.	Click the **Devices** icon.
2.	Scroll down on the *Order SoftLayer Products and Services* page to the *Devices* section. 
3.  Click on either **Dedicated Virtual Server Hourly** or **Dedicated Virtual Server Monthly** link. 

   **Note:** Dedicated servers are private servers.

You’re taken to the *Configure your Dedicated Virtual Server* page. It’s from this page that you can order a dedicated instance that is or is not associated with a dedicated host. More information on ordering instances can be found under [Provision your dedicated host instances]{: provision-dedicated-instances}.

4.	Click the **Create Host** button on the right side of the page.
5.	Enter the following information:
    
    <table>
    <CAPTION>Table 1. Dedicated host provisioning selections</CAPTION>
    <THEAD>
    <TR>
    <th>Field</th>
    <th>Value</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Location</td>
    <td>Select the IBM Cloud Data Center where you want to place your hosts. See About for the list of applicable data centers.</td>
    </tr>
    <tr>
    <td>Host size</td>
    <td>Defaults to 56 Cores X 242 GB RAM X 1.2 TB</td>
    </tr>
    <tr>
    <td>Host quantity</td>
    <td>Maximum of 2 per provisioning order</td>
    </tr>
    <tr>
    <td>Host name</td>
    <td>Unique identifier, for example, Companyname_data center (AcmeDAL10). Required for each host if provisioning two.</td>
    </tr>
    <tr>
    <td>POD selection</td>
    <td>Defaults to **Automatically assign** for your initial order. You can assign your hosts to specific PODs for subsequent orders.</td>
    </tr>
    </TBODY>
    </table>
    
    Your Order Summary displays on the right side of the *Configuration* page. 
    
6.  Click the **Add to Order** button.
7.  Confirm your selections on the *Checkout* page and click the **Cloud Service terms** and **3rd Party Software Terms Red Hat Agreement** checkboxes.
8.  Confirm or enter your payment information and click the **Submit** button. You will be redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

    A series of emails are sent to your administrator—acknowledgement of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email will include a link that will take you directly to your **Device Details** page after logging in to Bluemix. Another option would be to log directly in to the Customer Portal.

## Provision your dedicated host instances
{: #provision-dedicated-instances}
You can provision your dedicated host instances two ways—through the **Devices** menu or the **Devices** icon.

### Provisioning your dedicated host instances through the Devices menu
{: #ordering-dedicated-devices-menu}

Your first option is to provision your dedicated host instances through the **Devices** menu from the main Customer Portal page. The following steps take you through this process.

1.	Click **Devices > Device List**. 
 
    The *Devices* page displays all device types—dedicated hosts, virtual servers, bare metal servers and NetScaler application delivery controllers—within your account. 

2.	Select the host for your dedicated host instances by clicking on its link under **Device Name**.
    
    You’re on the **Configuration** tab of the *Device Details* page. The **Tickets** tab lists your active support tickets and the **Allocations** tab displays your memory usage for your selected billing period. See Using Device Details to manage your dedicated host and instances for more information on the tabs.

3.	Scroll down to the **Instances** frame.

    How your dedicated host is billed (monthly or hourly) determines the billing of your dedicated host instances. Note that if you have monthly-billed hosts, you can provision both hourly- and monthly-billed dedicated host instances. There are two links—**Add hourly** and **Add monthly**—available when provisioning your instances. Hourly-billed dedicated hosts can only provision hourly-billed dedicated host instances and will only see the **Add hourly** link. 

4.	Click the **Add hourly** link if your host is billed hourly or monthly; click the **Add monthly** link if your host is billed monthly. You’re redirected to the *Configure your Dedicated Virtual Server* page. 

5.	Enter the following information:
       
    <table>
    <CAPTION>Table 2. Dedicated host instances selections</CAPTION>
    <THEAD>
    <TR>
    <th>Field</th>
    <th>Value</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantity</td>
    <td>The number of dedicated hosts instances to be deployed on a single host. </td>
    </tr>
    <tr>
    <td>Host Placement</td>
    <td>
    <ul>
    <li>Auto Assign – Bluemix automatically assigns your instance to a host versus you specifying one. Your instance will be placed in a data center that has capacity. If you auto-assign your instance, you will not be using any of your dedicated hosts's capacity.</li>
    <li>Specify Host – Your dedicated host associated with your account will display in the **Host** field by default if you only have one host. If you have multiple hosts, a drop-down box will be available for you to choose your host.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Host</td>
    <td>Select the dedicated host where the instances are to be provisioned. This will default if you only have one host. If you have multiple hosts, a drop-down box will be available for you to choose your host.</td>
    </tr>
    <tr>
    <td>Virtual Server Configuration</td>
    <td> Use the slide button to select memory and CPU for each instance in a provisioning order.</td>
    </tr>
    <tr>
    <td>Operating Systems</td>
    <td>Select the operating system for the instance. Note that an error message is issued if there is a conflict between the server and operating system. For example, selecting Linux on a Microsoft SQL server.</td>
    </tr>
    <tr>
    <td>Boot Disk</td>
    <td>Select either SAN or Local for each instance in an order.</td>
    </tr>
    <tr>
    <td>Additional Disks</td>
    <td>You can provision up to four additional boot disks—SAN or Local—per dedicated host instance.</td>
    </tr>
    </TBODY>
    </table> 

6.	Click the **Create** button.

You will receive an email once your dedicated host instances have been provisioned.

### Provisioning your dedicated host instances through the Devices icon
The second option to provision dedicated host instances is to use the **Device** icon on the Customer Portal home page. The following steps take you through this process.

1.	Click the **Devices** icon and select **Hourly** or **Monthly** under Dedicated Virtual Servers.
2.	Follow the steps under [Provisioning your dedicated host instances through the Devices](#ordering-dedicated-devices-menu) menu, beginning with Step 5.

### What's Next?
After your virtual server is provisioned, you can start managing it. For more information, see [Managing virtual servers](../vsi/vsi_managing.html).


