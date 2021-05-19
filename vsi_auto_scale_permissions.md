---

copyright:
  years: 2014, 2021
lastupdated: "2021-05-19"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:external: target="_blank" .external}

# Setting up user permissions for auto scale
{: #user-permissions-required-to-use-auto-scale}

Access to auto scale options requires a special user permission beyond the ability to order and manage {{site.data.keyword.virtualmachinesshort}}. To access the auto scale features, you must have permission to manage all of the virtual servers on the account in addition to any future virtual devices added.

If you are the account administrator and you want to grant users permission to access auto scale options, complete the following steps:

1. Log in to the [Access (IAM)](https://cloud.ibm.com/iam/overview){: external} page in the {{site.data.keyword.cloud}} console. 
2. In the **Users** tab, select **View by: My classic infrastructure users**.
3. Select a user, then click the **Classic infrastructure** tab.
4. Expand the **Devices** category in the **Permissions tab** and select **Manage Auto Scale Groups**.
5. Click **Apply**.

## Next steps
{: #next-steps-user-permissions-auto-scale}

After you have permission to access and use the auto scale options, you're ready to use the feature. To get started, review the following information:

1. [Managing traffic spikes with schedule-based auto scaling](/docs/virtual-servers?topic=virtual-servers-managing-schedule-based-auto-scaling)
2. [Managing traffic spikes with resource-based auto scaling](/docs/virtual-servers?topic=virtual-servers-managing-resourced-based-auto-scaling)
3. [FAQs: Auto scale](/docs/virtual-servers?topic=virtual-servers-faqs-auto-scale)

