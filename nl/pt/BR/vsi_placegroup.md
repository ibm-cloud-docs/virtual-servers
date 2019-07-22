---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Grupos de posicionamento
{: #placement-groups}

A alta disponibilidade (HA) é um aspecto importante de qualquer implementação de nuvem. Se ela for um website para seu negócio de e-commerce ou um banco de dados de produção que é usado pelo aplicativo de chave de sua empresa, ela precisa estar funcional. Para esse fim, a construção de uma infraestrutura resiliente é algo que nossos clientes de arquitetura de TI trabalham duro para implementar na busca de porcentagens cada vez maiores de "tempo de atividade". Embora o tempo de atividade seja monitorado de perto dentro das organizações de TI, ele pode cair abaixo de níveis de chave ou lidar com indisponibilidades substanciais, o que é um grande problema para o negócio inteiro.

A construção em redundância em cada nível de sua infraestrutura para eliminar qualquer ponto único de falha (SPOF) é a chave para executar bem nessa métrica. Para cargas de trabalho em execução em servidores virtuais, isso significa implementar soluções de failover com múltiplos servidores virtuais que podem preencher automaticamente um ao outro no evento de um travamento.

No entanto, a menos que seus servidores virtuais públicos sejam provisionados em data centers diferentes, não há realmente nenhuma maneira de determinar onde eles seriam colocados em relação uns aos outros. Isso poderá ser problemático se você estiver 1) construindo para HA e 2) seus servidores virtuais estiverem no mesmo host físico, deixando-os vulneráveis a uma indisponibilidade em uma única parte de hardware. Ainda que isso possa parecer improvável, os gerentes de TI não podem contar com a possibilidade de um SPOF para aplicativos críticos. A construção entre os data centers é uma opção, mas isso pode introduzir alguns desafios de rede que requerem dispositivos extras ou latência de aumento, especialmente em regiões com apenas um único data center.

O design de grupos de colocação para os servidores virtuais do {{site.data.keyword.cloud}} soluciona esse problema. Os grupos de colocação fornecem uma medida de controle sobre o host no qual um novo servidor virtual público é colocado. Com essa liberação, há uma regra de "difusão", o que significa que os servidores virtuais dentro de um grupo de colocação são todos distribuídos em hosts diferentes. É possível construir um aplicativo de alta disponibilidade em um data center sabendo que seus servidores virtuais estão isolados uns dos outros.

Os grupos de colocação com a regra de "difusão" estão disponíveis para criar em data centers do {{site.data.keyword.cloud_notm}} selecionados. Depois de criado, é possível provisionar um novo servidor virtual para esse grupo e garantir que ele não esteja no mesmo host que qualquer um de seus outros servidores virtuais. A melhor parte? Não há absolutamente nenhum encargo para usar esse recurso. Mediante disponibilidade, os grupos de colocação para servidores virtuais do {{site.data.keyword.cloud_notm}} são um recurso grátis.

É possível criar seu grupo de colocação e, em seguida, designar até cinco novas instâncias de servidor virtual. Com a regra de "difusão", cada um de seus servidores virtuais é provisionado em hosts físicos diferentes.

## Próximas Etapas

Para criar e gerenciar novos grupos de posicionamento, consulte
[Gerenciando os grupos de posicionamento](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup#vsi_managing_placegroup).
