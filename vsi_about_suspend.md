---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-23"

keywords: suspend billing feature, suspend billing

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Suspend billing
{: #requirements}

When you power off {{site.data.keyword.BluVirtServers}} that support the suspend billing feature, you don't accrue costs for certain compute resources. Billing stops automatically when the server is powered off. The suspend billing feature helps you reduce cost and prevents you from having to reprovision a virtual server when you need its resources again. Suspend billing does not apply to secondary public IP addresses and storage. A minimum 25% usage charge is applied to an instance that is powered off during its billing cycle.
{: shortdesc}

If your profile doesn't support the suspend billing option or you choose not to suspend your instances, you are billed for your usage. The usage rate is based on the normal hourly or monthly rates for your instance configuration.

Most virtual server instances that were created before 1 November 2018 and instances that are billed monthly don't support the suspend billing feature. To find out whether your virtual server instance supports the suspend billing feature, see [Viewing the suspend billing feature](/docs/virtual-servers?topic=virtual-servers-viewing-suspend-billing-feature).
{: important}

## Before you begin
{: #suspend-billing-prereqs}

To provision a virtual server instance that supports the suspend billing feature, the virtual server instance must be configured with the following settings:

1. Hourly SAN
2. Public profiles from one of the following families:
    * Balanced
    * Compute
    * Memory
    * Variable compute

For suspend billing to work properly, your instance must meet the preceding requirements and you must specify a profile.
{: important}

You can use the suspend billing feature as a faster alternative to provisioning and reclaiming a virtual server instance.

Billing is suspended only when you power off your virtual server instance through the {{site.data.keyword.cloud_notm}} console, CLI, or {{site.data.keyword.slapi_short}}. If you power off your virtual server instance directly through the OS, billing isn't suspended for that instance.
{: important}

## Provisioning details
{: #provisioning-details}

You can provision a virtual server instance that supports the suspend billing feature through the {{site.data.keyword.cloud_notm}} catalog (cloud.ibm.com), CLI, or the {{site.data.keyword.slapi_short}}. You can't provision a virtual server instance that supports the suspend billing feature through the {{site.data.keyword.slportal}} (control.softlayer.com). For more information about provisioning public virtual server instances, see [Provisioning public instances](/docs/virtual-servers?topic=virtual-servers-ordering-vs-public#ordering-vs-public).

For the {{site.data.keyword.cloud_notm}} catalog, you must have an upgraded account to order virtual servers. For more information about upgrading your account, see [Account types](/docs/account?topic=account-accounts).

### Provisioning through the API
{: #provisioning-through-API}

You can provision a virtual server instance that supports the suspend billing feature through the {{site.data.keyword.slapi_short}}. For API examples, see [Provisioning a public instance with Place Order Object](/docs/virtual-servers?topic=virtual-servers-api-rest-public#provisioning-a-public-instance-using-place-order-object).

You must specify the specific suspend billing package ID during the provisioning process. You can query in the {{site.data.keyword.slapi_short}} for the suspend billing package ID by using the keyName `SUSPEND_CLOUD_SERVER`. For an example of searching for server packages, see [Understanding and building an order with the {{site.data.keyword.slapi_short}} order CLI](https://sldn.softlayer.com/article/understanding-ordering/){: external}.

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
{: summary="This table has row and column headers. The row headers identify the resource. The column headers identify whether billing stops or persists when your instance is powered off. To understand whether billing stops or persists for a resource, go to the row in the table, and find the billing information that you are interested in."}

When you provision a virtual server instance that supports suspend billing, the usage times are calculated per second. Usage includes both the in use time and suspended time of your virtual server instance. Even if you never initiate the suspend billing feature by powering off your instance, the billing is calculated per second of the instance's lifecycle.

### Minimum usage charge
{: #minimum-usage-charge}

Virtual server instances that support suspend billing have a minimum usage charge. This minimum usage charge is applied when a virtual server instance is powered off during its billing cycle whether the server was used.

- If usage is fewer than 25% of the allotted hours, you are charged the minimum 25% of the allotted hours - no matter how few hours that the server used.
- If usage is greater than 25% of the allotted hours, you are billed for all of the hours that the server used.

### Billing invoice
{: #billing-invoice}

When you suspend billing on a virtual server, a few changes appear in your billing invoice. The relevant charges now appear as usage-based details. For example, you might see the following additions that reflect hours available, hours that were used, and total number of hours charged:

```text
Computing instance usage...
RAM usage...
Operating system usage...
```
{: screen}

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

After you provision a virtual server that supports suspend billing, you can start suspend and resume billing on the device.

When billing is suspended on a virtual server instance, you can't complete all of the same actions on the instance until you resume billing for the device. You can view whether your device is stopped, and the relevant date when the status changed, through the {{site.data.keyword.slapi_short}} or by accessing the **Device details** page in the {{site.data.keyword.slportal}}.

To suspend billing on a virtual server instance, power off the virtual server. For more information, see [Managing virtual servers](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers).
