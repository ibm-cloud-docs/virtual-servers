---

copyright:
  years: 2017, 2021
lastupdated: "2021-05-20"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Dedicated hosts and dedicated instances
{: #dedicated-hosts-and-dedicated-instances}

Dedicated hosts are virtual servers that you can use to specify the data center and POD in which you want your host. You then assign instances, or virtual machines, to a specific host for maximum control over workload placement and for flexible cost-provisioning options.
{:shortdesc}

## Guaranteed capacity
{: #guaranteed-capacity}

You're guaranteed capacity within the data center and POD in which your host is placed. For example, if the POD containing your dedicated host and dedicated instances reaches capacity, you can continue to assign dedicated instances to your host if your host has appropriate space.

## Visible workloads
{: #visible-workloads}

You can view overall resource consumption for all dedicated instances that are assigned to a dedicated host on one page. View core, RAM, and local storage usage, which helps you determine whether you need to migrate dedicated instances to another dedicated host. This level of granularity gives you the ability to manage your workloads with maximum control.

## Post-deployment management
{: #post-deployment-management}

In addition to guaranteed capacity and visibility to your workloads, you can migrate your dedicated instances between dedicated hosts for maximum control over workload placement.

## Maintenance
{: #maintenance}

Occasionally, infrastructure maintenance requires a dedicated host to restart. For example, the Xen hypervisor might need an update. If you have multiple dedicated hosts, you have the following options to minimize maintenance downtime.
* Maintenance is done by PODs within a data center. You can deploy your dedicated hosts to separate PODs to spread out the maintenance.
* You can create a support ticket for a dedicated host to delay the scheduled maintenance request. During that time, you can migrate offline dedicated instances between dedicated hosts that are in the same POD.

## High availability
{: #high-availability}

If a dedicated host fails, the workloads on the dedicated host are automatically migrated to a new dedicated host. Dedicated instances remain dedicated throughout the lifecycle of the virtual server.

For high availability scenarios, you might want to consider an extra dedicated host. For example, the extra dedicated host provides you the flexibility to migrate workloads for maintenance windows.
