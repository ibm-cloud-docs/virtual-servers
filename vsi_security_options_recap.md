---

copyright:
  years: 2025
lastupdated: "2025-08-20"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Security options for {{site.data.keyword.BluVirtServers_short}} for Classic
{: #security-options}

With {{site.data.keyword.BluVirtServers}} for Classic, you have several security options that you can take advantage of including firewalls, security groups, SSL certificates, and SSH keys.
{: shortdesc}


## Firewalls
{: #firewalls-overview}

With {{site.data.keyword.BluVirtServers}}, you have several firewall options that provide an essential security layer. The firewall options are provisioned on demand, without service interruptions. The firewall services prevent unwanted traffic from reaching your servers, reducing the likelihood of an attack, and by allowing your server resources to be dedicated for their intended use.

Firewalls are available as an add-on feature for all servers on the infrastructure public network.

As part of the ordering process, you can select device-specific hardware or a software firewall to provide protection. Alternatively, you can deploy dedicated firewall appliances to the environment and deploy the virtual server to a protected VLAN.

You can't protect a virtual server with two firewall appliances on the same interface.
{: note}

For more information, see [Hardware firewalls (Shared)](/docs/hardware-firewall-shared?topic=hardware-firewall-shared-getting-started).


## Security groups
{: #security-groups-overview}

With security groups for {{site.data.keyword.BluVirtServers}}, you can enact a set of IP filter rules that define how to handle incoming and
outgoing traffic to both the public and private interfaces of a virtual server. A security group creates a type of virtual firewall.

For more information about security groups, see [Getting started with security groups](/docs/security-groups?topic=security-groups-getting-started).

## SSL certificates
{: #ssl-certificates-overview}

SSL Certificate Order is deprecated. As of 15 April 2024, the SSL Certificate Order is no longer available for purchase. As of 15 December 2024, SSL Certificate Order is no longer supported for new orders or reorders. Only existing certificates that are not expired are still available for you to download, reissue, or revoke. For more information, see [Deprecation of SSL Certificates](/docs/ssl-certificates?topic=ssl-certificates-deprecation). {: deprecated}

Secure Sockets Layer (SSL) is a technology that encrypts traffic between the client application and the server application that is involved in the conversation. This encryption is accomplished through a public key or private key system by using an SSL certificate.

The SSL certificate contains the server’s public key, dates for the valid certificate, a hostname for the valid certificate is valid, and a signature from the certificate-issuing authority. With this information and some protocol information from the beginning of a session, you can be reasonably certain that the server is the one to which it is intending to talk.


## SSH keys
{: #ssh-keys-overview}

Secure Socket Shell (SSH) is a network protocol that enables a user or client computer to connect, through a secure channel, to a remote computer over the internet and have access to issue commands on the remote computer.

SSH keys are the public-key credentials that are used by the SSH protocol for authentication and encryption.

For more information about SSH keys, see [Getting started with SSH keys](/docs/ssh-keys?topic=ssh-keys-getting-started-tutorial).
