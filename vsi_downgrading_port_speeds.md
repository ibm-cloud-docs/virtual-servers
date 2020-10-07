---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-29"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Downgrading port speeds
{: #downgrading-port-speeds}

You can temporarily downgrade port speeds for your virtual server instance without opening a ticket. You can only downgrade, disconnect, or reconnect at a maximum of whatever you are already paying for. You cannot upgrade from this option. The changes stay in the console until you change it back. No billing changes are made from this, and downgrading your server temporarily does not lower your bill. If you need a permanent change to your port speed, you must open a sales ticket.
{:shortdesc}

## Before you begin
{: #before-you-begin-downgrading-port-speeds}

First, navigate to the device menu and ensure you have the correct account permissions to complete the task. 

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions. 

For more information about permissions, see [Classic infrastructure permissions](/docs/account?topic=account-infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Downgrading port speeds
{: #downgrade-port-speed}

Complete the following steps to downgrade port speeds.

1. From the **Devices** menu, select **Device List**.
2. Select the server that you want to update.
3. In the **Overview** tab, go to **Network details.**
4. Select the drop-down menu in **Speed** (for either public or private network) to downgrade or disconnect the port speed.

When changing port speeds or disconnecting your ports for any reason, you must manually change the server itself.
{:tip}
