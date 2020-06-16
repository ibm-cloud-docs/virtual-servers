---

copyright:
  years:  2020
lastupdated: "2020-06-16"

keywords: Sysdig, IBM Cloud, sysdig light, sysdig no driver

subcollection: vpc_vpn

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

#  {{site.data.keyword.mon_full_notm}} Light 'no driver mode'
{: #sysdig-light-no-driver}

When you provision an {{site.data.keyword.mon_full_notm}} instance, you can enable the 'no driver mode'. You can access metrics through the pre-built dashboards that are available in Sysdig Monitor in the {{site.data.keyword.cloud_notm}} dashboards section.
{: shortdesc}

Sysdig agent 9.9.0 or higher is required for 'no driver mode'.
{: note}

## Configuring {{site.data.keyword.mon_full_notm}} 'no driver mode'
{: #provision-sysdig-light}

To enable 'no driver mode', you need to configure a Sysdig agent in each environment that you want to use 'no driver mode'. 
{: shortdesc}

Use these steps to enable 'no driver mode'. 

**1** Follow the steps that correspond to your provisioned environment by following the steps in [Configuring a Sysdig agent](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-config_agent).

**2** Add the following configuration to the `dragent.yaml` file:

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

**3** Restart the agent.

<!--For more information about configuring {{site.data.keyword.mon_full_notm}} 'no driver mode', see [Sysdig Monitor Light](https://docs.sysdig.com/en/configure-sysdig-monitor-using-agent-modes.html#UUID-f8b35584-ba10-5637-ecf1-0617a9186159_UUID-0fdf06d6-9b6c-1695-0d16-9dc2017a274b){: external}-->

## {{site.data.keyword.mon_full_notm}} 'no driver mode' metrics
{: #sysdig-light-metrics}

{{site.data.keyword.mon_full_notm}} is operated by Sysdig in partnership with IBM and collects basic Gen 1 and Gen 2 virtual server instance metrics such as CPU usage, disk usage, network traffic, and memory. These metrics are stored in Sysdig. If you have a Sysdig account, then metrics are displayed for that Sysdig instance. You can access metrics through the prebuilt dashboard. 
{: shortdesc}

Use the following tables to see which metrics are supported by 'no driver mode'.

### Host metrics 
{: #host-metrics}

| Name | Description |
| ----------- | ----------- |
| host.hostName | Host name | 
| host.proclist.main | Number of CPUs on host | 
| memory.bytes.total | Physical memory size | 
| cpu.used.percent | Percentage of system level CPU utilization | 
| cpu.stolen.percent | Percentage of time that a virtual machine CPU is in a state of involuntary wait because the physical CPU is shared among virtual machines. | 
| cpu.idle.percent | Percentage of time that the CPUs were idle and the system had no outstanding disk I/O requests.  | 
| cpu.system.percent | Percentage of system level CPU utilization  | 
| capacity.user.percent | Percentage of user level CPU utilization  | 
| cpu.iowait.percent | Percentage of time that the CPUs were idle and the system did an outstanding disk I/O requests  | 
| cpu.nice.percent | Percentage of user level CPU utilization with 'Nice' priority | 
| memory.bytes.used | Memory usage | 
| proc.count | Number of processors | 
| thread.count | Number of CPU threads or virtual cores |  
| uptime | Percentage of time the selected entity or entities was down over the defined time window. |
{: caption="Table 1. Host metrics" caption-side="top"}

| Network interface card metrics | Description |
|----|----|
|	net.client.ip | Client IP address (IPv4 address) | 

{: caption="Table 2. NIC metrics" caption-side="top"}

<!--Network interface list-->
<!--NIC card name-->
<!--NIC netmask-->

| File system I/O metrics | Description |
|----|----|
| file.bytes.in | Number of bytes read from the file |
| file.bytes.out | Number of bytes written from the file |
{: caption="Table 3. File system I/O metrics" caption-side="top"}

| External network metrics| Description |
|----|----|
| net.bytes.in | Network bytes in |
| net.bytes.out | Network bytes out |
{: caption="Table 4. External network metrics" caption-side="top"}

<!--Sysdig metrics Description -->
<!--Sysdig agent version 
Agent mode
Agent internal metrics-->
<!--"Table 5. Sysdig metrics" caption-side="top"-->

### Process (per process) metrics
{: #process-metrics}

| Process metric | Description | 
|----|----|
| proc.name | Process name | 
| container.id | Container ID | 
| cpu.cores.used.percent | CPU core usage percent for each container | 
| memory.bytes.used  | Memory usage | 
| thread.count | Number of CPU threads or virtual cores | 
{: caption="Table 6. Process (per process) metrics" caption-side="top"}

<!--PID-->

### Container (per container) metrics
{: #container-metrics}

| Container metrics | Description |
| -----| ----|
| container.id | Container ID | 
| container.name | Container name | 
|	container.image | Name of the imagee used to run the container | 
| cpu.cores.used.percent | CPU core usage percent for each container  | 
| memory.bytes.used | Memory being used | 
| cpu.shares.used.percent | Percentage used container's allocated CPU shares | 
| cpu.quota.used.percent | Percentage of a container CPU quota used over a period of time | 
| proc.count | Number of processes on host or container, excluding any processes that do not have .exe or command line parameters in the process table. | 
| thread.count | Number of CPU threads or virtual cores | 
| file.iops.total | Number of file read and write operations per second  | 
| net.bytes.total | Network I/O | 
{: caption="Table 7. Container (per container) metrics" caption-side="top"}

<!--Containerruntime
container label
container mounts-->

### File system (per mount on host) metrics 
{: #file-system-per-mount-metrics}

| File system metrics | Description |
| ---- | ---- |
| fs.device | File system device | 
| fs.mountDir | File system mount directory. | 
|	fs.type | File system type  | 
|	fs.bytes.total | File system size | 
|	fs.free.percent | available | 
|	fs.inodes.total.count | Total file read operations per second | 
|	fs.inodeds.used.count | Used inodes | 
{: caption="Table 8. File system (per mount on host) metrics" caption-side="top"}

### Host 'no driver mode' Explorer metrics
{: #light-mode-explorer-metrics}

You can segment many of these metrics by container or process.
{: note}

| Name | Description |
|----|----|
| cpu.cores.used | CPU core usage of each container |
| cpu.cores.used.percent | CPU core usage percenrage of each container |
| cpu.idle.percent | Percentage of time that the CPUs were idle and the system did not have an outstanding disk I/O requests |
| cpu.iowait.percent | Percentage of time that the CPUs were idle and the system did an outstanding disk I/O requests |
|	cpu.nice.percent | Percentage of user level CPU utilization with 'Nice' priority |
|	cpu.stolen.percent | Percentage of time that a virtual machine CPU is in a state of involuntary wait because the physical CPU is shared among virtual machines. |
|	cpu.system.percent | Percentage of system level CPU utilization |
|	cpu.used.percent |  CPU usage for each container |
|	cpu.user.percent | Percentage of user level CPU utilization |
|	load.average.percpu.1m | Average number of jobs in the CPU run queue or waiting for disk I/O averaged over 1 minute for all cores.  |
|	load.average.percpu.5m | Average number of jobs in the CPU run queue or waiting for disk I/O averaged over 5 minutes for all cores. |
|	load.average.percpu.15m | Average number of jobs in the CPU run queue or waiting for disk I/O averaged over 15 minutes for all cores. |
|	memory.bytes.available | Available memory |
| memory.bytes.total | Total memory of a host |
|	memory.bytes.used | Physical memory being used |
|	memory.bytes.virtual | Virutal memory size of the process |
|	memory.pageFault.major | Count of the condition that occurs when a program accesses a memory page that is mapped in the virtual address space, but not loaded in physical memory.  |
|	memory.pageFault.minor | A count of the condition in which a memory page was loaded in memory at the time the page fault was generated, but was not marked in the memory management unit as being loaded in memory.  |
|	memory.swap.bytes.available | The swap memory available. Determined by the sum of the free and cached swap memory. |
|	memory.swap.bytes.total | Total amount of swap memory |
|	memory.swap.bytes.used | Amount of swap memory used |
{: caption="Table 9 Host 'no driver mode' Explorer metrics" caption-side="top"}

| Host help Explorer metrics | Description |
|----|----| 
| memory.swap.used.percent | Percentage of swap memory used |
|	memory.used.percent | Percentage of physical memory in use |
|	file.bytes.in | Bytes read from the file |
|	file.bytes.out | Bytes writtem to the file |
|	file.bytes.total | Total number of bytes written to, and read from, the file  |
|	file.iops.in | File read operations per second |
|	file.iops.out |  File write operations per second |
|	file.iops.total | Total number of file read and write operations per second  |
|	file.open.count | Number of times file was opened |
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
|	fs.largest.used.percent | Percentage of largest file system |
|	fs.root.used.percent | Percentage of root file system used |
|	fs.used.percent | Percentage of the file system used |
|	net.bytes.in | Inbound network bytes |
|	net.bytes.out | Outbound network bytes |
|	net.bytes.total | Total network bytes |
|	proc.count | Number of processes on host or container - excluding any processes that do not have .exe or command line parameters in the process table.  |
|	thread.count | Number of CPU threads or virtual cores |
|	container.count | Numbers of containers |
|	system.uptime | Total system uptime |
|	uptime | Percentage of time the selected entity or entities was down over the defined time window. |
{: caption="Table 10. Host help Explorer metrics" caption-side="top"}

<!--dragent.analyzer.fl.ms-->
