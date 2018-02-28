---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Provisioning transient instances
{: #ordering-vs-transient}
You can provision your transient virtual server instances through the {{site.data.keyword.slportal_full}}.
{:shortdesc}

## Before you begin
Before you begin, review the following prerequisites.

  1. Ensure that you have your {{site.data.keyword.slportal}} credentials set up.

  2. Review virtual server instance capacity considerations.  For more information, see [Capacity considerations](ts_capacity_bp.html).

## Logging in
Ensure that you are logged in to the {{site.data.keyword.slportal}}:

  1. Access the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.

The main page of the {{site.data.keyword.slportal}} opens.

## Provisioning a transient virtual server instance
{: #ordering-transient-instance}
After you complete the prerequisites, provision a transient virtual server instance. You can provision your transient instances two ways: through the **Devices** menu or the **Devices** icon.

### Provisioning a transient virtual server instance through the Devices icon
To provision your transient virtual server instance through the *Devices* icon, complete the following steps:

1.  From the {{site.data.keyword.slportal}}, locate the **Order** section and click **Devices**.
2.  Under *Public Virtual Server* on the *Devices* page, click **Transient** for the Virtual Server offering.
3.  On the *Configure your Cloud Server* page, complete all the relevant information.
4.  Click **Add to Order** to continue.
5.  Confirm or edit the domain information for the server.
5.  Click the **Cloud Service terms** and the **Third-Party Service Agreement** check box.
6.  Confirm or enter your payment information and click **Submit Order**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page.

### Provisioning a transient virtual server instance through the Devices menu
{: #ordering-transient-devices-menu}

You can also provision your transient virtual server instances through the *Devices* menu on the main {{site.data.keyword.slportal}} page.

1. Click **Devices > Device List**.

   The Devices page displays all device types: dedicated hosts, virtual servers, bare metal servers, and NetScaler application delivery controllers—within your account.
2. Click the **Order Devices** link in the upper right corner.
3. Under *Public Virtual Server* on the *Devices* page, click **Transient** for the Virtual Server offering.
4. On the *Configure your Cloud Server* page, complete all the relevant information.
5. Click **Add to Order**to continue.
6. Confirm or edit the domain information for the server.
7. Click the **Cloud Service terms** and the **Third-Party Service Agreement** check box.
8. Confirm or enter your payment information and click **Submit Order**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page.

You can also provision a transient virtual server by using the {{site.data.keyword.slapi_short}}. For an example, see [Provisioning a transient instance using Create Object](../vsi/vsi_provision_api.html#api-rest-transient).
{:tip}

## Next Steps
After your virtual server is provisioned, you can start managing it. For more information, see [Managing your virtual server](../vsi/vsi_managing.html).
