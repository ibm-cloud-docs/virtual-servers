---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Managing dedicated hosts and instances
{: #managing-virtual-servers}

The Device Details page is where you manage your dedicated host and instances, track your support tickets, and monitor your host’s availability. You can access and view your dedicated host instances two ways from the Device List—as part of their host or as an individual instance.
{:shortdesc}

## Host Configuration tab
You can perform several tasks from the **Configuration** tab for the dedicated host, including manage your dedicated host instances. Under the Actions drop-down menu, you can rename the host or cancel it. All assigned dedicated host instances must be canceled or migrated first before a host can be canceled, otherwise an error message is received.

Notes can be kept on the host and its instances; for example, Migration from myDallasHost to myTorHost is scheduled for XX/XX/XXXX. The General, System, and Network frames of the page provide you with at-a-glance details about the host. Note that the Storage frame refers to local storage capacity.

The Instances frame contains the instances assigned to a specific host, as well as the ability to add instances to the host. Click on the Actions menu for an instance to do the following to it:

* Reboot
* Power on and off
* Rename
*	View audit logs
*	Upgrade or downgrade
*	Cancel
*	Migrate

## Host Tickets tab
Use the Tickets tab to open support tickets for the host and any of its instances by clicking the Add a Ticket for this Device link.

## Host Allocations tab
The Allocations tab lets you view available cores, RAM, and local storage for your dedicated host. The blue slice of the “pie” represents what’s in use and the white slice is what’s available.

## Dedicated host instance tab
The dedicated host instance Device Details page can be reached either through its host’s Device Details page or directly from the Device List. There are more tabs at the dedicated host instance level; Configuration and Tickets are similar to the tabs found at the host level. The Modify Device Configuration link, on the Configuration tab, lets you make changes to your system (core, RAM, and local storage) and network (bandwidth and uplink port speeds) setup.

Usage displays a time-plot graph based on CPU usage by date. You can roll over the graph to see CPU usage for a specific date and time, which is helpful when trying to determine if you need to add processing capacity.

Bandwidth is another time-plot graph that lets you enter parameters to see how much bandwidth is being used over time. The Storage tab displays any additional block or file storage on the instance.

# Cancel a dedicated host
You can cancel a dedicated host at any time. A prerequisite to canceling a host is to either have migrated the dedicated instances assigned to it to another dedicated host or have canceled the instances, too. 
## Cancel a dedicated host from the Device List
Use the following steps to cancel a dedicated host from the Device List.

1. Select **Device** > **Device List**.
2. Find the dedicated host to be canceled and click the **Actions** drop-down menu.
3. Select **Cancel Host**. 
4. A pop-up window containing a list dedicated instances assigned to the host will appear. You will need to either migrate or cancel the instances, if you haven't done so already, prior to canceling the host. Click **OK**.

You'll receive a message that the dedicated host is canceled. There will be a link to the support ticket to cancel the dedicated host.
## Cancel a dedicated host from the Device Details page
Use the following steps to cancel the dedicated host from the Device Details page.

1. Select **Device** > **Device List**.
2. Find the dedicated host to be canceled and double click on it.
3. Verify that all the dedicated instances assigned to the dedicated host have either been migrated or canceled.
4. Click the **Actions** drop-down menu and select **Cancel Host**.

You'll receive a message that the dedicated host is canceled. There will be a link to the support ticket to cancel the dedicated host.

### Cancel a dedicated instance

Before you can cancel a dedicated host, the dedicated instances assigned to it have to be canceled. Dedicated instances can be canceled directly from the Device List, the Device Details page of their assigned host, or their own Device Details page. 

1. Select the dedicated instance to be canceled and click the **Actions** drop-down menu.
2. Select **Cancel Device**.
3. A warning message will appear. Click the **Reason** drop-down menu and select the reason you're canceling the dedicated instance and click **Continue**.

You'll receive a message that the dedicated instance is canceled. There will be a link to the support ticket to cancel the dedicated instance.

