---



copyright:
  years: 2017
lastupdated: "2017-12-19"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Capacity considerations

## What's happening

When you provision a virtual server, you might receive the following error message: 

```
There is insufficient capacity to complete the request.
```
{:screen}

## Why it's happening

A capacity error occurs when there are insufficient resources available in the router or data center to fulfill the service request. There are a number of reasons that you could receive this error. Resource availability changes frequently, so you might wait and try again later.

## How to fix it 

You can attempt to provision again by using the following strategies:

1. Provision specifying a different router.  
2. Provision without specifying a router.
3. Provision in a different data center.
4. Provision fewer instances. 
5. Spread out instances by provisioning to multiple data centers.
6. Provision smaller instance sizes.

When provisioning fails, all the virtual server instances within that particular request fail.
{:tip}


