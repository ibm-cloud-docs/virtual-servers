---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-03"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Provisionando instâncias temporárias
{: #ordering-vs-transient}
É possível fornecer as instâncias de servidor virtual temporárias por meio do catálogo do {{site.data.keyword.cloud}} ou do {{site.data.keyword.slportal}}.
{:shortdesc}

## Antes de iniciar
Antes de iniciar, revise os pré-requisitos a seguir.

  1. Assegure-se de que você tenha o catálogo do {{site.data.keyword.cloud_notm}} ou as credenciais do {{site.data.keyword.slportal}} configuradas.
  
  **Nota:** para o catálogo do {{site.data.keyword.Bluemix_notm}}, deve-se ter uma conta com upgrade para pedir servidores virtuais. Para obter mais informações sobre como fazer upgrade de sua conta, veja [Alternando para o IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).

  2. Revise as considerações de capacidade da instância de servidor virtual. Para obter mais informações, veja [Considerações de capacidade](ts_capacity_bp.html).

## Provisionando uma instância de servidor virtual temporária 
Depois de preencher os pré-requisitos, é possível começar a fornecer a instância de servidor virtual temporária. É possível fornecer a instância por meio do catálogo do {{site.data.keyword.cloud_notm}} ou do {{site.data.keyword.slportal}}.

### Fornecendo as instâncias de servidor virtual temporárias por meio do catálogo do IBM Cloud
Para fornecer uma instância de servidor virtual temporária por meio do catálogo do {{site.data.keyword.cloud_notm}}, conclua as etapas a seguir:

  1. Efetue login no catálogo do [{{site.data.keyword.cloud_notm}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/catalog/){: new_window} usando as credenciais exclusivas.  
  2. Na seção **Infraestrutura de cálculo**, clique no bloco **Virtual Servers**.
  3. Selecione a opção **Virtual Server temporário**.
  4. Clique em **Criar**.
  5. Preencha todas as informações relevantes para a instância de servidor virtual.
  6. Depois de revisar o resumo do pedido, clique na caixa de seleção **Contrato de Prestação de Serviços de terceiro**.
  7. Clique em **Provisão**.
  
### Fornecendo as instâncias de servidor virtual temporárias por meio do portal do cliente
Para fornecer uma instância de servidor virtual temporária por meio do {{site.data.keyword.slportal}}, conclua as etapas a seguir:

  1. Efetue login no [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.
  2. Localize a seção **Ordem** e clique em **Dispositivos**.
  3. Em *Virtual Server público* na página *Dispositivos*, clique em **Temporário** para a oferta Virtual Server.
  4. Na página *Configurar seu servidor em nuvem*, conclua todas as informações relevantes.
  5. Clique em **Incluir no pedido** para continuar.
  6. Confirme ou edite as informações de domínio para o servidor.
  7. Clique nas caixas de seleção **Termos do serviço de nuvem** e **Contrato de prestação de serviços de terceiro**.
  8. Confirme ou insira suas informações de pagamento e clique em **Enviar pedido**. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

 Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail de fornecimento concluído inclui um link para sua página *Detalhes do dispositivo*.

Também é possível provisionar um servidor virtual temporário usando o {{site.data.keyword.slapi_short}}. Para obter um exemplo, veja [Provisionando uma instância temporária usando Criar objeto](../vsi/vsi_provision_api.html#api-rest-transient).
{:tip}

## Próximas Etapas
Depois que seu servidor virtual for provisionado, será possível começar a gerenciá-lo. Para obter mais informações, veja [Gerenciando seu servidor virtual](../vsi/vsi_managing.html).
