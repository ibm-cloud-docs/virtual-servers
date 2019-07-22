---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-29"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Fazendo downgrade de velocidades da porta
{: #downgrading-port-speeds}

É possível fazer downgrade temporariamente das velocidades de porta para a instância de servidor virtual sem abrir um chamado. Só é possível fazer downgrade, desconectar ou reconectar o máximo do que você já estiver pagando. Não é possível fazer upgrade por meio dessa opção. As mudanças permanecem no console até que você as mude de volta. Não são feitas mudanças de faturamento daí e fazer downgrade do servidor provisoriamente não diminui sua conta. Se você precisa de uma mudança permanente para a velocidade da porta, deve-se abrir um chamado de vendas.
{:shortdesc}

## Antes de iniciar
Primeiro, navegue para o menu de dispositivo e assegure-se de que tenha as permissões de conta corretas para concluir a tarefa. 

* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assegure-se de ter quaisquer permissões de conta necessárias e de ter acesso ao dispositivo. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões. 

Para obter mais informações sobre permissões, veja [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Fazendo downgrade de velocidades da porta
Conclua as etapas a seguir para fazer downgrade das velocidades de porta.

1. No menu **Dispositivos**, selecione **Lista de dispositivos**.
2. Selecione o servidor que você deseja atualizar.
3. Na guia **Visão geral**, acesse **Detalhes da rede**.
4. Selecione o menu suspenso em **Velocidade** (para rede pública ou privada) para fazer downgrade ou desconectar a velocidade da porta.

Quando as velocidades ou a desconexão das portas mudam por qualquer motivo, deve-se mudar manualmente o próprio servidor.
{:tip}
