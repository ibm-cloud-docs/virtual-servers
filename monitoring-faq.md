---

copyright:
  years: 2020, 2024
lastupdated: "2024-07-23"

keywords:

subcollection: cloud-infrastructure

---

{{site.data.keyword.attribute-definition-list}}

# FAQs: {{site.data.keyword.mon_full_notm}}
{: #faq-monitoring}

## Why did {{site.data.keyword.cloud}} transition from Advanced Monitoring by Nimsoft to {{site.data.keyword.mon_full_notm}}?
{: #why-transition-monitoring}
{: faq}

{{site.data.keyword.cloud}} is committed to providing you with the highest quality of service and is making the transition to a new monitoring offering. {{site.data.keyword.mon_full_notm}} offers an improved customer experience, robust functionality, and customizable dashboards for your resource monitoring needs. For more information, see [{{site.data.keyword.mon_full_notm}}](/docs/monitoring?topic=monitoring-getting-started).

## What benefits does {{site.data.keyword.mon_full_notm}} provide?
{: #what-are-new-benefits}
{: faq}

* A cloud-native and container intelligence management system that you can include as part of your {{site.data.keyword.cloud}} architecture.
* Provides real-time operational visibility into the performance and health of your applications, IBM services, and platforms.
* A visual representation of your infrastructure. {{site.data.keyword.mon_full_notm}} automatically collects important metrics such as CPU usage, used and available memory, response times, network latency, and more.
* Administrators, DevOps teams, and developers full-stack have telemetry with advanced features to monitor and troubleshoot, define alters, and design custom dashboards.

## How does {{site.data.keyword.mon_full_notm}} pricing work?
{: #will-monitoring-cost-more}
{: faq}

{{site.data.keyword.mon_full_notm}} offers different pricing plans.

* Light plan
* Graduated Tier plan

For more information about plans and pricing, see [{{site.data.keyword.mon_full_notm}} pricing](/docs/monitoring?topic=monitoring-pricing_plans).

## How do I install {{site.data.keyword.mon_full_notm}}?
{: #how-do-i-install-monitoring}
{: faq}

You can install and configure an {{site.data.keyword.mon_full_notm}} agent for any of the following environments:

* Kubernetes, GKE, and Red Hat OpenShift
* Docker containers or for noncontainerized services
* Mesos&reg;, Marathon, and DCOS
* Linux installations

In addition to the previously listed environments, you can see all of the {{site.data.keyword.cloud}} services that are {{site.data.keyword.mon_full_notm}}-enabled [here](/docs/monitoring?topic=monitoring-cloud_services).

For information about installing {{site.data.keyword.mon_full_notm}}, see [Getting started tutorial](/docs/monitoring?topic=monitoring-getting-started).

## How do I get started with {{site.data.keyword.mon_full_notm}}?
{: #how-do-i-get-started-monitoring}
{: faq}

For information about provisioning, configuring your agent, managing data, and alerting, see {{site.data.keyword.mon_full_notm}}, see [Getting started tutorial](/docs/monitoring?topic=monitoring-getting-started).

## What if I used custom images with Advanced Monitoring by Nimsoft?
{: #what-if-i-use-custom-images-with-nimsoft}
{: faq}

To simplify this transition, {{site.data.keyword.cloud}} automatically removed the "Advanced Monitoring" attribute from all of your custom images to prevent provisioning failures after **8 May 2020** when Advanced Monitoring by Nimsoft is no longer available. By removing this attribute, you can continue to use custom images without interruption. If you want to continue with resource monitoring, you need to manually install {{site.data.keyword.mon_full_notm}} after a new resource is provisioned.

## How do I get help if I have issues with this transition?
{: #how-do-i-get-transition-help}
{: faq}

If you need help transitioning to {{site.data.keyword.mon_full_notm}}, you can contact your CSM or see [Getting support](https://cloud.ibm.com/unifiedsupport/supportcenter){: external} to open a support ticket.

## What are the important dates that are associated with Advanced Monitoring by Nimsoft EOS?
{: #what-are-important-transition-dates}
{: faq}

* **End of Marketing (EOM): 8 May 2020** After this date, Advanced Monitoring by Nimsoft is no longer available for purchase.
* **End of service (EOS): 8 July 2020** After this date, Advanced Monitoring by Nimsoft is no longer supported and usage is withdrawn by {{site.data.keyword.cloud}}.

## What happens if I can't make the transition on time?
{: #what-if-i-cannot-transition-on-time}
{: faq}

Advanced Monitoring by Nimsoft is available for purchase until **8 May 2020**. After this date, {{site.data.keyword.mon_full_notm}} supports all new monitoring purchases. For any resources with Advanced Monitoring by Nimsoft that were enabled before 8 May 2020, you can continue to use Advanced Monitoring by Nimsoft until support and usage is withdrawn on **8 July 2020**. Failure to move your resource monitoring to {{site.data.keyword.mon_full_notm}} by **8 July 2020** results in a gap in your resource monitoring. 
