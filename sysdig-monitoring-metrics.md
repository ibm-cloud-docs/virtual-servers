---

copyright:
  years:  2020
lastupdated: "2020-03-30"

keywords: Sysdig, IBM Cloud, monitoring, platform metrics, metrics

subcollection: vsi

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

# Sysdig monitoring metrics
{: #sysdig-monitoring-metrics}

{{site.data.keyword.mon_full_notm}} is operated by Sysdig in partnership with {{site.data.keyword.IBM_notm}} and collects basic Gen 1 and Gen 2 virtual server instance metrics such as CPU usage, disk usage, network traffic, and memory. These metrics are stored in Sysdig. If you have a Sysdig account, then metrics are displayed for that Sysdig instance. You can access metrics through the prebuilt dashboard.
{:shortdesc}

## Platform metrics overview
{: platform-metrics-overview}

You can view platform metrics when you enable Sysdig services on your {{site.data.keyword.cloud_notm}} platform. A Sysdig instance must be configured in a region to monitor these metrics. For more information about enabling Platform metrics, see [Enabling platform metrics](https://test.cloud.ibm.com/docs/Monitoring-with-Sysdig?topic=Sysdig-platform_metrics_enabling).

Before you enable Sysdig on your platform, keep the following information in mind:

* You can configure only one instance of the {{site.data.keyword.mon_full_notm}} service per region to collect platform metrics.

* Platform metrics are regional. Metrics are monitored only from Sysdig services that are in the same region of the instance that you want to monitor. 

* Metrics are collected automatically and are available for monitoring through the Sysdig-enabled instance. 

## Metrics available by compute virtual server generation
{: metrics-by-plan}

Use the following table to see which metrics are supported by either Gen 1 or Gen 2 virtual server instances.

| Metric name |Gen 1 Compute|Gen 2 Compute|
|-----------|--------|--------|
| [Average CPU usage percentage](#avg-cpu-usage) |  ![Checkmark icon](../../icons/checkmark-icon.svg) | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Bytes received for a network interface](#network-int-bytes-received) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Bytes sent for a network interface](#network-bytes-sent) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [CPU usage](#cpu-usage-cumulative) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [CPU usage percentage](#cpu-usage-percentage) |  ![Checkmark icon](../../icons/checkmark-icon.svg) | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Free memory](#free-memory) |  ![Checkmark icon](../../icons/checkmark-icon.svg) | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [I/O requests in flight](#IO-requests-in-flight) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Memory usage percentage](#memory-usage-percentage) |  ![Checkmark icon](../../icons/checkmark-icon.svg) | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Network in bps](#network-received-bps) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Network out bps](#network-out-bps) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Number of bytes read for a volume](#bytes-read-for-volume) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Number of bytes written for a volume](#bytes-written-for-volume) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Number of dropped incoming packets for a network interface](#dropped-incoming-packets) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Number of dropped outgoing packets for a network interface](#dropped-outgoing-packets) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Number of packets received for a network interface](#network-packets-received) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Number of packets sent for a network interface](#network-packets-sent) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Number of read requests for a volume](#volume-read-requests) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Number of receiving errors for a network interface](#network-errors-receiving) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Number of sending errors for a network interface](#network-errors-sending) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Number of write requests for a volume](#volume-write-requests) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Total CPU usage](#total-cpu-usage-nanoseconds) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Total Number of CPUs](#total-cpus) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Total memory](#total-memory-kib) |  ![Checkmark icon](../../icons/checkmark-icon.svg) | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Used memory](#used-memory-kib) |    | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| [Volume I/O throughput read](#volume-io-throughput-read) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume I/O throughput total](#volume-io-throughput-total-mib) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume I/O throughput write](#volume-io-throughput-written-mib) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume I/O wait](#volume-io-wait) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume read bytes per second](#volume-read-requests-bps) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume read iops](#volume-read-iops) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume read latency](#volume-read-latency-microseconds) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume total iops](#volume-total-iops) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume write bps](#volume-write-bps) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume write iops](#volume-write-iops) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |
| [Volume write latency](#volume-write-latency-microseconds) |  ![Checkmark icon](../../icons/checkmark-icon.svg) |   |

{: caption="Table 1: Metrics available by service plan name" caption-side="top"}

## Metric definitions
{: metric-definitions}

The following tables define each basic Gen 1 and Gen 2 virtual server instance metrics.

### Average CPU usage percentage
{: #avg-cpu-usage}

Average percentage of time that elapsed executing instructions across all CPUs

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_average_cpu_usage_percentage`|
| `Metric type` | `gauge` |
| `Value type`  | `percent` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name` |

{: caption="Table 2: Average CPU usage percentage metric metadata" caption-side="top"}

### Bytes received for a network interface
{: #network-int-bytes-received}

Cumulative number of bytes received for a network interface since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_in_bytes`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, MAC address of the network interface` |

{: caption="Table 2: Average CPU usage percentage metric metadata" caption-side="top"}

### Bytes sent for a network interface
{: #network-bytes-sent}

Cumulative number of bytes sent for a network interface since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_out_bytes`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, MAC address of the network interface` |

{: caption="Table 4: Bytes sent for a network interface metric metadata" caption-side="top"}

### CPU usage
{: #cpu-usage-cumulative}

Cumulative elapsed time that a CPU is executing instructions since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_cpu_usage_nanoseconds`|
| `Metric type` | `gauge` |
| `Value type`  | `second` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, Virtual CPU index` |

{: caption="Table 5: Cumulative CPU usage metric metadata" caption-side="top"}

### CPU usage percentage
{: #cpu-usage-percentage}

Average percentage of time that a CPU is executing instructions

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_cpu_usage_percentage`|
| `Metric type` | `gauge` |
| `Value type`  | `percent` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, Virtual CPU index` |

{: caption="Table 6: Average CPU usage metric metadata" caption-side="top"}

### Free memory
{: #free-memory}

Free memory of the virtual server instance in kibibytes (1024 bytes)

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_memory_free_kib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name` |

{: caption="Table 7: Free memory metric metadata" caption-side="top"}

### I/O requests in flight
{: #IO-requests-in-flight}

Number of I/O requests in flight

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_in_flight`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 8: I/O requests in flight metric metadata" caption-side="top"}

### Memory usage percentage
{: #memory-usage-percentage}

Percent of used memory of the virtual server instance

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_memory_usage_percentage`|
| `Metric type` | `gauge` |
| `Value type`  | `percent` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name` |

{: caption="Table 9: Memory usage percentage metric metadata" caption-side="top"}

### Network received in bytes per second
{: #network-received-bps}

Bytes per second received for a network interface

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_in_bps`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, Network interface index` |

{: caption="Table 10: Network in bytes per second metric metadata" caption-side="top"}

### Network out bytes per second
{: #network-out-bps}

Bytes per second transmitted for a network interface

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_out_bps`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, Network interface index` |

{: caption="Table 11: Network out bytes per second metric metadata" caption-side="top"}

### Number of bytes read for a volume
{: #bytes-read-for-volume}

Cumulative number of bytes read for a volume since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_read_bytes`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume` |

{: caption="Table 12: Number of bytes read for a volume metric metadata" caption-side="top"}

### Number of bytes written for a volume
{: #bytes-written-for-volume}

Cumulative number of bytes written for a volume since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_write_bytes`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume` |

{: caption="Table 13: Number of bytes written for a volume metric metadata" caption-side="top"}

### Number of dropped incoming packets for a network interface
{: #dropped-incoming-packets}

Cumulative number of dropped incoming packets for a network interface since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_in_dropped_packets`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, MAC address of the network interface` |

{: caption="Table 14: Number of dropped incoming packets for a network interface metric metadata" caption-side="top"}

### Number of dropped outgoing packets for a network interface
{: #dropped-outgoing-packets}

Cumulative number of dropped outgoing packets for a network interface since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_out_dropped_packets`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, MAC address of the network interface` |

{: caption="Table 15: Number of dropped outgoing packets for a network interface metric metadata" caption-side="top"}

### Number of packets received for a network interface
{: #network-packets-received}

Cumulative number of packets received for a network interface since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_in_packets`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, MAC address of the network interface` |

{: caption="Table 16: Number of packets received for a network interface metric metadata" caption-side="top"}

### Number of packets sent for a network interface
{: #network-packets-sent}

Cumulative number of packets sent for a network interface since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_out_packets`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, MAC address of the network interface` |

{: caption="Table 17: Number of packets sent for a network interface metric metadata" caption}

### Number of read requests for a volume
{: #volume-read-requests}

Cumulative number of read requests for a volume since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_read_requests`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume` |

{: caption="Table 18: Number of read requests for a volume metric metadata" caption}

### Number of receiving errors for a network interface
{: #network-errors-receiving}

Cumulative number of receiving errors for a network interface since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_in_errors`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, MAC address of the network interface` |

{: caption="Table 19: Number of receiving errors for a network interface metric metadata" caption-side="top"}

### Number of sending errors for a network interface
{: #network-errors-sending}

Cumulative number of sending errors for a network interface since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_out_errors`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, MAC address of the network interface` |

{: caption="Table 20: Number of sending errors for a network interface metric metadata" caption-side="top"}

### Number of write requests for a volume
{: #volume-write-requests}

Cumulative number of write requests for a volume since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_write_requests`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume` |

{: caption="Table 21: Number of write requests for a volume metric metadata" caption-side="top"}

### Total CPU usage
{: #total-cpu-usage-nanoseconds}

Cumulative time elapsed executing instructions across all CPUs since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_total_cpu_usage_nanoseconds`|
| `Metric type` | `gauge` |
| `Value type`  | `second` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name` |

{: caption="Table 22: Total CPU usage metric metadata" caption-side="top"}

### Total number of CPUs
{: #total-cpus}

Total Number of CPUs

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_cpus`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name` |

{: caption="Table 23: Total number of CPUs metric metadata" caption-side="top"}

### Total memory
{: #total-memory-kib}

Total memory of the virtual server instance in kibibytes (1024 bytes)

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_memory_total_kib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name` |

{: caption="Table 24: Total memory in kibibytes metric metadata" caption-side="top"}

### Used memory
{: #used-memory-kib}

Used memory of the virtual server instance in kibibytes (1024 bytes)

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_memory_used_kib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name` |

{: caption="Table 25: Used memory metric metadata" caption-side="top"}

### Volume I/O throughput read
{: #volume-io-throughput-read}

Data read from the volume (MiB/s).

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_io_throughput_read_mib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 26: Volume I/O throughput read metric metadata" caption-side="top"}

### Volume I/O throughput total
{: #volume-io-throughput-total-mib}

All volume I/O, in MiB/s.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_io_throughput_total_mib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 27: Volume I/O throughput total metric metadata" caption-side="top"}

### Volume I/O throughput written
{: #volume-io-throughput-written-mib}

Data written to the volume (MiB/s)

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_io_throughput_write_mib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 28: Volume I/O throughput written metric metadata" caption-side="top"}

### Volume I/O wait time
{: #volume-io-wait}

Total I/O wait time (all requests) per second

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_io_wait`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 29: Volume I/O wait time metric metadata" caption-side="top"}

### Volume read requests bytes per second
{: #volume-read-requests-bps}

Read requests in bytes per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_read_bps`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 30: Volume read requests bytes per second metric metadata" caption-side="top"}

### Volume read requests I/O operations per second
{: #volume-read-iops}

Volume read requests per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_read_iops`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 31: Volume read I/O operations per second metric metadata" caption-side="top"}

### Volume read latency
{: #volume-read-latency-microseconds}

Read latency from volume, in microseconds

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_read_latency_microseconds`|
| `Metric type` | `gauge` |
| `Value type`  | `second` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 32: Volume read latency metric metadata" caption-side="top"}

### Volume total I/O operations per second
{: #volume-total-iops}

I/O requests per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_total_iops`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 33: Volume total I/O operations per second metric metadata" caption-side="top"}

### Volume write bytes per second
{: #volume-write-bps}

Write requests in bytes per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_write_bps`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 34: Volume write bytes per second metric metadata" caption-side="top"}

### Volume write I/O operations per second
{: #volume-write-iops}

Write requests per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_write_iops`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 35: Volume write I/O operations per second metric metadata" caption-side="top"}

### Volume write latency
{: #volume-write-latency-microseconds}

Write latency from volume, in microseconds

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_write_latency_microseconds`|
| `Metric type` | `gauge` |
| `Value type`  | `second` |
| `Segment by` | `IBM IS Generation, 1 or 2, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 36: Volume write latency metric metadata" caption-side="top"}

## Attributes for segmentation
{: attributes}

### Global attributes
{: global-attributes}

The following attributes are available for segmenting all of the metrics previously listed

| Attribute | Attribute Name | Attribute Description |
|-----------|----------------|-----------------------|
| `Cloud type` | `ibm_ctype` | Coud type is a value of public, dedicated, or local |
| `Location` | `ibm_location` | Location of the monitored resource - this can be a region, data center, or global |
| `Resource` | `ibm_resource` | Resource being measured by the service - typically an identifying name or GUID |
| `Resource type` | `ibm_resource_type` | Type of resource measured by the service |
| `Resource group` | `ibm_resource_group_name` | Resource group where the service instance was created |
| `Scope` | `ibm_scope` | Scope of the account, organization, or space GUID that is associated with this metric |
| `Service name` | `ibm_service_name` | Name of the service generating this metric |

{: caption="Table 37: Available attributes for segmenting" caption-side="top"}


### Additional Attributes
{: additional-attributes}

The following attributes are available for segmenting one or more attributes as described in the reference above. See the individual metrics for segmentation options.

| Attribute | Attribute Name | Attribute Description |
|-----------|----------------|-----------------------|
| `Disk name of the volume` | `ibm_is_disk_name` | Disk name of the volume attached to the virtual server instance, corresponds to output of `'ls -l /dev/disk/by-id'` |
| `IBM IS Generation, 1 or 2` | `ibm_is_generation` | IBM IS Generation (`1` for Gen. 1 or `2` for Gen. 2) |
| `MAC address of the network interface` | `ibm_is_mac_address` | MAC address of the corresponding network interface that is attached to the virtual server instance |
| `Network interface index` | `ibm_is_nic_index` | Index of the network interface that is attached to the virtual server instance, starting from 0 |
| `Resource name` | `ibm_resource_name` | Resource name - for example, the virtual server instance name |
| `UUID of storage volume` | `ibm_is_volume_id` | UUID of storage volume that is attached to the virtual server instance |
| `Virtual CPU index` | `ibm_is_vcpu_index` | Index of the virtual CPU within the virtual server instance, starting from 0 |

{: caption="Table 38: Available attributes for segmenting one or more attributes" caption-side="top"}
