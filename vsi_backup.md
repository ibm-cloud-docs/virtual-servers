---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Back-up services

## IBM Cloud Backup

{{site.data.keyword.backup_full}} is an automated agent-based backup system that is managed through the {{site.data.keyword.backup_notm}} WebCC browser-based management utility, providing users with a method to back up data between servers in one or more data centers on the {{site.data.keyword.BluSoftlayer}} network.  Administrators can set backups to follow an hourly, daily, weekly, or custom schedule that targets full systems, specific directories, or even individual files.  Additional plug-ins allow for compatibility with software like Microsoft Exchange and Microsoft SQL, as well as other types of third-party software and enables users to perform a Bare Metal Restore, when necessary.

For more information about {{site.data.keyword.backup_notm}} services, see [Getting Started with {{site.data.keyword.backup_notm}} services](/docs/infrastructure/Backup?topic=Backup-gettingstarted#gettingstarted).

## R1Soft CDP

Continuous Data Protection (CDP) is a high-performance backup software created by R1Soft that allows for backup of both physical and virtual devices. Idera CDP consists of three main components: the CDP server, the agent, and the database plugins, which are available for purchase separately from the first two components.  Because R1Soft CDP is a third-party backup solution, interactions with CDP take place entirely outside of {{site.data.keyword.Bluemix_short}} proprietary interfaces; however, R1Soft CDP passwords may be tracked and stored within {{site.data.keyword.slportal}}.  All other interactions with R1Soft CDP are documented on the R1Soft website.

For more information about R1Soft CDP back-up services, see [R1Soft Documentation ![External link icon](../icons/launch-glyph.svg "External link icon")](http://wiki.r1soft.com/display/ServerBackupManager/Home){: new_window}.
