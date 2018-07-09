---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Referência de API
{: #api-reference} 

O {{site.data.keyword.slapi_full}} é a interface de desenvolvimento que fornece aos desenvolvedores e administradores do sistema a interação direta com o sistema backend do {{site.data.keyword.cloud}}. O {{site.data.keyword.slapi_short}} impulsiona muitos dos recursos no {{site.data.keyword.slportal_full}}, o que geralmente significa que, se uma interação é possível no {{site.data.keyword.slportal}}, ela também pode ser executada na API. Como você pode interagir programaticamente com todas as partes do ambiente do {{site.data.keyword.BluSoftlayer_full}} dentro da API, o {{site.data.keyword.slapi_short}} permite automatizar tarefas. Por exemplo, é possível usar a API *SoftLayer_Virtual_Guest/createObject* para implementar uma instância de servidor virtual.
{:shortdesc}

O {{site.data.keyword.slapi_short}} é um sistema de Chamada de Procedimento Remoto. Cada chamada envolve enviar dados para um terminal de API e receber dados estruturados em retorno. O formato usado para enviar e receber dados com o {{site.data.keyword.slapi_short}} depende de qual implementação da API você escolher. O {{site.data.keyword.slapi_short}} usa atualmente SOAP, XML-RPC ou REST para transmissão de dados.

Para obter mais informações sobre o {{site.data.keyword.slapi_short}} e as APIs de servidor virtual, consulte os recursos a seguir no {{site.data.keyword.sldn_full}}:
* [{{site.data.keyword.slapi_short}} Visão geral ![Ícone de linkexterno](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/reference/softlayerapi/){: new_window}

* [Introdução ao {{site.data.keyword.slapi_short}} ![Ícone de linkexterno](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/article/getting-started/){: new_window}

* [Referência de API: SoftLayer_Virtual_Guest::createObject ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de linkexterno")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/){: new_window}

* [Referência de API: SoftLayer_Product_Order::placeOrder ![Ícone de linkexterno](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/){: new_window}


Para obter exemplos de uso da API, veja os recursos a seguir:
* [Entendendo e construindo um pedido usando a CLI de pedido do {{site.data.keyword.slapi_short}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/article/understanding-ordering/){: new_window}
* [{{site.data.keyword.slapi_short}} Python Client: Trabalhando com Virtual Servers ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [Exemplos de {{site.data.keyword.slapi_short}} - Notas sobre a Liberação ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/){: new_window}
* [Exemplos de Python ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/python/){: new_window}

## Exemplos de uso de servidores virtuais dedicados
* [Obter alocação de host dedicado ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/python/getDediHostAllocation/){: new_window}
* [Obter guests de host dedicado ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/python/getDedicatedHostGuests/){: new_window}
* [Migrar uma instância do servidor virtual entre hosts dedicados ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/python/migrateDedicatedHost.py/){: new_window}

## Exemplos de uso de servidores virtuais públicos
* [Exemplos da API softlayer_virtual_guest ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
