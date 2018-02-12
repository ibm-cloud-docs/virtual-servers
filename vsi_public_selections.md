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

# Provisioning selections
You must make the following selections when you provision a public virtual server.

## Location
You can select the specific data center to which you want to deploy. For new deployments, {{site.data.keyword.Bluemix}} automatically identifies the best data center (based on availability) and creates the appropriate public and private VLANs. For additions to existing environments, you can select the specific data center, VLAN, and subnet that is required for your design. For more information about VLANs and subnets, see [Getting started with VLANs](/docs/infrastructure/vlans/getting-started.html).

Selecting a subnet is optional and to be used only when you require your device to use an IP address from the subnet. If you select a subnet, verify that you have enough IP addresses to fulfill the request. If you do not have enough IP addresses for your subnet, your order can be delayed or canceled.
{:tip}

## Processors / RAM
When you order, you have core processor options from which to select. The core processor options follow standards for virtual server deployments. Each physical core on the server is hyper-threaded and presented as two virtual CPUs (vCPUs) or cores. The virtual server offering provides 2.0GHz or better per core with up to 56 cores available on a single virtual server.

RAM is extremely straight-forward. The offering fully dedicates the amount of RAM that you select to your virtual server, with up to 242GB on a single virtual server.

**Note:** Public and dedicated instances have slightly different configuration maximums. Very high allocations of either cores or memory limit the available options.

## Operating system

You also select the operating system to be deployed to the server. You can select a number of free options such as CentOS and Ubuntu. Paid  options such as Windows Server and Red Hat Enterprise Linux (RHEL) are also available. It is important to note that Windows requires a 100GB primary disk.

For existing customers, you can also deploy based on an Image Template through the {{site.data.keyword.slportal_full}} by navigating to **Devices -> Manage -> Images** and selecting **Order Virtual Server** from the *Actions* menu.  This automatically selects the appropriate operating system for the order.  Alternatively, you can order based on a standard image and then reload to an image template at any time.

## Storage

You have the option for SAN or local storage for each virtual server. You can supplement SAN or local storage with other storage products as needed. SAN and local storage are both exposed to the virtual server as local disks. Any changes to disks such as attach, detach, migrate, and so on, require a reboot of the virtual server. For more information, see [Storage options](../vsi/storage/vsi_about_storage.html).

## Hourly and monthly billing

You can select hourly or monthly billing for a virtual server. The primary difference, other than cost, is that hourly servers do not have an included bandwidth allocation. At the end of a billing period, the bandwidth usage and the number of hours each server was active on the account are calculated. A running total is available in the {{site.data.keyword.slportal}} under the Virtual Server View page with a link to a Details page, showing each line item, number of hours, and running charges per item.

## Bandwidth

The offering includes 250GB with monthly virtual servers that have a public uplink. You can purchase larger allocations at a reduced cost compared to the overage rate.

## Port speed

You can select the uplink speed for the virtual server, up to 1GB/s. These virtual uplinks are backed by redundant physical uplinks to the IBM public and dedicated networks. The public and dedicated speed is always the same at the time of order, with the option to upgrade or downgrade a link if needed.

## Software

You can select software to be installed by {{site.data.keyword.Bluemix_notm}} during the provisioning process. {{site.data.keyword.Bluemix_notm}} provides support for any software deployed during the provisioning process. You can also install your own software after the server is deployed.

## Security

Before deployment, consider your security options. As part of the order process, you can select a device-specific hardware or software firewall to provide protection. Alternatively, you can deploy dedicated firewall appliances to the environment and deploy the virtual server to a protected VLAN. 

**Note:** A virtual server cannot be protected by two firewall appliances on the same interface. 

You can also use security groups to enact a set of IP filter rules that define how to handle incoming and outgoing traffic to both the public and private interfaces of a virtual server instance.

For more information, see the following security topic collections.

* [Hardware Firewalls (Shared)](../infrastructure/hardware-firewall-shared/getting-started.html)
* [Hardware Firewalls (Dedicated)](../infrastructure/hardware-firewall-dedicated/getting-started.html)
* [Getting started with security groups](/docs/infrastructure/security-groups/sg_index.html)

## Monitoring

You can select from a variety of monitoring options for the virtual server. Options include the standard monitoring, which monitors via Ping and transmission control protocol (TCP) service response, and has optional responses in the event of failures. You can also add Advanced Monitoring which uses the Nimsoft software agent to provide a larger feature set for monitoring of the virtual server and installed software.

For more information, see [Monitoring](../infrastructure/SLmonitoring/monitoring_index.html).

## Backup

During the order process, you can add Evault backups. You can also choose to purchase an R1soft license for your existing R1soft backup environment or utilize a third party backup solution.

For more information, see [Re-registering your device with eVault](../infrastructure/Backup/how-do-i-re-register-evault.html).

## Post-provisioning scripts

Post-provisioning scripts can be associated with any virtual server order. This runs a customer-developed script after other provisioning tasks are completed. The scripts are commonly utilized to apply a customer-specific configuration to a server and to aid in automation of your scaling strategy.

For more information, see [Adding a custom provisioning script](vsi_add_script.html).

## What's Next?
When you are ready to provision your public virtual server, see [Provisioning public instances](vsi_provision_public.html).
