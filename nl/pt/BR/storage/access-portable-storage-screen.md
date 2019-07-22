---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# Gerenciando o armazenamento móvel
{: #accessing-portable-storage}

Os volumes de armazenamento móvel (PSVs) são uma solução de armazenamento auxiliar exclusiva para {{site.data.keyword.virtualmachinesshort}}. Dentro do console do {{site.data.keyword.cloud}}, é possível acessar volumes de armazenamento móvel e exibir todos os PSVs. Também é possível anexar, remover, trocar e editar volumes.
{:shortdesc}

Não é possível anexar nem trocar volumes de armazenamento móvel para uma instância de servidor virtual provisionada por meio de um modelo de imagem criptografada.
{:note}

## Antes de iniciar
Primeiro, navegue para o menu de armazenamento ou de dispositivos e assegure-se de ter as permissões de conta corretas para concluir as tarefas.

* Navegue para o menu de armazenamento ou de dispositivo do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assegure-se de ter quaisquer permissões de conta necessárias e de ter acesso ao dispositivo. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões.

Para obter mais informações sobre permissões, veja [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Anexando o armazenamento móvel

1. No menu **Armazenamento**, selecione **Armazenamento de bloco**.
2. Na seção **Armazenamento móvel**, selecione a opção de conexão para o armazenamento móvel que você deseja usar.
3. Na próxima tela, escolha o dispositivo que precisa do armazenamento e selecione **Anexar**.

## Gerenciando o armazenamento móvel conectado a um servidor

O armazenamento móvel conectado a um servidor é listado na página *Detalhes* do servidor.

1. No menu **Dispositivos**, selecione **Lista de dispositivos**.
2. Na **Lista de dispositivos**, selecione uma instância de servidor virtual para visualizar seus detalhes.
3. Clique na guia **Armazenamento** para visualizar o armazenamento móvel atualmente anexado à instância.
4. No menu **Ações**, é possível **Trocar** ou **Remover** o armazenamento.
