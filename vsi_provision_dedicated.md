---

copyright:
  years: 2017, 2019
lastupdated: "2019-09-26"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning dedicated hosts and instances
{: #ordering-vs-dedicated}

You have two options on how to provision your dedicated instances. The first is through the {{site.data.keyword.Bluemix}} catalog and the second is through the {{site.data.keyword.slportal_full}}. The catalog and {{site.data.keyword.slportal}} require unique log-in IDs. Your catalog user name and password won’t work for logging in to the portal and vice versa. See [Signing up for {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-signup#signup) to set up either your {{site.data.keyword.Bluemix_notm}} catalog or {{site.data.keyword.slportal}} credentials.
{:shortdesc}

## Provisioning dedicated hosts and instances
{: #provisioning-dedicated-hosts-and-instances}

You can provision your dedicated hosts and instances through the {{site.data.keyword.cloud_notm}} or the {{site.data.keyword.slportal}}.

### Provisioning dedicated hosts and instances through the IBM Cloud catalog
{: #provisioning-dedicated-hosts-and-instances-through-the-ibm-cloud-catalog}

To provision your dedicated hosts and dedicated host instances through the {{site.data.keyword.cloud_notm}} catalog, complete the following steps:

1. Log in to the [{{site.data.keyword.cloud_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/){: new_window} by using your unique credentials.
2. In the **Compute Infrastructure** section, click the **Virtual Server** tile.
3. Select **Dedicated** as your virtual server type.
4. In the **Dedicated Host** section, you can either select **Create Host**, where you can create a new dedicated host, or **Specify Host**, where you can select from your existing dedicated hosts.
5. Complete all of the relevant information for your dedicated host and dedicated virtual server instance.
6. After you review your order summary, click the **Third-Party Service Agreements** check box.
7. Click **Provision**.

### Provisioning dedicated hosts and instances through the customer portal
{: #provisioning-dedicated-hosts-and-instances-through-the-customer-portal}

To provision your dedicated hosts and dedicated host instances through the {{site.data.keyword.slportal}}, complete the following steps:

1. Log in to the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.

#### Provisioning your dedicated host
{: #provisioning-your-dedicated-host}

Use the following steps to provision your dedicated hosts.

1.	Click the **Devices** icon.
2.  Click on either **Dedicated Virtual Server Hourly** or **Dedicated Virtual Server Monthly** link.

   **Note:** Dedicated servers are private servers.

You’re taken to the *Configure your Cloud Server* page. It’s from this page that you can order a dedicated instance that is or is not associated with a dedicated host. More information on ordering instances can be found under [Provision your dedicated host instances](#provision-dedicated-instances).

4.	Click the **Create Host** button on the right side of the form.
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
    <td>Quantity</td>
    <td>Enter the number of dedicated hosts to be ordered. Note that only two dedicated hosts can be deployed per provisioning order.</td>
    </tr>
    <tr>
    <td>Location</td>
    <td>Select the {{site.data.keyword.cloud}} data center where you want to place your hosts. See About for the list of applicable data centers.</td>
    </tr>
    <td>Dedicated Host</td>
    <td>Defaults to 56 Cores X 242 RAM X 1.2 TB, but you can select from other configurations.</td>
    </tr>
    </TBODY>
    </table>

    Your Order Summary displays on the right side of the *Configuration* page.

6.  Click the **Add to Order** button.
7.  Confirm your selections on the *Checkout* page and scroll down to *Dedicated Host Advanced System Configuration*.
8.  Enter the following information:

    <table>
    <CAPTION>Table 2. Dedicated host Advanced System Configuration</CAPTION>
    <THEAD>
    <TR>
    <th>Field</th>
    <th>Value</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>POD Selection</td>
    <td>Click the drop-down box and select the POD where you want your dedicated host placed.</td>
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

9.  Click the **Cloud Service terms** checkbox.
10. Confirm or enter your payment information and click the **Submit** button. You will be redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

    A series of emails are sent to your administrator—acknowledgement of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email will include a link that will take you directly to your **Device Details** page after logging in to {{site.data.keyword.Bluemix_notm}}. Another option would be to log directly in to the {{site.data.keyword.slportal}}.

#### Provisioning your dedicated host instances
{: #provision-dedicated-instances}

To provision your dedicated host instances through the {{site.data.keyword.slportal}}, complete the following steps:

1.	Click **Devices > Device List**.

    The *Devices* page displays all device types—dedicated hosts, virtual servers, bare metal servers, and NetScaler application delivery controllers—within your account.

2.	Select the host for your dedicated host instances by clicking on its link under **Device Name**.

    You’re on the **Configuration** tab of the *Device Details* page. The **Tickets** tab lists your active support tickets and the **Allocations** tab displays your memory usage for your selected billing period. See Using Device Details to manage your dedicated host and instances for more information on the tabs.

3.	Scroll down to the **Instances** frame.

    How your dedicated host is billed (monthly or hourly) determines the billing of your dedicated host instances. Note that if you have monthly-billed hosts, you can provision both hourly- and monthly-billed dedicated host instances. There are two links—**Add hourly** and **Add monthly**—available when provisioning your instances. Hourly-billed dedicated hosts can only provision hourly-billed dedicated host instances and will only see the **Add hourly** link.

4.	Click the **Add hourly** link if your host is billed hourly or monthly; click the **Add monthly** link if your host is billed monthly. You’re redirected to the *Configure your Cloud Server* page.

5.	Enter the following information:

    <table>
    <CAPTION>Table 3. Dedicated host instances selections</CAPTION>
    <THEAD>
    <TR>
    <th>Field</th>
    <th>Value</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantity</td>
    <td>The number of dedicated hosts instances to be deployed on a single host.</td>
    </tr>
    <tr>
    <td>Placement</td>
    <td>
    <ul>
    <li>Auto Assign – {{site.data.keyword.Bluemix_notm}} automatically assigns your instance to a host versus you specifying one. Your instance will be placed in a data center that has capacity. If you auto-assign your instance, you will not be using any of your dedicated hosts's capacity.</li>
    <li>Specify Host – Your dedicated host associated with your account will display under Dedicated Host. </li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Dedicated Host</td>
    <td>Select the dedicated host from the list where the instances are to be provisioned.</td>
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
    <td>You can provision up to four additional boot disks—SAN or Local—per dedicated host instance.</td>
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

6.	Click the **Add to Order** button.
7.  Enter the following information on the *Checkout* page under *Advanced System Configuration*:

<table>
    <CAPTION>Table 4. Dedicated host instance Advanced System Configuration</CAPTION>
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

8.  Click the **Cloud Service terms** and **Third-Party Services Agreement** checkboxes.
9. Confirm or enter your payment information and click the **Submit** button. You will be redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.


You will receive an email once your dedicated host instances have been provisioned.

## Next steps
{: #next-steps-provisioning-dedicated-instances-hosts}

After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.cloud_notm}} console or {{site.data.keyword.slapi_short}}. For more information, see [Configuring virtual servers](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
