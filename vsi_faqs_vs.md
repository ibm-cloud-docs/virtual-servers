---



copyright:
  years: 2017
lastupdated: "2017-09-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# FAQs: Public virtual servers  

## What types of virtual servers are available for use?
{{site.data.keyword.BluSoftlayer_full}} offers a couple types of virtual servers. The standard offering is a public-based virtual server, which is a multi-tenant environment, suitable for a variety of needs. If you're looking for a single-tenant environment, consider the Dedicated Virtual Server offering. The dedicated virtual server option is ideal for applications with more stringent resource requirements. For more information about the current virtual server offerings see, [Getting started with virtual servers](../vsi/vsi_index.html).

## Where can I find pricing information for public instance types?
For pricing information, see [Build your virtual server](https://www.ibm.com/cloud-computing/bluemix/virtual-servers).

## Can I add disk storage to my hourly or monthly Virtual Server?
You may upgrade or downgrade disk storage for any virtual server by updating your storage options in the *First Disk* through *Fifth Disk* fields in the *Configuration* screen of the device you want to update. For more information, see [Reconfiguring an existing virtual server](../vsi/vsi_reconfigure.html).

## How many hourly Virtual Servers can I start up?

By default, an account has a limit of 20 instances that can run on public virtual servers, dedicated virtual servers, and bare metal servers, at any given time.  If you would like to increase this limit, please contact support to tell us a little more about what you are doing and how many concurrent instances you might need.

## How will I be billed for bandwidth for my hourly Virtual Servers?

Hourly Virtual billing is broken down for inbound and outbound traffic. All inbound traffic to your Virtual Server is free of charge. Outbound traffic is metered and charged per GB, with totals assessed at the end of your billing period.

## What is the difference between a virtual server and a virtual private server (VPS)?

A virtual server is similar to the virtual private server (VPS) or virtual dedicated server (VDS) platforms you might already be familiar with. These "virtual server" environments allow for distinct environments to be provisioned privately and securely on a single hardware node, but VDS and VPS are more limited in their capabilities. VPS and VDS options are generally confined to a single-server architecture, so the only resources that can be added/divvied up between each virtual server on a VDS or VPS are the resources physically installed on that single server.

Virtual servers are provisioned on a multi-server cloud architecture that pools all available hardware resources for individual instances to use. Virtual servers can leverage a shared high-capacity SAN-based primary storage platform or high-performance local disk storage. Because each instances is part of the larger cloud environment, communication between all virtual servers is instantaneous.

## I'm unable to connect to the virtualization API. How can I fix this?

This error generally occurs because a password is outdated. To fix this, update the root or Administrator password for the virtual server's operating system in the Customer Portal.
