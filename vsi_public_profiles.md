---

copyright:
  years: 2017, 2025
lastupdated: "2025-05-09"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Profiles
{: #about-virtual-server-profiles}

When you provision {{site.data.keyword.BluVirtServers}}, you can select from supported families of profiles. A profile is a combination of vCPU and RAM that can be instantiated quickly to start a virtual server instance. In the {{site.data.keyword.cloud_notm}} console, you can choose from popular profile configurations or select from a list of profiles that best fit your needs.
{: shortdesc}

## Profile families
{: #available-virtual-server-profile-families}

The following virtual server instance families are available.

Depending on your instance type, some profile families might not be available.
{: note}

| Profile family  | Description                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- |
| [Balanced](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#balanced) | Best for common workloads that require a balance of performance and scalability. Uses network-attached storage. |
| [Balanced local storage](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage) | Best for large database workloads that require high I/O performance with low latency. |
| [Variable compute](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#variable-compute)  | Best for workloads that don’t require steady, high-CPU performance. |
| [Compute](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#compute) | Best for moderate to high web traffic workloads.|
| [Memory](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#memory)  | Best for memory caching and real-time analytics workloads. |
| [GPU](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles#gpu)  | Best for high-performance workloads. |
{: caption="Public virtual server family selections" caption-side="top"}

## Balanced
{: #balanced}

Balanced profiles (with network-attached storage) are ideal for common cloud workloads that require a balance of performance and scale. Network performance ranges from standard to premium.

The offering is available in the following profiles:

| Profile   | vCPU    | RAM     | Storage type |
| --------- | ------- | ------- | ------------ |
| B1.1x2    | 1       | 2 GB    | SAN          |
| B1.1x4    | 1       | 4 GB    | SAN          |
| B1.2x4    | 2       | 4 GB    | SAN          |
| B1.2x8    | 2       | 8 GB    | SAN          |
| B1.4x8    | 4       | 8 GB    | SAN          |
| B1.4x16   | 4       | 16 GB   | SAN          |
| B1.8x16   | 8       | 16 GB   | SAN          |
| B1.8x32   | 8       | 32 GB   | SAN          |
| B1.16x32  | 16      | 32 GB   | SAN          |
| B1.16x64  | 16      | 64 GB   | SAN          |
| B1.32x64  | 32      | 64 GB   | SAN          |
| B1.32x128 | 32      | 128 GB  | SAN          |
| B1.48x192 | 48      | 192 GB  | SAN          |
{: caption="Balanced profiles with network-attached storage" caption-side="top"}

### Storage notes
{: #storage-notes-balanced}

* SAN primary boot disk (25 or 100 GB) with more disks available, up to 2 TB each (five total disks allowed).
* Pricing for public virtual servers that use SAN storage includes virtual CPU, memory, and minimum primary boot disk. Extra disk prices depend on the disk size and quantity that you select.

All supported operating systems (such as RHEL, CentOS, Windows, Ubuntu, and others), databases that are supported, and software add-ons are also available with this offering.

## Balanced local storage
{: #balanced-local-storage}

Balanced local storage profiles are primarily for large database workloads that require high I/O performance with low latency. Network performance ranges from standard to premium.

### Local HDD
{: #HDD}

|Profile|vCPU|RAM|Secondary disks|Storage type|
|---|---|---|---|---|
|BL1.1x2|1|2 GB|25, 100 GB|Local HDD
|BL1.1x4|1|4 GB|25, 100 GB|Local HDD|
|BL1.2x4|2|4 GB|100, 200 GB|Local HDD|
|BL1.2x8|2|8 GB|100, 200 GB|Local HDD|
|BL1.4x8|4|8 GB|150, 300 GB|Local HDD|
|BL1.4x16|4|16 GB|150, 300 GB|Local HDD|
|BL1.8x16|8|16 GB|250 GB, (2 x 250 GB)|Local HDD|
|BL1.8x32|8|32 GB|250 GB, (2 x 250 GB)|Local HDD|
|BL1.16x32|16|32 GB|300 GB, (2 x 300 GB)|Local HDD|
|BL1.16x64|16|64 GB|300 GB, (2 x 300 GB)|Local HDD|
|BL1.32x64|32|64 GB|400 GB, (2 x 400 GB)|Local HDD|
|BL1.32x128|32|128 GB|400 GB, (2 x 400 GB)|Local HDD|
{: caption="Balanced local storage profiles using local HDD" caption-side="top"}

#### Storage notes
{: #storage-notes-local-hdd}

* Balanced local profiles automatically come with a 100 GB local storage boot disk. Then, you can select a second disk (options are shown in Table 3). Any additional local disks are optional. If you require over 500 GB, then two extra disks are required (for example, 8 cores require 2 x 250 GB of local storage).
*	Maximum local storage is limited by cores.
*	Balanced local storage is globally available; however, the type of storage (local SSD or local HDD) depends on the data center location.
*	You can't detach primary or secondary disks.

All supported operating systems (such as RHEL, CentOS, Windows, Ubuntu, and others), databases that are supported, and software add-ons are also available with this offering.

### Local SSD
{: #SSD}

|Profile|vCPU|RAM|Secondary disks |Storage type|
|---|---|---|---|---|
|BL2.1x2|1|2 GB|25, 100 GB|Local SSD|
|BL2.1x4|1|4 GB|25, 100 GB|Local SSD|
|BL2.2x4|2|4 GB|100, 200 GB|Local SSD|
|BL2.2x8|2|8 GB|100, 200 GB|Local SSD|
|BL2.4x8|4|8 GB|150, 300 GB|Local SSD|
|BL2.4x16|4|16 GB|150, 300 GB|Local SSD|
|BL2.8x16|8|16 GB|250 GB, (2 x 250 GB)|Local SSD|
|BL2.8x32|8|32 GB|250 GB, (2 x 250 GB)|Local SSD|
|BL2.16x32|16|32 GB|300 GB, (2 x 300 GB)|Local SSD|
|BL2.16x64|16|64 GB|300 GB, (2 x 300 GB)|Local SSD|
|BL2.32x64|32|64 GB|400 GB, (2 x 400 GB)|Local SSD|
|BL2.32x128|32|128 GB|400 GB, (2 x 400 GB)|Local SSD|
{: caption="Balanced local storage profiles using local SSD" caption-side="top"}

#### Storage notes
{: #storage-notes-local-ssd}

* Balanced local profiles automatically come with a 100 GB local storage boot disk. Then, you can select a second disk (options are shown in Table 7). Any extra local disks are optional. If you require over 500 GB, then two extra disks are required (for example, 8 cores require 2 x 250 GB of local storage).
*	Maximum local storage is limited by cores.
*	Balanced local storage is globally available; however, the type of storage (local SSD or local HDD) depends on the data center location.
*	You can't detach primary or secondary disks.

All supported operating systems (such as RHEL, CentOS, Windows, Ubuntu, and others), databases that are supported, and software add-ons are also available with this offering.

## Variable compute
{: #variable-compute}

Variable compute profiles are best for workloads that don’t require steady, high-CPU performance. Due to the level of CPU oversubscription that is allowed on the hosts for variable compute server instances, CPU performance levels might be less than other public profiles with the same number of cores, while RAM and storage remain consistent. These variable compute profiles are a lower-cost alternative. For example, you can use this function to test a new feature without incurring the higher cost of a full-performance virtual server instance.

The offering is available in the following profiles:

| Profile      | vCPU     | RAM       | Storage Type |
| ------------ | -------- | --------- | ------------ |
| U1.1x2       | 1        | 2 GB      | SAN          |
| U1.2x4       | 2        | 4 GB      | SAN          |
| U1.4x8       | 4        | 8 GB      | SAN          |
{: caption="Variable compute profiles" caption-side="top"}

### Storage notes
{: #storage-notes-variable-compute}

* SAN primary boot disk (25 or 100 GB) with an extra disk available, up to 2 TB. You can add one extra secondary disk to your variable compute instance.
* Pricing for public virtual servers that use SAN storage includes virtual CPU, memory, and minimum primary boot disk. Extra disk prices depend on the disk size and quantity that you select.

Supported operating systems (such as RHEL, CentOS, Ubuntu, and others), databases that are supported, and software add-ons are also available with this offering.

## Compute
{: #compute}

Compute profiles are best for workloads with intensive CPU demands, such as high web traffic workloads, production batch processing, and front-end web servers.

The offering is available in the following profiles:

| Profile      | vCPU     | RAM       | Storage Type |
| ------------ | -------- | --------- | ------------ |
| C1.1x1       | 1        | 1 GB      | SAN          |
| C1.2x2       | 2        | 2 GB      | SAN          |
| C1.4x4       | 4        | 4 GB      | SAN          |
| C1.8x8       | 8        | 8 GB      | SAN          |
| C1.16x16     | 16       | 16 GB     | SAN          |
| C1.32x32     | 32       | 32 GB     | SAN          |
{: caption="Compute profiles" caption-side="top"}

### Storage notes
{: #storage-notes-compute}

* SAN primary boot disk (25 or 100 GB) with extra disks available, up to 2 TB each (five total disks allowed).
* Pricing for public virtual servers that use SAN storage includes virtual CPU, memory, and minimum primary boot disk. Extra disk prices depend on the disk size and quantity that you select.

All supported operating systems (such as RHEL, CentOS, Windows, Ubuntu, and others), databases that are supported, and software add-ons are also available with this offering.

## Memory
{: #memory}

Memory profiles are best for memory intensive workloads, such as large caching workloads, intensive database applications, or in-memory analytics workloads.

The offering is available in the following profiles:

| Profile      | vCPU     | RAM       | Storage Type |
| ------------ | -------- | --------- | ------------ |
| M1.1x8       | 1        | 8 GB      | SAN          |
| M1.2x16      | 2        | 16 GB     | SAN          |
| M1.4x32      | 4        | 32 GB     | SAN          |
| M1.8x64      | 8        | 64 GB     | SAN          |
| M1.16x128    | 16       | 128 GB    | SAN          |
| M1.30x240    | 30       | 240 GB    | SAN          |
| M1.48x384    | 48       | 384 GB    | SAN          |
| M1.56x448    | 56       | 448 GB    | SAN          |
| M1.64x512    | 64       | 512 GB    | SAN          |
{: caption="Memory profiles" caption-side="top"}

### Storage notes
{: #storage-notes-memory}

* SAN primary boot disk (25 or 100 GB) with extra disks available, up to 2 TB each (five total disks allowed).
* Pricing for public virtual servers that use SAN storage includes virtual CPU, memory, and minimum primary boot disk. Extra disk prices depend on the disk size and quantity that you select.

All supported operating systems (such as RHEL, CentOS, Windows, Ubuntu, and others), supported databases, and software add-ons are also available with this offering.

## GPU
{: #gpu}

GPU profiles are best for high-performance workloads that require more compute density to reduce resource management and costs. The GPU profiles are ideal for artificial intelligence processes, intense graphic and data applications, or developing new applications that require fast performance.

Powered by NVDIA Tesla GPUs, {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” and "ac2" profiles both offer block and local SSD storage. The following GPU profiles are available globally for you to choose from:

|Profile|GPU|GPU RAM (GB)|vCPU|vCPU RAM (GB)|Storage Type|Boot Disk (GB)|Secondary Disks (2 and 3) (GB)|
|---|---|---|---|---|---|---|---|
|ac1.8x60x25|1 P100|16|8|60|Block (SAN)|25|None|
|ac1.8x60x100|1 P100|16|8|60|Local SSD or SAN|100|None (SAN), 300 (Local)|
|ac1.16x120x25|2 P100|32|16|120|Block (SAN)|25|None|
|ac1.16x120x100|2 P100|32|16|120|Local SSD or SAN|100|None (SAN), 600 (Local)|
{: caption="P100 GPU profiles" caption-side="top"}

|Profile|GPU|GPU RAM (GB)|vCPU|vCPU RAM (GB)|Storage Type|Boot Disk (GB)|Secondary Disks (2 and 3) (GB)|
|---|---|---|---|---|---|---|---|
|ac2.8x60x25|1 V100|16|8|60|Block (SAN)|25|None|
|ac2.8x60x100|1 V100|16|8|60|Local SSD or SAN|100|None (SAN), 300 (Local)|
|ac2.16x120x25|2 V100|32|16|120|Block (SAN)|25|None|
|ac2.16x120x100|2 V100|32|16|120|Local SSD or SAN|100|None (SAN), 600 (Local)|
{: caption="V100 GPU profiles" caption-side="top"}

### GPU prerequisites
{: #gpu-prerequisites}

Review the following GPU prerequisites.

1. GPU-profile virtual servers are available only on operating systems that support Hardware Virtual Machine (HVM) boot mode. See the following list for operating systems that support HVM boot mode.
   - Debian 8
   - Debian 9
   - RHEL 7
   - Ubuntu 16
   - Ubuntu 18
   - Windows 2012 R2
   - Windows 2016
   - Windows 2022

2. Appropriate NVIDIA drivers and software must be installed. For more information about software and NVIDIA drivers, see [Installing GPU drivers and software packages](/docs/virtual-servers?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages).

The software that you install might have prerequisite software and operating system-specific configurations.
{: note}

### Adding or removing GPUs
{: #adding-or-removing-gpus}

You can change the number of GPUs on your virtual server after your initial order. But, that depends on how many GPUs you provisioned. You have one of the following options.

- If one GPU is provisioned, you can add another GPU
- If two GPUs are provisioned, you can fall back to one GPU

### NVIDIA GRID
{: #nvidia-grid}

{{site.data.keyword.cloud_notm}} does not currently support GRID drivers for virtual GPUs. For GRID support, provision a GPU on a bare metal server and install the appropriate GRID driver. For more information, see [NVIDIA GPU support](/docs/bare-metal?topic=bare-metal-about-bm#bm-gpu-support){: external}.
