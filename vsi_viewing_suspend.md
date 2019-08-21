---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-28"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Viewing suspend billing feature
{: #viewing-suspend-billing-feature}

## Before you begin
{: #before-you-begin-viewing-suspend}

First, navigate to the device menu and ensure you have the correct account permissions to complete the task. 

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/vsi?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions. 

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Viewing the suspend billing feature
{: #viewing-the-suspend-billing-feature}

To determine if your virtual server instance supports the suspend billing feature, use the following steps:

1. From the **Devices** menu, select **Device List**. 
2. From the **Device List**, click the name of your virtual server instance. 
3. In the **Instance details** section, you can view whether your virtual server instance supports the suspend billing feature. 

| Field                                 | Value                     |
| --------------------------------------| ------------------------- |
| Suspended billing: Enabled on Power Off | Feature is supported.     |
| Suspended billing: Unavailable          | Feature is not supported. |
{: caption="Table 1. Suspend billing details" caption-side="top"}

## Viewing the suspend billing feature through the SoftLayer API
{: #viewing-the-suspend-billing-feature-through-the-softlayer-api}

The following command is an example request of verifying if your virtual server instance supports the suspend billing feature through the {{site.data.keyword.slapi_short}}.

The following JSON request and response is a generic example. 
{:note}

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

The following is the example JSON response to the request:

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

For more information, see the [SLDN API documentation ![External link icon](../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}.

## Next steps
{: #next-steps-suspend-billing-feature}

To learn more about the suspend billing feature, review the following information:
1. [Suspend billing](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [Managing virtual servers](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

