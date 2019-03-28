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

# Designando endereços IP do servidor
{: #assigning-server-ip-addresses}

O {{site.data.keyword.cloud}} configura as instâncias do servidor virtual com um endereço de Protocolo da Internet versão 4 na rede privada e, se solicitado, um endereço de Protocolo da Internet versão 4 público (voltado para a Internet). Além disso, é possível solicitar um endereço de Protocolo da Internet versão 6 na rede pública. Todos esses endereços IP são coletivamente referidos como _Endereços IP primários_.
{:shortdesc}

Endereços IP adicionais podem ser ligados às instâncias de servidor virtual após a compra de sub-redes secundárias por meio do [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com). Endereços IP comprados dessa maneira e gerenciados por você são referidos como _Endereços IP secundários_.

Para obter mais informações sobre as opções disponíveis para a aquisição de endereços IP, consulte [Subnets e IPs](/docs/infrastructure/subnets?topic=subnets-getting-started-with-subnets-and-ips#getting-started-with-subnets-and-ips).

## Ligando endereços IP secundários

Depois que uma sub-rede secundária é comprada e roteada, deve-se configurar o sistema operacional para usar um ou mais dos endereços IP recém-disponíveis. As etapas de configuração para os novos endereços IP são diferentes para cada sistema operacional, mas a configuração geralmente é referida como uma configuração de "aliases de interface". Consulte a documentação do sistema operacional para obter os detalhes de configuração adicionais.
