---

copyright:
  years: 2021, 2024
lastupdated: "2023-09-13"

keywords: classic virtual servers, access kvm console, connect to virtual server, kvm console, kvm virtual servers, virtual server kvm, vsi kvm, classic kvm

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Accessing the KVM console for virtual servers
{: #access-kvm-console}

You can now access the KVM console of your virtual servers from the {{site.data.keyword.cloud}} console.
{: shortdesc}

The KVM console for virtual servers provides a graphical user interface and accepts both mouse and keyboard input. You can open the KVM console by using any of the {{site.data.keyword.cloud}} supported browsers. For more information about {{site.data.keyword.cloud}} supported browsers, see [Browsers](/docs/overview?topic=overview-prereqs-platform#browsers-platform).

The KVM console is a quick way for you to configure and administer your virtual servers. It applies to situations where a boot failure or kernel crash occurred. When these situations happen, you can use the KVM console to examine the issue.

## Prerequisites
{: #prereqs}

* Before you can access the KVM console of a virtual server, you must establish a VPN connection to the private network. For more information about connecting to the VPN, see [Connecting to SSL VPN](/docs/iaas-vpn?topic=iaas-vpn-standalone-vpn-clients).

* The virtual server must be powered on.

## Using the {{site.data.keyword.cloud}} console to connect to the KVM console
{: #connect-to-console-using-ui}

Use the following steps to connect to a console by using {{site.data.keyword.cloud}} console.

1. In the {{site.data.keyword.cloud}} UI console, find your virtual server in the **Device List** and click the name of the virtual server to enter the details page.

2. Click **Actions** > **KVM Console**.

3. In the VPN notification window, click **Continue**.

4. In the KVM console window, enter your credentials to log in to the virtual server.

## Actions that are available in the KVM console window
{: #available-actions}

In the KVM console window, you can restart, power on, and power off the virtual server. To perform these actions, click the overflow icon on the upper right of the console's window, then click the appropriate action.

You can also use the **Ctrl + Alt + Del** key combination from the actions, which works with all OSes.
{: tip}

If the console disconnects, you can reconnect by clicking **Reconnect**. 

## Disconnecting from the KVM console
{: #disconnect}

When you're finished with the console, you can disconnect from it by closing the browser window.

### Notes on the KVM console
{: #notes}

The **KVM Console disconnected** notification appears anytime the console either can’t connect or gets disconnected in the middle of a session. The code in the text is displayed only if the disconnection was unexpected. This code helps the debugging tool troubleshoot the connection. On a regular disconnection, no code is displayed.

The KVM Console opens in a new browser tab or window. If the KVM Console doesn't open, check the browser for any blocked new windows.

If you can't access your server through the KVM, [open a support case](/docs/get-support?topic=get-support-get-supportfaq#open-support-case) or [contact support](/docs/get-support?topic=get-support-support-plans).
