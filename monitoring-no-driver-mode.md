---

copyright:
  years:  2020, 2024
lastupdated: "2024-11-20"

keywords: monitoring light, monitoring no driver, no driver monitor,

subcollection: cloud-infrastructure

---

{{site.data.keyword.attribute-definition-list}}

# Enabling {{site.data.keyword.mon_full_notm}} agent for non-orchestrated environments
{: #enabling-monitoring-light-no-driver}

When you provision a monitoring instance, you can enable the agent for non-orchestrated environments. You can access metrics through the pre-built dashboards that are available in the {{site.data.keyword.cloud_notm}} dashboards section.
{: shortdesc}

## Configuring {{site.data.keyword.mon_full_notm}} agent for non-orchestrated environments
{: #provision-monitoring-light}

To enable 'no driver mode' and monitor and manage metrics, you need to configure a monitoring agent for non-orchestrated environments in each environment that you want to use 'no driver mode'.
{: shortdesc}

Use these steps to enable 'no driver mode'.

1. Provision a Graduated tier monitoring instance by following the steps in [Provisioning a monitoring instance](/docs/monitoring?topic=monitoring-provision). For more information about the Graduate tier, see [Monitoring service plans](/docs/monitoring?topic=monitoring-pricing_plans).

2. Enable monitoring 'no driver mode' by following the steps that correspond to your provisioned environment by following the steps in [Configuring a monitoring agent](/docs/monitoring?topic=monitoring-agent_linux).

3. Add the following configuration to the `dragent.yaml` file:

   ```yaml
   feature:
     mode: `monitor_light`
     Available options for the feature mode are: `monitor_light | monitor | none`.
   ```
   {: codeblock}

   **OR**

   Alternatively, you can use the following curl command:

   ```sh
   curl -sL https://ibm.biz/install-sysdig-agent | sudo bash -s -- -a SYSDIG_ACCESS_KEY -c COLLECTOR_ENDPOINT --collector_port 6443 --secure true -ac "feature:\n mode: monitor_light"
   ```
   {: codeblock}

   Where
   
   `SYSDIG_ACCESS_KEY` is the ingestion key for the instance.
   
   `COLLECTOR_ENDPOINT` is the ingestion URL for the region where the monitoring instance is available.

4. Restart the agent.

   After you complete the previous steps, limited functionality is implemented and you see the reduced pricing on your invoice.
   {: note}

### What's next
{: #monitoring-light-whats-next}

After you provision your monitoring agent and enable 'no driver mode', you need to configure a monitoring agent in each environment that you want to monitor. For more information about configuring a monitoring agent, see [Configuring a monitoring agent](/docs/monitoring?topic=monitoring-agent_linux).

## {{site.data.keyword.mon_full_notm}} 'no driver mode' metrics
{: #monitoring-light-metrics}

{{site.data.keyword.mon_full_notm}} collects basic virtual server instance metrics such as CPU usage, disk usage, network traffic, and memory. These metrics are stored in {{site.data.keyword.mon_full_notm}}. You can access metrics through the prebuilt monitoring dashboard.
{: shortdesc}

Use the following table to see which metrics are available in 'no driver mode'.

| Name | Description |
| ----------- | ----------- |
| cpu.cores.used	| CPU core usage |
| cpu.cores.used.percent | CPU core usage percent for each container |
| cpu.idle.percent	| The percentage of time that the CPUs were idle and the system had no outstanding disk I/O requests |
| cpu.iowait.percent | The percentage of time that the CPUs were idle and the system did an outstanding disk I/O requests |
| cpu.nice.percent	| The percentage of user level CPU utilization with 'Nice' priority |
| cpu.stolen.percent | 	The percentage of time that a virtual machine CPU is in a state of involuntary wait because the physical CPU is shared among virtual machines. |
| cpu.system.percent |  The percentage of system level CPU utilization  |
| cpu.used.percent	| The percentage of system level CPU utilization |
| cpu.user.percent	| The percentage of user level CPU utilization |
| load.average.percpu.1m	| The average number of jobs in the CPU run queue or waiting for disk I/O averaged over 1 minute for all cores. |
| load.average.percpu.5m	| The average number of jobs in the CPU run queue or waiting for disk I/O averaged over 5 minutes for all cores |
| load.average.percpu.15m	| The average number of jobs in the CPU run queue or waiting for disk I/O averaged over 15 minutes for all cores |
| memory.bytes.available	| Available memory |
| memory.bytes.total	| Total memory of a host |
| memory.bytes.used	| Total memory used |
| memory.bytes.virtual	| Physical memory in use |
| memory.pageFault.major	| Count of the condition that occurs when a program accesses a memory page that is mapped in the virtual address space, but not loaded in physical memory |
| memory.pageFault.minor	| A count of the condition in which a memory page was loaded in memory at the time when the page fault was generated, but was not marked in the memory management unit as being loaded in memory. |
| memory.swap.bytes.available	| The swap memory is available. Determined by the sum of the free and cached swap memory. |
| memory.swap.bytes.total	| Total amount of swap memory |
| memory.swap.bytes.used	| Amount of swap memory used |
| memory.swap.used.percent	| The percentage of swap memory used |
| memory.used.percent	| The percentage of physical memory in use |
|	file.bytes.in | Bytes read from the file |
|	file.bytes.out | Bytes written to the file |
| file.bytes.total	| Total number of bytes written to, and read from, the file  |
|	file.iops.in | File read operations per second |
|	file.iops.out |  File write operations per second |
|	file.iops.total | Total number of file read and write operations per second  |
| file.open.count	| Number of times a file was opened |
|	file.time.in | Time reading a file |
|	file.time.out | Time writing a file |
|	file.time.total | Total time during file I/O |
|	fs.bytes.free | Total number of free bytes |
|	fs.bytes.total | Size of the file system |
|	fs.bytes.used | Total number or bytes used |
|	fs.free.percent | The percentage of file system free |
|	fs.inodes.total.count | Number of inodes in the file system |
|	fs.inodes.used.count | Number of inodes used in the file system |
|	fs.inodes.used.percent | The percentage of file system inodes used |
| fs.largest.used.percent	| The percentage of largest file system |
| fs.root.used.percent	| The percentage of root file system used |
| fs.used.percent	| The percentage of the file system used |
|	net.bytes.in | Inbound network bytes |
|	net.bytes.out | Outbound network bytes |
|	net.bytes.total | Total network bytes |
| proc.count	| Number of processors |
| thread.count	| Number of CPU threads or virtual cores |  
| container.count | Numbers of containers |
| system.uptime	| Total system uptime |
| uptime	| The percentage of time the selected entity or entities was down over the defined time window |
{: caption="Monitoring 'no driver mode' metrics" caption-side="top"}

## {{site.data.keyword.mon_full_notm}} 'no driver mode' troubleshooting metrics
{: #monitoring-light-troubleshooting-metrics}

To switch to **Troubleshooting mode**, add the following configuration to the `dragent.yaml` file:

```yaml
feature:  
      mode: troubleshooting
```

Then, restart the agent.

### 'no driver mode' troubleshooting metrics
{: #no-driver-mode-troubleshooting-metrics}

Use the following table to see which troubleshooting metrics are available in 'no driver mode'.

| Metric | Description |
|-----|-----|
| file.error.total.count | Number of errors that are caused by accessing files |
| file.bytes.total | Total number of bytes written to, and read from, the file |
| file.bytes.in | Number of bytes read from the file  |
| file.bytes.out | Number of bytes written from the file  |
| file.open.count | Number of times the file was opened |
| file.time.total | Time that was spent during file I/O |
| host.count | Number of system calls |
| host.error.count | The number of system call errors |
| proc.count | Number of processes on host or container |
| proc.start.count | Number of process starts on host or container |
{: caption="'no driver mode' troubleshooting metrics" caption-side="top"}
