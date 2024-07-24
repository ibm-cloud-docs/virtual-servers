---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-24"

keywords: troubleshoot virtual server, virtual servers troubleshooting, tips, error, problem, insufficient capacity

subcollection: virtual-servers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why does my server have connectivity issues?
{: #vsi-troubleshoot-server-connectivity-issues}
{: troubleshoot}
{: support}

You are having connectivity issues with your virtual server instance.
{: tsSymptoms}

If your server has connectivity issues, the server might experience packet drops or packet loss and intermittent network connectivity.
{: tsCauses}

When your server faces a connectivity issue, you need to gather the following information if you need to escalate the issue with {{site.data.keyword.cloud}} support.
{: tsResolve}

* Nongraphical MTR and traceroute from the server to user location.
* Nongraphical MTR and traceroute from user location to the server.
* Hundred ping count from the server to user location.
* Hundred ping count from user location to the server.

If your server uses Linux, run the following command to gather the nongraphical MTR information.

   `mtr -r -c 100 -n`

To gather the Linux traceroute information, use the following Linux command.

   `traceroute`

If your server uses Windows, you can use the [WinMTR tool](http://sourceforge.net/projects/winmtr/){: external} to gather the nongraphical MTR and traceroute information. To gather the Windows traceroute information, run the `tracert` command in the command prompt.

After the tests complete, paste the results into the support case. You can also attach the results as a file or image. Make sure that you include the IP address that you are using to connect to the server. Disable your firewall, or allow echo and ICMP requests so that server traffic isn't dropped. For more help, contact [support](/docs/get-support?topic=get-support-get-supportfaq#contactsupport).
