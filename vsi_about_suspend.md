---

copyright:
  years: 2017, 2020
lastupdated: "2020-09-11"

keywords: suspend billing feature, suspend billing

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}

# Suspend billing
{: #requirements}

When you power off {{site.data.keyword.BluVirtServers}} that support the suspend billing feature, you don't accrue costs for certain compute resources. Billing stops automatically when the server is powered off. The suspend billing feature helps you reduce cost and prevents you from having to reprovision a virtual server when you need its resources again.
{:shortdesc}

If your profile doesn't support suspend billing or you choose not to suspend your instances, you are billed for your usage based on the normal hourly or monthly rates for your instance configuration.
{:note}

Most virtual server instances created before November 1st, 2018 don't support the suspend billing feature. To find out if your virtual server instance supports the suspend billing feature, see [Viewing suspend billing feature](/docs/virtual-servers?topic=virtual-servers-viewing-suspend-billing-feature).

## Before you begin
{: #suspend-billing-prereqs}

To provision a virtual server instance that supports the suspend billing feature, the virtual server instance must be configured with the following settings:

1. Hourly SAN
2. Public profiles from one of the following families:
    * Balanced
    * Compute
    * Memory
    * Variable compute

For suspend billing to work properly, your instance must meet the requirements above and you must specify a profile (also known as flavor).
{:important} 

You can use the suspend billing feature as a faster alternative to provisioning and reclaiming a virtual server instance.

Billing is suspended only when you power off your virtual server instance through the {{site.data.keyword.cloud_notm}} console, CLI, or {{site.data.keyword.slapi_short}}. If you power off your virtual server instance directly through the OS, billing isn't suspended for that instance.
{:note}

## Provisioning details
{: #provisioning-details}

You can provision a virtual server instance that supports the suspend billing feature through the {{site.data.keyword.cloud_notm}} catalog (cloud.ibm.com), CLI, or the {{site.data.keyword.slapi_short}}. You can't provision a virtual server instance that supports the suspend billing feature through the {{site.data.keyword.slportal}} (control.softlayer.com). For more information on provisioning public virtual server instances, see [Provisioning public instances](/docs/virtual-servers?topic=virtual-servers-ordering-vs-public#ordering-vs-public).

For the {{site.data.keyword.cloud_notm}} catalog, you must have an upgraded account to order virtual servers. For more information about upgrading your account, see [Switching to IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

### Provisioning through the Softlayer API
{: #provisioning-through-API}

You can provision a virtual server instance that supports the suspend billing feature through the {{site.data.keyword.slapi_short}}. For API examples, see [Provisioning a public instance using Place Order Object](/docs/virtual-servers?topic=virtual-servers-api-rest-public#provisioning-a-public-instance-using-place-order-object).

You must specify the specific suspend billing package ID during the provisioning process. You can query in the {{site.data.keyword.slapi_short}} for the suspend billing package ID by using the keyName `SUSPEND_CLOUD_SERVER`. For an example on searching for server packages, see [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Billing details
{: #billing-details}

It's important to understand what costs stop accruing and what costs persist when your virtual server instance is powered off.

| Resource                      | Billing stopped   | Billing persists |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          | ![Checkmark icon](../icons/checkmark-icon.svg) |                  |
| RAM                           | ![Checkmark icon](../icons/checkmark-icon.svg) |                  |
| Port speed                    | ![Checkmark icon](../icons/checkmark-icon.svg) |                  |
| Operating system licenses     | ![Checkmark icon](../icons/checkmark-icon.svg) |                  |
| Monitoring add-ons            | ![Checkmark icon](../icons/checkmark-icon.svg) |                  |
| Secondary public IP addresses |                   | ![Checkmark icon](../icons/checkmark-icon.svg) |
| Storage                       |                   | ![Checkmark icon](../icons/checkmark-icon.svg) |
{: row-headers}
{: class="comparison-table"}
{: caption="Table 1. Resource billing details" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the resource. The column headers identify whether billing stops or persists when your instance is powered off. To understand whether billing stops or persists for a resource, navigate to the row in the table, and find the billing information you are interested in."}  

When you provision a virtual server instance that supports the suspend billing feature, the usage times are calculated per second, for both the in use time and suspended time of your virtual server instance. Even if you never initiate the suspend billing feature by powering off your instance, the billing is calculated per second of the instance's lifecycle.
{:note}

### Minimum usage charge
{: #minimum-usage-charge}

Virtual server instances that support the suspend billing feature can have a minimum usage charge that is applied in some cases. If usage is greater than 25%, you are billed for that usage. If usage is less than 25%, you are charged for 25% of the hours that the instance existed within the current billing cycle.

### Billing invoice
{: #billing-invoice}

When you suspend billing on a virtual server, you will see a few changes in your billing invoice. The relevant charges now appear as usage-based details. For example, you might see the following additions that reflect hours available, hours used, and total number of hours charged:

```
Computing instance usage...
RAM usage...
Operating system usage...
```
{:screen}

## Resource details
{: #resource-details}

### Storage
{: #storage}

When you suspend billing on a virtual server instance, the billing for the associated storage persists, but you cannot access the stored data while the virtual server instance is powered off. When you resume billing on the instance, you can access your data again.

### IP addresses
{: #ip-addresses}

All public IP addresses are retained for you when billing is suspended for your virtual server instance.

### Limitations
{: #limitations-suspend-billing}

Virtual server instances that are suspended continue to count toward your account-wide device quota. For more information about instance limits, see [FAQ: Virtual servers](/docs/virtual-servers?topic=virtual-servers-faqs-virtual-servers#concurrent).

## Next steps
{: #next-steps-suspend-billing}

After you provision a virtual server that supports suspend billing, you can begin to suspend and resume billing on the device.

When billing is suspended on a virtual server instance, you can't complete all of the same actions on the instance until you resume billing for the device. You can view whether your device is stopped, as well as the relevant date when the status changed, through the {{site.data.keyword.slapi_short}} or by accessing the Device details page in the {{site.data.keyword.slportal}}.

To suspend billing on a virtual server instance, power off the virtual server. For more information, see [Managing virtual servers](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers).
