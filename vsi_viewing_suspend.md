---

copyright:
  years: 2018, 2019
lastupdated: "2019-03-01"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Viewing suspend billing feature
You can view whether your virtual server instance supports the suspend billing feature in the {{site.data.keyword.slportal_full}} or through the {{site.data.keyword.slapi_short}}.

## Viewing the suspend billing feature in the customer portal
To determine if your virtual server instance supports the suspend billing feature in the {{site.data.keyword.slportal}}, use the following steps:

1. Log in to the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
2. From the **Devices** menu, select **Device List**.
3. From the **Device List**, click the name of your virtual server instance.
4. On the **Configuration** tab in the **General** section, you can view whether your virtual server instance supports the suspend billing feature.

| Field                                 | Value                     |
| --------------------------------------| ------------------------- |
| Suspend Billing: Enabled on Power Off | Feature is supported.     |
| Suspend Billing: Unavailable          | Feature is not supported. |
{: caption="Table 1. Suspend billing details" caption-side="top"}

## Viewing the suspend billing feature through the Softlayer API

The following command is an example request of verifying if your virtual server instance supports the suspend billing feature in the {{site.data.keyword.slapi_short}}.

**Note**: The following JSON request and response is a generic example.

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

To learn more about the suspend billing feature, review the following information:
1. [About suspend billing](/docs/vsi?topic=virtual-servers-requirements)
2. [Managing virtual servers](/docs/vsi?topic=virtual-servers-managing-virtual-servers)
