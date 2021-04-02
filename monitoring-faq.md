---

copyright:
  years: 2020, 2021
lastupdated: "2021-04-02"

keywords: 

subcollection: cloud-infrastructure

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# FAQs: {{site.data.keyword.mon_full_notm}}
{: #faq-monitoring}

## Why is {{site.data.keyword.cloud}} making the transition from Advanced Monitoring by Nimsoft to {{site.data.keyword.mon_full_notm}}?
{: #why-transition-monitoring}
{: faq}

IBM Cloud is committed to providing you the highest quality of service and is making the transition to a new monitoring offering. {{site.data.keyword.mon_full_notm}} offers an improved customer experience, robust functionality, and customizable dashboards for your resource monitoring needs. For more information, see [{{site.data.keyword.mon_full_notm}}](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-getting-started).

## What benefits does {{site.data.keyword.mon_full_notm}} provide?
{: #what-are-new-benefits}
{: faq}

* A cloud native and container intelligence management system that you can include as part of your {{site.data.keyword.cloud}} architecture.

* Provides real-time operational visibility into the performance and health of your applications, IBM services and platforms.

* A visual representation of your infrastructure. {{site.data.keyword.mon_full_notm}} automatically collects important metrics such as CPU usage, used and available memory, response times, network latency, and more. <!--For more information about {{site.data.keyword.mon_full_notm}} metrics, see [{{site.data.keyword.mon_full_notm}} metrics](/docs/cloud-infrastructure?topic=cloud-infrastructure-sysdig-monitoring-metrics).-->

* Offers administrators, DevOps teams, and developers full stack telemetry with advanced features to monitor and troubleshoot, define alters, and design custom dashboards. 

## Will {{site.data.keyword.mon_full_notm}} cost me more? If yes, how much?
{: #will-monitoring-cost-more}
{: faq}

Depending on which Advanced Monitoring by Nimsoft plan you are using, you might see an increase in your monthly resource monitoring cost. {{site.data.keyword.mon_full_notm}} offers different pricing plans.

* Light plan
* Graduated Tier plan

For more information about plans and pricing, see [{{site.data.keyword.mon_full_notm}} pricing](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-pricing_plans).

## How do I install {{site.data.keyword.mon_full_notm}}?
{: #how-do-i-install-monitoring}
{: faq}

You can install and configure an {{site.data.keyword.mon_full_notm}} agent for any of the following environments:
* Kubernetes, GKE, and OpenShift
* Docker containers or for non-containerized services
* Mesos, Marathon, and DCOS
* Linux installations

In addition to the previously listed environments, you can see all of the IBM Cloud services that are {{site.data.keyword.mon_full_notm}}-enabled [here](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-cloud_services).

For information about installing {{site.data.keyword.mon_full_notm}}, see [Getting started tutorial](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-getting-started).

## How do I get started with {{site.data.keyword.mon_full_notm}}?
{: #how-do-i-get-started-monitoring}
{: faq}

For information about provisioning, configuring your agent, managing data, and alerting, see {{site.data.keyword.mon_full_notm}}, see [Getting started tutorial](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-getting-started).

<!--## How do I uninstall Advanced Monitoring by Nimsoft?
{: #how-do-i-uninstall-nimsoft}
{: faq}-->

<!--For information about uninstalling Advanced Monitoring by Nimsoft, see [Uninstalling Advanced Monitoring by Nimsoft](/docs/cloud-infrastructure?topic=cloud-infrastructure-faq-sysdig-monitoring#how-do-i-uninstall-nimsoft).-->

## What if I am using custom images with Advanced Monitoring by Nimsoft?
{: what-if-i-use-custom-images-with-nimsoft}
{: faq}

To simplify this transition, IBM Cloud will automatically remove the "Advanced Monitoring" attribute from all of your custom images to prevent provisioning failures after **8 May 2020** when Advanced Monitoring by Nimsoft is no longer available. By removing this attribute, you can continue to use custom images without interruption. If you want to continue with resource monitoring, you need to manually install {{site.data.keyword.mon_full_notm}} after a new resource is provisioned.


## How do I get help if I have issues with this transition?
{: #how-do-i-get-transition-help}
{: faq}

If you need help transitioning to {{site.data.keyword.mon_full_notm}}, you can contact your CSM or see [Getting support](https://cloud.ibm.com/unifiedsupport/supportcenter){: external} to open a support ticket.

## What are the important dates that are associated with Advanced Monitoring by Nimsoft EOS?
{: #what-are-important-transition-dates}
{: faq}

* **End of Marketing (EOM): 8 May 2020** After this date, Advanced Monitoring by Nimsoft is no longer available for purchase.
* **End of Service (EOS): 8 July 2020** After this date, Advanced Monitoring by Nimsoft is no longer supported and usage is withdrawn by IBM Cloud.

## What happens if I can't make the transition on time?
{: #what-if-i-cannot-transition-on-time}
{: faq}

Advanced Monitoring by Nimsoft is available for purchase until **8 May 2020**. After this date, {{site.data.keyword.mon_full_notm}} will support all new monitoring purchases. For any resources with Advanced Monitoring by Nimsoft that were enabled before 8 May 2020, you can continue to use Advanced Monitoring by Nimsoft until support and usage is withdrawn on **8 July 2020**. Failure to move your resource monitoring to {{site.data.keyword.mon_full_notm}} by **8 July 2020** will result in a gap in your resource monitoring. 
