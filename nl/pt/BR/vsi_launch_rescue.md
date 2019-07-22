---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Ativando o kernel de resgate
{: #launching-rescue}

O kernel de resgate é um ambiente de resgate ativo projetado para fornecer a você a capacidade de colocar um servidor bare metal ou servidor virtual on-line para solucionar problemas do sistema que normalmente seriam resolvidos apenas por meio de recarregamento do S.O. O kernel de resgate deve ser iniciado no console do {{site.data.keyword.cloud}}. Use as etapas a seguir para ativar o Rescue Kernel para um dispositivo.
{:shortdesc}

## Antes de iniciar
Primeiro, navegue para o menu de dispositivos e assegure-se de ter as permissões de conta corretas para concluir as tarefas.

* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assegure-se de ter quaisquer permissões de conta necessárias e de ter acesso ao dispositivo. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões.

Para obter mais informações sobre permissões, veja [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Ativando o kernel de resgate

1. No menu **Dispositivos**, selecione **Lista de dispositivos**.
2. Na **Lista de dispositivos**, clique no nome do dispositivo que você deseja resgatar.
3. No menu *Ações*, selecione **Modo de resgate**.
4. Clique em **Sim** para fazer a transição de seu dispositivo para o kernel de resgate imediatamente.

## Ativando o kernel de resgate para uma instância do Windows

1. No menu **Dispositivos**, selecione **Lista de dispositivos**.
2. Na **Lista de dispositivos**, clique no nome do dispositivo que você deseja resgatar.
3. No menu *Ações*, selecione **Inicializar por meio da imagem**.
4. Selecione **Inicializar por meio dessa imagem** próximo à imagem pública, *WindowsRescueStandalone.iso*.

## Próximas Etapas
Após ativar o Rescue Kernel, o dispositivo é desligado e reinicializado no kernel de resgate para o sistema operacional do dispositivo. Isso pode levar vários minutos.

O acesso remoto ao dispositivo está disponível por meio do endereço IP do dispositivo. É possível acessar o dispositivo no kernel de resgate usando as credenciais raiz ou de administrador para os dispositivos que são registrados no console do {{site.data.keyword.cloud_notm}}. Ao usar o Rescue Kernel, é possível solucionar problemas, descobrir problemas e resolver problemas como você faria em um dispositivo regularmente inicializado. Se necessário, é possível montar unidades no OS do Rescue Kernel. Para sair do kernel de resgate e retornar seu dispositivo para seu ambiente regular, reinicialize o dispositivo no console do {{site.data.keyword.cloud_notm}} ou reinicialize por meio do S.O. do kernel de resgate.

Para obter mais informações sobre como reinicializar um dispositivo, consulte [Gerenciando Servidores Virtuais](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
