---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-29"

keywords: virtual servers, provisioning process, IBM Cloud Virtual Servers

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Tutorial Introdução
{: #getting-started-tutorial}

É possível implementar {{site.data.keyword.BluVirtServers}} em uma questão de minutos. Os servidores virtuais são implementados por meio de sua escolha de imagens do servidor virtual e na região geográfica que faz sentido para suas cargas de trabalho.
{:shortdesc}

Experimente os nossos servidores virtuais em uma nuvem particular virtual! Para obter mais informações, consulte [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started).
{:tip}

Ao criar um servidor virtual na infraestrutura clássica, é possível escolher entre um ambiente público (ocupação variada) ou um ambiente dedicado (ocupação única). Em seguida, dependendo do ambiente escolhido, deve-se também selecionar servidores virtuais horários, mensais ou temporários. No caso de servidores virtuais públicos, você também escolhe usar o armazenamento baseado na SAN ou o armazenamento local.

## Antes de iniciar

Antes de iniciar, revise os pré-requisitos a seguir.

  1. Deve-se ter uma conta com upgrade para pedir servidores virtuais. Esse processo pode levar algum tempo e requer que sua solicitação seja aprovada antes de poder continuar. Para obter mais informações sobre como fazer upgrade de sua conta, veja [Alternando para o IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
  2. Revise e escolha suas opções de implementação. Para obter informações adicionais, consulte os
seguintes tópicos:

|              Opções de implementação                           |  Descrição                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Servidor virtual público](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)            | Implementações de servidor virtual de ocupação variada gerenciadas pela IBM|
|[Servidor virtual temporário](/docs/vsi?topic=virtual-servers-about-vs-transient)| Implementações de servidor virtual de ocupação variada gerenciadas pela IBM oferecidas a um custo reduzido e mais adequadas para cargas de trabalho flexíveis |
|[Servidor virtual reservado](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers)  | Implementações de servidor virtual de ocupação variada gerenciadas pela IBM com capacidade garantida por um prazo de contrato |
|[Servidor virtual dedicado](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers)      | Implementações de servidor virtual de ocupação única gerenciadas pela IBM            |
{: caption="Tabela 1. Opções de implementação" caption-side="top"}   

## Provisionando um servidor virtual

Depois de decidir sobre uma opção de implementação, inicie o processo de fornecimento.

|              Instruções de provisionamento                                         |  Descrição                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisionando instâncias públicas](/docs/vsi?topic=virtual-servers-ordering-vs-public)                | Provisione instâncias públicas com várias opções             |
|[Provisionando instâncias temporárias](/docs/vsi?topic=virtual-servers-ordering-vs-transient)                | Provisione instâncias temporárias com várias opções            |
|[Provisionando a capacidade e as instâncias reservadas](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances)            | Fornecimento de capacidade e instâncias reservadas com várias opções |
|[Provisionando hosts e instâncias dedicadas](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)| Provisionar instâncias privadas ou instâncias dedicadas em hosts dedicados|
{: caption="Tabela 2. Provisionando informações" caption-side="top"}

## Próximas Etapas

Depois que seu servidor virtual for provisionado e estiver disponível para uso, será possível configurar seus servidores virtuais usando o console do {{site.data.keyword.cloud_notm}} ou o {{site.data.keyword.slapi_short}}. Para obter mais informações, veja [Configurando servidores virtuais](/docs/vsi?topic=virtual-servers-configuring-virtual-servers).
