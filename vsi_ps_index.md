---

copyright:
  years: 2014, 2022
lastupdated: "2022-02-16"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# Provisioning scripts
{: #provisioning-scripts}

A provisioning script is a script that can either be downloaded to, or downloaded and run on, a device during the provisioning process. For existing accounts, provisioning scripts are managed within the {{site.data.keyword.cloud}} console. During the ordering process, you can manually enter scripts for new accounts or scripts that are not yet tracked.

Alternatively, you can use a cloud-init enabled image and provide user data to automatically perform configuration tasks or run scripts. For more information, see [Provisioning with a cloud-init enabled image](/docs/image-templates?topic=image-templates-provisioning-with-a-cloud-init-enabled-image).
{: tip}

During the provisioning process, scripts that are associated with an HTTP URL are downloaded to the device. After provisioning, an administrator must run the script manually on the device. Scripts that are associated with an HTTPS URL are downloaded and run automatically. Provisioning scripts are currently available on only Linux operating systems (CentOS, RHEL, Fedora, Debian, or Ubuntu), and Windows and FreeBSD. The provisioning script can be any type of file that is run by the operating system, including combined binary files or any OS supported language.

For more information, see [Managing a provisioning script](/docs/virtual-servers?topic=virtual-servers-managing-a-provisioning-script#managing-a-provisioning-script).
