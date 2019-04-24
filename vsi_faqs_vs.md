---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-23"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:faq: data-hd-content-type='faq'}


# FAQs: Virtual servers  
{: #faqs-virtual-servers}

## What types of virtual servers are available for use?
{:faq}

{{site.data.keyword.BluSoftlayer_full}} offers a couple types of virtual servers. The standard offering is a public-based virtual server, which is a multi-tenant environment, suitable for a variety of needs. If you're looking for a single-tenant environment, consider the Dedicated Virtual Server offering. The dedicated virtual server option is ideal for applications with more stringent resource requirements. For more information about the current virtual server offerings see, [Getting started with virtual servers](/docs/vsi?topic=virtual-servers-getting-started-tutorial).

## Where can I find pricing information for public instance types?
{:faq}

For pricing information, see [Build your virtual server ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers){: new_window}.

## Where can I find pricing information for virtual public instances?
{:faq}

For pricing information, see the [Virtual servers provisioning calculator ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

## Can I add disk storage to my hourly or monthly Virtual Server?
{:faq}

You may upgrade or downgrade disk storage for any virtual server by updating your storage options in the *First Disk* through *Fifth Disk* fields in the *Configuration* screen of the device you want to update. For more information, see [Reconfiguring an existing virtual server](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers).

## How many hourly Virtual Servers can I start up?
{:faq}

By default, an account has a limit of 20 instances that can run on public virtual servers, dedicated virtual servers, and bare metal servers, at any given time.  If you would like to increase this limit, please contact support to tell us a little more about what you are doing and how many concurrent instances you might need.

## How will I be billed for bandwidth for my hourly Virtual Servers?
{:faq}

Hourly virtual billing is broken down for inbound and outbound traffic. All inbound traffic to your virtual server is free of charge. Outbound traffic is metered and charged per GB, with totals assessed at the end of your billing period.

## In what cases is my virtual server migrated to a different host?
{:faq}
In limited cases a virtual server might need to be migrated to a different host. If a migration is required, the virtual server is shut down, migrated, and then restarted. A virtual server might be migrated in the following cases:

* A hypervisor needs to be updated, a host is being decommissioned, or a host is not allowed to take on new instances. If a host is marked for any of these changes, when one of its virtual server is rebooted from the {{site.data.keyword.slportal_full}}, the reboot automatically triggers the virtual server to be migrated to a different host.
* Infrastructure maintenance. You might receive an email indicating that maintenance is required on a system that is hosting your virtual server. Your virtual server might need to be migrated as part of the infrastructure maintenance.
* An upgrade to an existing instance. For consistent performance, if you upgrade an instance it might be migrated to a different host to ensure that it receives the appropriate dedicated CPU and memory.

During a maintenance window you might see a **Migrate Host** option display in the **Actions** menu of your device in the {{site.data.keyword.slportal}}. **Migrate Host** allows you to migrate the virtual server to a new host at your convenience during a specified maintenance period. If you do not initiate the migration during the maintenance period, then the virtual server is automatically migrated to complete the required maintenance. The **Migrate Host** option does not persist and is only available during maintenance periods that are communicated through maintenance notifications.

You might also see the **Migrate Host** option if one of your virtual servers is required to have a certain level of hypervisor that is not available on the current host.

## What happens to my data when my portable storage is deleted?
{:faq}

When storage is deleted, any pointers to the data on that volume are removed, thus the data becomes completely inaccessible. If the physical storage is reprovisioned to another account, a new set of pointers are assigned. There is no way for the new account to access any data that might have been on the physical storage. The new set of pointers shows all 0's. When new data is written to the volume/LUN, any inaccessible data that still exists gets overwritten.

## Can I use a Red Hat Cloud Access subscription to create a virtual server?
{:faq}

Yes. When you import an image, you can specify that you will provide the operating system license. For more information, see [Use Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription). Then you can order a virtual server from that image template and use your existing [Red Hat Cloud Access ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} subscription.

## What is the difference between a virtual server and a virtual private server (VPS)?
{:faq}
A virtual server is similar to the virtual private server (VPS) or virtual dedicated server (VDS) platforms you might already be familiar with. These "virtual server" environments allow for distinct environments to be provisioned privately and securely on a single hardware node, but VDS and VPS are more limited in their capabilities. VPS and VDS options are generally confined to a single-server architecture, so the only resources that can be added or divvied up between each virtual server on a VDS or VPS are the resources physically installed on that single server.

Virtual servers are provisioned on a multi-server cloud architecture that pools all available hardware resources for individual instances to use. Virtual servers can leverage a shared high-capacity SAN-based primary storage platform or high-performance local disk storage. Because each instances is part of the larger cloud environment, communication between all virtual servers is instantaneous.

<!--## I'm unable to connect to the virtualization API. How can I fix this?-->

<!--This error generally occurs because a password is outdated. To fix this, update the root or Administrator password for the virtual server's operating system in the {{site.data.keyword.slportal_full}}.-->

## Why do I receive a capacity error when provisioning a virtual server?
{:faq}

When you provision a virtual server, you might receive an error message stating that there is insufficient capacity to complete the request. When provisioning fails, all the virtual server instances within that particular request fail. A capacity error occurs when there are insufficient resources available in the router or data center to fulfill the service request. There are a number of reasons that you could receive this error. Resource availability changes frequently, so you might wait and try again later. For more information on strategies to avoid this error, see [Resource considerations for virtual server instances](/docs/vsi?topic=virtual-servers-capacity-considerations).
