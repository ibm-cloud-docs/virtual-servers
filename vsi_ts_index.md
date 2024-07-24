---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-24"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Getting help and support for virtual servers
{: #virtual-server-help-and-support}

If you experience an issue or have questions with a virtual server, you can use the following resources before you open a support case.
{: shortdesc}

* Review the [FAQs](/docs/virtual-servers?topic=virtual-servers-faqs-virtual-servers) in the product documentation.
* Review the [troubleshooting documentation](/docs/virtual-servers?topic=virtual-servers-vsi-troubleshoot-vs-why-vs-read-only) to troubleshoot and resolve common issues.
* Check the status of the {{site.data.keyword.Bluemix_notm}} platform and resources by going to the [Status page](https://cloud.ibm.com/status){: external}.
* Review [Stack Overflow](https://stackoverflow.com/questions){: external} to see whether other users experienced the same problem. When you ask a question, tag the question with `ibm-cloud` and `virtual servers` so the {{site.data.keyword.Bluemix_notm}} development teams see it.
* If you have technical questions about {{site.data.keyword.baremetal_short}}, post your question on [Stack Overflow](http://stackoverflow.com/search?q=bare-metal+ibm-cloud){: external} and tag your question with `ibm-cloud` and `bare-metal`.
* For questions about the service and getting started instructions, use the [IBM Support forum](https://community.ibm.com/community/user/home){: external}. Include the `ibm cloud` tag.

If you still can't resolve the problem, you can open a support case. For more information, see [Creating support cases](/docs/get-support?topic=get-support-open-case). And, if you're looking to provide feedback, see [Submitting feedback](/docs/overview?topic=overview-feedback).



## Providing support case details
{: #virtual-server-support-case-details}

To make sure that the support team can start investigating your case to provide a timely resolution, you must include detailed information along with steps to re-create the issue, if applicable. Review the following types of information to include in your support case for issues with bare metal servers.

### Connectivity issues
{: #virtual-server-connectivity-issues}

When your server faces a connectivity issue, you need to gather the following information if you need to escalate the issue with {{site.data.keyword.cloud}} support.

* Nongraphical MTR and traceroute from the server to user location.
* Nongraphical MTR and traceroute from user location to the server.
* Hundred ping count from the server to user location.
* Hundred ping count from user location to the server.
* IP address that you are using the connect to the server.

| Information to gather | Command |
|-----|-----|
| Nongeographical MTR information | `mtr -r -c 100 -n` |
| Traceroute information |  `traceroute` |
{: caption="Table 1. Information to collect for connectivity issues - Linux" caption-side="bottom"}
{: #connectivity-linux}
{: tab-title="Linux"}
{: tab-group="Connectivity"}
{: class="simple-tab-table"}
{: summary="How to gather Linux MTR and traceroute information."}

| Information to gather | Command |
|-----|-----|
| Nongeographical MTR information | [WinMTR tool](http://sourceforge.net/projects/winmtr/){: external} |
| Traceroute information | [WinMTR tool](http://sourceforge.net/projects/winmtr/){: external} or run the `tracert` command in the command prompt. |
{: caption="Table 2. Information to collect for connectivity issues - Windows" caption-side="bottom"}
{: #connectivity-windows}
{: tab-title="Windows"}
{: tab-group="Connectivity"}
{: class="simple-tab-table"}
{: summary="How to gather Windows MTR and traceroute information."}


## Why is my migration not working?
{: #troubleshoot-migration-stuck}

If your migration is stuck or didn't complete properly, create a [support case](/docs/get-support?topic=get-support-get-supportfaq#open-support-case) for assistance.
