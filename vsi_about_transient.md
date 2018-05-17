---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Transient virtual servers
The {{site.data.keyword.BluVirtServers}} transient offering is a good option if you have flexible workloads and want cost savings. You will save money by running your workload on a transient virtual server. Transient instances are provisioned when there is unused capacity available. Therefore, when data center resources are needed for full, on-demand accounts, you can also lose those resources. Transient instances are de-provisioned on a first-on, first-off basis when those resources need to be reclaimed.   

Transient virtual servers are ideal for non-production workloads. For example, you might use a transient instance to test and develop applications, or test scalability in environments that don't require constant uptime.

## Requirements
To take advantage of transient instances, you must provision using the following public virtual server selections:
* Transient
* Your host location; you can select from the following data centers:
    * MEX01 
    * SEO01
    * PAR01

Transient instances are public instances that use SAN-backed storage.

## Notifications
You can use the {{site.data.keyword.slapi_short}} to receive notifications when resources are available for a transient instance. You can also use the API to programmatically provision a transient virtual server when resources become available. Likewise, you can use the API to programmatically stop provisioning instances when resources become unavailable. For more information, see [Configuring automated reclaim notifications](configuring-automated-reclaim-notifications.html).

## Limitations
Consider the following limitations before provisioning a transient virtual server.

* The number of supported, concurrent instances are part of your account-wide device quota. For more information about concurrent instance limits, see [FAQ: Virtual servers](../vsi/vsi_faqs_vs.html#concurrent).
* Transient instances cannot be upgraded or downgraded.
* Resources can be reclaimed at any time, without notification.
* Transient instances cannot use local storage.
* Transient instances only use SAN-backed storage (balanced, compute, memory).
* Transient instances cannot use GPU-based flavors.


## Next Steps

After you review and select your virtual server flavor, it's time to provision your transient virtual server. To get started, review the following information:
1. [Provisioning selections](../vsi/vsi_public_selections.html)
2. [Provisioning transient instances](../vsi/vsi_provision_transient.html)
