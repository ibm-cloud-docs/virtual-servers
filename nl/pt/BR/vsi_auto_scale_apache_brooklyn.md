---

copyright:
  years: 2014, 2019
lastupdated: "2019-02-06"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Escala automática com o Apache Brooklyn
{: #auto-scale-with-apache-brooklyn}

## Introdução

Uma empresa que fornece dados críticos do consumidor diariamente para mais de um bilhão de usuários móveis nos pediu para fornecer funcionalidade para criar grupos de auto-scaling de servidores que estão em uma rede privada. Um requisito chave foi a elasticidade, em que, com base nas demandas de carga de trabalho e de tempo de resposta de experiência do usuário, sistemas aumentam e reduzem automaticamente a escala com base em políticas predeterminadas.

O ajuste de escala automático é baseado no uso da CPU. Se o uso médio de CPU dos servidores em um grupo for maior do que o limite mais alto ou o evento acionador, mais recursos precisarão ser provisionados ou terem a capacidade aumentada. Se o uso médio da CPU dos servidores em um grupo for menor do que o limite mais baixo ou o evento acionador, os recursos precisarão ser reduzidos. O cliente tinha os requisitos a seguir:

1. Capacidade de especificar os parâmetros a seguir:
  * Número inicial de servidores no grupo
  * Número mínimo e máximo de servidores no grupo
  * Limites alto e baixo de CPU
  * Número de servidores adicionais para aumentar e reduzir a escala em um evento acionador
2. Integrar o Sistema de Nomes de Domínio (DNS)
  * Após um servidor no grupo ser provisionado ou ter a capacidade aumentada e disponibilizado, um registro do DNS apropriado deverá ser criado para ele.
  * Quando o servidor é reduzido, o registro de DNS para ele deve ser removido.
3. Integrar um balanceador de carga
  * Após um servidor no grupo ser provisionado, ou ter a escala aumentada e disponibilizado, o registro do servidor deve ser incluído no balanceador de carga NetScaler apropriado e ligado ao grupo de balanceamento de carga apropriado.
  * Quando o servidor é reduzido, ele deve ser desvinculado do grupo de balanceamento de carga e o registro do servidor deve ser removido do NetScaler.
4. Integrar o Chef
  * Após um servidor no grupo ser provisionado, ou ter a escala aumentada e disponibilizado, o cliente Chef deve executar e registrar o nó no servidor Chef.
  * Quando o servidor tem a escala reduzida, o nó de servidor e o registro do cliente devem ser removidos do servidor Chef.
5. Requisitos de fornecimento do servidor
  * Todos os servidores no grupo devem ser provisionados como máquinas virtuais (VMs) com uplinks somente privados, velocidade da porta de 1.000 Mbps e uma VLAN privada especificada.
  * As VMs devem ser provisionadas por meio do modelo padrão de vários discos, criados pelo cliente no {{site.data.keyword.cloud}}.
6. Sistema operacional
  * CentOS 7.

Baseado nos requisitos do cliente, o Apache Brooklyn foi selecionado como a ferramenta de ajuste automático de escala para implementar a solução.

## Visão geral do Apache Brooklyn

O Apache Brooklyn é uma estrutura para modelagem, monitoramento e gerenciamento de aplicativos por meio de blueprints autônomos. Para obter mais informações, consulte o site [Apache Brooklyn ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo") ](https://brooklyn.incubator.apache.org/){: new_window}.

### Conceitos do Apache Brooklyn

A documentação do Apache Brooklyn fornece definições dos conceitos do Apache Brooklyn como

* Entidades
* Aplicativo
* Configuração de pai e associação
* Sensores e efetores
* Contexto de ciclo de vida e gerenciamento
* Configuração dependente
* Local, políticas
* Execução
* Implementação

### Integrando o DNS, o NetScaler e o Chef

O Apache Brooklyn fornece uma classe base para customizar local, `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`, que contém métodos que permitem a criação de parâmetros adicionais quando as máquinas são provisionadas. As ações podem ser executadas depois que uma máquina é provisionada e antes e depois de ela ter sido liberada quando cancelada.

Nós criamos nossa própria classe do customizador de local que estendeu o `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer` fornecido pelo Brooklyn. Para esse exemplo, refira-se a ele como `brooklyn.location.jclouds.ProjectJcloudsLocationCustomizer`.

Os três métodos a seguir foram substituídos:

1. `public void customize(JcloudsLocation location, ComputeService computeService, TemplateOptions templateOptions)` - O método é iniciado antes de chamar a API da nuvem para provisionar um servidor. Nós ativamos a capacidade de fornecer as propriedades de fornecimento como `privateNetworkOnly, primaryBackendNetworkComponentVlanId, portSpeed,` e outras.

* `public void customize(JcloudsLocation location, ComputeService computeService, JcloudsSshMachineLocation machine)` - O método é iniciado após uma máquina ser provisionada e iniciada, portanto, todos os parâmetros do servidor, como endereço IP do servidor, estão disponíveis. O código para incluir um servidor no DNS e o balanceador de carga devem ser colocados nesse método. O DNS e a API de REST do NetScaler são usados para criar os registros DNS e ligar o servidor ao NetScaler. Nós usamos um pacote fornecido por `Brooklyn, brooklyn.util.http`, para enviar chamadas de REST para APIs do DNS e do NetScaler.

* `public void preRelease(JcloudsSshMachineLocation machine)` - O método é iniciado no cancelamento da máquina antes de o servidor ser interrompido. Incluímos chamadas REST para o DNS e o NetScaler aqui para remover os registros de DNS e NetScaler e desvincular o servidor do grupo do NetScaler.

Nós não fizemos nada específico para conectar o novo servidor ao Chef. A imagem, que foi usada para provisionar o servidor, tinha um cliente Chef instalado nela e o script de inicialização (o script executa o cliente Chef e o conecta ao servidor Chef). Se você preferir, será possível usar a integração do Brooklyn com o Chef para criar blueprints.

Também incluímos uma chamada REST para o servidor Chef para remover registros do cliente e do nó apropriados.

### Blueprint do aplicativo

Dentro do blueprint do aplicativo, nós customizamos o local, os parâmetros de coleta de métrica e as propriedades de ajuste automático de escala dos servidores. Os comandos a seguir são usados para customizar cada componente.

    name: Group1
    location:

      jclouds:softlayer:tor01:
      customizerType: brooklyn.location.jclouds.ProjectJcloudLocationCustomizer
      privateNetworkOnly: true
      primaryBackendNetworkComponentVlanId: 12345
      portSpeed: 1000
      imageId: 123456
      dnsZoneId: 12345
      netscalerGroup: app1
      netscalerGroupPort: 8080
      netscalerUrl: http://user:password@10.10.10.10/nitro/v1/

    services:
    - type: brooklyn.entity.group.DynamicCluster
      id: cluster
      name: dynamic cluster
      initialSize: 1
      memberSpec:
        $brooklyn:entitySpec:
        name: VMinSL
        type: brooklyn.entity.basic.EmptySoftwareProcess
        brooklyn.initializers:
        - type: brooklyn.entity.software.ssh.SshCommandSensor brooklyn.config: name: server.cpucount command: "LANG=en_US.UTF-8 sar -u 1 1|grep Average | awk '{print 100 - $8}'"
            targetType: java.lang.Double period: 10s brooklyn.config: post.launch.command: "sudo apt-get install -y sysstat"

      brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $brooklyn:sensor("server.cpucount")
          enricher.targetSensor: $brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average
        brooklyn.policies:
        - policyType: brooklyn.policy.autoscaling.AutoScalerPolicy
        brooklyn.config:
          metric: $brooklyn:sensor("server.cpucount.averaged")
          metricLowerBound: 10
          metricUpperBound: 60
          minPoolSize: 1
          maxPoolSize: 5

### Local

Na seção de local do blueprint, especificamos as propriedades de fornecimento, como

* Onde o servidor deve ser provisionado (data center e VLAN)
* Se o servidor será provisionado com privateNetworkOnly
* Um ID da imagem do modelo {{site.data.keyword.cloud_notm}} padrão ou imagem flex,
* Velocidade da porta

Também especificamos o ID da zona de DNS, que é usado pelo `ProjectJcloudLocationCustomizer` para incluir e excluir registros na zona DNS e informações do NetScaler para ligar e desvincular o servidor do NetScaler.

    local:

      jclouds:softlayer:tor01:
        customizerType: brooklyn.location.jclouds.ProjectJcloudLocationCustomizer
        privateNetworkOnly: true
        primaryBackendNetworkComponentVlanId: 12345
        portSpeed: 1000
        dnsZoneId: 12345
        netscalerGroup: app1
        netscalerGroupPort: 8080
        netscalerUrl: http://user:password@10.10.10.10/nitro/v1/

### Serviços

Na seção Serviços do blueprint, nós especificamos

* Que estávamos implementando um grupo de servidores
* Qual Brooklyn deveria ser instalado em cada servidor
* Como as métricas de CPU deveriam ser coletadas e usadas
* Os parâmetros da política de ajuste automático de escala

#### Especificação do aplicativo

    services:
    - type: brooklyn.entity.group.DynamicCluster #group of servers
      id: cluster
      name: dynamic cluster
      initialSize: 1 #number of servers initially created in the group

#### Especificação do membro

A chamada de `brooklyn.entity.basic.EmptySoftwareProcess` foi usada porque o Apache Brooklyn precisa apenas provisionar servidores de uma imagem e nenhuma instalação ou configuração adicional é necessária. Essa seção também especificou um a sensor - server.cpucount – que coleta periodicamente a utilização da CPU do servidor.

    memberSpec:
      $brooklyn:entitySpec:
      name: VMinSL
      type: brooklyn.entity.basic.EmptySoftwareProcess
      brooklyn.initializers:
      - type: brooklyn.entity.software.ssh.SshCommandSensor
        brooklyn.config:
          name: server.cpucount
          command: "LANG=en_US.UTF-8 sar -u 1 1|grep Average | awk '{print 100 - $8}'"
          targetType: java.lang.Double
          period: 10s
      brooklyn.config:
        post.launch.command: "sudo apt-get install -y sysstat"

### Métricas

Na seção Métricas do blueprint, as métricas de servidores individuais são coletadas e a média é designada ao sensor de nível do cluster.

    brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $me0$brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average

### Políticas de ajuste automático de escala

Nessa seção, as propriedades de política de ajuste automático de escala são definidas:

    brooklyn.policies:
    - policyType: brooklyn.policy.autoscaling.AutoScalerPolicy
      brooklyn.config:
        metric: $brooklyn:sensor("server.cpucount.averaged")
        metricLowerBound: 10
        metricUpperBound: 60
        minPoolSize: 1
        maxPoolSize: 5
        minPeriodBetweenExecs: 10m
        resizeUpIterationIncrement: 2
        resizeUpIterationMax: 2
        resizeDownIterationIncrement: 2
        resizeDownIterationMax: 2

Assim que a solução foi implementada, os usuários conseguiram aumentar facilmente a capacidade da escala automática e diminuir seus aplicativos em tempo hábil, registrando e cancelando os registros do sistema com servidores de balanceamento de carga, DNS e Chef.
