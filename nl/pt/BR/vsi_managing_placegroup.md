---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:note: .note}
{:new_window: target="_blank"}

# Gerenciando os grupos de posicionamento
{: #vsi_managing_placegroup}

É possível gerenciar grupos de colocação usando a página de grupos de colocação ou a página de detalhes do dispositivo no console do {{site.data.keyword.cloud}}.
{:shortdesc}

## Incluindo grupos de colocação

Para incluir grupos de colocação por meio da página de grupos de colocação, conclua as etapas a seguir:
{:shortdesc}

1. Abra a página [Grupos de colocação ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. Na página de grupos de colocação, clique em **Novo grupo**.
3. Insira um nome, uma localização, um pod e uma regra para o grupo de colocação e clique em **Criar**.

As instâncias existentes não podem ser incluídas em um grupo de posicionamento; somente é possível incluir uma instância de servidor virtual em um grupo de posicionamento no fornecimento. 
{:note}

## Gerenciando os grupos de posicionamento

Para gerenciar os grupos de colocação por meio da página de grupos de colocação, conclua as etapas a seguir:
{:shortdesc}

1. Abra a página [Grupos de colocação ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. Na seção do grupo de colocação, é possível concluir várias tarefas de gerenciamento.
     * Visualizar uma lista de grupos de colocação e o número de instâncias designadas
     * Incluir um grupo
     * Renomear um grupo
     * Provisionar uma instância
     * Excluir um grupo
     
Deve-se remover os servidores designados do grupo de colocação antes que ele possa ser excluído. Para remover uma instância de um grupo de posicionamento, deve-se excluí-la ou recuperá-la.
{:note}
