---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Provisioning dedicated instances

You have two options on how to provision your dedicated instances. The first is through the {{site.data.keyword.Bluemix}} catalog and the second is through the {{site.data.keyword.slportal_full}}. The catalog and {{site.data.keyword.slportal}} require unique log-in IDs. Your catalog user name and password won’t work for logging in to the portal and vice versa. See [Signing up for {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-signup#signup) to set up either your {{site.data.keyword.Bluemix_notm}} catalog or {{site.data.keyword.slportal}} credentials.
{:shortdesc}

## Provisioning dedicated virtual server instances
{: #provision-dedicated-instances}
You can provision your dedicated virtual server instance through the {{site.data.keyword.cloud_notm}} catalog or the {{site.data.keyword.slportal}}.

### Provisioning a dedicated virtual server instance through the IBM Cloud catalog
To provision a dedicated virtual server instance through the {{site.data.keyword.cloud_notm}} catalog, complete the following steps:

  1. Log in to the [{{site.data.keyword.cloud_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/){: new_window} by using your unique credentials.
  2. In the **Compute Infrastructure** section, click the **Virtual Servers** tile.
  3. Select the **Dedicated Virtual Server** option.
  4. Click **Create**.
  5. In the **Dedicated Host** section, select **Auto Assign**. {{site.data.keyword.cloud_notm}} then automatically assigns your instance to a host in your selected data center.

     **Note**: For dedicated hosts, select **Specify Host** or **Create Host**. For more information about dedicated hosts and dedicated host instances, see [Dedicated virtual servers](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers).

  5. Complete all of the relevant information for your dedicated virtual server instance.
  6. After you review your order summary, click the **Third-Party Service Agreements** check box.
  7. Click **Provision**.

### Provisioning a dedicated virtual server instance through the customer portal
To provision a dedicated virtual server instance through the {{site.data.keyword.slportal}}, complete the following steps:

1. Log in to the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
2. Locate the **Order** section and click **Devices**. The **Order SoftLayer Product and Services** window displays.
3.  Select **Hourly** or **Monthly** under Dedicated Virtual Servers. You’re redirected to the *Configure your Cloud Server* page.

4.	Enter the following information:

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
    <li>Auto Assign – {{site.data.keyword.Bluemix_notm}} automatically assigns your instance to a host in your selected data center.</li>
    <li>Specify Host – Used with dedicated host instances. See [Dedicated virtual servers](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers) for more information on dedicated hosts and dedicated host instances.</li>
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

5.	Click the **Add to Order** button. You'll be redirected to the Checkout page.
6.  Enter the following information on the *Checkout* page under *Advanced System Configuration*:

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

7.  Click the **Cloud Service terms** and **Third-Party Services Agreement** checkboxes.
8. Confirm or enter your payment information and click the **Submit Order** button. You will be redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

    A series of emails are sent to your administrator—acknowledgement of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email will include a link that will take you directly to your **Device Details** page after logging in to {{site.data.keyword.Bluemix_notm}}. Another option would be to log directly in to the {{site.data.keyword.slportal}}.

## Next Steps
After your virtual server is provisioned, you can start managing it. For more information, see [Managing virtual servers](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
