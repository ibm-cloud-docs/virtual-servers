---

copyright:
  years: 2018, 2024
lastupdated: "2023-10-16"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Provisioning reserved capacity and instances
{: #provisioning-reserved-capacity-and-instances}

## Before you begin
{: #before-you-begin-provisioning-reserved}

You can provision your reserved capacity and instances through the {{site.data.keyword.cloud}} catalog. You must provision your reserved capacity before your virtual server instances.
{: shortdesc}

If you are not the account administrator, your user account must include the **Manage Reserved Capacities** permission. The account administrator can grant user permission from the **Portal permissions** tab in the console. For more information about updating permissions, see [Managing infrastructure access](/docs/account?topic=account-mngclassicinfra#mngclassicinfra).
{: note}

## Provisioning reserved capacity
{: #provisioning-reserved-capacity}

In the {{site.data.keyword.cloud_notm}} catalog, complete the following steps to provision your reserved capacity.

1. Open the [reserved virtual server instance](https://cloud.ibm.com/gen1/infrastructure/provision/vs?guestType=reserved&cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: external} page from the catalog.
2. Select **New capacity +**. From the **Reserved capacity** page, enter or select the following information:

| Field                   | Value               |                                                                                                     
| ----------------------- | ------------------- |
| Name                    | A name is required for your reserved capacity. |                                                                         
| Virtual server capacity | Select the number of instances you want to assign to this reserved capacity (limit of 20 instances). |
| Plan terms              | A 1-year contract term. |  
| Location                | Select the specific location for your workloads. Locations are composed of regions; each region is a separate geographic area.  \n You can't select individual locations for each virtual server instance that you provision within this reserved capacity. Your selection is the location for all virtual server instances that you provision within this reserved capacity. |
| Pod                     | Select the pod that is specific to your location. |                                                                               
| Profile                 | Select a profile that meets your needs (balanced, memory, or compute).  \n You can't combine different profile sizes within the set of virtual server instances that are assigned to this capacity and you can't change them later. The set of virtual server instances that you reserve must be the same size. |
{: caption="Reserved capacity provisioning selections" caption-side="top"}

## Provisioning reserved instances
{: #provisioning-reserved-instances}

After you provision your reserved capacity, you can provision your reserved virtual server instances. You can provision reserved virtual server instances at any time during the contract term because your capacity is available. Complete the following steps to provision your reserved instances.

1. Open the [reserved virtual server instance](https://cloud.ibm.com/gen1/infrastructure/provision/vs?guestType=reserved&cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: external} page from the catalog.
2. Enter or select the following information:

| Field                     | Value               |                                                                                                   
| ------------------------- | ------------------- |
| Name                      | A name is required for your reserved virtual server instance. |                                                         
| Billing                   | Select either hourly or monthly billing. |                                                                             
| Reserved capacity         | Select your reserved capacity or select **New capacity +** to provision extra reserved capacity. |                     
| Add-ons                   | Choose any extra storage, network, or software. |                                                                       
{: caption="Reserved instances provisioning selections" caption-side="top"}

## Next steps
{: #next-steps-provisioning-reserved}

After your virtual server is provisioned and available to use, you can configure your virtual servers by using the
{{site.data.keyword.cloud_notm}} console or the API. For more information, see [Configuring virtual servers](/docs/virtual-servers?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).

If you have questions about reserved capacity and instances, see [FAQs: Reserved capacity and instances](/docs/virtual-servers?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances).
