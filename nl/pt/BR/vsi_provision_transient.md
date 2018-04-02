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
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Provisionando instâncias temporárias
{: #ordering-vs-transient}
É possível provisionar suas instâncias de servidor virtual temporárias por meio do {{site.data.keyword.slportal_full}}.
{:shortdesc}

## Antes de iniciar
Antes de iniciar, revise os pré-requisitos a seguir.

  1. Assegure-se de que as credenciais do {{site.data.keyword.slportal}} estejam configuradas.

  2. Revise as considerações de capacidade da instância de servidor virtual. Para obter mais informações, veja [Considerações de capacidade](ts_capacity_bp.html).

## Efetuando login
Assegure-se de que esteja conectado ao {{site.data.keyword.slportal}}:

  1. Acesse o [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.

A página principal do {{site.data.keyword.slportal}} é aberta.

## Provisionando uma instância de servidor virtual temporária
{: #ordering-transient-instance}
Depois de concluir os pré-requisitos, provisione uma instância de servidor virtual temporária. É possível provisionar instâncias temporárias de duas maneiras: por meio do menu **Dispositivos** ou do ícone **Dispositivos**.

### Provisionando uma instância de servidor virtual temporária por meio do ícone Dispositivos
Para provisionar sua instância de servidor virtual temporária por meio do ícone *Dispositivos*, conclua as etapas a seguir:

1.  No {{site.data.keyword.slportal}}, localize a seção **Pedido** e clique em **Dispositivos**.
2.  Em *Servidor virtual público* na página *Dispositivos*, clique em **Temporário** para a oferta Servidor virtual.
3.  Na página *Configurar seu servidor em nuvem*, conclua todas as informações relevantes.
4.  Clique em **Incluir no pedido** para continuar.
5.  Confirme ou edite as informações de domínio para o servidor.
5.  Clique nas caixas de seleção **Termos do serviço de nuvem** e **Contrato de prestação de serviços de terceiro**.
6.  Confirme ou insira suas informações de pagamento e clique em **Enviar pedido**. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

 Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail de fornecimento concluído inclui um link para sua página *Detalhes do dispositivo*.

### Provisionando uma instância de servidor virtual temporária por meio do menu Dispositivos
{: #ordering-transient-devices-menu}

Também é possível provisionar suas instâncias de servidor virtual temporárias por meio do menu *Dispositivos* na página principal do {{site.data.keyword.slportal}}.

1. Clique em **Dispositivos > Lista de dispositivos**.

   A página Dispositivos exibe todos os tipos de dispositivo: hosts dedicados, servidores virtuais, servidores bare metal e controladores de entrega do aplicativo NetScaler, em sua conta.
2. Clique no link **Pedir dispositivos** no canto superior direito.
3. Em *Servidor virtual público* na página *Dispositivos*, clique em **Temporário** para a oferta Servidor virtual.
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
