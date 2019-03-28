---

copyright:
  years: 2018
lastupdated: "2018-08-01"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Affectation d'adresses IP de serveur
{: #assigning-server-ip-addresses}

{{site.data.keyword.cloud}} configure les instances de serveur virtuel avec une adresse IPv4 sur le réseau privé, et à la demande, une adresse IPv4 publique (face à Internet). De plus, vous pouvez demander une adresse IPv6 sur le réseau public. Toutes ces adresses IP sont collectivement appelées _adresses IP primaires_.
{:shortdesc}

Des adresses IP supplémentaires peuvent être liées à des instances de serveur virtuel après l'achat de sous-réseaux secondaires via le [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com). Les adresses IP ainsi achetées et gérées par vous sont appelées _adresses IP secondaires_.

Pour en savoir plus sur les options disponibles pour acquérir des adresses IP, voir [Sous-réseaux et IP](/docs/infrastructure/subnets?topic=subnets-getting-started-with-subnets-and-ips#getting-started-with-subnets-and-ips).

## Liaisons d'adresses IP secondaires

Après l'achat et le routage d'un sous-réseau secondaire, vous devez configurer le système d'exploitation pour utiliser la ou les nouvelles adresses IP disponibles. Les étapes de configuration des nouvelles adresses IP sont différentes dans chaque système d'exploitation, mais la configuration est généralement connue comme celle des "alias d'interface". Consultez la documentation de votre système d'exploitation pour obtenir plus de détails sur la configuration.
