---

copyright:
  years: 2019, 2024
lastupdated: "2024-07-23"

keywords: jumbo frames, virtual server improved network performance

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Configuring virtual server settings for improved network performance
{: #configuring-network-performance}

{{site.data.keyword.BluVirtServers}} bandwidth is capped only if you select the 100 Mbps rate-limited uplink port speed during the provisioning process. If you select the 100 Mbps rate-limited uplink port speed during provisioning, the maximum virtual server instance throughput is limited only by the physical bandwidth available to the virtual server host. You can achieve higher network performance through extra configuration if you provision with the 1 Gbps non rate-limited uplink port speed.

If you select the 1 Gbps non rate-limited uplink port speed and want to achieve higher network performance, higher than 5 Gbps, consider enabling jumbo frames in the networking configuration of your virtual server instance.

In addition to configuring jumbo frames, the use of multiple TCP connections can also help you achieve higher network performance on your workloads. Support for multiple TCP connections is application-dependent, so you can refer to your application documentation to determine whether you can use multiple TCP connections.

Another configuration setting to consider that can impact network performance is the number of vCPUs in your virtual server instance. To achieve higher than 5 Gbps network throughput, you need to select a profile with more than 1 vCPU. You can experiment with several profiles with different numbers of vCPUs to determine which configuration best meets your network performance expectations.

## Configuring jumbo frames
{: #configuring-jumbo-frames}

You can configure jumbo frames in the networking configuration for your virtual server instances to help achieve higher network performance.

### Configuring jumbo frames for Debian and Ubuntu
{: #jumbo-frames-debian-ubuntu}

To increase the maximum transmission unit (MTU) to support Ethernet jumbo frames if you are running Debian or Ubuntu, complete the following steps:

1. Check the current setting by running the command `- ifconfig| grep -i MTU`.
2. Change the current setting to support 9000 MTU by running the command `ifconfig eth0 mtu 9000`.
3. Change the setting so that it persists after the system is restarted. Edit the file `/etc/network/interfaces`, and add `MTU=9000`.

### Configuring jumbo frames for CentOS and Red Hat Enterprise Linux
{: #jumbo-frames-centos-rhel}

To increase the maximum transmission unit (MTU) to support Ethernet jumbo frames if you are running CentOS or Red Hat Enterprise Linux, complete the following steps:

1. Check the current setting by running the command `ip link show dev eth0`
2. Change the current setting to support 9000 MTU by running the command `ip link set mtu 9000 dev eth0`.
3. Change the setting so that it persists after the system is restarted. Edit the file `/etc/sysconfig/network-scripts/ifcfg-eth0`, and add `MTU=9000`.

### Configuring jumbo frames for Windows
{: #jumbo-frames-windows}

To increase the maximum transmission unit (MTU) to support Ethernet jumbo frames if you are running Windows, complete the following steps:

1. Check the current setting by running the command `netsh interface ipv4 show interfaces`
2. Change the current setting to support 9000 MTU by running the command `netsh interface ipv4 set subinterface “12”  mtu=9000 store=persistent`.
