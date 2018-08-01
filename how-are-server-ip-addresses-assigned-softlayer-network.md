---

copyright:
  years: 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Assigning server IP addresses

{{site.data.keyword.cloud}} configures servers with an IPv4 address on the
private network, and if requested, a public (internet facing) IPv4 address. Also
available is an IPv6 address on the public network, if requested. All of these
IP addresses are collectively referred to as **Primary IP Addresses**.

Additional IP addresses can be bound to servers after purchasing **Secondary
Subnets** through the [{{site.data.keyword.slportal_full}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com).
IP addresses purchased in this way and managed by you are referred to as
**Secondary IP Addresses**.

To learn more about the options available for acquiring IP addresses, please
review the documentation on
[Subnets and IPs](https://console.bluemix.net/docs/infrastructure/subnets/).


## Binding secondary IP addresses

Once a secondary subnet has been purchased and routed, it is necessary to
configure the operating system to use one or more of the newly available IP
addresses. Each operating system goes about this configuration differently, but
is typically referred to as setting up "interface aliases". See your operating system documentation for additional configuration details.
