---



copyright:
  years: 2017
lastupdated: "2017-09-05"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Dedicated virtual servers
The IBM® Bluemix® infrastructure dedicated host offering is a virtualized, single-tenant, dedicated server. It provides you with maximum control over workload placement and flexible post-provisioning options. You can decide which pre-determined IBM® Cloud Data Center your virtual servers are placed in and can be assured capacity by allocating your host(s) directly to your account.
{:shortdesc}

The offering includes the following features: 

* Affinity and anti-affinity. You can specify host-to-virtual server and virtual server-to-virtual server relationships that should remain, which are known as affinity and anti-affinity rules. These rules help you make sure that your workloads are placed appropriately based on your workload requirements.
* Post-deployment management. You can migrate virtual servers between dedicated hosts based on your workload requirements.
* Workload visibility. You can view resource consumption—core, RAM and local storage—for each host, giving you maximum control over your workload management.

You have the choice of two deployment models: dedicated hosts and dedicated instances. Dedicated hosts help with control over workload placement and dedicated instances offer single-tenant isolation. 

**Note:** Dedicated instances do not provide some of the control features offered by dedicated hosts.  See the following table for more details. 
<table>
<CAPTION>Table 1. Control features</CAPTION>
<THEAD>
<TR>
<th>Dedicated virtual server feature</th>
<th>Dedicated hosts instances</th>
<th>Dedicated instances</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>Single-tenant isolation</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td>Virtual server placement control</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Resource visibility</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Instance billing</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td>Host billing<sup>(1)</sup></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Post-deployment control</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Capacity reservations</td>
<td>X</td>
<td></td>
</tr>
</TBODY>
</table>


<sup>(1)</sup>Pricing of host is inclusive of core, RAM, Local SSD and network speeds. Premium operating system (OS), storage area network (SAN) storage and software add-ons will be priced per instance with existing pricing and licensing in an hourly or monthly model.

Keep in mind the following when you’re ordering a dedicated host(s) and dedicated host instances:

* Your host location; you can select from the following IBM Cloud Data Centers:
      
| Data Centers          ||
| ------------ | ------- | 
|AMS01         |  MON01  |
|AMS03         |  OSL01  |
|CHE01         |  PAR01  |
|DAL05         |  SAO01  |
|DAL06         |  SEO01  |
|DAL09         |  SJC01  |
|DAL10         |  SJC03  |
|DAL12         |  SJC04  |
|DAL13         |  SNG01  | 
|FRA02         |  SYD01  |
|HKG02         |  SYD04  |
|HOU02         |  TOK02  |
|LON02         |  TOR01  |
|LON04         |  WDC01  |
|MEL01         |  WDC04  |
|MEX01         |  WDC06  |
|MIL01         |  WDC07  |
{: caption="Table 2. Supported data centers" caption-side="top"}

* The size of your host(s) is determined by your workloads that you will be running on it. The default is 56 Cores X 242 GB RAM X 1.2 TB. 
* You can order only two hosts at a time. For example, if you need six hosts, you will need to place three separate orders.
* Each host will need its own unique name and you can automatically assign your POD.

## Next Steps

After you have reviewed and decided upon your deployment options, it is time to provision your virtual server. To get started, see [Provisioning dedicated hosts and instances](../vsi/vsi_provision_dedicated.html).



  
