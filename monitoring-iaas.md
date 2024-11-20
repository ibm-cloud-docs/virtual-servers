---

copyright:
  years: 2020, 2024
lastupdated: "2024-11-20"

subcollection: cloud-infrastructure

---

{{site.data.keyword.attribute-definition-list}}

# {{site.data.keyword.mon_full_notm}}
{: #monitoring-iaas}

You can use {{site.data.keyword.mon_full_notm}} to monitor classic infrastructure metrics such as CPU usage, disk usage, network traffic, and memory. These metrics are stored in {{site.data.keyword.mon_full_notm}}. You can access metrics through the prebuilt dashboards.
{: shortdesc}

{{site.data.keyword.mon_full_notm}} metrics are available if you deploy the monitoring agent for non-orchestrated environments. For more information, see [{{site.data.keyword.mon_full_notm}} agent for non-orchestrated environments metrics](/docs/cloud-infrastructure?topic=cloud-infrastructure-enabling-monitoring-light-no-driver#monitoring-light-metrics).
{: important} 

## Basic monitoring
{: #basic-monitoring}

You use basic monitoring to initiate service and slow pings to make sure that the device is online and responsive. 

| Basic monitoring service types | Description |
|--------------------------------|-------------|
| SERVICE PING                   | Test ping to address |
| SLOW PING | Test ping to address - doesn't fail on slow server response due to high latency or high server load. |
{: caption="Basic monitoring service types" caption-side="bottom"}

The source of service ping and slow ping monitoring depends on the data center where the server is located. To use public IP monitoring, you need to allow ICMP from the server's data center [public service network](/docs/cloud-infrastructure?topic=cloud-infrastructure-ibm-cloud-ip-ranges#front-end-network). For private IP monitoring, you need to allow ICMP from the server's data center [private service network](/docs/cloud-infrastructure?topic=cloud-infrastructure-ibm-cloud-ip-ranges#service-network).

If an echo isn't received in the allotted time frame (1 second for service pings, 5 seconds for slow pings), an alert is sent to the email address on the account. A status of **Up** in the **Status** field indicates that an echo was received, while **Down** indicates that the echo wasn't received.
{: tip}

### Host ping and TCP service monitoring
{: #basic-monitoring-addons}

**Host ping** is the default basic monitoring option. If you want more basic monitoring options, you need to select **Host ping and TCP service monitoring**. This selection gives you access to the following add-on monitoring services.

| Add-on monitoring service types | Description |
| ----- | ----- |
| DNS | Test generic `nslookup` on address |
| DNS CUSTOM | Test `nslookup` for specified domain on address |
| FTP | Test for FTP connection to port 21 on address |
| HTTP | Test for HTTP connection to port 80 on address |
| HTTP CUSTOM | Test for HTTP connection to port 80 on address, checks for given response text | 
| HTTPS | Test for HTTP connection to port 443 on address |
| IMAP | Test for IMAP connection on address |
| LDAP | Test for LDAP connection on address |
| NNTP | Test for NNTP connection on address |
| POP | Test for POP connection on address |
| SMTP | Test for SMTP connection on address |
| SSH | Test for SSH connection to port 22 on address |
| TCP CUSTOM | Test for TCP connection to specified port on address |
| TELNET | Test for telnet connection to port 23 on address |
| UDP SIP | Test for UDP connection to specified port on address |
{: caption="Add-on monitoring service types" caption-side="bottom"}

## Viewing configured monitors
{: #view-configured-monitors}

To view configured monitors, use the following steps:
1. Go to your console's device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
2. From the **Devices** menu, select **Device List** and select the device.
3. Click the **Monitoring** tab. All current pings are viewable on the landing page.

The **Monitoring** tab is only visible if at least one monitor is configured.
{: note}

## Health dashboard for classic infrastructure
{: #health-dashboard}

With the health monitoring dashboard, you can see important stats about your environment that might need attention. From the health dashboard, you can quickly see the following information:

* All your devices and their associated monitoring statuses
* Quickly see any servers that might require firmware updates
* See whether any operating systems are no longer supported and if an OS reload is required 

### Viewing the health dashboard for classic infrastructure
{: #viewing-health-dashboard}

To view your health dashboard, use the following steps.

1. Log in to the [{{site.data.keyword.cloud}} console](/login){: external} and click the menu icon ![Menu icon](../icons/icon_hamburger.svg "Menu").
1. Click **Classic Infrastructure** ![Classic icon](../icons/classic.svg "Classic").
1. Click **Devices** > **Device list** > [**Health dashboard**](/gen1/infrastructure/health-dashboard){: external}.

For more information about operating system support cycles, see [Lifecycle for operating systems and add-ons](/docs/bare-metal?topic=bare-metal-product-lifecycle-classic).
{: tip}

## Next steps
{: #monitoring-next-steps}

For more information about monitoring your infrastructure and environments, see the following information.

* [Getting started with {{site.data.keyword.mon_full_notm}}](/docs/monitoring?topic=monitoring-getting-started).
* If you're ready to provision a monitoring instance, see [Provisioning an instance](/docs/monitoring?topic=monitoring-provision).
* If you're interested in monitoring plans and pricing, see [Pricing](/docs/monitoring?topic=monitoring-pricing_plans).
