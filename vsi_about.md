---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-29"

keywords: scalable virtual servers, virtual servers, key features

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# About virtual servers
{: #about-virtual-servers}

{{site.data.keyword.BluVirtServers}} are scalable virtual servers that are purchased with cores and memory allocations. They are a great option if you are looking for compute resources, that can be added in minutes, with access to features like image templates. The hypervisor is fully managed by {{site.data.keyword.cloud_notm}} and you can perform configuration and management tasks by using both the {{site.data.keyword.cloud_notm}} console and the {{site.data.keyword.slapi_short}}. Virtual servers are deployed to the same VLANs as physical servers, allowing you to spread workloads across virtual servers and bare metal servers, while maintaining interoperability. Virtual servers are fully customizable when you order them, with options to scale up as your compute needs grow.
{:shortdesc}

Newer version available. Try our Virtual Servers for VPC. For more information, see [Virtual Private Cloud](/docs/vpc?topic=vpc-getting-started).
{:tip}

When you create a virtual server, you can choose between a public (multi-tenancy) environment or a dedicated (single-tenancy) environment. You can also choose between hourly or monthly billing, and high-performance local disks or enterprise SAN storage.

## Key features
The following information lists the key features that are included with virtual servers.

### Seamless integration
Virtual servers are deployed to the same pod and network as bare metal servers and network appliances. This gives you the flexibility to use the best technology for each workload. Multiple virtual servers are commonly deployed behind a load balancer to serve web traffic. These servers can have direct layer 2 private network access to bare metal database servers and other more intensive workloads.

### Fully customizable
You can build-to-suit any virtual server with a number of options. There are no pre-defined package requirements, so you can tune each server to the workload it supports.

### Rapid provisioning
Virtual servers are provisioned in as few as 5 minutes, giving you minimal wait time between order and provisioning.

### Remote management
Like all of our services and solutions, you have the ability to manage your virtual servers remotely. View and manage all of your device details by using the {{site.data.keyword.cloud_notm}} console or {{site.data.keyword.slapi_short}}. You can also interact with the server through the provided KVM functions or log in to the server with full administrative control through the public or private interfaces.

### Easily scalable
After your virtual server is provisioned, you can quickly and easily scale your instance up or down and add or remove extra instances on demand. You can take an image template of the server once it is configured and tuned, and then create more virtual servers based on that original image.
