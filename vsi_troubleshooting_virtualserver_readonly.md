---

copyright:
  years: 2017, 2023
lastupdated: "2023-09-28"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why is my virtual server read-only?
{: #vsi-troubleshoot-vs-why-vs-read-only}
{: troubleshoot}
{: support}

The virtual server is in read-only status.
{: tsSymptoms}

A virtual server might receive a read-only issue because of unplanned networking incidents or outages.
{: tsCauses}

To bring back your server from a read-only status, you need to restart the server to rescue kernel, and you need to run a file system check on all your file systems.
{: tsResolve}

1. From your device list, click the **name of the server** > **Actions menu** > **Rescue kernel**.
1. When your server restarts in rescue mode, log in to the server by using SSH with the root user credentials.
1. Run a file system check by using the following command:
   `fsck -y -C /dev/xvda1`
1. Run the same command if you have more files systems such as _/dev/xvda2_, _/dev/xvda3_, and so on.

For more help, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp) or open a support case.

Running a file system check might cause data loss, so make sure that your data is backed up.
{: note}
