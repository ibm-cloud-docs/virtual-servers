---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Migrating a dedicated host instance to another host
{: #migrating-dedicated-host}

You can migrate your dedicated host instances from one host to another within the same POD. Select the instance to be migrated from either the host’s Device Details page or the instance’s Device Details page. Note that only two instances can be migrated at a time and the time needed to migrate depends on the disk. SAN disks are migrated quicker because local disks require copying the disk. The migrating instances are offline while being migrated; the host does remain up for any of its other dedicated host instances.
{:shortdesc}

Use the following steps to migrate dedicated host instances to another dedicated host within the same POD from the Device Details page of the *original dedicated host*.

1. Access the [{{site.data.keyword.slportal_full}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) by using your unique credentials.
2. Click **Device > Device List** and select either the host or the hosted instance from the list.
3. Click the **Actions** drop-down list next to the dedicated instance to be migrated.
4. Select **Migrate** and enter the host where the instance is migrating to; remember, the target host must be within the same POD as the original host.
5. Click the **Migrate** button.

The migration will begin immediately. During the migration, the dedicated instance is offline until on its new host. You can view the target host’s Device Details page to make sure the instance migrated correctly.

Use the following steps to migrate dedicated host instances to another dedicated host within the same POD from the Details page of the *dedicated host instance*.

1. Access the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) by using your unique credentials.
2. Click **Device > Device List** and select the hosted instance to be migrated from the list.
3. Click the **Migrate** link on the right side of the page.
4. Select the target host to migrate the instance to; remember, the target host must be within the same POD as the original host.
5. Click the **Migrate** button.

The migration will begin immediately. During the migration, the dedicated instance is offline until on its new host. You can view the target host’s Device Details page to make sure the instance migrated correctly.

## Next Steps
After you migrate a dedicated host instance, confirm the migration worked by verifying that its Status is green on the new dedicated host's Device Details page.
