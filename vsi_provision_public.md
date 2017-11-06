---



copyright:
  years: 2017
lastupdated: "2017-10-24"


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
You have two options to provision your public virtual server instances. The first is through the {{site.data.keyword.Bluemix}} catalog and the second is through the {{site.data.keyword.slportal_full}}. The catalog and {{site.data.keyword.slportal}} require unique log-in IDs. Your catalog user name and password won’t work for logging in to the portal and vice versa.
{:shortdesc}

Before you begin, review the following prerequisites.

  1. Ensure that you have either your {{site.data.keyword.Bluemix_notm}} catalog or {{site.data.keyword.slportal}} credentials set-up. 
  
     **Note:** For the {{site.data.keyword.Bluemix_notm}} catalog, you must have an upgraded account to order virtual servers. For more information about upgrading your account, see [Upgrading and unifying Bluemix and SoftLayer billing accounts](https://console.ng.bluemix.net/docs/admin/softlayerlink.html).
  
  2. If you haven't done so, review the deployment options available to you. For more information, see [Deployment options: Public virtual server](../vsi/vsi_public.html).

## Logging in 
Ensure that you are logged in, either through {{site.data.keyword.Bluemix_notm}} catalog or {{site.data.keyword.slportal}}: 

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
   <li>Click <b>Create</b>. The main page of the {{site.data.keyword.slportal}} opens.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Customer Portal</td>
   <td>
   <ol>
   <li>Open a new browser window and enter <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Enter your User name and Password, and click <b>Log In</b>. Or, click <b>Log in with IBMid</b>. Then, enter your email or IBMid and click <b>Continue</b>. Enter your password and click <b>Log In</b>. The main page of the {{site.data.keyword.slportal}} opens.</li>
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

1.  From the {{site.data.keyword.slportal}}, locate the **Order** section and click **Devices**.
2.  On the Devices page, click **Hourly** or **Monthly** for one of the Virtual Server offerings.
3.  On the *Configure your Cloud Server* page, complete all the relevant information.
4.  Click the **Add to Order** button to continue.
5.  Confirm or edit the domain information for the server.
5.  Click the **Cloud Service terms** and the **Third-Party Service Agreement** check box.
6.  Confirm or enter your payment information and click the **Submit Order** button. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.Bluemix_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

### Provisioning a public virtual server instance through the Devices menu
{: #ordering-public-devices-menu}

You can also provision your public virtual server instances through the *Devices* menu on the main {{site.data.keyword.slportal}} page. 

1. Click **Devices > Device List**.

   The Devices page displays all device types: dedicated hosts, virtual servers, bare metal servers, and NetScaler application delivery controllers—within your account.
2. Click the **Order Devices** link in the upper right-hand corner.
3. On the Devices page, click **Hourly** or **Monthly** for one of the Virtual Server offerings.
4. On the *Configure your Cloud Server* page, complete all the relevant information.
5. Click the **Add to Order** button to continue.
6. Confirm or edit the domain information for the server.
7. Click the **Cloud Service terms** and the **Third-Party Service Agreement** check box.
8. Confirm or enter your payment information and click the **Submit Order** button. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.Bluemix_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

### Next Steps
After your virtual server is provisioned, you can start managing it. For more information, see [Managing your virtual server](../vsi/vsi_managing.html).
