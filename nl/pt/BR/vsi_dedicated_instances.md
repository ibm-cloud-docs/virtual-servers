---



copyright: years: 2017 lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Provisionando instâncias dedicadas

Você tem duas opções sobre como provisionar suas instâncias dedicadas. O primeiro é por meio do catálogo do {{site.data.keyword.Bluemix}} e o segundo é por meio do {{site.data.keyword.slportal_full}}. O catálogo e o {{site.data.keyword.slportal}} requerem IDs de login exclusivos. Seu nome do usuário e senha do catálogo não funcionarão para efetuar login no portal e vice-versa. Veja [Inscrevendo-se para o {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} para configurar o catálogo do {{site.data.keyword.Bluemix_notm}} ou as credenciais do {{site.data.keyword.slportal}}.
{:shortdesc}

## Efetuar login no Catálogo do Bluemix
Use as etapas a seguir para efetuar login no {{site.data.keyword.Bluemix_notm}} para iniciar o fornecimento de suas instâncias dedicadas. 

1. Abra uma nova janela do navegador e insira [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/){: new_window}.
2.	Clique no link **Efetuar Login** (canto superior direito). 
3.	Insira seu e-mail ou IBMid e clique em **Continuar**.
4.	Insira sua senha e clique em **Efetuar login**.
5.	Selecione **Infraestrutura > Calcular**.
6.  Clique no tile **Serviços virtuais**.
7.	Selecione a opção **Servidores virtuais dedicados**.
8.  Clique em **Criar**. 

Você estará na página principal do {{site.data.keyword.slportal}}.

## Efetuar login no Portal do Cliente
Use as etapas a seguir para efetuar login no {{site.data.keyword.slportal}} para iniciar o pedido para suas instâncias dedicadas.

1.	Abra uma nova janela do navegador e insira [https://control.softlayer.com](https://control.softlayer.com){: new_window}. 
2.	Insira seu Nome do usuário e Senha e clique em **Efetuar login** OU clique em **Efetuar login com o IBMid**.
3.	Insira seu e-mail ou IBMid e clique em **Continuar**.
4.	Insira sua Senha e clique em **Efetuar login**.

Você estará na página principal do {{site.data.keyword.slportal}}.

## Provisionar suas instâncias dedicadas
{: #provision-dedicated-instances}
É possível provisionar suas instâncias dedicadas de duas maneiras, por meio do ícone **Dispositivos** ou do menu **Dispositivos**.

### Fornecendo suas instâncias do host dedicado por meio do ícone Dispositivos
{: #ordering-dedicated-devices-menu}
A primeira opção para provisionar instâncias de host dedicado é usar o ícone **Dispositivo** na página inicial do {{site.data.keyword.slportal}}. As etapas a seguir conduzem você por esse processo.

1.	Clique no ícone **Dispositivos**. A janela **Pedir produto e serviços SoftLayer** é exibida. 
2.  Selecione **Por hora** ou **Mensal** sob Servidores virtuais dedicados. Você é redirecionado para a página *Configurar seu servidor em nuvem*. 

3.	Digite as informações a seguir:
       
    <table>
    <CAPTION>Tabela 1. Seleções de instâncias de host dedicado</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantidade</td>
    <td>O número de instâncias dedicadas a serem implementadas.</td>
    </tr>
    <tr>
    <td>Posicionamento</td>
    <td>
    <ul>
    <li>Designar automaticamente – o {{site.data.keyword.Bluemix_notm}} designa sua instância automaticamente a um host em seu data center selecionado.</li>
    <li>Especificar Host – usado com instâncias de host dedicado. Veja [Servidor virtual dedicado](../vsi/vsi_dedicated.html) para obter mais informações sobre hosts dedicados e instâncias de host dedicado.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Datacenter</td>
    <td>Selecione o data center no qual as instâncias devem ser provisionadas.</td>
    </tr>
    <tr>
    <td>Calculando a instância</td>
    <td> Selecione memória e CPU para cada instância em uma ordem de fornecimento.</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> Selecione a RAM para cada instância em uma ordem de fornecimento.</td>
    </tr>
    <tr>
    <td>Sistema operacional</td>
    <td>Selecione o sistema operacional para a instância. Observe que uma mensagem de erro será emitida se houver um conflito entre o servidor e o sistema operacional. Por exemplo, selecionar Linux em um Microsoft SQL server.</td>
    </tr>
    <tr>
    <td>Primeiro disco</td>
    <td>Selecione SAN ou Local para cada instância em uma ordem.</td>
    </tr>
    <tr>
    <td>Discos adicionais</td>
    <td>É possível provisionar até quatro discos de inicialização adicionais, SAN ou Local, por instância dedicada.</td>
    </tr>
    <td>Opções de rede</td>
    <td> Selecione as opções apropriadas ou use os valores padrão.</td>
    </tr>
    <tr>
    <td>Complementos</td>
    <td> Selecione as opções apropriadas ou use os valores padrão.</td>
    </tr>
    <tr>
    </TBODY>
    </table> 

4.	Clique no botão **Incluir na ordem**. Você será redirecionado para a página de Check-out.
5.  Insira as informações a seguir na página *Efetuar check-out* sob a *Configuração do sistema avançado*:

<table>
    <CAPTION>Tabela 2. Configuração do sistema avançado de instância dedicada</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Seleção de VLAN</td>
    <td>Inclua o novo servidor em uma VLAN sob sua conta se você já tiver pedido pelo menos um servidor.</td>
    </tr>
    <tr>
    <td>Provisionar scripts</td>
    <td>Forneça um script que permita automatizar determinadas etapas após o fornecimento.</td>
    </tr>
    <tr>
    <td>Chaves SSH</td>
    <td>Forneça uma chave pública de sua chave SSH, que permitirá efetuar login em seu servidor depois que ela for provisionada.</td>
    </tr>
    <tr>
    <td>Metadados do usuário</td>
    <td>Metadados opcionais para scripts de fornecimento customizado.</td>
    </tr>
    <tr>
    <td>Nome do host</td>
    <td>Insira um nome permanente ou provisório para seu servidor, por exemplo, server1.</td>
    </tr>
    <tr>
    <td>Domínio</td>
    <td>Insira um nome de subdomínio que não será conflitante com um nome do domínio da Internet, por exemplo, test.acme.com.</td>
    </tr>
    </TBODY>
    </table>

6.  Clique nas caixas de seleção **Termos do serviço de nuvem** e **Contrato de prestação de serviços de terceiro**.
7. Confirme ou insira suas informações de pagamento e clique no botão **Enviar ordem**. Você será redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

    Uma série de e-mails é enviada a seu administrador — confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail completo de fornecimento incluirá um link que o levará diretamente para sua página **Detalhes do dispositivo**, depois de efetuar login no {{site.data.keyword.Bluemix_notm}}. Outra opção seria registrar-se diretamente no {{site.data.keyword.slportal}}.

### Provisionando suas instâncias dedicadas por meio do menu Dispositivos

Sua segunda opção é provisionar suas instâncias dedicadas por meio do menu **Dispositivos** da página principal do {{site.data.keyword.slportal}}. As etapas a seguir conduzem você por esse processo.

1.	Clique em **Dispositivos > Lista de dispositivos**. 
 
    A página *Dispositivos* exibe todos os tipos de dispositivo — servidores virtuais, servidores bare metal, hosts dedicados e controladores de entrega do aplicativo NetScaler — em sua conta. 

2.	Clique no link **Pedindo dispositivos** no lado direito da página.
    A janela **Pedir produto e serviços SoftLayer** é exibida.
3.	Siga as etapas sob o menu [Provisionando suas instâncias dedicadas por meio dos Dispositivos](#ordering-dedicated-devices-menu), iniciando com a Etapa 2.

### Próximas Etapas
Depois que seu servidor virtual for provisionado, será possível começar a gerenciá-lo. Para obter mais informações, veja [Gerenciando servidores virtuais](../vsi/vsi_managing.html).
