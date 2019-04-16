---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-11"

subcollection: virtual-servers

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
You have two options to provision your public virtual server instances. The first is through the {{site.data.keyword.Bluemix}} catalog and the second is through the {{site.data.keyword.slportal}}. The catalog and {{site.data.keyword.slportal}} require unique log-in IDs. Your catalog user name and password won’t work for logging in to the portal and vice versa.
{:shortdesc}

Before you begin, review the following prerequisites.

  1. Ensure that you have either your {{site.data.keyword.Bluemix_notm}} catalog or {{site.data.keyword.slportal}} credentials set-up.

     **Note:** For the {{site.data.keyword.Bluemix_notm}} catalog, you must have an upgraded account to order virtual servers. For more information about upgrading your account, see [Switching to IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).

  2. If you haven't done so, review the deployment options available to you. For more information, see [Deployment options: Public virtual server](/docs/vsi?topic=virtual-servers-about-public-virtual-servers).

  3. Review virtual server instance capacity considerations.  For more information, see [Capacity considerations](/docs/vsi?topic=virtual-servers-capacity-considerations).

## Provisioning a public virtual server instance
{: #ordering-public-instance}

After you complete the prerequisites, you can begin to provision a public virtual server instance. You can provision your public instance through the {{site.data.keyword.cloud_notm}} catalog or the {{site.data.keyword.slportal}}.

### Provisioning a public virtual server instance through the IBM Cloud catalog
To provision a public virtual server instance through the {{site.data.keyword.cloud_notm}} catalog, complete the following steps:

  1. Log in to the [{{site.data.keyword.cloud_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/){: new_window} by using your unique credentials.
  2. In the **Compute Infrastructure** section, click the **Virtual Servers** tile.
  3. Select the **Public Virtual Server** option.
  4. Click **Create**.
  5. Complete all of the relevant information for your virtual server instance.
  6. After you review your order summary, click the **Third-Party Service Agreements** check box.
  7. Click **Provision**.

### Provisioning a public virtual server instance through the customer portal
To provision your public virtual server instance through the {{site.data.keyword.slportal}}, complete the following steps:

  1. Log in to the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
  2. Locate the **Order** section and click **Devices**.
  3. On the Devices page, click **Hourly SAN**, **Hourly local**, **Monthly**, or **Transient** for one of the Virtual Server offerings.
  4. On the *Configure your Cloud Server* page, complete all the relevant information.
  5. Click the **Add to Order** button to continue.
  6. Confirm or edit the domain information for the server.
  7. Click the **Cloud Service terms** and the **Third-Party Service Agreement** check box.
  8. Confirm or enter your payment information and click the **Submit Order** button. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.Bluemix_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

## Next Steps
After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.slportal_full}} or {{site.data.keyword.slapi_full}}. For more information, see [Configuring virtual servers](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
