---

copyright:
  years: 2017, 2018
lastupdated: "2018-02-12"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Seleções de fornecimento
{: #provisioning-selections}

Você deverá fazer as seleções a seguir quando provisionar um servidor virtual público.

## Local
É possível selecionar o data center específico no qual você deseja implementar. Para novas implementações, o {{site.data.keyword.Bluemix}} identifica automaticamente o melhor data center (com base na disponibilidade) e cria as VLANs públicas e privadas apropriadas. Para adições a ambientes existentes, é possível selecionar o data center, a VLAN e a sub-rede específicos que são necessários para seu design. Para obter mais informações sobre VLANs e sub-redes, veja [Introdução às VLANs](/docs/infrastructure/vlans?topic=vlans-getting-started-with-vlans).

A seleção de uma sub-rede é opcional e só deverá ser usada quando você requerer que seu dispositivo use um endereço IP da sub-rede. Se você selecionar uma sub-rede, verifique se possui endereços IP suficientes para cumprir a solicitação. Se você não tiver endereços IP suficientes para sua sub-rede, seu pedido poderá atrasar ou ser cancelado.
{:tip}

## Processadores/RAM
Ao fazer a ordem, você tem opções de processador de núcleo entre as quais selecionar. As opções de processador de núcleo seguem padrões para implementações de servidor virtual. Cada núcleo físico no servidor é hyper-threading e apresentado como duas CPUs virtuais (vCPUs) ou núcleos. A oferta de servidor virtual fornece 2,0 GHz ou mais por núcleo com até 56 núcleos disponíveis em um único servidor virtual.

A RAM é muito simples. A oferta dedica totalmente a quantia de RAM que você seleciona a seu servidor virtual, com até 242 GB em um único servidor virtual.

**Nota:** as instâncias pública e dedicada têm máximos de configuração um pouco diferentes. As alocações muito altas de núcleos ou memória limitam as opções disponíveis.

## Sistema operacional

Você também seleciona o sistema operacional a ser implementado no servidor. É possível selecionar várias opções grátis, como CentOS e Ubuntu. As opções pagas, como Windows Server e Red Hat Enterprise Linux (RHEL), também estão disponíveis. É importante observar que o Windows requer um disco primário de 100 GB.

Para clientes existentes, também é possível implementar com base em um Modelo de Imagem por meio do {{site.data.keyword.slportal_full}} navegando para **Dispositivos-> Gerenciar-> Imagens** e selecionando **Pedir Virtual Server** no menu *Ações*.  Isso seleciona automaticamente o sistema operacional apropriado para a ordem.  Como alternativa, é possível pedir com base em uma imagem padrão e, em seguida, recarregar em um modelo de imagem a qualquer momento.

## Armazenamento

Você tem a opção para SAN ou armazenamento local para cada servidor virtual. É possível complementar a SAN ou o armazenamento local com outros produtos de armazenamento conforme necessário. O SAN e o armazenamento local são expostos ao servidor virtual como discos locais. Quaisquer mudanças nos discos, como conectar, remover, migrar e assim por diante, requerem uma reinicialização do servidor virtual. Para obter mais informações, consulte [Opções de Armazenamento](/docs/vsi?topic=virtual-servers-storage-options#storage-options).

## Faturamento por hora e mensal

É possível selecionar o faturamento por hora ou mensal para um servidor virtual. A diferença primária, além de custo, é que os servidores por hora não têm uma alocação de largura da banda incluída. No término de um período de faturamento, o uso da largura da banda e o número de horas que cada servidor ficou ativo na conta são calculados. Um total de execução está disponível no {{site.data.keyword.slportal}} sob a página Visualização do Virtual Server com um link para uma página Detalhes, mostrando cada item de linha, número de horas e encargos de execução por item.

## Largura de Banda

A oferta inclui 250 GB com servidores virtuais mensais que possuem um link público. É possível comprar alocações maiores a um custo reduzido em comparação com a taxa excedente.

## Velocidade da porta

É possível selecionar a velocidade de uplink para o servidor virtual, até 1 GB/s. Esses uplinks virtuais são auxiliados por uplinks físicos redundantes para as redes pública e dedicada IBM. A velocidade pública e dedicada é sempre a mesma no momento da ordem, com a opção de fazer upgrade ou downgrade de um link se necessário.

## Software

É possível selecionar o software a ser instalado pelo {{site.data.keyword.Bluemix_notm}} durante o processo de fornecimento. O {{site.data.keyword.Bluemix_notm}} fornece suporte para qualquer software implementado durante o processo de fornecimento. É possível também instalar o seu próprio software depois que o servidor for implementado.

## Segurança

Antes da implementação, considere suas opções de segurança. Como parte do processo de ordem, é possível selecionar um hardware específico do dispositivo ou um firewall de software para fornecer proteção. Como alternativa, é possível implementar dispositivos de firewall dedicados no ambiente e implementar o servidor virtual em uma VLAN protegida.

**Nota:** um servidor virtual não pode ser protegido por dois dispositivos de firewall na mesma interface.

Também é possível usar grupos de segurança para determinar um conjunto de regras de filtro de IP que definem como manipular o tráfego de entrada e de saída para as interfaces pública e privada de uma instância de servidor virtual.

Para obter mais informações, veja as coleções de tópicos de segurança a seguir.

* [Hardware Firewalls (Shared)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-getting-started-with-hardware-firewall-shared)
* [Hardware Firewalls (Dedicated)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-getting-started-with-hardware-firewall-dedicated)
* [Introdução aos grupos de segurança](/docs/infrastructure/security-groups?topic=security-groups-getting-started-with-security-groups)

## Monitoramento
{: #about-monitoring}

É possível selecionar entre uma variedade de opções de monitoramento para o servidor virtual. As opções incluem o monitoramento padrão, que monitora via Ping e resposta de serviço do protocolo de controle de transmissão (TCP) e tem respostas opcionais no caso de falhas. É possível também incluir o Advanced Monitoring que usa o agente de software Nimsoft para fornecer um conjunto maior de recursos para monitoramento do servidor virtual e do software instalado.

Para obter mais informações, veja [Monitoramento](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring).

## Backup

Durante o processo de pedido, é possível incluir o {{site.data.keyword.backup_notm}}. Também é possível escolher comprar uma licença R1soft para o ambiente de backup R1soft existente ou utilizar uma solução de backup de terceiros.

Para obter mais informações, consulte [Registrando novamente uma área segura](/docs/infrastructure/Backup?topic=Backup-reregister#reregister).

## Scripts de pós-fornecimento

Os scripts de pós-fornecimento podem ser associados a qualquer ordem de servidor virtual. Isso executa um script desenvolvido pelo cliente após outras tarefas de fornecimento serem concluídas. Os scripts são comumente utilizados para aplicar uma configuração específica do cliente a um servidor e ajudar na automação de sua estratégia de ajuste de escala.

Para obter mais informações, veja [Incluindo um script de fornecimento customizado](/docs/vsi?topic=virtual-servers-adding-post-script).

## O que vem a seguir?
Quando você estiver pronto para provisionar seu servidor virtual público, veja [Provisionando instâncias públicas](/docs/vsi?topic=virtual-servers-ordering-vs-public).
