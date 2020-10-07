---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-19"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning reserved capacity and instances
{: #provisioning-reserved-capacity-and-instances}

## Before you begin
{: #before-you-begin-provisioning-reserved}

You can provision your reserved capacity and instances through the {{site.data.keyword.cloud}} catalog. You must provision your reserved capacity before your virtual server instances.

If you are not the account administrator, your user account must include the **Manage Reserved Capacities** permission. The account administrator can grant user's permission from the **Portal Permissions** tab in the console. For more information about updating permissions, see [Managing infrastructure access](/docs/account?topic=account-mngclassicinfra#mngclassicinfra).
{:note}

## Provisioning reserved capacity
{: #provisioning-reserved-capacity}

In the {{site.data.keyword.cloud_notm}} catalog, complete the following steps to provision your reserved capacity.

  1. Open the [reserved virtual server instance ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?guestType=reserved&cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} page from the catalog.
  2. To create new reserved capacity, select **New capacity +**. From the **Reserved capacity** page, enter or select the following information:

| Field                   | Value               |                                                                                                                                                                                                                                                                                                                                 
| ----------------------- | ------------------- |
| Name                    | A name is required for your reserved capacity. |                                                                                                                                                                                                                                                                                                       
| Virtual server capacity | Select the number of instances you want to assign to this reserved capacity (limit of 20 instances). |
| Plan Terms              | Choose between either a one or three year contract term. |  
| Location                | Select the specific location that is required for your workloads. Locations are composed of regions; each region is a separate geographic area. **Note:** You can't select individual locations for each virtual server instance that you provision within this reserved capacity. Your selection is the location for all virtual server instances that you provision within this reserved capacity. |
| Pod                     | Select the pod specific to your location. |                                                                                                                                                                                                                                                                                          
| Profile                 | Select from popular profiles or all available vCPU and RAM combinations of SAN-backed storage (balanced, memory, or compute). **Note:** You cannot combine different profile sizes within the set of virtual server instances assigned to this capacity or change them later. The set of virtual server instances you reserve must be the same size. |
{: caption="Table 1. Reserved capacity provisioning selections" caption-side="top"}


## Provisioning reserved instances
{: #provisioning-reserved-instances}

After you've provisioned your reserved capacity, it's time to provision your reserved virtual server instances. Reserved virtual server instances can be provisioned at any time during the contract term because your capacity is guaranteed. Complete the following steps to provision your reserved instances.

1. Open the [reserved virtual server instance ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?guestType=reserved&cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} page from the catalog.
2. To provision a reserved virtual server instance, enter or select the following information:

| Field                     | Value               |                                                                                                                                                                                                                                                                                                                                 
| ------------------------- | ------------------- |
| Name                      | A name is required for your reserved virtual server instance. |                                                                                                                                                                                                                                                                                                       
| Billing                   | Select either hourly or monthly billing. |                                                                                                                                                                                                                                                
| Reserved Capacity         | Select your reserved capacity or select **New Capacity +** to provision additional reserved capacity. |                                                                                                                                                                                                     
| Add-ons                   | Choose any additional storage, network, or software. |                                                                                                                                                                                                                                                                                            
{: caption="Table 2. Reserved instances provisioning selections" caption-side="top"}

## Next steps
{: #next-steps-provisioning-reserved}

After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.cloud_notm}} console or {{site.data.keyword.slapi_short}}. For more information, see [Configuring virtual servers](/docs/virtual-servers?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).

If you have questions about reserved capacity and instances, see [FAQs: Reserved capacity and instances](/docs/virtual-servers?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances). 
