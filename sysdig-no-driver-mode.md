---

copyright:
  years:  2020, 2021
lastupdated: "2021-04-02"

keywords: monitoring light, monitoring no driver, no driver monitor, monitoring lite

subcollection: cloud-infrastructure

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}
{:important: .important}
{:note: .note}
{:external: .external}

#  Enabling {{site.data.keyword.mon_full_notm}} 'no driver mode'
{: #enabling-monitoring-light-no-driver}

When you provision a monitoring instance, you can enable the 'no driver mode' (Light). You can access metrics through the pre-built dashboards that are available in the {{site.data.keyword.cloud_notm}} dashboards section.
{: shortdesc}

<!--Sysdig agent 9.9.0 or higher is required for 'no driver mode'.
{: note}-->

## Configuring {{site.data.keyword.mon_full_notm}} 'no driver mode'
{: #provision-monitoring-light}

To enable 'no driver mode' and monitor and manage metrics, you need to configure a monitoring agent in each environment that you want to use 'no driver mode'.
{: shortdesc}

Use these steps to enable 'no driver mode'.

**1.** Provision a Graduated tier monitoring instance by following the steps in [Provisioning a monitoring instance](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-provision). For more information about the Graduate tier, see [Monitoring service plans](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-pricing_plans).

**2.** Enable monitoring 'no driver mode' by following the steps that correspond to your provisioned environment by following the steps in [Configuring a monitoring agent](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-config_agent).

**3.** Add the following configuration to the `dragent.yaml` file:

```
feature:
  mode: `monitor_light`
  Available options for the feature mode are: `monitor_light | monitor | none`.
```

**OR**

Alternativelty, you can use the following curl command:

```
curl -sL https://ibm.biz/install-sysdig-agent | sudo bash -s -- -a SYSDIG_ACCESS_KEY -c COLLECTOR_ENDPOINT --collector_port 6443 --secure true -ac "feature:\n mode: monitor_light"
```

Where

`SYSDIG_ACCESS_KEY` is the ingestion key for the instance.

`COLLECTOR_ENDPOINT` is the ingestion URL for the region where the monitoring instance is available.

**4.** Restart the agent.

After you complete the previous steps, limited funcationaity is implemented and you see the reduced pricing on your invoice.
{: note}

### What's next
{: #monitoring-light-whats-next}

After you provision your monitoring agent and enable 'no driver mode', you need to configire an monitoring agent in each environment that you want to monitor. For information about configuring a monitoring agent, see [Configuring a monitoring agent](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-config_agent).

## {{site.data.keyword.mon_full_notm}} 'no driver mode' metrics
{: #monitoring-light-metrics}

{{site.data.keyword.mon_full_notm}} collects basic Gen 1 and Gen 2 virtual server instance metrics such as CPU usage, disk usage, network traffic, and memory. These metrics are stored in {{site.data.keyword.mon_full_notm}}. You can access metrics through the prebuilt monitoring dashboard.
{: shortdesc}

Use the following table to see which metrics are available in 'no driver mode'.

| Name | Description |
| ----------- | ----------- |
| cpu.cores.used	| CPU core usage |
| cpu.cores.used.percent | CPU core usage percent for each container |
| cpu.idle.percent	| Percentage of time that the CPUs were idle and the system had no outstanding disk I/O requests. |
| cpu.iowait.percent | Percentage of time that the CPUs were idle and the system did an outstanding disk I/O requests |
| cpu.nice.percent	| Percentage of user level CPU utilization with 'Nice' priority |
| cpu.stolen.percent | 	Percentage of time that a virtual machine CPU is in a state of involuntary wait because the physical CPU is shared among virtual machines. |
| cpu.system.percent |  Percentage of system level CPU utilization  |
| cpu.used.percent	| Percentage of system level CPU utilization |
| cpu.user.percent	| Percentage of user level CPU utilization |
| load.average.percpu.1m	| Average number of jobs in the CPU run queue or waiting for disk I/O averaged over 1 minute for all cores.  |
| load.average.percpu.5m	| Average number of jobs in the CPU run queue or waiting for disk I/O averaged over 5 minutes for all cores.  |
| load.average.percpu.15m	| Average number of jobs in the CPU run queue or waiting for disk I/O averaged over 15 minutes for all cores.  |
| memory.bytes.available	| Available memory |
| memory.bytes.total	| Total memory of a host |
| memory.bytes.used	| Total memory used |
| memory.bytes.virtual	| Physical memory being used |
| memory.pageFault.major	| Count of the condition that occurs when a program accesses a memory page that is mapped in the virtual address space, but not loaded in physical memory.  |
| memory.pageFault.minor	| A count of the condition in which a memory page was loaded in memory at the time the page fault was generated, but was not marked in the memory management unit as being loaded in memory.  |
| memory.swap.bytes.available	| The swap memory available. Determined by the sum of the free and cached swap memory. |
| memory.swap.bytes.total	| Total amount of swap memory |
| memory.swap.bytes.used	| Amount of swap memory used |
| memory.swap.used.percent	| Percentage of swap memory used |
| memory.used.percent	| Percentage of physical memory in use |
|	file.bytes.in | Bytes read from the file |
|	file.bytes.out | Bytes writtem to the file |
| file.bytes.total	| Total number of bytes written to, and read from, the file  |
|	file.iops.in | File read operations per second |
|	file.iops.out |  File write operations per second |
|	file.iops.total | Total number of file read and write operations per second  |
| file.open.count	| Number of times file was opened |
|	file.time.in | Time reading file |
|	file.time.out | Time writing file |
|	file.time.total | Total time during file I/O |
|	fs.bytes.free | Total number of free bytes |
|	fs.bytes.total | Size of the file system |
|	fs.bytes.used | Total number or bytes used |
|	fs.free.percent | Percentage of file system free |
|	fs.inodes.total.count | Number of inodes in the file system |
|	fs.inodes.used.count | Number of inodes used in the file system |
|	fs.inodes.used.percent | Percentage of file system inodes used |
| fs.largest.used.percent	| Percentage of largest file system |
| fs.root.used.percent	| Percentage of root file system used |
| fs.used.percent	| Percentage of the file system used |
|	net.bytes.in | Inbound network bytes |
|	net.bytes.out | Outbound network bytes |
|	net.bytes.total | Total network bytes |
| proc.count	| Number of processors |
| thread.count	| Number of CPU threads or virtual cores |  
| container.count | Numbers of containers |
| system.uptime	| Total system uptime |
| uptime	| Percentage of time the selected entity or entities was down over the defined time window. |
{: caption="Table 1. Monitoring 'no driver mode' metrics" caption-side="top"}

## {{site.data.keyword.mon_full_notm}} 'no driver mode' troubleshooting metrics
{: #monitoring-light-troubleshooting-metrics}


To switch to **Troubleshooting mode**, add the following configuration to the `dragent.yaml` file:

```
feature:  
      mode: troubleshooting
```

Then restart the agent.

### 'no driver mode' troubleshooting metrics
{: #no-driver-mode-troubleshooting-metrics}

Use the following table to see which troubleshooting metrics are available in 'no driver mode'.

| Metric | Description |
|-----|-----|
| file.error.total.count | Number of errors caused by accessing files |
| file.bytes.total | Total number of bytes written to, and read from, the file |
| file.bytes.in | Number of bytes read from the file  |
| file.bytes.out | Number of bytes written from the file  |
| file.open.count | Number of times the file was opened |
| file.time.total | Time spent during file I/O |
| host.count | Number of system calls |
| host.error.count | The number of system call errors |
| proc.count | Number of processes on host or container |
| proc.start.count | Number of process starts on host or container |
{: caption="Table 2. 'no driver mode' troubleshooting metrics" caption-side="top"}
