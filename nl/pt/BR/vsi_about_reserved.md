---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-25"

keywords: reserved virtual servers, cost savings, guaranteed capacity 
subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Servidores virtuais reservados
{: #about-reserved-virtual-servers}

A oferta de instâncias reservadas do {{site.data.keyword.BluVirtServers}} é uma ótima opção se você deseja
recursos garantidos para implementações futuras e economia de custo. Você escolhe entre um prazo de contrato de um ou
três anos para a capacidade reservada. Dentro dessa capacidade reservada, é possível reservar um conjunto de até 20
instâncias de servidor virtual de um tamanho específico e fornecer essas instâncias quando precisar delas. Essa capacidade é garantida dentro do POD e do data center de sua escolha durante o prazo do contrato.

As instâncias de servidor virtual reservadas oferecem muitas vantagens, incluindo o seguinte:

* **Capacidade garantida**

    Ao reservar a capacidade, ela é garantida durante o prazo do contrato. 
    
* **Disponibilidade global**
    
    A oferta do servidor virtual reservado está disponível em data centers em todo o mundo.

* **Fornecimento confiável**
   
   É possível fornecer e recuperar as instâncias de servidor virtual para as capacidades reservadas a
qualquer momento.

* **Economia de custo**
    
    A escolha de um prazo de contrato de um ou três anos permite pagamentos mensais consistentes e custos
reduzidos em comparação com os ciclos de faturamento mensais ou por hora do servidor virtual.

Instâncias de servidor virtual reservadas são instâncias públicas que usam armazenamento suportado por SAN. As seguintes famílias de instâncias públicas estão disponíveis para essa oferta.

| Famílias  | Descrição                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Balanceado](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Melhor para cargas de trabalho de nuvem comuns que requerem um balanceamento de desempenho e escalabilidade. Usa armazenamento conectado à rede.|
| [Cálculo](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Melhor para cargas de trabalho de trafego da web moderado a alto.|
| [Memória](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Melhor para cargas de trabalho de armazenamento em cache de memória e de analítica em tempo real. |
{: caption="Tabela 1. Seleções de família do servidor virtual público" caption-side="top"}

## Limitações 

Considere as limitações a seguir antes de reservar a capacidade e fornecer as instâncias de servidor
virtual reservadas:
  
  * Não é possível fazer upgrade ou fazer downgrade das instâncias.
  * A capacidade reservada não pode ser cancelada; no entanto, é possível recuperar as instâncias de servidor
virtual nessa capacidade.
    
## Notificações

Você receberá uma notificação por e-mail um mês antes do término do prazo da capacidade do servidor virtual
reservada.

## Próximas Etapas

Depois de ter revisado e decidido as suas opções, é hora de fornecer a capacidade e as instâncias reservadas. Para iniciar, revise as informações a seguir:

   1. [Fornecendo a capacidade e as instâncias reservadas](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)
   2. [Perguntas frequentes: capacidade e instâncias reservadas](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances)
