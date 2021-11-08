---

copyright:
  years: 2018, 2021
lastupdated: "2021-11-08"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:note: .note}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Viewing suspend billing feature
{: #viewing-suspend-billing-feature}

From your **Device List**, you can see what virtual server instances are using the suspend billing feature. Use the following steps to see which of your devices support suspend billing.
{: shortdesc}

Your virtual server instances must be configured with the following settings to support the suspend billing feature.

- Hourly SAN
- A public profile from one of the following families
   - Balanced
   - Compute
   - Memory
   - Variable compute

## Before you begin
{: #before-you-begin-viewing-suspend}

First, go to the device menu and make sure that you have the correct account permissions to complete the task. 

* Go to your console's device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions. 

For more information about permissions, see [Classic infrastructure permissions](/docs/account?topic=account-infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Viewing the suspend billing feature
{: #viewing-the-suspend-billing-feature}

To determine whether your virtual server instance supports the suspend billing feature, use the following steps:

1. From the **Devices** menu, select **Device List**. 
2. From the **Device List**, click the name of your virtual server instance. 
3. In the **Instance details** section, you can view whether your virtual server instance supports the suspend billing feature. 

| Field                                 | Value                     |
| --------------------------------------| ------------------------- |
| Suspended billing: Enabled on Power Off | Feature is supported.     |
| Suspended billing: Unavailable          | Feature is not supported. |
{: caption="Table 1. Suspend billing details" caption-side="top"}

## Viewing the suspend billing feature through the {{site.data.keyword.cloud}} API
{: #viewing-the-suspend-billing-feature-through-the-softlayer-api}

The following command is an example request of verifying whether your virtual server instance supports the suspend billing feature through the {{site.data.keyword.cloud}} API.

The following JSON request and response is a generic example. 
{: note}

```bash
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```
{: pre}

The following example is the JSON response to the request:

```bash
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```
{: pre}

For more information, see the [SLDN API documentation](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: external}.

## Next steps
{: #next-steps-suspend-billing-feature}

For more information about the suspend billing feature, see the following information:
1. [Suspend billing](/docs/virtual-servers?topic=virtual-servers-requirements)
2. [Managing virtual servers](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)
