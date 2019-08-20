---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-10"

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

Dedicated hosts are virtual servers that allow you to specify the data center and POD in which you want your host placed. You then assign instances, or virtual machines, to a specific host for maximum control over workload placement and for flexible cost-provisioning options.
{:shortdesc}

## Guaranteed capacity
{: #guaranteed-capacity}

You're guaranteed capacity within the data center and POD in which your host is placed. For example, if the POD containing your dedicated host and dedicated instances reaches capacity, you can continue to assign dedicated instances to your host if your host has appropriate space.

## Visible workloads
{: #visible-workloads}

You can view overall resource consumption for all dedicated instances assigned to a dedicated host on one page. View core, RAM, and local storage usage, which helps you determine if you need to migrate dedicated instances to another dedicated host. This level of granularity gives you the ability to manage your workloads with maximum control.

## Post-deployment management
{: #post-deployment-management}

In addition to guaranteed capacity and visibility to your workloads, you can migrate your dedicated instances between dedicated hosts for maximum control over workload placement.

## Maintenance
{: #maintenance}

Occasionally, infrastructure maintenance requires a dedicated host to restart. For example, the Xen hypervisor might need an update. If you have multiple dedicated hosts, you have the following options to minimize maintenance downtime.
* Maintenance is done by PODs within a data center. You can deploy your dedicated hosts to separate PODs to spread out the required maintenance.
* You can create a support ticket for a dedicated host to request that a scheduled maintenance be delayed. During that time, you can migrate dedicated instances (offline) between dedicated hosts in the same POD.

## High availability
{: #high-availability}

If a dedicated host fails, the workloads on the dedicated host are automatically migrated to a new dedicated host. Dedicated instances remain dedicated throughout the lifecycle of the virtual server.

For high availability scenarios, you might want to consider having an extra dedicated host designated. For example, the additional dedicated host provides you the flexibility to migrate workloads for maintenance windows.
