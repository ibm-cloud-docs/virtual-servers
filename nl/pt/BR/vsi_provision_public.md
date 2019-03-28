---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-11"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisionando instâncias públicas
{: #ordering-vs-public}

## Antes de iniciar
Você tem duas opções para provisionar suas instâncias de servidor virtual público. O primeiro é por meio do catálogo do {{site.data.keyword.Bluemix}} e o segundo é por meio do {{site.data.keyword.slportal}}. O catálogo e o {{site.data.keyword.slportal}} requerem IDs de login exclusivos. Seu nome do usuário e senha do catálogo não funcionarão para efetuar login no portal e vice-versa.
{:shortdesc}

Antes de iniciar, revise os pré-requisitos a seguir.

  1. Assegure-se de que você tenha seu catálogo do {{site.data.keyword.Bluemix_notm}} ou as credenciais do {{site.data.keyword.slportal}} configuradas.

     **Nota:** para o catálogo do {{site.data.keyword.Bluemix_notm}}, deve-se ter uma conta com upgrade para pedir servidores virtuais. Para obter mais informações sobre como fazer upgrade de sua conta, veja [Alternando para o IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).

  2. Caso ainda não tenha feito isso, revise as opções de implementação disponíveis para você. Para obter mais informações, veja [Opções de implementação: servidor virtual público](/docs/vsi?topic=virtual-servers-about-public-virtual-servers).

  3. Revise as considerações de capacidade da instância de servidor virtual.  Para obter mais informações, veja [Considerações de capacidade](/docs/vsi?topic=virtual-servers-capacity-considerations).

## Provisionando uma instância de servidor virtual público
{: #ordering-public-instance}

Depois de preencher os pré-requisitos, é possível começar a fornecer uma instância de servidor virtual pública. É possível fornecer a instância pública por meio do catálogo do {{site.data.keyword.cloud_notm}} ou do {{site.data.keyword.slportal}}.

### Fornecendo uma instância de servidor virtual pública por meio do catálogo do IBM Cloud
Para fornecer uma instância de servidor virtual pública por meio do catálogo do {{site.data.keyword.cloud_notm}}, conclua as seguintes etapas:

  1. Efetue login no catálogo do [{{site.data.keyword.cloud_notm}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/catalog/){: new_window} usando as credenciais exclusivas.
  2. Na seção **Infraestrutura de cálculo**, clique no bloco **Virtual Servers**.
  3. Selecione a opção **Virtual Server público**.
  4. Clique em **Criar**.
  5. Preencha todas as informações relevantes para a instância de servidor virtual.
  6. Depois de revisar o resumo do pedido, clique na caixa de seleção **Contrato de Prestação de Serviços de terceiro**.
  7. Clique em **Provisão**.

### Fornecendo uma instância de servidor virtual pública por meio do portal do cliente
Para fornecer a instância de servidor virtual pública por meio do {{site.data.keyword.slportal}}, conclua as etapas a seguir:

  1. Efetue login no [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.
  2. Localize a seção **Ordem** e clique em **Dispositivos**.
  3. Na página Dispositivos, clique em **SAN por hora**, **Local por hora**, **Mensal** ou **Temporário** para uma das ofertas de Virtual Server.
  4. Na página *Configurar seu servidor em nuvem*, conclua todas as informações relevantes.
  5. Clique no botão **Incluir na ordem** para continuar.
  6. Confirme ou edite as informações de domínio para o servidor.
  7. Clique nas caixas de seleção **Termos do serviço de nuvem** e **Contrato de prestação de serviços de terceiro**.
  8. Confirme ou insira suas informações de pagamento e clique no botão **Enviar ordem**. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

 Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail completo de fornecimento inclui um link para sua página *Detalhes do dispositivo*, depois de efetuar login no {{site.data.keyword.Bluemix_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.

## Próximas Etapas
Depois que seu servidor virtual for provisionado, será possível começar a gerenciá-lo. Para obter mais informações, veja [Gerenciando seu servidor virtual](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
