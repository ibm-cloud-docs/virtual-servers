---

copyright:
  years: 2017, 2019
lastupdated: "2019-10-23"

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
There is insufficient capacity to complete the request.
```
{:screen}

When provisioning fails, all the virtual server instances within that particular request fail.
{:tip}

## Why it's happening
{: #why-it-s-happening}

An error occurs when there are insufficient resources available in the router or data center to fulfill the service request. There are a number of reasons that you could receive this error. Resource availability changes frequently, so you might wait and try again later.

## How to fix it
{: #how-to-fix-it}

You can attempt to provision again by using the following strategies:

1. Provision specifying a different router.  
2. Provision without specifying a router.
3. Provision in a different data center.

   GPU provisioning is allowed only in datacenters dal10, dal12, dal13, lon04, lon06, wdc07, tok02, syd04, and fra02
   {:note}

4. Provision fewer instances.
5. Spread out instances by provisioning to multiple data centers.
6. Provision smaller instance sizes.
7. Alter the instance storage from SAN to LOCAL or LOCAL to SAN.
