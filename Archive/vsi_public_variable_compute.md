---

copyright:
  years: 2019
lastupdated: "2019-03-13"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:table: .aria-labeledby="caption"}

# Archived 6/3/19 - Variable compute
{: #about-variable-compute}

Variable compute profiles are best for workloads that don’t require steady, high-CPU performance. CPU performance levels might be less than other public profiles with the same number of cores, while RAM and storage remain consistent, which makes variable compute profiles a lower-cost alternative. For example, you can use this function to test a new feature without incurring the higher cost of a full-performance virtual server instance.
{: shortdesc}

The offering is available in the following profiles:

| Profile      | vCPU     | RAM       | Storage Type |
| ------------ | -------- | --------- | ------------ |
| U1.1x1       | 1        | 1 GB      | SAN          |
| U1.1x2       | 1        | 2 GB      | SAN          |
| U1.2x4       | 2        | 4 GB      | SAN          |
| U1.4x8       | 4        | 8 GB      | SAN          |
{: caption="Table 1. Variable compute profiles" caption-side="top"}

**Storage notes** 
* SAN primary boot disk (25 or 100 GB) with extra disks available, up to 2 TB each (five total disks allowed).
* Pricing for public virtual servers by using SAN storage includes virtual CPU, memory, and minimum primary boot disk. Extra disk prices depend on the disk size and quantity that you select.  

Variable compute profiles are available in all data centers.

Supported operating systems (such as RHEL, CentOS, Ubuntu, and others), supported databases, and software add-ons are also available with this offering.
