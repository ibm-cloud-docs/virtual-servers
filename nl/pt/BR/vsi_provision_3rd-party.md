---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# Provisionando uma instância de servidor virtual por meio de uma imagem de terceiro
{: #ordering-3P}

É possível provisionar uma instância de servidor virtual por meio de uma imagem que foi criada por um fornecedor de terceiro. As imagens de terceiro estão disponíveis por meio do link Imagens da nuvem do catálogo do {{site.data.keyword.cloud}}.
{:shortdesc}

## Antes de iniciar
Antes de iniciar, assegure-se de que você tenha as suas credenciais do catálogo do {{site.data.keyword.cloud_notm}} configuradas.

Para o catálogo do {{site.data.keyword.Bluemix_notm}}, deve-se ter uma conta atualizada para solicitar
os servidores virtuais. Para obter mais informações sobre como fazer upgrade de sua conta, veja [Alternando para o IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

## Selecionando uma imagem de servidor virtual
1. Efetue login no catálogo do [{{site.data.keyword.cloud_notm}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/catalog/){: new_window} usando as credenciais exclusivas.
2. Na seção **Imagens da nuvem**, localize e clique na imagem de terceiro que deseja implementar.
3. Revise os detalhes da imagem customizada e clique em **Continuar**. A página **Instância do servidor virtual - imagem customizada** é exibida com sua imagem customizada pré-selecionada.

## Revisando e escolhendo suas opções de implementação
Para obter informações adicionais, consulte os
seguintes tópicos:

|              Opções de implementação                           |  Descrição                                        |
| --------------------------------------------------------- | --------------------------------------------------- |
|[Servidor virtual público](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)            | Implementações de servidor virtual de ocupação variada gerenciadas pela IBM|
|[Servidor virtual temporário](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)| Implementações de servidor virtual de ocupação variada gerenciadas pela IBM oferecidas a um custo reduzido e mais adequadas para cargas de trabalho flexíveis |
|[Servidor virtual reservado](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  | Implementações de servidor virtual de ocupação variada gerenciadas pela IBM com capacidade garantida por um prazo de contrato |
|[Servidor virtual dedicado](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)      | Implementações de servidor virtual de ocupação única gerenciadas pela IBM            |
{: caption="Tabela 1. Opções de implementação" caption-side="top"}

## Provisionando um servidor virtual
Depois de decidir sobre uma opção de implementação, inicie o processo de fornecimento. Para obter mais informações, consulte os tópicos a seguir.

Como você iniciou o processo de provisionamento com uma imagem customizada, não é possível mudar o tipo de imagem durante o processo de provisionamento.
{:note}

|              Instruções de provisionamento                                         |  Descrição                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[Provisionando instâncias públicas](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                | Provisione instâncias públicas com várias opções             |
|[Provisionando instâncias temporárias](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                | Provisione instâncias temporárias com várias opções            |
|[Provisionando a capacidade e as instâncias reservadas](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            | Fornecimento de capacidade e instâncias reservadas com várias opções |
|[Provisionando hosts e instâncias dedicadas](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)| Provisione instâncias privadas ou instâncias dedicadas em hosts dedicados.|
{: caption="Tabela 2. Provisionando informações" caption-side="top"}


## Próximas Etapas
Depois que seu servidor virtual for provisionado e estiver disponível para uso, será possível configurar seus servidores virtuais usando o console do {{site.data.keyword.cloud_notm}} ou o {{site.data.keyword.slapi_short}}. Para obter mais informações, veja [Configurando servidores virtuais](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
