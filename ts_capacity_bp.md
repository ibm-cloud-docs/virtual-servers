---

copyright:
  years: 2017, 2021
lastupdated: "2021-05-18"

keywords: insufficient capacity to complete the request

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Resource considerations for virtual server instances
{: #capacity-considerations}

## What's happening
{: #what-s-happening}

When you provision a virtual server, you might receive the following error message:

```
Insufficient capacity to complete the request.
```
{:screen}

When provisioning fails, all the virtual server instances within that particular request fail.
{:tip}

## Why it's happening
{: #why-it-s-happening}

An error occurs when the router or data center has insufficient available resources to fulfill the service request. Resource availability changes frequently, so you might wait and try again later.

## How to fix it
{: #how-to-fix-it}

You can attempt to provision again by using the following strategies:

* Provision specifying a different router.  
* Provision without specifying a router.
* Provision in a different data center.

   You can provision GPUs only in the following data centers: dal10, dal12, dal13, lon04, lon06, wdc07, tok02, syd04, and fra02
   {:note}

* Provision fewer instances.
* Spread out instances by provisioning to multiple data centers.
* Provision smaller instance sizes.
* Alter the instance storage from SAN to LOCAL or LOCAL to SAN.
