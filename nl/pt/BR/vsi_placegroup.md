---

copyright:
  years: 2018
lastupdated: "2018-10-31"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Grupos de posicionamento
{: #placement-groups}

Com os grupos de posicionamento para o {{site.data.keyword.BluVirtServers}}, é possível usar as instâncias públicas para a construção de alta disponibilidade em um data center ou o fornecimento de um nível adicional de tolerância a falhas em uma implementação maior.
{:shortdesc}

Crie o grupo de posicionamento e, em seguida, designe até 5 novas instâncias de servidor virtual. Com a regra de difusão, cada um dos servidores virtuais é fornecido em hosts físicos diferentes.

Para iniciar, siga estas etapas:

1. No navegador, abra o [{{site.data.keyword.slportal}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){:new_window} e efetue login na conta.
2. Na página Grupos de posicionamento, clique em **Incluir grupo de posicionamento**.
3. Insira um nome, uma descrição e um data center para o grupo de posicionamento e clique em **Incluir**.
4. Localize a seção **Ordem** e clique em **Dispositivos**.
5. Na página Dispositivos, clique em **Por hora** ou **Mensal** para uma das ofertas de servidor virtual.
6. Conclua quaisquer outras informações necessárias e clique em **Incluir na ordem**. A página Efetuar check-out é aberta.
7. É possível selecionar qualquer grupo de posicionamento existente. **Difusão** significa que as instâncias estão em um hardware físico diferente.
8. Por último, clique em **Enviar ordem**.

##Limitações
As instâncias existentes não podem ser incluídas em um grupo de posicionamento; somente é possível incluir uma instância de servidor virtual em um grupo de posicionamento no fornecimento.

Para remover uma instância de um grupo de posicionamento, deve-se excluí-la ou recuperá-la.

## Próximas Etapas

Para criar e gerenciar novos grupos de posicionamento, consulte
[Gerenciando os grupos de posicionamento](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup).
