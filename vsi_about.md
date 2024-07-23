---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-23"

keywords: scalable virtual servers, virtual servers, key features

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# About virtual servers
{: #about-virtual-servers}

{{site.data.keyword.BluVirtServers}} are scalable virtual servers that are purchased with cores and memory allocations. These servers are a great option if you are looking for compute resources that can be added in minutes with access to features like image templates. For more information about image templates, see [Image templates](/docs/virtual-servers?topic=virtual-servers-image-templates).
{: shortdesc}

Virtual servers are deployed to the same VLANs as physical servers, which spread workloads across virtual servers and bare metal servers, while interoperability is maintained. Virtual servers are fully customizable when you order them, with options to scale up as your compute needs grow.

Newer version available! Try our Virtual Servers for VPC. For more information, see [Virtual Private Cloud](/docs/vpc?topic=vpc-getting-started).
{: tip}

When you create a virtual server, you can choose between a public (multi-tenancy) environment or a dedicated (single-tenancy) environment. You can also choose between hourly or monthly billing, and high-performance local disks or enterprise SAN storage.

The hypervisor is fully managed by {{site.data.keyword.cloud_notm}} and you can perform configuration and management tasks by using both the {{site.data.keyword.cloud_notm}} console and the {{site.data.keyword.slapi_short}}.

## Key features
{: #virtual-servers-key-features}

The following information lists the key features that are included with virtual servers.

### Seamless integration
{: #virtual-servers-seamless}

Virtual servers are deployed to the same POD and network as bare metal servers and network appliances. This type of deployment gives you the flexibility to use the best technology for each workload. Multiple virtual servers are commonly deployed behind a load balancer to serve web traffic. These servers can have direct layer 2 private network access to bare metal database servers and other more intensive workloads.

### Fully customizable
{: #virtual-servers-customizable}

You can build-to-suit any virtual server with a number of options. With no pre-defined package requirements, you can tune each server to the workload it supports.

### Rapid provisioning
{: #virtual-servers-rapid-provisioning}

Virtual servers are provisioned in as few as 5 minutes, giving you minimal wait time between order and provisioning.

### Remote management
{: #virtual-servers-remote-manage}

Like all of our services and solutions, you can manage your virtual servers remotely. View and manage all of your device details by using the {{site.data.keyword.cloud_notm}} console or {{site.data.keyword.slapi_short}}. You can also interact with the server through the provided KVM functions or log in to the server with full administrative control through the public or private interfaces.

### Easily scalable
{: #virtual-servers-scalable}

After you provision a virtual server, you can quickly and easily scale your instance up or down and add or remove extra instances on demand. You can take an image template of the server after it is configured and tuned, and then create more virtual servers based on that original image.
