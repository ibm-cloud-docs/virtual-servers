---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-03"


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
You can provision your transient virtual server instances through the {{site.data.keyword.cloud}} catalog or the {{site.data.keyword.slportal}}.
{:shortdesc}

## Before you begin
Before you begin, review the following prerequisites.

  1. Ensure that you have either your {{site.data.keyword.cloud_notm}} catalog or {{site.data.keyword.slportal}} credentials set up.
  
  **Note:** For the {{site.data.keyword.Bluemix_notm}} catalog, you must have an upgraded account to order virtual servers. For more information about upgrading your account, see [Switching to IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).

  2. Review virtual server instance capacity considerations. For more information, see [Capacity considerations](/docs/vsi/ts_capacity_bp.html).

## Provisioning a transient virtual server instance 
After you complete the prerequisites, you can begin to provision your transient virtual server instance. You can provision your instance through the {{site.data.keyword.cloud_notm}} catalog or the {{site.data.keyword.slportal}}.

### Provisioning transient virtual server instances through the IBM Cloud catalog
To provision a transient virtual server instance through the {{site.data.keyword.cloud_notm}} catalog, complete the following steps:

  1. Log in to the [{{site.data.keyword.cloud_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/){: new_window} by using your unique credentials.  
  2. In the **Compute Infrastucture** section, click the **Virtual Servers** tile.
  3. Select the **Transient Virtual Server** option.
  4. Click **Create**.
  5. Complete all of the relevant information for your virtual server instance.
  6. After you review your order summary, click the **Third-Party Service Agreements** check box.
  7. Click **Provision**.
  
### Provisioning transient virtual server instances through the customer portal
To provision a transient virtual server instance through the {{site.data.keyword.slportal}}, complete the following steps:

  1. Log in to the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
  2. Locate the **Order** section and click **Devices**.
  3. Under *Public Virtual Server* on the *Devices* page, click **Transient** for the Virtual Server offering.
  4. On the *Configure your Cloud Server* page, complete all the relevant information.
  5. Click **Add to Order** to continue.
  6. Confirm or edit the domain information for the server.
  7. Click the **Cloud Service terms** and the **Third-Party Service Agreement** check box.
  8. Confirm or enter your payment information and click **Submit Order**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page.

You can also provision a transient virtual server by using the {{site.data.keyword.slapi_short}}. For an example, see [Provisioning a transient instance using Create Object](/docs/vsi/vsi_provision_api.html#api-rest-transient).
{:tip}

## Next Steps
After your virtual server is provisioned, you can start managing it. For more information, see [Managing your virtual server](/docs/vsi/vsi_managing.html).
