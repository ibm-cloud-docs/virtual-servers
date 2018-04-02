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


# Configurando servidores virtuais
{: #configuring-virtual-servers}

Quando você tiver acesso ao seu servidor virtual, assegure-se de configurá-lo para atender às necessidades de seu ambiente.
{:shortdesc}

## Efetuar login 
Efetue login no [{{site.data.keyword.slportal_full}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} com as credenciais que você recebeu em um e-mail quando sua conta foi criada inicialmente.

## Localizar seu servidor virtual
Localize seu servidor virtual na Lista de Dispositivos no {{site.data.keyword.slportal}}. Na Lista de dispositivos, é possível gerenciar dispositivos, fazer upgrade de dispositivos ou gerar gráficos de uso da largura da banda. Para obter mais informações, veja [Gerenciando servidores virtuais](../vsi/vsi_managing.html).

## Registrar endereços IP e credenciais
Mantenha um log de endereços IP e credenciais para o servidor em um local seguro para que você possa acessá-los rapidamente sem precisar efetuar login no {{site.data.keyword.slportal}}. 
- Os endereços IP de dispositivo individual podem ser visualizados na Lista de dispositivos.
- As senhas raiz de dispositivo individual podem ser visualizadas na Visualização de captura instantânea do dispositivo. Clique na seta ao lado do nome do dispositivo para expandir a visualização.
- Os endereços IP de dispositivo múltiplo podem ser visualizados usando a ação Fazer download do CSV na Lista de dispositivos. Selecione Fazer download do CSV na engrenagem Configurações para fazer download de uma lista integral de dispositivos e detalhes no formato de planilha.

## Atualizar as credenciais de software
Todo software que foi carregado em seu dispositivo durante o processo de fornecimento foi designado a credenciais provisórias. Essas credenciais são visualizadas e gerenciadas na guia Senhas de cada dispositivo no {{site.data.keyword.slportal}}. Use essas credenciais provisórias para acessar seu software pela primeira vez. Como uma melhor prática, mude a senha para seu software depois de acessá-lo pela primeira vez. Use uma senha forte que consista em uma combinação de letras, números e símbolos.

Opcionalmente, atualizações de senha podem ser armazenadas na guia Senhas para cada dispositivo; no entanto, entenda que, quando você armazena senhas no {{site.data.keyword.slportal}}, qualquer pessoa com acesso à conta e permissões apropriadas pode visualizar as senhas que estão armazenadas na tela Senhas.

Para obter mais informações sobre como visualizar e gerenciar suas credenciais de software, veja [Gerenciando o acesso à infraestrutura](../iam/mnginfra.html).

## Acessar seu servidor na rede privada
A rede privada é a precursora para interagir com seus dispositivos por meio de área de trabalho remota (RDP) usando SSH e KVM sobre IP. A ferramenta de Acesso à VPN permite a conexão de rede privada ao terminal VPN SSL mais próximo ou ao terminal de sua escolha. O acesso à VPN também é necessário para interagir com vários serviços que são oferecidos. Para obter mais informações, veja [Introdução à Virtual Private Networking (VPN)](../infrastructure/iaas-vpn/getting-started.html).

## Configurar o monitoramento
O monitoramento é usado principalmente como um recurso para verificar o tempo de atividade do seu servidor, mas também pode ser útil para saber quando escalar. Os serviços Standard Monitoring e Nimsoft Monitoring estão disponíveis para cobrir várias necessidades de monitoramento. O Standard Monitoring, às vezes referido como “Basic Monitoring”, geralmente é usado no método executar ping e responder usando um ping lento ou de serviço que é iniciado usando o {{site.data.keyword.slportal}}. O Nimsoft Monitoring também é referido como "Advanced Monitoring" e está disponível em três camadas: Básico, Avançado e Premium. Esse serviço também está acessível por meio do {{site.data.keyword.slportal}}. Para obter mais informações, veja [Monitoramento](../infrastructure/SLmonitoring/monitoring_index.html).

## Assegurar seu sistema
Os firewalls de hardware estão disponíveis para assegurar que seu dispositivo esteja sempre seguro. Os firewalls de hardware são provisionados sob demanda sem tempo de inatividade. Se as regras são estabelecidas corretamente, um firewall pode proteger seu servidor de atividades indesejadas. Depois que você solicita um firewall, ele deve ser ativado e as regras devem ser configuradas. Para obter mais informações sobre como obter o máximo de firewalls.

Para obter mais informações, veja as coleções de tópicos de segurança a seguir.

* [Hardware Firewalls (Shared)](../infrastructure/hardware-firewall-shared/getting-started.html)
* [Hardware Firewalls (Dedicated)](../infrastructure/hardware-firewall-dedicated/getting-started.html)

Os grupos de segurança são outra opção para limitar o tráfego de rede em seus servidores virtuais. É possível usar grupos de segurança para determinar um conjunto de regras de filtro de IP que definem como manipular o tráfego de entrada e de saída para as interfaces pública e privada de uma instância de servidor virtual. Para obter mais informações, consulte [Introdução aos grupos de segurança](/docs/infrastructure/security-groups/sg_index.html).

## Planejar backups 
Os backups asseguram que seus dados sejam armazenados com segurança fora do seu dispositivo e protegidos se forem perdidos. Os serviços de backup a seguir estão disponíveis para armazenar seus dados em um local seguro no caso de você precisar recarregar suas informações em seu dispositivo:
- EVault Backup é um sistema de backup automatizado baseado em agente. Essa é uma solução "configurar e esquecer" popular para gerenciar seu dispositivo. Ela é compatível com o software Microsoft, incluindo Exchange e SQL, por meio de plug-ins extras. Os usuários do EVault interagem com esse serviço por meio do aplicativo baseado na web WebCC do EVault. Para obter mais informações, veja [Introdução aos serviços de backup](../infrastructure/Backup/index.html).
- A Proteção Contínua de Dados R1Soft é um software de backup que pode ser instalado no servidor ou máquina virtual autogerenciada. Ele é recomendado se você deseja que uma única interface gerencie todos os seus backups. Você interage com o CDP R1Soft por meio de seu sistema de gerenciamento proprietário, que permite que os agentes sejam instalados em máquinas virtuais e oferece plug-ins de dados para funções extras. Para obter mais informações, veja [Introdução aos serviços de backup](../infrastructure/Backup/index.html).

## Próximas Etapas
Após seu servidor virtual ser configurado, é possível começar a gerenciá-lo. Para obter mais informações, veja [Gerenciando seu servidor virtual](../vsi/vsi_managing.html).



