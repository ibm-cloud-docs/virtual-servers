---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Introdução aos servidores virtuais
É possível implementar {{site.data.keyword.BluVirtServers}} em uma questão de minutos. Os servidores virtuais são implementados por meio de sua escolha de imagens do servidor virtual e na região geográfica que faz sentido para suas cargas de trabalho.
{:shortdesc}

Ao criar um servidor virtual, é possível escolher entre um ambiente público (ocupação variada) ou um ambiente dedicado (ocupação única). Em seguida, dependendo do ambiente escolhido, deve-se também selecionar servidores virtuais horários, mensais ou temporários. No caso de servidores virtuais públicos, você também escolhe usar o armazenamento baseado na SAN ou o armazenamento local.

## Antes de iniciar

Antes de iniciar, revise os pré-requisitos a seguir.

  1. Deve-se ter uma conta com upgrade para pedir servidores virtuais. Esse processo pode levar algum tempo e requer que sua solicitação seja aprovada antes de poder continuar. Para obter mais informações sobre como fazer upgrade de sua conta, veja [Alternando para o IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).
  2. Revise e escolha suas opções de implementação. Para obter informações adicionais, consulte os
seguintes tópicos:

|              Opções de implementação                           |  Descrição                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Servidor virtual público](../vsi/vsi_public.html)            | Implementações de servidor virtual de ocupação variada gerenciadas pela IBM|
|[Servidor virtual temporário](../vsi/vsi_about_transient.html)| Implementações de servidor virtual de ocupação variada gerenciadas pela IBM oferecidas a um custo reduzido e mais adequadas para cargas de trabalho flexíveis |
|[Servidor virtual dedicado](../vsi/vsi_dedicated.html)      | Implementações de servidor virtual de ocupação única gerenciadas pela IBM            |
{: caption="Tabela 1. Opções de implementação" caption-side="top"}   

## Provisionando um servidor virtual

Depois de decidir sobre uma opção de implementação, inicie o processo de fornecimento.

|              Instruções de fornecimento                                         |  Descrição                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisionando instâncias públicas](../vsi/vsi_provision_public.html)                | Provisione instâncias públicas com várias opções             |
|[Provisionando instâncias temporárias](../vsi/vsi_provision_transient.html)                | Provisione instâncias temporárias com várias opções            |
|[Provisionando hosts e instâncias dedicadas](../vsi/vsi_provision_dedicated.html)| Provisione instâncias privadas ou instâncias dedicadas em hosts dedicados.|
{: caption="Tabela 2. Provisionando informações" caption-side="top"}

## Próximas Etapas

Depois que seu servidor virtual for provisionado e estiver disponível para uso, será possível configurar os servidores virtuais usando
o {{site.data.keyword.slportal_full}} ou o {{site.data.keyword.slapi_full}}. Para obter mais informações, veja [Configurando servidores virtuais](../vsi/vsi_configuring.html).
