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

# Gerenciando hosts e instâncias dedicadas
{: #managing-virtual-servers}

A página Detalhes do Dispositivo é onde você gerencia seu host dedicado e instâncias, rastreia seus chamados de suporte e monitora a disponibilidade de seu host. É possível acessar e visualizar suas instâncias de host dedicado de duas maneiras na Lista de dispositivos, como parte do seu host ou como uma instância individual.
{:shortdesc}

## Guia Configuração de host
É possível executar várias tarefas na guia **Configuração** para o host dedicado, incluindo gerenciar suas instâncias de host dedicado. No menu suspenso Ações, é possível renomear o host ou cancelá-lo. Todas as instâncias de host dedicado designadas devem ser canceladas ou migradas primeiro antes que um host possa ser cancelado, caso contrário, uma mensagem de erro será recebida.

Notas podem ser mantidas no host e em suas instâncias; por exemplo, a migração de myDallasHost para myTorHost está planejada para XX/XX/XXXX. Os quadros Geral, Sistema e Rede da página fornecem detalhes em uma visão rápida sobre o host. Observe que o quadro Armazenamento refere-se à capacidade de armazenamento local.

O quadro Instâncias contém as instâncias designadas a um host específico, bem como a capacidade de incluir instâncias no host. Clique no menu Ações para que uma instância faça o seguinte nele:

* Reinicalização
* Ligar e desligar
* Renomear
*	Visualizar logs de auditoria
*	Fazer upgrade ou downgrade
*	Cancelar
*	Migrar

## Guia Chamados do host
Use a guia Chamados para abrir chamados de suporte para o host e qualquer uma de suas instâncias, clicando em Incluir um chamado para esse link de Dispositivo.

## Guia Alocações do host
A guia Alocações permite visualizar núcleos disponíveis, RAM e armazenamento local para seu host dedicado. A fatia azul da "pizza" representa o que está em uso e a fatia branca é o que está disponível.

## Guia da instância do host dedicado
A página Detalhes do dispositivo da instância do host dedicado pode ser atingida por meio da página Detalhes do dispositivo de seu host ou diretamente na Lista de dispositivos. Há mais guias no nível de instância do host dedicado; Configuração e Chamados são semelhantes às guias localizadas no nível do host. O link Modificar Configuração do Dispositivo, na guia Configuração, permite fazer mudanças em sua configuração de sistema (núcleo, RAM e armazenamento local) e de rede (largura da banda e velocidades da porta de uplink).

O uso exibe um gráfico de plot de tempo com base no uso de CPU por data. É possível rolar o gráfico para ver o uso de CPU para uma data e hora específica, que é útil ao tentar determinar se você precisa incluir capacidade de processamento.

Largura da banda é outro gráfico de plot de tempo que permite inserir parâmetros para ver a quantia de largura da banda que está sendo usada ao longo do tempo. A guia Armazenamento exibe qualquer armazenamento de bloco ou arquivo adicional na instância.

# Cancelar um host dedicado
É possível cancelar um host dedicado a qualquer momento. Um pré-requisito para cancelar um host é ter migrado as instâncias dedicadas designadas a ele para outro host dedicado ou ter cancelado as instâncias também. 
## Cancelar um host dedicado da Lista de dispositivos
Use as etapas a seguir para cancelar um host dedicado na Lista de dispositivos.

1. Selecione **Dispositivo** > **Lista de dispositivos**.
2. Localize o host dedicado a ser cancelado e clique no menu suspenso **Ações**.
3. Selecione **Cancelar host**. 
4. Uma janela pop-up contendo uma lista de instâncias dedicadas designadas ao host aparecerá. Você precisará migrar ou cancelar as instâncias, caso ainda não tenha feito isso, antes de cancelar o host. Clique em **OK**.

Você receberá uma mensagem de que o host dedicado foi cancelado. Haverá um link para o chamado de suporte para cancelar o host dedicado.
## Cancelar um host dedicado na página Detalhes do dispositivo
Use as etapas a seguir para cancelar o host dedicado na página Detalhes do dispositivo.

1. Selecione **Dispositivo** > **Lista de dispositivos**.
2. Localize o host dedicado a ser cancelado e clique duas vezes nele.
3. Verifique se todas as instâncias dedicadas designadas ao host dedicado foram migradas ou canceladas.
4. Clique no menu suspenso **Ações** e selecione **Cancelar host**.

Você receberá uma mensagem de que o host dedicado foi cancelado. Haverá um link para o chamado de suporte para cancelar o host dedicado.

### Cancelar uma instância dedicada

Antes de poder cancelar um host dedicado, as instâncias dedicadas designadas a ele devem ser canceladas. Instâncias dedicadas podem ser canceladas diretamente na Lista de Dispositivos, na página Detalhes do Dispositivo de seu host designado ou em sua própria página Detalhes do Dispositivo. 

1. Selecione a instância dedicada a ser cancelada e clique no menu suspenso **Ações**.
2. Selecione **Cancelar dispositivo**.
3. Uma mensagem de aviso aparecerá. Clique no menu suspenso **Razão** e selecione a razão pela qual você está cancelando a instância dedicada e clique em **Continuar**.

Você receberá uma mensagem de que a instância dedicada foi cancelada. Haverá um link para o chamado de suporte para cancelar a instância dedicada.

