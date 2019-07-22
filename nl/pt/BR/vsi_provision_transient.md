---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-21"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:note: .note}
{:important: .important}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Provisionando instâncias temporárias
{: #ordering-vs-transient}

## Antes de iniciar
Você tem duas opções para provisionar suas instâncias de servidor virtual temporárias. A primeira é por meio do console do {{site.data.keyword.cloud}} e a segunda é por meio do {{site.data.keyword.slportal}}. O console e o {{site.data.keyword.slportal}} requerem IDs de log-in exclusivos. Não é possível usar o nome de usuário do console e a senha para efetuar login no portal e vice-versa.
{:shortdesc}

Para o console do {{site.data.keyword.cloud_notm}}, deve-se ter uma conta com upgrade para pedir servidores virtuais. Para obter mais informações sobre como fazer upgrade de sua conta, consulte [Conta pré-paga](/docs/account?topic=account-accounts#paygo).
{:note}

Antes de iniciar, revise os pré-requisitos a seguir.

  1. Revise as opções de implementação disponíveis. Para obter mais informações, consulte [Servidores virtuais temporários](/docs/vsi?topic=virtual-servers-about-vs-transient).

  2. Revise as considerações de capacidade da instância de servidor virtual.  Para obter mais informações, consulte [Considerações de recurso para instâncias de servidor virtual](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).
  
  3. Abra a página [Instância do servidor virtual ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?guestType=transient&cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} do console do {{site.data.keyword.cloud_notm}}.

## Provisionando uma instância de servidor virtual temporária
{: #ordering-transient-instance}

Para provisionar uma instância de servidor virtual temporária, é necessário considerar as informações a seguir.

Deve-se estar com login efetuado para ver todas as opções disponíveis.
{:tip}

### Instância temporária

| Campo    | Detalhes     |
| -------- | ----------- |
| Faturamento  | Instâncias temporárias estão disponíveis apenas como instâncias por hora. Se você cancelar a sua instância por hora após 10 dias, pagará apenas as horas para esses 10 dias. |
| Nome do host | Pode conter rótulos que são feitos de caracteres alfanuméricos e traços, separados por pontos. Rótulos não podem ser somente numéricos, começar ou terminar com um traço, nem ter traços ou pontos consecutivos. |
| Domínio | Deve ter dois ou mais rótulos que podem ser feitos de caracteres alfanuméricos e traços, separados por pontos. Rótulos não podem começar nem terminar com um traço ou ter traços ou pontos consecutivos. O último rótulo deve conter apenas letras. |
| Grupo de colocação | É possível selecionar um grupo de colocação para a sua instância. Se você incluir um grupo de colocação, a regra de "difusão" significará que as instâncias estão em um hardware físico diferente. Para obter mais informações, consulte [Grupos de posicionamento](/docs/vsi?topic=virtual-servers-placement-groups). |
| Local  | Os locais são compostos de regiões (áreas geográficas específicas) e zonas (data centers tolerantes a falhas em uma região). Selecione o local no qual deseja que a sua instância seja criada. |
| Perfis populares | Considere selecionar entre configurações de perfil populares que suportam os casos de uso mais comuns. Os perfis contêm instâncias pré-configuradas que estão prontas para uso em uma questão de minutos. |
| Todos os perfis | Para obter mais informações sobre as opções de perfil disponíveis para instâncias temporárias, consulte [Servidores virtuais temporários](/docs/vsi?topic=virtual-servers-about-vs-transient). |
| Chaves SSH     | As chaves SSH permitem acesso a uma instância sem usar uma senha de clientes correspondentes para cada chave pública implementada na instância. Se você decidir incluir uma chave SSH, forneça uma chave pública de sua chave SSH, que pode ser usada para efetuar login em sua instância depois que ela for provisionada. |
| Imagem        |  Uma imagem é o sistema operacional implementado para a sua instância. É possível selecionar várias opções grátis, como CentOS e Ubuntu. As opções pagas, como Windows Server e Red Hat Enterprise Linux (RHEL), também estão disponíveis. É importante observar que o Windows requer um disco primário de 100 GB. |
{: caption="Tabela 1. Opções de instância temporária" caption-side="top"}

### Complementos de instância temporária 

Se você escolher qualquer complemento de software, ele deverá ser compatível com sua imagem para evitar um erro quando você estiver pedindo a sua instância. Por exemplo, não é possível provisionar uma imagem RedHat com um banco de dados Microsoft.
{:important}

| Campo     | Detalhes     |
| --------- | ----------- |
| Software de banco de dados      | É possível selecionar um software de banco de dados a ser instalado. O {{site.data.keyword.cloud_notm}} suporta qualquer software de banco de dados que é implementado durante o processo de provisionamento. Também é possível instalar seu próprio software de banco de dados depois que o servidor for implementado. |
| Serviços | Alguns serviços são selecionados automaticamente, dependendo da seleção de imagem. É possível escolher entre qualquer um dos complementos de serviço restantes para a sua instância. |
| Script de provisão | Os scripts de provisionamento são comumente usados para aplicar uma configuração específica do cliente a um servidor e para auxiliar na automação de sua estratégia de ajuste de escala. Os scripts de provisionamento podem ser qualquer arquivo que o sistema operacional (S.O.) possa executar, incluindo arquivos binários combinados ou qualquer idioma suportado pelo S.O. Os scripts de provisionamento não podem ser usados em imagens cloud-init. Para obter mais informações, consulte [Scripts de provisionamento](/docs/vsi?topic=virtual-servers-provisioning-scripts). |
| Dados do usuário        | É possível incluir dados do usuário que executam automaticamente tarefas de configuração comuns ou executam scripts. Os dados do usuário podem ser usados em imagens cloud-init e não cloud-init.  |
{: caption="Tabela 2. Complementos de instância temporária" caption-side="top"}

### Discos de armazenamento conectados

Se você precisar de armazenamento extra, será possível anexar discos de armazenamento à sua instância. O tipo de discos de armazenamento disponíveis depende do perfil selecionado. 

### Interface de rede

| Campo    | Detalhes     |
| -------- | ----------- |
| Velocidades de porta de Upl | É possível selecionar a velocidade de uplink para a sua instância até 1 GB/s. Esses uplinks virtuais são auxiliados por uplinks físicos redundantes para as redes pública e dedicada IBM. A velocidade pública e dedicada é sempre a mesma no momento da ordem, com a opção de fazer upgrade ou downgrade de um link se necessário. |
| Grupo de segurança privado e público  | É possível usar grupos de segurança para decretar um conjunto de regras de filtro de IP que definem como manipular o tráfego de entrada e de saída para as interfaces pública e privada de sua instância. Para obter mais informações, consulte [Sobre os grupos de segurança IBM](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups). |
| VLAN privada e pública | Sua instância de servidor virtual é colocada em uma VLAN designada automaticamente por padrão. Será possível escolher uma VLAN diferente se você já tiver uma em seu data center selecionado. Para obter mais informações, consulte [Sobre VLANs](/docs/infrastructure/vlans?topic=vlans-about-vlans). |
| Sub-rede privada e pública | A seleção de uma sub-rede é opcional e só deverá ser usada quando você requerer que seu dispositivo use um endereço IP da sub-rede. Se você selecionar uma sub-rede, verifique se possui endereços IP suficientes para cumprir a solicitação. Se você não tiver endereços IP suficientes para sua sub-rede, seu pedido poderá atrasar ou ser cancelado. Para obter mais informações, consulte [Sobre sub-redes e IPs](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
{: caption="Tabela 3. Opções de interface de rede" caption-side="top"}

### Complementos da interface de rede

| Campo    | Detalhes     |
| -------- | ----------- |
| Largura de Banda | A alocação de largura da banda não está incluída com instâncias de servidor virtual temporárias. |
| Firewalls de hardware e de software  | Os serviços de firewall evitam o tráfego indesejado em seus servidores, reduzem a probabilidade de um ataque e permitem que os recursos do servidor sejam dedicados para seu uso desejado. |
| Endereço IP primário | Um endereço IP primário é designado automaticamente à sua instância. |
| Endereços IP secundários públicos | Essas sub-redes são sua propriedade pela duração de sua instância de servidor virtual. É possível cancelar a sub-rede separadamente, mas, caso você cancele a sua instância, a sub-rede também é removida. Para obter mais informações, consulte [Sobre sub-redes e IPs](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
| Endereços IPv6 e IPv6 estático público | É possível selecionar um endereço IPv6 ou endereços IPv6 estáticos públicos para a sua instância. |
| Gerenciamento de VPN | Essa opção é selecionada automaticamente para a sua instância com usuários de VPN SSL ilimitados. Para obter mais informações, consulte [Sobre a VPN](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn). |
{: caption="Tabela 4. Complementos da interface de rede" caption-side="top"}

## Fornecendo as instâncias de servidor virtual temporárias por meio do portal do cliente
Para fornecer uma instância de servidor virtual temporária por meio do {{site.data.keyword.slportal}}, conclua as etapas a seguir:

  1. Efetue login no [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.
  2. Localize a seção **Ordem** e clique em **Dispositivos**.
  3. Em *Virtual Server público* na página *Dispositivos*, clique em **Temporário** para a oferta Virtual Server.
  4. Na página *Configurar seu servidor em nuvem*, conclua todas as informações relevantes.
  5. Clique em **Incluir no pedido** para continuar.
  6. Confirme ou edite as informações de domínio para o servidor.
  7. Clique nas caixas de seleção **Termos do serviço de nuvem** e **Contrato de prestação de serviços de terceiro**.
  8. Confirme ou insira suas informações de pagamento e clique em **Enviar pedido**. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

Também é possível provisionar um servidor virtual temporário usando o {{site.data.keyword.slapi_short}}. Para ver um exemplo, consulte [Provisionando uma instância temporária usando Create Object](/docs/vsi?topic=virtual-servers-api-rest-public#api-rest-transient).
{:tip}

## Próximas Etapas
Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail de fornecimento concluído inclui um link para sua página *Detalhes do dispositivo*.
 
Depois que seu servidor virtual for provisionado e estiver disponível para uso, será possível configurar seus servidores virtuais usando o console do {{site.data.keyword.cloud_notm}} ou o {{site.data.keyword.slapi_short}}. Para obter mais informações, veja [Configurando servidores virtuais](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
