---



copyright:
  years: 2017
lastupdated: "2017-04-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning public instances
{: #ordering-vs-public}

## Before you begin
You have two options to provision your public virtual server instances. The first is through the IBM® Bluemix® Catalog and the second is through the Customer Portal. Note that the catalog and portal require unique log-in IDs. Your catalog username and password won’t work for logging in to the portal and vice versa.
{:shortdesc}

Before you begin, review the following prerequisites.

  1. Ensure you have either your Bluemix Catalog or Customer Portal credentials set up. 
  
     **Note:** For the Bluemix catalog, you must have an upgraded account to order virtual servers. For more information about upgrading your account, see [Upgrading and unifying Bluemix and SoftLayer billing accounts](https://console.ng.bluemix.net/docs/admin/softlayerlink.html).
  
  2. If you haven't done so, review the deployment options available to you. For more information, see [Deployment options: Public virtual server](../vsi/vsi_public.html).

## Logging in 
Ensure that you are logged in, either through Bluemix Catalog or Customer Portal: 

  <table>
   <CAPTION>Table 1. Choose a log in location</CAPTION>
   <THEAD>
   <TR>
   <th>If you want to log in with...</th>
   <th>Then...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Bluemix Catalog</td>
   <td>
   <ol>
   <li>Open a new browser window and enter  <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Click the <b>Log in</b> link (lower-right corner). </li>
   <li>Enter your email or IBMid and click <b>Continue.</b></li>
   <li>Enter your Password and click <b>Log in.</b></li>
   <li>Select <b>Infrastructure</b> > <b>Compute</b>.</li>
   <li>Click the <b>Virtual Servers</b> tile.</li>
   <li>Select the <b>Public Virtual Servers</b> option.</li>
   <li>Click <b>Create</b>. The main page of the Customer Portal opens.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Customer Portal</td>
   <td>
   <ol>
   <li>Open a new browser window and enter <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Enter your Username and Password, and click <b>Log In</b>. OR, click <b>Log in with IBMid</b>. Then enter your email or IBMid and click <b>Continue</b>. Enter your password and click <b>Log In</b>. The main page of the Customer Portal opens.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Provisioning a public virtual server instance
{: #ordering-public-instance}
After you have completed the prerequisites, you can begin to provision a public virtual server instance. You can provision your public instances two ways -- through the **Devices** menu or the **Devices** icon.

### Provisioning a public virtual server instance through the Devices icon
To provision your public virtual server instance through the *Devices* icon, complete the following steps:

1.  On the Customer Portal main page, click the **Devices** icon under *Order*.
2.  Scroll down on the Order SoftLayer Products and Services page to the *Devices* section. Click on either **Public Virtual Server (Hourly)** or **Public Virtual Server (Monthly)** link.
3.  On the *Configure your Cloud Server* page, complete all the relevant information.
4.  Click the **Add to Order** button to continue.
5.  Click the **Create** button to complete your order.

### Provisioning a public virtual server instance through the Devices menu
{: #ordering-public-devices-menu}

You can also provision your public virtual server instances through the *Devices* menu on the main Customer Portal page. 

1. Click **Devices > Device List**.

   The Devices page displays all device types: dedicated hosts, virtual servers, bare metal servers, and NetScaler application delivery controllers—within your account.
2. Select the host for your public instances by clicking on its link under *Device Name*.
   
   **Note:** If you have no devices, click the **Order Devices** link in the upper right-hand corner.
3. On the *Configure your Cloud Server* page, complete all the relevant information.
4. Click the **Add to Order** button to continue.
5. Click the **Create** button to complete your order.

### What's Next?
After your virtual server is provisioned, you can start managing it. For more information, see [Managing your virtual server](../vsi/vsi_managing.html).
