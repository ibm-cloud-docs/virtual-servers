---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Migrando uma instância de host dedicado para outro host
{: #migrating-dedicated-host}

É possível migrar suas instâncias de host dedicado de um host para outro dentro do mesmo POD. Selecione a instância a ser migrada da página de detalhes do dispositivo do host ou da página de detalhes do dispositivo da instância. Observe que somente duas instâncias podem ser migradas por vez e o tempo necessário para migrar depende do disco. Os discos SAN são migrados mais rápido porque os discos locais requerem copiar o disco. As instâncias em migração ficam off-line enquanto estão sendo migradas; o host permanece ativo para quaisquer de suas outras instâncias de host dedicado.
{:shortdesc}

## Antes de iniciar
Primeiro, navegue para o menu de dispositivos e assegure-se de ter as permissões de conta corretas para concluir as tarefas.

* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assegure-se de ter quaisquer permissões de conta necessárias e de ter acesso ao dispositivo. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões.

Para obter mais informações sobre permissões, veja [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Migrando do host dedicado
Use as etapas a seguir para migrar instâncias de host dedicadas para outro host dedicado dentro do mesmo POD da página de detalhes do dispositivo do *host dedicado original*. 

1. No menu **Dispositivos**, selecione **Lista de dispositivos**.
2. Selecione na lista o host ou a instância hospedada.
3. Clique na lista suspensa **Ações** ao lado da instância dedicada a ser migrada.
4. Selecione **Migrar** e insira o host para o qual a instância está sendo migrada; lembre-se, o host de destino deve estar dentro do mesmo POD que o host original.
5. Clique em **Migrar** para iniciar a migração. 

A migração é iniciada imediatamente. Durante a migração, a instância dedicada fica off-line até que seja ligada em seu novo host. É possível visualizar a página Detalhes do dispositivo do host de destino para assegurar que a instância tenha sido migrada corretamente.

## Migrando da instância dedicada
Use as etapas a seguir para migrar as instâncias de host dedicadas para outro host dedicado dentro do mesmo POD da página de detalhes da *instância do host dedicada*.

1. No menu **Dispositivos**, selecione **Lista de dispositivos**.
2. Selecione na lista a instância hospedada a ser migrada.
3. Clique em **Migrar**.
4. Selecione o host de destino para o qual migrar a instância; lembre-se, o host de destino deve estar dentro do mesmo POD que o host original.
5. Clique em **Migrar** para iniciar a migração.

A migração é iniciada imediatamente. Durante a migração, a instância dedicada fica off-line até que seja ligada em seu novo host. É possível visualizar a página de detalhes do dispositivo do host de destino para assegurar que a instância tenha sido migrada corretamente.

## Próximas Etapas
Depois de migrar uma instância de host dedicada, confirme se a migração funcionou, verificando se seu status está verde na página de detalhes do dispositivo do novo host dedicado.

