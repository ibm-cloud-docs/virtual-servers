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

# Provisionando hosts e instâncias dedicadas
{: #ordering-vs-dedicated}

Você tem duas opções sobre como provisionar suas instâncias dedicadas. O primeiro é por meio do catálogo do {{site.data.keyword.Bluemix}} e o segundo é por meio do {{site.data.keyword.slportal_full}}. O catálogo e o {{site.data.keyword.slportal}} requerem IDs de login exclusivos. Seu nome do usuário e senha do catálogo não funcionarão para efetuar login no portal e vice-versa. Veja [Inscrevendo-se para o {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window} para configurar o catálogo do {{site.data.keyword.Bluemix_notm}} ou as credenciais do {{site.data.keyword.slportal}}.
{:shortdesc}

## Efetuar login no catálogo do IBM Cloud
Use as etapas a seguir para efetuar login no catálogo do {{site.data.keyword.Bluemix_notm}} para começar a provisionar seus hosts dedicados e instâncias de host dedicado. 

1. Abra uma nova janela do navegador e insira [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/){: new_window}.
2.	Clique no link **Efetuar login** (canto superior direito). 
3.	Insira seu e-mail ou IBMid e clique em **Continuar**.
4.	Insira sua senha e clique em **Efetuar login**.
5.	Selecione **Infraestrutura > Calcular**.
6.  Clique no tile **Serviços virtuais**.
7.	Selecione a opção **Servidores virtuais dedicados**.
8.  Clique em **Criar**. 

Você estará na página principal do {{site.data.keyword.slportal}}.

## Efetuar login no Portal do Cliente
Use as etapas a seguir para efetuar login no {{site.data.keyword.slportal}} para iniciar o pedido para seus hosts dedicados e instâncias de host dedicado.

1.	Abra uma nova janela do navegador e insira [https://control.softlayer.com](https://control.softlayer.com){: new_window}. 
2.	Insira seu Nome do usuário e Senha e clique em **Efetuar login** OU clique em **Efetuar login com o IBMid**.
3.	Insira seu e-mail ou IBMid e clique em **Continuar**.
4.	Insira sua Senha e clique em **Efetuar login**.

Você estará na página principal do {{site.data.keyword.slportal}}.

## Provisionar seu host dedicado 
Use as etapas a seguir para provisionar seus hosts dedicados.

1.	Clique no ícone **Dispositivos**.
2.  Clique no link **Servidor virtual dedicado por hora** ou **Servidor virtual dedicado mensal**. 

   **Nota:** os servidores dedicados são servidores privados.

Você é conduzido para a página *Configurar seu servidor em nuvem*. Nessa página, é possível pedir uma instância dedicada que está ou não associada a um host dedicado. Mais informações sobre como pedir instâncias podem ser localizadas em [Provisionar suas instâncias de host dedicado](#provision-dedicated-instances).

4.	Clique no botão **Criar host** no lado direito do formulário.
5.	Digite as informações a seguir:
    
    <table>
    <CAPTION>Tabela 1. Seleções de fornecimento de host dedicado</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantidade</td>
    <td>Insira o número de hosts dedicados a serem pedidos. Observe que somente dois hosts dedicados podem ser implementados por ordem de fornecimento.</td>
    </tr>
    <tr>
    <td>Local</td>
    <td>Selecione o data center do {{site.data.keyword.cloud}} no qual deseja colocar seus hosts. Veja Sobre a lista de data centers aplicáveis.</td>
    </tr>
    <td>Host dedicado</td>
    <td>Assume por padrão 56 núcleos X 242 X 1,2 TB de RAM</td>
    </tr>
    </TBODY>
    </table>
    
    Seu Resumo de ordem é exibido no lado direito da página *Configuração*. 
    
6.  Clique no botão **Incluir na ordem**.
7.  Confirme suas seleções na página *Check-out* e role para baixo até *Configuração do sistema avançado de host dedicado*.
8.  Digite as informações a seguir:

    <table>
    <CAPTION>Tabela 2. Configuração do sistema avançado de host dedicado</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Seleção de POD</td>
    <td>Clique na caixa suspensa e selecione o POD no qual você deseja que seu host dedicado seja colocado.</td>
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

9.  Clique na caixa de seleção **Termos do serviço de nuvem**.
10. Confirme ou insira suas informações de pagamento e clique no botão **Enviar**. Você será redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

    Uma série de e-mails é enviada a seu administrador — confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail completo de fornecimento incluirá um link que o levará diretamente para sua página **Detalhes do dispositivo**, depois de efetuar login no {{site.data.keyword.Bluemix_notm}}. Outra opção seria registrar-se diretamente no {{site.data.keyword.slportal}}.

## Provisionar sua instância de host dedicado
{: #provision-dedicated-instances}
É possível provisionar suas instâncias de host dedicado de duas maneiras, por meio do menu **Dispositivos** ou do ícone **Dispositivos**.

### Provisionando suas instâncias de host dedicado por meio do menu Dispositivos
{: #ordering-dedicated-devices-menu}

Sua primeira opção é provisionar suas instâncias de host dedicado por meio do menu **Dispositivos** da página principal do {{site.data.keyword.slportal}}. As etapas a seguir conduzem você por esse processo.

1.	Clique em **Dispositivos > Lista de dispositivos**. 
 
    A página *Dispositivos* exibe todos os tipos de dispositivo — hosts dedicados, servidores virtuais, servidores bare metal e controladores de entrega do aplicativo NetScaler — em sua conta. 

2.	Selecione o host para suas instâncias de host dedicado clicando em seu link sob **Nome do dispositivo**.
    
    Você está na guia **Configuração** da página *Detalhes do dispositivo*. A guia **Chamados** lista seus chamados de suporte ativos e a guia **Alocações** exibe seu uso de memória para o período de faturamento selecionado. Veja Usando detalhes do dispositivo para gerenciar seu host dedicado e instâncias para obter mais informações nas guias.

3.	Role para baixo até o quadro **Instâncias**.

    A forma como seu host dedicado é faturado (mensal ou por hora) determina o faturamento de suas instâncias de host dedicado. Observe que se você tiver hosts faturados mensalmente, será possível provisionar instâncias de host dedicado faturadas por hora ou mensalmente. Há dois links, **Incluir por hora** e **Incluir mensalmente**, disponíveis ao provisionar suas instâncias. Os hosts dedicados faturados por hora podem provisionar somente instâncias de host dedicado faturadas por hora e verão somente o link **Incluir por hora**. 

4.	Clique no link **Incluir por hora** se seu host for faturado por hora ou mensalmente; clique no link **Incluir mensalmente** se seu host for faturado mensalmente. Você é redirecionado para a página *Configurar seu servidor em nuvem*. 

5.	Digite as informações a seguir:
       
    <table>
    <CAPTION>Tabela 3. Seleções de instâncias de host dedicado</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantidade</td>
    <td>O número de instâncias de hosts dedicados a serem implementadas em um único host.</td>
    </tr>
    <tr>
    <td>Posicionamento</td>
    <td>
    <ul>
    <li>Designar automaticamente – o {{site.data.keyword.Bluemix_notm}} designa sua instância automaticamente a um host versus uma especificada por você. Sua instância será colocada em um data center que tenha capacidade. Se você designar automaticamente sua instância, não usará nenhuma capacidade de seus hosts dedicados...</li>
    <li>Especificar host – seu host dedicado associado à sua conta será exibido sob Host dedicado. </li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Host dedicado</td>
    <td>Selecione o host dedicado na lista em que as instâncias devem ser provisionadas.</td>
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
    <td>É possível provisionar até quatro discos de inicialização adicionais, SAN ou Local, por instância de host dedicado.</td>
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

6.	Clique no botão **Incluir na ordem**.
7.  Insira as informações a seguir na página *Efetuar check-out* sob a *Configuração do sistema avançado*:

<table>
    <CAPTION>Tabela 4. Configuração do sistema avançado de instância de host dedicado</CAPTION>
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

8.  Clique nas caixas de seleção **Termos do serviço de nuvem** e **Contrato de prestação de serviços de terceiro**.
9. Confirme ou insira suas informações de pagamento e clique no botão **Enviar**. Você será redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.


Você receberá um e-mail quando suas instâncias de host dedicado tiverem sido provisionadas.

### Fornecendo suas instâncias do host dedicado por meio do ícone Dispositivos
A segunda opção para provisionar instâncias de host dedicado é usar o ícone **Dispositivo** na página inicial do {{site.data.keyword.slportal}}. As etapas a seguir conduzem você por esse processo.

1.	Clique no ícone **Dispositivos** e selecione **Por hora** ou **Mensal** em Servidores virtuais dedicados.
2.	Siga as etapas em [Provisionando suas instâncias de host dedicado por meio do menu Dispositivos](#ordering-dedicated-devices-menu), iniciando com a Etapa 5.

### Próximas Etapas
Depois que seu servidor virtual for provisionado, será possível começar a gerenciá-lo. Para obter mais informações, veja [Gerenciando servidores virtuais](../vsi/vsi_managing.html).


