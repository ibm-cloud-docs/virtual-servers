---

copyright:
  years: 2021, 2025
lastupdated: "2025-03-03"

keywords:

subcollection: virtual-servers

content-type: release-note

---

{{site.data.keyword.attribute-definition-list}}

# Release notes for {{site.data.keyword.BluVirtServers}} for Classic
{: #release-notes}

Use the release notes to learn the latest updates to {{site.data.keyword.BluVirtServers}} for the Classic infrastructure that are grouped by date.
{: shortdesc}

For more information about changes to the {{site.data.keyword.BluVirtServers}} API, see [{{site.data.keyword.BluVirtServers}} API reference overview](/docs/virtual-servers?topic=virtual-servers-api-reference).

## March 2025
{: #virtual-servers-mar25}

### 03 March 2025
{: #virtual-servers-mar0325}
{: release-note}

Add-on support for Rocky Linux

:   Rocky Linux on {{site.data.keyword.BluVirtServers}} for Classic now supports add-ons. For more information, see [Rocky Linux Documentation](https://docs.rockylinux.org/){: external}.

## September 2024
{: #virtual-servers-sep2024}

### 10 September 2024
{: #virtual-servers-sep102024}

New add-on support for Ubuntu 22.04
:   {{site.data.keyword.cloud}} Classic infrastructure now supports cPanel, Plesk, and R1Soft for Ubuntu 22.04.

## February 2024
{: #virtual-servers-feb24}

### 07 February 2024
{: #virtual-servers-jan1624}
{: release-note}

Ubuntu 20.04 LTS
:   now supports Ubuntu 20.04 LTS. For more information, see [Ubuntu releases](https://releases.ubuntu.com/){: external}.

## January 2024
{: #virtual-servers-jan24}

### 16 January 2024
{: #virtual-servers-jan1624}
{: release-note}

Debian 12
:   {{site.data.keyword.BluVirtServers}} for Classic now supports Debian 12. For more information, see [Debian "bookworm" release information](https://www.debian.org/releases/bookworm/){: external}.

## December 2023
{: #virtual-servers-dec23}

### 15 December 2023
{: #virtual-servers-dec1523}
{: release-note}

SSL Certificate Order is deprecated
:   As of 15 April 2024, SSL Certificate Order is no longer available for purchase. As of 15 December 2024, SSL Certificate Order is no longer supported for new orders or reorders. Only existing certificates that are not expired are still available for you to download, reissue, or revoke. For more information, see [Deprecation of SSL Certificates](/docs/ssl-certificates?topic=ssl-certificates-deprecation).
{: deprecated}

### 07 December 2023
{: #virtual-servers-dec1223}
{: release-note}

CentOS Stream 9
:   {{site.data.keyword.BluVirtServers}} for Classic now supports CentOS Stream 9. For more information, see [CentOS Stream 9](https://centos.org/stream9/){: external}.

## October 2023
{: #virtual-servers-oct23}

### 27 October 2023
{: #virtual-servers-oct2723}
{: release-note}

Microsoft&reg; SQL Server 2019 and 2022
:   Classic infrastructure bare metal and virtual servers now support Microsoft SQL Server [2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019){: external} and [2022](https://www.microsoft.com/en-us/sql-server/sql-server-2022){: external}.

## May 2023
{: #virtual-servers-may23}

### 15 May 2023
{: #virtual-servers-may1123}
{: release-note}

Red Hat Enterprise Linux 9 (RHEL 9)
:   IBM Cloud&reg; server software now supports RHEL 9 as an OS option for virtual servers. For more information, see the virtual servers tab in [Supported operating systems for IBM Cloud&reg; server software](/docs/bare-metal?topic=bare-metal-about-software#supported-operating-systems-for-ibm-cloud-servers).

## September 2022
{: #virtual-servers-sep22}

### 30 September 2022
{: #virtual-servers-sep3022}
{: release-note}

End of service (EOS) for Autoscale
:   *End of service (EOS): 30 September 2022* After this date, Autoscale for {{site.data.keyword.BluVirtServers}} is no longer supported. Any autoscale schedules that still exist after that date are deleted. You can use Auto scale for your virtual servers that are on {{site.data.keyword.vpc_short}}. For more information, see [Creating an instance group for auto scaling](/docs/vpc?topic=vpc-creating-auto-scale-instance-group).

## June 2022
{: #virtual-servers-jun22}

### 27 June 2022
{: #virtual-servers-jun2722}
{: release-note}

End of Marketing (EOM) for Autoscale
:   *End of Marketing (EOM): 30 July 2022* After this date, Autoscale for {{site.data.keyword.BluVirtServers}} is no longer available for purchase. You can use Auto scale for your virtual servers that are on {{site.data.keyword.vpc_short}}. For more information, see [Creating an instance group for auto scaling](/docs/vpc?topic=vpc-creating-auto-scale-instance-group).

## June 2021
{: #virtual-servers-jun21}

### 08 June 2021
{: #virtual-servers-jun0821}
{: release-note}

KVM console is now available
:   You can now access the KVM console of your virtual servers directly from IBM Cloud console. For more information, see [Accessing the KVM console for virtual servers](/docs/virtual-servers?topic=virtual-servers-access-kvm-console).

## July 2020
{: #virtual-servers-jul20}

### 22 July 2020
{: #virtual-servers-jul2220}
{: release-note}

IBM Cloud Monitoring
:   {{site.data.keyword.mon_full}} collects classic infrastructure and VPC virtual server instance metrics such as CPU usage, disk usage, network traffic, and memory. These metrics are stored in {{site.data.keyword.mon_full_notm}}. For more information, see [IBM Cloud Monitoring](/docs/cloud-infrastructure?topic=cloud-infrastructure-monitoring-iaas).

## February 2020
{: #virtual-servers-feb20}

### 11 February 2020
{: #virtual-servers-feb1120}
{: release-note}

Veeam Backup for Microsoft Office 365 is now available
:   Veeam Backup for Microsoft Office 365 is now available for virtual servers monthly. For more information about Veeam Backup for Microsoft Office 365, see [Veeam backup for Office 365](/docs/virtual-servers?topic=virtual-servers-veeam-backup-o365).

## September 2019
{: #virtual-servers-sep19}

### 12 September 2019
{: #virtual-servers-sep1219}
{: release-note}

Improve network performance by configuring jumbo frames
:   You can improve network performance on your virtual server instance by configuring jumbo frames in your virtual server settings. You can configure jumbo frames for the following operating systems.

   * Linux: Debian, Ubuntu, CentOS, Red Hat Enterprise Linux
   * Windows

## May 2019
{: #virtual-servers-may19}

### 07 May 2019
{: #virtual-servers-may0719}
{: release-note}

Autoscale now available for virtual servers
:   Auto scale for {{site.data.keyword.BluVirtServers}} provides you with the ability to automate the manual scaling process that's associated with adding or removing instances to support your business applications. This automation sets up new instances automatically as more resources are needed and then those instances are shut down and removed when the extra load subsides. Auto scale uses groups to contain the policies that change how your environment expands or shrinks. These policies use actions to add or remove a virtual server based on your business and application needs.

## April 2019
{: #virtual-servers-apr19}

### 15 April 2019
{: #virtual-servers-apr1519}
{: release-note}

View and update device details for virtual servers
:   You can now view the existing usernames and passwords for a device or update those values from the device details page. For more information, see [Viewing and managing device usernames and passwords](/docs/virtual-servers?topic=virtual-servers-view-update-user-name-password-for-device).

### 24 April 2019
{: #virtual-servers-apr2419}
{: release-note}

New profile families for virtual server
:   When you provision {{site.data.keyword.BluVirtServers}}, you can select from supported families of profiles. A profile is a combination of vCPU and RAM that can be instantiated quickly to start a virtual server instance. In the {{site.data.keyword.cloud_notm}} console, you can choose from popular profile configurations or select from a list of profiles that best fit your needs. For more information, see [Profiles](/docs/virtual-servers?topic=virtual-servers-about-virtual-server-profiles).

## October 2018
{: #virtual-servers-oct18}

### 03 October 2018
{: #virtual-servers-oct0318}
{: release-note}

Provision a virtual server by using 3rd-party images (deprecated)
:   Provisioning a virtual server instance from an image that was created by a 3rd party vendor by using the IBM Cloud catalog Cloud Images link is now deprecated.
{: deprecated}

### 30 October 2018
{: #virtual-servers-oct3018}
{: release-note}

View suspended billing on your virtual server
:   You can now view whether your virtual server instance supports billing. For more information, see [Viewing suspend billing](/docs/virtual-servers?topic=virtual-servers-viewing-suspend-billing-feature).

### 31 October 2018
{: #virtual-servers-oct3118}
{: release-note}

Placement groups are available on virtual servers
:   With placement groups, you can use public instances to build for high availability within a data center or provide and extra level of fault tolerance within a larger deployment. Each placement group can be assigned a maximum of 5 new virtual server instances. Each virtual server is provisioned on different physical hosts. For more information, see [Placement groups](https://cloud.ibm.com/docs/virtual-servers?topic=virtual-servers-placement-groups).

## September 2018
{: #virtual-servers-sep18}

### 26 September 2018
{: #virtual-servers-sep2618}
{: release-note}

Reserved servers are now available
:   Reserved servers offer guaranteed resources for future deployments and with one or three year contract terms, offers you cost savings. You can reserve up to 20 virtual server instances of a specific size. Reserved capacity must be provisioned first before other virtual server instances. For more information, see [Reserved virtual servers](/docs/virtual-servers?topic=virtual-servers-about-reserved-virtual-servers).
