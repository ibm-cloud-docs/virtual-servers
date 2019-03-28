---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

keywords: public virtual servers, network traffic, virtual server deployment

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Sobre servidores virtuais públicos
{: #about-public-virtual-servers}

As ofertas de {{site.data.keyword.BluVirtServers}} são implementações de servidores virtuais de diversos locatários gerenciados pela IBM. Elas fornecem escalabilidade rápida e eficácia de custo mais alto com tamanhos predefinidos que atendem todos os requisitos de negócios para colocar rapidamente em funcionamento.  
{:shortdesc}

Os servidores virtuais públicos têm muitas vantagens, incluindo as seguintes:

* **Disponibilidade global**

    A oferta de servidor virtual público está disponível em data centers ao redor do globo.

* **Opções de configuração, implementação rápida e escalabilidade**

    A oferta de servidor virtual público fornece opções de servidor virtual pequeno ou grande para atender a vários requisitos de carga de trabalho.

O tráfego de rede para os servidores virtuais públicos, que engloba a SAN da VSI e outro armazenamento conectado à
rede, não tem garantia. Se o tráfego de rede de uma instância de servidor virtual começar a ter um impacto
negativo significativo em outros servidores virtuais, essa instância poderá ser reiniciada em um novo host ou, em casos
extremos, desativada completamente. Esse impacto negativo é frequentemente observado à medida que os níveis de tráfego
se aproximam de 20 mil a 30 mil pacotes por segundo (PPS).  Para uma rede garantida, o uso da oferta Virtual Server
dedicado é recomendado. Para obter mais informações, consulte o ambiente de locatário único, a oferta [Servidor virtual dedicado](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers).

As instâncias públicas residem em um hypervisor que é compartilhado com outros clientes; no entanto, os processadores e a memória são dedicados ao servidor virtual, tornando o desempenho do servidor confiável.

Os servidores virtuais públicos a seguir estão disponíveis.

| Servidores virtuais públicos  | Descrição                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- |
| [Balanceado](/docs/vsi?topic=virtual-servers-balanced#balanced) | Melhor para cargas de trabalho de nuvem comuns que requerem um balanceamento de desempenho e escalabilidade. Usa armazenamento conectado à rede.|
| [Armazenamento local balanceado](/docs/vsi?topic=virtual-servers-balanced-local-storage#balanced-local-storage) | Melhor para clusters de banco de dados grandes que requerem desempenho de E/S alto e de baixa latência.|
| [Cálculo](/docs/vsi?topic=virtual-servers-compute#compute) | Melhor para cargas de trabalho de trafego da web moderado a alto.|
| [Memória](/docs/vsi?topic=virtual-servers-memory#memory)  | Melhor para cargas de trabalho de armazenamento em cache de memória e de analítica em tempo real. |
| [GPU](/docs/vsi?topic=virtual-servers-gpu#gpu)  | Melhor para cargas de trabalho de alto desempenho.
{: caption="Tabela 1. Servidores virtuais públicos suportados" caption-side="top"}

Algumas dessas famílias também estão disponíveis para o IBM Cloud Virtual Servers for VPC. Para obter mais informações, consulte [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen).
{:tip}

## Próximas Etapas

Depois de revisar e decidir sobre o tipo de servidor virtual, é hora de provisionar seu servidor virtual público. Para iniciar, revise as informações a seguir:
1. [Seleções de fornecimento](/docs/vsi?topic=virtual-servers-provisioning-selections)
2. [Provisionando instâncias públicas](/docs/vsi?topic=virtual-servers-ordering-vs-public)
