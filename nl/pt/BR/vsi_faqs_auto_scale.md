---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQs: escala automática
{: #faqs-auto-scale}

## A escala automática suporta instâncias do Bare Metal Auto Scale?
{: faq}

Atualmente, a escala automática não suporta instâncias do Bare Metal Auto Scale.

## A escala automática funciona com balanceadores de carga?
{: faq}

Sim, a escala automática funciona atualmente para os balanceadores de carga locais e usa uma parte da API do balanceador de carga. Para obter mais informações, consulte [Balanceadores de carga de escala](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Quais são as diferentes políticas de finalização de escala automática?
{: faq}

Há três políticas de finalização de escala automática: a mais nova, a mais antiga e ma ais próxima da próxima carga. Elas descrevem como o grupo escolhe qual membro retirar ao reduzir a escala. Para obter mais informações, consulte [Política de término](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## O que são políticas de escala automática?
{: faq}

Uma política contém um conjunto de ações e um conjunto de acionadores. As políticas geralmente são compostas por esses elementos: nome, resfriamento, ação e acionadores. Para obter mais informações, consulte [Políticas](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## O que são acionadores de escala automática?
{: faq}

Os acionadores são condicionantes que podem ser satisfeitos (apenas quando o grupo está ativo). Há três tipos de acionadores: único, de repetição e uso de recurso. Para obter mais informações, consulte [Acionadores](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## O que é a Contagem Máxima de Membros do VSI?
{: faq}

É a maioria dos membros que um grupo permite estar presente. Para obter mais informações, consulte [Contagem máxima de membros do VSI](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## O que é Contagem Mínima de Membros do VSI?
{: faq}

É o menor número de membros que um grupo permite estar presente. Para obter mais informações, consulte [Contagem mínima de membros do VSI](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## O que é um ativo de escala automática?
{: faq}

Um ativo é um membro fixo em um grupo que não contribui para a contagem do membro e que não é controlado automaticamente de nenhuma maneira. O ativo está presente para fornecer informações adicionais para os acionadores de política. Por exemplo, um ativo pode contribuir para a porcentagem de CPU do grupo inteiro se a porcentagem de CPU está sendo usada como um acionador. Atualmente, um grupo pode ter somente ativos de convidado virtual e não há limite para quantos. Além disso, um grupo não é necessário.

## O que é um grupo de escala automática?
{: faq}

Um grupo (grupo de escala) é uma coleção específica do grupo de ativos, membros, balanceadores de carga de escala, VLANs e políticas. Um grupo tem todos os parâmetros para ajuste de escala, incluindo os limites de contagem de membros e os modelos de membros da instância de servidor virtual escalados.

## O que é um membro de escala automática?
{: faq}

Um membro é uma unidade escalada em um grupo. Os membros são provisionados ou recuperados automaticamente com base nas ações de política. Atualmente, todos os membros são instâncias de servidor virtual. Em um grupo ativo, nunca há menos membros do que o mínimo ou mais membros do que o máximo. Embora os membros geralmente sejam incluídos por ações de uma política, eles também podem ser incluídos manualmente por um usuário.
