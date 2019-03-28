---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Provisionando instâncias dedicadas
{: #provisioning-dedicated-instances}

Você tem duas opções sobre como provisionar suas instâncias dedicadas. O primeiro é por meio do catálogo do {{site.data.keyword.Bluemix}} e o segundo é por meio do {{site.data.keyword.slportal_full}}. O catálogo e o {{site.data.keyword.slportal}} requerem IDs de login exclusivos. Seu nome do usuário e senha do catálogo não funcionarão para efetuar login no portal e vice-versa. Veja [Inscrevendo-se para o {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-signup#signup) para configurar o catálogo do {{site.data.keyword.Bluemix_notm}} ou as credenciais do {{site.data.keyword.slportal}}.
{:shortdesc}

## Fornecimento de instâncias de servidor virtual dedicadas
{: #provision-dedicated-instances}
É possível fornecer a instância de servidor virtual dedicada por meio do catálogo do {{site.data.keyword.cloud_notm}} ou do {{site.data.keyword.slportal}}.

### Fornecimento de uma instância de servidor virtual dedicada por meio do catálogo do IBM Cloud
Para fornecer uma instância de servidor virtual dedicada por meio do catálogo do
{{site.data.keyword.cloud_notm}}, conclua as seguintes etapas:

  1. Efetue login no catálogo do [{{site.data.keyword.cloud_notm}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/catalog/){: new_window} usando as credenciais exclusivas.
  2. Na seção **Infraestrutura de cálculo**, clique no bloco **Virtual Servers**.
  3. Selecione a opção **Virtual Server dedicado**.
  4. Clique em **Criar**.
  5. Na seção **Host dedicado**, selecione **Designação automática**. O {{site.data.keyword.cloud_notm}}, então, designa automaticamente a instância para um host no data center selecionado.

     **Nota**: para os hosts dedicados, selecione **Especificar host** ou **Criar host**. Para obter mais informações sobre os hosts dedicados e as instâncias de host dedicadas, consulte [Servidores virtuais dedicados](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers).

  5. Preencha todas as informações relevantes para a instância de servidor virtual dedicada.
  6. Depois de revisar o resumo do pedido, clique na caixa de seleção **Contrato de Prestação de Serviços de terceiro**.
  7. Clique em **Provisão**.

### Fornecimento de uma instância dedicada de servidor virtual por meio do portal do cliente
Para fornecer uma instância de servidor virtual dedicada por meio do {{site.data.keyword.slportal}}, conclua as seguintes etapas:

1. Efetue login no [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.
2. Localize a seção **Ordem** e clique em **Dispositivos**. A janela **Pedir produto e serviços SoftLayer** é exibida.
3.  Selecione **Por hora** ou **Mensal** sob Virtual Servers dedicados. Você é redirecionado para a página *Configurar seu servidor em nuvem*.

4.	Digite as informações a seguir:

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
    <li>Especificar Host – usado com instâncias de host dedicado. Consulte [Servidores virtuais dedicados](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers) para obter mais informações sobre os hosts dedicados e as instâncias de host dedicadas.</li>
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

5.	Clique no botão **Incluir na ordem**. Você será redirecionado para a página de Check-out.
6.  Insira as informações a seguir na página *Efetuar check-out* sob a *Configuração do sistema avançado*:

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

7.  Clique nas caixas de seleção **Termos do serviço de nuvem** e **Contrato de prestação de serviços de terceiro**.
8. Confirme ou insira suas informações de pagamento e clique no botão **Enviar ordem**. Você será redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

    Uma série de e-mails é enviada a seu administrador — confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail completo de fornecimento incluirá um link que o levará diretamente para sua página **Detalhes do dispositivo**, depois de efetuar login no {{site.data.keyword.Bluemix_notm}}. Outra opção seria registrar-se diretamente no {{site.data.keyword.slportal}}.

## Próximas Etapas
Depois que seu servidor virtual for provisionado, será possível começar a gerenciá-lo. Para obter mais informações, veja [Gerenciando servidores virtuais](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
