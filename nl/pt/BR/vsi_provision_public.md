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

# Provisionando instâncias públicas
{: #ordering-vs-public}

## Antes de iniciar
Você tem duas opções para provisionar suas instâncias de servidor virtual público. O primeiro é por meio do catálogo do {{site.data.keyword.Bluemix}} e o segundo é por meio do {{site.data.keyword.slportal_full}}. O catálogo e o {{site.data.keyword.slportal}} requerem IDs de login exclusivos. Seu nome do usuário e senha do catálogo não funcionarão para efetuar login no portal e vice-versa.
{:shortdesc}

Antes de iniciar, revise os pré-requisitos a seguir.

  1. Assegure-se de que você tenha seu catálogo do {{site.data.keyword.Bluemix_notm}} ou as credenciais do {{site.data.keyword.slportal}} configuradas. 
  
     **Nota:** para o catálogo do {{site.data.keyword.Bluemix_notm}}, deve-se ter uma conta com upgrade para pedir servidores virtuais. Para obter mais informações sobre como fazer upgrade de sua conta, veja [Alternando para o IBMid](https://console.bluemix.net/docs/admin/softlayerlink.html).
  
  2. Caso ainda não tenha feito isso, revise as opções de implementação disponíveis para você. Para obter mais informações, veja [Opções de implementação: servidor virtual público](../vsi/vsi_public.html).

## Efetuando login 
Assegure-se de que você tenha efetuado login por meio do catálogo do {{site.data.keyword.Bluemix_notm}} ou do {{site.data.keyword.slportal}}: 

  <table>
   <CAPTION>Tabela 1. Escolher um log no local</CAPTION>
   <THEAD>
   <TR>
   <th>Se você deseja efetuar login com...</th>
   <th>Então...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Catálogo do IBM Cloud</td>
   <td>
   <ol>
   <li>Abra uma nova janela do navegador e insira <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Clique no link <b>Efetuar login</b> (canto inferior direito). </li>
   <li>Insira seu e-mail ou IBMid e clique em <b>Continuar</b>.</li>
   <li>Insira sua senha e clique em <b>Efetuar login</b>.</li>
   <li>Selecione <b>Infraestrutura</b> > <b>Cálculo</b>.</li>
   <li>Clique no tile <b>Serviços virtuais</b>.</li>
   <li>Selecione a opção <b>Servidores virtuais públicos</b>.</li>
   <li>Clique em <b>Criar</b>. A página principal do {{site.data.keyword.slportal}} é aberta.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Portal do Cliente</td>
   <td>
   <ol>
   <li>Abra uma nova janela do navegador e insira <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Insira seu Nome do usuário e Senha e clique em <b>Efetuar login</b>. Ou clique em <b>Efetuar login com o IBMid</b>. Em seguida, insira seu e-mail ou IBMid e clique em <b>Continuar</b>. Insira sua senha e clique em <b>Efetuar login</b>. A página principal do {{site.data.keyword.slportal}} é aberta.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Provisionando uma instância de servidor virtual público
{: #ordering-public-instance}
Depois de ter concluído os pré-requisitos, é possível começar a provisionar uma instância de servidor virtual público. É possível provisionar suas instâncias públicas de duas maneiras, por meio do menu **Dispositivos** ou do ícone **Dispositivos**.

### Provisionando uma instância de servidor virtual público por meio do ícone Dispositivos
Para provisionar sua instância de servidor virtual público por meio do ícone *Dispositivos*, conclua as etapas a seguir:

1.  No {{site.data.keyword.slportal}}, localize a seção **Pedido** e clique em **Dispositivos**.
2.  Na página Dispositivos, clique em **Por hora** ou **Mensal** para uma das ofertas de servidor virtual.
3.  Na página *Configurar seu servidor em nuvem*, conclua todas as informações relevantes.
4.  Clique no botão **Incluir na ordem** para continuar.
5.  Confirme ou edite as informações de domínio para o servidor.
5.  Clique nas caixas de seleção **Termos do serviço de nuvem** e **Contrato de prestação de serviços de terceiro**.
6.  Confirme ou insira suas informações de pagamento e clique no botão **Enviar ordem**. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

 Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail completo de fornecimento inclui um link para sua página *Detalhes do dispositivo*, depois de efetuar login no {{site.data.keyword.Bluemix_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.

### Provisionando uma instância de servidor virtual público por meio do menu Dispositivos
{: #ordering-public-devices-menu}

Também é possível provisionar suas instâncias de servidor virtual público por meio do menu *Dispositivos* da página principal do {{site.data.keyword.slportal}}. 

1. Clique em **Dispositivos > Lista de dispositivos**.

   A página Dispositivos exibe todos os tipos de dispositivo: hosts dedicados, servidores virtuais, servidores bare metal e controladores de entrega do aplicativo NetScaler, em sua conta.
2. Clique no link **Pedir dispositivos** no canto superior direito.
3. Na página Dispositivos, clique em **Por hora** ou **Mensal** para uma das ofertas de servidor virtual.
4. Na página *Configurar seu servidor em nuvem*, conclua todas as informações relevantes.
5. Clique no botão **Incluir na ordem** para continuar.
6. Confirme ou edite as informações de domínio para o servidor.
7. Clique nas caixas de seleção **Termos do serviço de nuvem** e **Contrato de prestação de serviços de terceiro**.
8. Confirme ou insira suas informações de pagamento e clique no botão **Enviar ordem**. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail completo de fornecimento inclui um link para sua página *Detalhes do dispositivo*, depois de efetuar login no {{site.data.keyword.Bluemix_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.

### Próximas Etapas
Depois que seu servidor virtual for provisionado, será possível começar a gerenciá-lo. Para obter mais informações, veja [Gerenciando seu servidor virtual](../vsi/vsi_managing.html).
