---

copyright:
  years:  2020, 2021
lastupdated: "2021-04-02"

keywords: IBM Cloud monitoring, platform metrics, metrics, virtual server monitoring metrics, classic monitoring metrics, classic metrics

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

# Classic virtual server instance metrics definitions
{: #classic-monitoring-metrics}

The following metrics are available only if you use the {{site.data.keyword.mon_full_notm}} full agent. If you provisioned a 'no driver mode' instance, see [Monitoring 'no driver mode' metrics](/docs/cloud-infrastructure?topic=cloud-infrastructure-enabling-monitoring-light-no-driver#monitoring-light-metrics).
{:important}

The following tables define basic Classic virtual server instance metrics.

## Average CPU usage percentage
{: #avg-cpu-usage-gen1}

Average percentage of time that elapsed executing instructions across all CPUs

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_average_cpu_usage_percentage`|
| `Metric type` | `gauge` |
| `Value type`  | `percent` |
| `Segment by` | `IBM IS Generation, 1, resource name` |

{: caption="Table 1: Average CPU usage percentage metric metadata" caption-side="top"}

## CPU usage
{: #cpu-usage-cumulative-gen1}

Cumulative elapsed time that a CPU is executing instructions since virtual server instance start

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_cpu_usage_nanoseconds`|
| `Metric type` | `gauge` |
| `Value type`  | `second` |
| `Segment by` | `IBM IS Generation, 1, resource name, Virtual CPU index` |

{: caption="Table 2: Cumulative CPU usage metric metadata" caption-side="top"}

## CPU usage percentage
{: #cpu-usage-percentage-gen1}

Average percentage of time that a CPU is executing instructions

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_cpu_usage_percentage`|
| `Metric type` | `gauge` |
| `Value type`  | `percent` |
| `Segment by` | `IBM IS Generation, 1, resource name, Virtual CPU index` |

{: caption="Table 3: Average CPU usage metric metadata" caption-side="top"}

## Free memory
{: #free-memory-gen1}

Free memory of the virtual server instance in kibibytes (1024 bytes)

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_memory_free_kib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1, resource name` |

{: caption="Table 4: Free memory metric metadata" caption-side="top"}

## I/O requests in flight
{: #IO-requests-in-flight-gen1}

Number of I/O requests in flight

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_in_flight`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 5: I/O requests in flight metric metadata" caption-side="top"}

## Memory usage percentage
{: #memory-usage-percentage-gen1}

Percent of used memory of the virtual server instance

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_memory_usage_percentage`|
| `Metric type` | `gauge` |
| `Value type`  | `percent` |
| `Segment by` | `IBM IS Generation, 1, resource name` |

{: caption="Table 6: Memory usage percentage metric metadata" caption-side="top"}

## Network received in bytes per second
{: #network-received-bps-gen1}

Bytes per second received for a network interface

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_in_bps`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1, resource name, Network interface index` |

{: caption="Table 7: Network in bytes per second metric metadata" caption-side="top"}

## Network out bytes per second
{: #network-out-bps-gen1}

Bytes per second transmitted for a network interface

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_network_out_bps`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1, resource name, Network interface index` |

{: caption="Table 8: Network out bytes per second metric metadata" caption-side="top"}

## Total memory
{: #total-memory-kib-gen1}

Total memory of the virtual server instance in kibibytes (1024 bytes)

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_memory_total_kib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1, resource name` |

{: caption="Table 9: Total memory in kibibytes metric metadata" caption-side="top"}

## Volume I/O throughput read
{: #volume-io-throughput-read-gen1}

Data read from the volume (MiB/s).

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_io_throughput_read_mib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 10: Volume I/O throughput read metric metadata" caption-side="top"}

## Volume I/O throughput total
{: #volume-io-throughput-total-mib-gen1}

All volume I/O, in MiB/s.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_io_throughput_total_mib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 11: Volume I/O throughput total metric metadata" caption-side="top"}

## Volume I/O throughput written
{: #volume-io-throughput-written-mib-gen1}

Data written to the volume (MiB/s)

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_io_throughput_write_mib`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 12: Volume I/O throughput written metric metadata" caption-side="top"}

## Volume I/O wait time
{: #volume-io-wait-gen1}

Total I/O wait time (all requests) per second

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_io_wait`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 13: Volume I/O wait time metric metadata" caption-side="top"}

## Volume read requests bytes per second
{: #volume-read-requests-bps-gen1}

Read requests in bytes per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_read_bps`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 14: Volume read requests bytes per second metric metadata" caption-side="top"}

## Volume read requests I/O operations per second
{: #volume-read-iops-gen1}

Volume read requests per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_read_iops`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 15: Volume read I/O operations per second metric metadata" caption-side="top"}

## Volume read latency
{: #volume-read-latency-microseconds-gen1}

Read latency from volume, in microseconds

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_read_latency_microseconds`|
| `Metric type` | `gauge` |
| `Value type`  | `second` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 16: Volume read latency metric metadata" caption-side="top"}

## Volume total I/O operations per second
{: #volume-total-iops-gen1}

I/O requests per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_total_iops`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 17: Volume total I/O operations per second metric metadata" caption-side="top"}

## Volume write bytes per second
{: #volume-write-bps-gen1}

Write requests in bytes per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_write_bps`|
| `Metric type` | `gauge` |
| `Value type`  | `byte` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 18: Volume write bytes per second metric metadata" caption-side="top"}

### Volume write I/O operations per second
{: #volume-write-iops-gen1}

Write requests per second.

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_write_iops`|
| `Metric type` | `gauge` |
| `Value type`  | `none` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 19: Volume write I/O operations per second metric metadata" caption-side="top"}

### Volume write latency
{: #volume-write-latency-microseconds-gen1}

Write latency from volume, in microseconds

| Metadata | Description |
|----------|-------------|
| `Metric name` | `ibm_is_instance_volume_write_latency_microseconds`|
| `Metric type` | `gauge` |
| `Value type`  | `second` |
| `Segment by` | `IBM IS Generation, 1, resource name, disk name of the volume, UUID of storage volume` |

{: caption="Table 20: Volume write latency metric metadata" caption-side="top"}
