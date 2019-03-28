---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Hosts dedicados e instâncias dedicadas
{: #dedicated-hosts-and-dedicated-instances}

Hosts dedicados são servidores virtuais que permitem especificar o data center e o POD no qual você deseja que o seu host seja colocado. Em seguida, você designa instâncias ou máquinas virtuais para um host específico para obter controle máximo sobre o posicionamento de carga de trabalho e para obter opções flexíveis de provisionamento de custos.
{:shortdesc}

## Capacidade garantida
Você tem capacidade garantida dentro do data center e POD no qual o host é colocado. Por exemplo, se o POD que contém seu host dedicado e instâncias dedicadas atingir a capacidade, será possível continuar a designar instâncias dedicadas ao seu host se ele tiver espaço apropriado.

## Cargas de trabalho visíveis
É possível visualizar o consumo de recursos geral para todas as instâncias dedicadas designadas a um host dedicado em uma página. Visualizar núcleo, RAM e uso de armazenamento local, o que ajuda a determinar se você precisa migrar instâncias dedicadas para outro host dedicado. Esse nível de granularidade fornece a capacidade de gerenciar as cargas de trabalho com o controle máximo.

## Gerenciamento pós-implementação
Além da capacidade garantida e visibilidade para suas cargas de trabalho, é possível migrar suas instâncias dedicadas entre hosts dedicados para o controle máximo sobre o posicionamento de carga de trabalho.

## Manutenção
Ocasionalmente, a manutenção de infraestrutura requer um host dedicado para reiniciar. Por exemplo, o hypervisor Xen pode precisar de uma atualização. Se você tiver vários hosts dedicados, você terá as opções a seguir para minimizar o tempo de inatividade de manutenção.
* A manutenção é feita por PODs em um data center. É possível implementar seus hosts dedicados em PODs separados para difundir a manutenção necessária.
* É possível criar um chamado de suporte para um host dedicado para solicitar que uma manutenção planejada seja atrasada. Durante esse tempo, é possível migrar instâncias dedicadas (off-line) entre hosts dedicados no mesmo POD.

## Alta disponibilidade
Se um host dedicado falhar, as cargas de trabalho no host dedicado serão migradas automaticamente para um novo host dedicado. As instâncias dedicadas permanecem dedicadas em todo o ciclo de vida do servidor virtual.

Para cenários de alta disponibilidade, talvez seja considerado ter um host dedicado extra designado. Por exemplo, o host dedicado adicional fornece a flexibilidade para migrar cargas de trabalho para janelas de manutenção.
