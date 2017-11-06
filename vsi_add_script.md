---



copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Adding a custom provisioning script 
{: #adding-post-script}

Custom provisioning scripts allow users to specify a URL to a script that is run on a newly provisioned device. You can post and manage custom provisioning scripts within {{site.data.keyword.slportal_full}}.
{:shortdesc}

When ordering a device, you can select a custom provisioning script if it has been posted to the Provisioning Scripts screen of the {{site.data.keyword.slportal}}. If a script has not been added, you can provide a URL. Provisioning scripts can be any file that the operating system (OS) can execute, including combined binary files or any OS-supported language. Use the following steps to add a custom provisioning script on the {{site.data.keyword.slportal}}.

**Note:** This feature is currently available to Linux and Unix-based operating systems only.

## Adding a provisioning script

1. From the **Devices** menu in the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window}, select **Manage** > **Provisioning Scripts**.
2. Click **Add Provisioning Script**.
4. In the Name field, enter a unique script name.
5. In the URL field, enter the exact URL to be associated with the script.
6. Click **Add**.

## Next steps
After an order that contains a provisioning script is submitted, the device is provisioned similar to any other device. Before the device becomes available, the specified script is downloaded to the device. The origin of the provisioning script determines the behavior during this last step of the provisioning process. If the script is supplied from an HTTPS URL, the script is downloaded and runs with no additional interaction required of the user. If the script is supplied over HTTP, the script is downloaded only. For scripts provided over HTTP, the administrator must log in to the device and run the script manually.
