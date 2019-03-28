---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:faq: data-hd-content-type='faq'}


# FAQs: hosts e instâncias dedicadas
{: #faqs-dedicated-hosts-and-instances}

## O que é um host dedicado?
{:faq}

Hosts dedicados do {{site.data.keyword.Bluemix}} são servidores físicos confirmados em um grupo de usuários. Os hosts dedicados oferecem a capacidade de fornecimento do servidor virtual e o controle de posicionamento máximo.

## Quais são os benefícios de usar os hosts dedicados sobre instâncias dedicadas?
{:faq}

Ambas as ofertas têm ocupação única garantida. Os hosts dedicados fornecem a flexibilidade para especificar em qual host provisionar instâncias de host dedicado, bem como:
   * Controle sobre qual data center do {{site.data.keyword.cloud}} o servidor é colocado
   * Capacidade para gerenciar seus servidores à medida que os requisitos de carga de trabalho mudam; por exemplo, migrar servidores virtuais entre os hosts dedicados no mesmo POD

## Posso manter minhas instâncias dedicadas existentes ou preciso configurar um host dedicado e instâncias de host dedicado?
{:faq}

Sim, é possível manter suas instâncias dedicadas existentes.

## Posso trocar o fornecimento de instâncias dedicadas (autodesignadas) e instâncias de host dedicado?
{:faq}

Não. As instâncias dedicadas autodesignadas existentes não podem ser reprovisionadas em hosts dedicados. Caso o posicionamento do servidor virtual seja requerido, será necessário provisioná-las em hosts dedicados como instâncias de host dedicado.

## Qual tipo de servidor, virtual ou bare metal, suporta a oferta de host dedicado?
{:faq}

A oferta é suportada em servidores virtuais; {{site.data.keyword.Bluemix_notm}} tem uma oferta bare metal. As diferenças entre hosts virtuais e servidores bare metal são o tempo para provisionar e o gerenciamento de virtualização.

## Qual é o ciclo de vida de fornecimento de um host dedicado?
{:faq}

Os hosts dedicados são alocados para usuários quando provisionados. Eles persistirão para a conta até que ela seja recuperada. Os hosts dedicados são oferecidos somente em precificação sob demanda, por hora ou mensal, portanto, quando recuperados, os modelos de faturamento cobrarão como ofertas do {{site.data.keyword.BluSoftlayer_full}} por hora ou mensais.

## Como esta oferta de host dedicado é faturada?
{:faq}

É possível comprar hosts dedicados sob demanda com o faturamento por hora ou mensal. Os hosts somente por hora permitem que somente instâncias por hora sejam provisionadas; os hosts somente mensais permitem provisionar instâncias mensais *e* por hora. A precificação para hosts dedicados inclui núcleo, RAM, armazenamento SSD local e velocidades de porta de rede. Os sistemas operacionais premium, o armazenamento da rede de área de armazenamento (SAN) e os preços e licenciamentos de complementos de software são cobrados com base na instância implementada — por hora ou mensal — no host dedicado. O mesmo modelo de precificação que instâncias públicas e dedicadas do {{site.data.keyword.Bluemix_notm}} é seguido para esses itens.

## Estou executando um host dedicado sob demanda; como eu sou faturado?
{:faq}

Você será faturado na taxa sob demanda por hora ou mensal para hosts dedicados. As instâncias de host dedicado provisionadas em hosts dedicados podem incorrer em encargos de instâncias como observado na resposta para **Como uma oferta de host dedicado é faturada**.

## Como a ocupação é especificada ao provisionar hosts dedicados e instâncias de host dedicado?
{:faq}

A ocupação padrão para instâncias dedicadas é um locatário único. Você terá a opção de provisionar instâncias dedicadas em um host dedicado (instâncias de host dedicado) ou um host designado automaticamente (instâncias dedicadas). As instâncias dedicadas em hosts designados automaticamente não oferecem o mesmo nível de gerenciamento que aquelas em um host dedicado.

## Posso combinar e corresponder diferentes configurações da instância de host dedicado no meu host dedicado?
{:faq}

Sim. É possível provisionar diferentes tamanhos de servidor virtual em hosts dedicados dentro de suas dotações de capacidade.

## Como eu sei quantas instâncias de host dedicado podem ser executadas em cada host dedicado?
{:faq}

Cada host dedicado tem uma dotação específica de núcleo, RAM e armazenamento SSD local. Você será capaz de visualizar as alocações de recursos na guia Alocações do host para saber quantas instâncias de host dedicado são provisionadas, a capacidade atual do host usada e o que está disponível.

## Quais imagens podem ser provisionadas em hosts dedicados?
{:faq}

É possível provisionar o banco de imagens do servidor virtual do {{site.data.keyword.Bluemix_notm}} ou importar suas próprias imagens, conforme indicado no contrato de terceiros.

## Há um limite de quantos hosts dedicados podem ser alocados para uma única conta?
{:faq}

Sim, as limitações de recursos são por conta, conforme definido para todos os recursos do {{site.data.keyword.BluSoftlayer_notm}} como Serviço. É possível ter múltiplos pedidos por conta, mas somente dois hosts dedicados por ordem de fornecimento.

## As implementações de host dedicado podem ser sobrecarregadas?
{:faq}

Não, é possível somente provisionar a capacidade listada em hosts dedicados.
