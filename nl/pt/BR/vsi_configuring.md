---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Configurando servidores virtuais
{: #configuring-virtual-servers}

Quando você tiver acesso a seu servidor virtual, certifique-se de mudar sua senha e considere configurar o SSH para uma solução de autenticação mais segura. Há muitas outras opções para configurar seu servidor virtual para atender às necessidades de seu ambiente.
{:shortdesc}

## Efetuar login
Efetue login no console do [{{site.data.keyword.cloud}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/classic?){: new_window} com as credenciais que você recebeu em um e-mail quando sua conta foi criada inicialmente. Como alternativa, é possível efetuar login no [{{site.data.keyword.slportal}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){:new_window}.

## Localizar seu servidor virtual
Localize o servidor virtual na Lista de dispositivos no console do {{site.data.keyword.cloud_notm}}. Na Lista de dispositivos, é possível gerenciar dispositivos, fazer upgrade de dispositivos ou gerar gráficos de uso da largura da banda. Para obter mais informações, veja [Gerenciando servidores virtuais](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).

## Mude sua senha
Mude sua senha usando as diretrizes de senha forte. Consulte [Visualizando e gerenciando nomes de usuário e senhas do dispositivo](/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device#view-update-user-name-password-for-device).

## Configurar o SSH
O SSH fornece uma melhor solução de segurança do que a autenticação de senha. Consulte [Introdução às chaves SSH](/docs/infrastructure/ssh-keys?topic=ssh-keys-getting-started-tutorial#getting-started-tutorial).

## Registrar endereços IP e credenciais
Mantenha um log de endereços IP e credenciais para o servidor em um local seguro para que seja possível acessá-los rapidamente sem ter que efetuar login no console do {{site.data.keyword.cloud_notm}}.
- Os endereços IP de dispositivo individual podem ser visualizados na Lista de dispositivos.
- As senhas raiz de dispositivo individual podem ser visualizadas na Visualização de captura instantânea do dispositivo. Clique na seta ao lado do nome do dispositivo para expandir a visualização.
- Os endereços IP de dispositivo múltiplo podem ser visualizados usando a ação Fazer download do CSV na Lista de dispositivos. Selecione Fazer download do CSV na engrenagem Configurações para fazer download de uma lista integral de dispositivos e detalhes no formato de planilha.

## Atualizar as credenciais de software
Todo software que foi carregado em seu dispositivo durante o processo de fornecimento foi designado a credenciais provisórias. Essas credenciais são visualizadas e gerenciadas na guia Senhas de cada dispositivo no console do {{site.data.keyword.cloud_notm}}. Use essas credenciais provisórias para acessar seu software pela primeira vez. Como uma melhor prática, mude a senha para seu software depois de acessá-lo pela primeira vez. Use uma senha forte que consista em uma combinação de letras, números e símbolos.

Opcionalmente, as atualizações de senha podem ser armazenadas na guia Senhas para cada dispositivo. No entanto, entenda que, quando você armazena senhas dentro do console do {{site.data.keyword.cloud_notm}}, qualquer pessoa com acesso à conta e permissões apropriadas pode visualizar senhas que são armazenadas na tela Senhas.

Para obter mais informações sobre como visualizar e gerenciar suas credenciais de software, consulte [Gerenciando o acesso de infraestrutura clássica](/docs/vsi?topic=iam-mngclassicinfra).

## Acessar seu servidor na rede privada
A rede privada é a precursora para interagir com seus dispositivos por meio de área de trabalho remota (RDP) usando SSH e KVM sobre IP. A ferramenta de Acesso à VPN permite a conexão de rede privada ao terminal VPN SSL mais próximo ou ao terminal de sua escolha. O acesso à VPN também é necessário para interagir com vários serviços que são oferecidos. Para obter mais informações, veja [Introdução à Virtual Private Networking (VPN)](/docs/infrastructure/iaas-vpn?topic=VPN-gettingstarted-with-virtual-private-networking).

## Configurar o monitoramento
O monitoramento é usado principalmente como um recurso para verificar o tempo de atividade do seu servidor, mas também pode ser útil para saber quando escalar. Os serviços Standard Monitoring e Nimsoft Monitoring estão disponíveis para cobrir várias necessidades de monitoramento. O monitoramento padrão, às vezes chamado de "monitoramento básico", é geralmente usado no método executar ping e responder usando um ping lento ou de serviço que é iniciado usando o console do {{site.data.keyword.cloud_notm}}. O Nimsoft Monitoring também é referido como "Advanced Monitoring" e está disponível em três camadas: Básico, Avançado e Premium. Esse serviço também é acessível por meio do console do {{site.data.keyword.cloud_notm}}. Para obter mais informações, veja [Monitoramento](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring#monitoring).

## Configurar grupos de segurança
É possível usar grupos de segurança para limitar o tráfego de rede em seus servidores virtuais. Use grupos de segurança para decretar um conjunto de regras de filtro de IP que definem como manipular o tráfego de entrada e de saída para as interfaces pública e privada de uma instância de servidor virtual. Para obter mais informações, consulte [Introdução aos grupos de segurança](/docs/infrastructure/security-groups?topic=security-groups-getting-started).

## Configurar firewalls
Os firewalls de hardware também estão disponíveis para ainda mais proteção. Os firewalls de hardware são provisionados sob demanda sem tempo de inatividade. Se as regras são estabelecidas corretamente, um firewall pode proteger seu servidor de atividades indesejadas. Depois que você solicita um firewall, ele deve ser ativado e as regras devem ser configuradas.

Para obter mais informações, consulte as informações a seguir.

* [Hardware Firewalls (Shared)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Hardware Firewalls (Dedicated)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)

## Planejar backups
Os backups asseguram que seus dados sejam armazenados com segurança fora do seu dispositivo e protegidos se forem perdidos. Os serviços de backup a seguir estão disponíveis para armazenar seus dados em um local seguro no caso de você precisar recarregar suas informações em seu dispositivo:
- O {{site.data.keyword.backup_notm}} é um sistema de backup automatizado baseado em agente. Essa é uma solução "configurar e esquecer" popular para gerenciar seu dispositivo. Ela é compatível com o software Microsoft, incluindo Exchange e SQL, por meio de plug-ins extras. Os usuários do {{site.data.keyword.backup_notm}} interagem com esse serviço por meio do aplicativo baseado na web WebCC do {{site.data.keyword.backup_notm}}. Para obter mais informações, consulte [Introdução aos serviços do {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).
- A Proteção Contínua de Dados R1Soft é um software de backup que pode ser instalado no servidor ou máquina virtual autogerenciada. Ele é recomendado se você deseja que uma única interface gerencie todos os seus backups. Você interage com o CDP R1Soft por meio de seu sistema de gerenciamento proprietário, que permite que os agentes sejam instalados em máquinas virtuais e oferece plug-ins de dados para funções extras. Para obter mais informações, consulte [Introdução aos serviços do {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).

## Próximas Etapas
Após seu servidor virtual ser configurado, é possível começar a gerenciá-lo. Para obter mais informações, veja [Gerenciando seu servidor virtual](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
