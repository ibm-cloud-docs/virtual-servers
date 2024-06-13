---

copyright:
  years: 2017, 2024
lastupdated: "2023-09-28"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why does the server have insufficient capacity?
{: #vsi-troubleshooting-capacity-considerations}
{: troubleshoot}
{: support}


When you provision a virtual server, you might receive the following error message:
{: tsSymptoms}

_Insufficient capacity to complete the request._

When provisioning fails, all the virtual server instances within that particular request fail.
{: tip}

An error occurs when the router or data center has insufficient available resources to fulfill the service request. Resource availability changes frequently, so you might wait and try again later.
{: tsCauses}

You can attempt to provision again by using the following strategies:
{: tsResolve}


* Provision specifying a different router.
* Provision without specifying a router.
* Provision in a different data center.

   You can provision GPUs only in the following data centers: dal10, dal12, dal13, lon04, lon06, wdc07, tok02, syd04, and fra02
   {: note}

* Provision fewer instances.
* Spread out instances by provisioning to multiple data centers.
* Provision smaller instance sizes.
* Alter the instance storage from SAN to LOCAL or LOCAL to SAN.
