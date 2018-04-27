---
copyright:
  years: 2014, 2018
lastupdated: "2018-02-20"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Provisioning scripts

A provisioning script is a script that can either be downloaded to, or downloaded and run on, a device during the provisioning process. For existing accounts, provisioning scripts are managed within the {{site.data.keyword.slportal_full}}. During the ordering process, you can manually enter scripts for new accounts or scripts that are not yet tracked.

During the provisioning process, scripts that are associated with an HTTP URL are downloaded to the device. After provisioning, an administrator must run the script manually on the device. Scripts that are associated with an HTTPS URL are downloaded and run automatically. Provisioning scripts are currently available on standard Linux operating systems (Cent, RHEL, Fedora, Debian, or Ubuntu), and Windows and FreeBSD. Other systems such as Vyatta, Netscaler, XenServer, VMware are not supported. The provisioning script can be any type of file that is run by the operating system, including combined binary files or any OS supported language.

For more information, see [Managing a provisioning script](add-provisioning-script.html).
