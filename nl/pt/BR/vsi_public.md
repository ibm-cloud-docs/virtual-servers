---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Servidores virtuais públicos
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
dedicado é recomendado. Para obter mais informações, consulte a oferta
[Servidor virtual dedicado](../vsi/vsi_dedicated.html) com ambiente de único locatário.

As instâncias públicas residem em um hypervisor que é compartilhado com outros clientes; no entanto, os processadores e a memória são dedicados ao servidor virtual, tornando o desempenho do servidor confiável. 

Os servidores virtuais públicos a seguir estão disponíveis. 

| Servidores virtuais públicos  | Descrição                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Balanceado](../vsi/vsi_public_balanced.html) | Melhor para cargas de trabalho de nuvem comuns que requerem um balanceamento de desempenho e escalabilidade. Usa armazenamento conectado à rede.|
| [Armazenamento local balanceado](../vsi/vsi_public_balanced_local.html) | Melhor para clusters de banco de dados grandes que requerem desempenho de E/S alto e de baixa latência.|
| [Cálculo](../vsi/vsi_public_compute.html) | Melhor para cargas de trabalho de trafego da web moderado a alto.|
| [Memória](../vsi/vsi_public_memory.html)  | Melhor para cargas de trabalho de armazenamento em cache de memória e de analítica em tempo real.
| [GPU](../vsi/vsi_public_gpu.html)  | Melhor para cargas de trabalho de alto desempenho.
{: caption="Tabela 1. Servidores virtuais públicos suportados" caption-side="top"}

## Próximas Etapas

Depois de revisar e decidir sobre o tipo de servidor virtual, é hora de provisionar seu servidor virtual público. Para iniciar, revise as informações a seguir: 
1. [Seleções de fornecimento](../vsi/vsi_public_selections.html)
2. [Provisionando instâncias públicas](../vsi/vsi_provision_public.html)
