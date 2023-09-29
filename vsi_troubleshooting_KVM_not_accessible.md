---

copyright:
  years: 2017, 2023
lastupdated: "2023-09-28"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I access KVM through a browser?
{: #vsi-troubleshoot-vs-KVM-not-accessible-browser}
{: troubleshoot}
{: support}

You are unable to connect to the KVM console.
{: tsSymptoms}

This issue might be caused by one of the following reasons.
{: tsCauses}

* Your browser needs to be updated.
* You don't have an established VPN connection.
* Your credentials are invalid.

To attempt to resolve the issue, try the following troubleshooting tasks:
{: tsResolve}

* Browser needs updating

   1. Make sure that you're using a supported browser. For more information about {{site.data.keyword.cloud}}-supported browsers, see [Browsers](/docs/overview?topic=overview-prereqs-platform#browsers-platform).
   1. The KVM Console opens in a new browser tab or window. If the KVM Console doesn't open, check the browser for any blocked new windows.
   1. If you can't access KVM through your browser, you might need to update your browser. Update your browser and try to access KVM.

* A VPN connection isn't established

   Make sure that a connection is established by using the VPN. If a connection isn't established, a warning displays that a VPN connection is required. For more information, see [Getting started with IBM Cloud Virtual Private Networking](/docs/iaas-vpn?topic=iaas-vpn-getting-started).

* Your credentials are invalid

   Check that the credentials for the device are valid. Contact the account administrator to verify credentials, if necessary.
   
For more information about accessing the KVM, see [Accessing the KVM console for virtual servers](/docs/virtual-servers?topic=virtual-servers-access-kvm-console).

