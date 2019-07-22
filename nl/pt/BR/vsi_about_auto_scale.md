---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords: auto scale, virtual servers

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Sobre a escala automática
{: #about-auto-scale}

A escala automática para instâncias de servidor virtual do {{site.data.keyword.cloud}} fornece a capacidade de automatizar o processo de ajuste de escala manual que está associado à inclusão ou remoção de instâncias para suportar seus aplicativos de negócios. Isso permite que você configure novas instâncias automaticamente, pois mais recursos são necessários e, então, essas instâncias são encerradas e removidas quando o carregamento extra diminui. A escala automática usa grupos para conter as políticas que mudam a maneira como seu ambiente é expandido ou reduzido. Essas políticas usam ações para incluir ou remover o servidor virtual com base em suas necessidades de negócios e de aplicativos. 
{:shortdesc}

O ajuste automático de escala ativa os recursos a seguir:

* Aumento de escala automática e contínua de instâncias quando mais recursos são necessários devido à demanda
* Diminuição de escala automática e contínua de instâncias removendo recursos desnecessários quando a demanda diminui (economizando dinheiro)
* Acionadores de ajuste de escala flexíveis: porcentagem de CPU, largura da banda pública e privada de saída e largura da banda pública e privada recebida
* Atualizações de status quase em tempo real para atividade de ajuste de escala em grupos
* Integração opcional de LAN virtual (VLAN) e balanceadores de carga locais

Há duas soluções de negócios comuns para as quais o ajuste automático de escala pode ser aplicado:

| Solução | Descrição |
| -------- | ----------- |
| [Ajuste de escala baseado em planejamento](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling) | O ajuste de escala baseado em planejamento pode ser usado para configurar políticas para aumentos de uso baseados em tempo, como durante os fins de semana ou feriados. O ajuste de escala baseado em planejamento pode ser usado quando uma empresa está esperando o aumento de tráfego, por exemplo, um site de rede social que requer mais recursos com base em um planejamento. |
| [Ajuste de escala baseada em recurso](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling) | O planejamento baseado em recurso pode ser usado para configurar políticas para aumentos irregulares, com base no uso de recurso. Os aumentos irregulares no tráfego podem ocorrer quando há um esforço para colocar um produto no mercado ou um site de e-commerce está em promoção e recursos são necessários para manter os tempos de resposta. |
{: caption="Tabela 1. Soluções de escala automática" caption-side="top"}

Se você não for o administrador da conta, a sua conta do usuário deverá incluir permissão para usar a escala automática. O administrador de conta pode conceder a permissão do usuário por meio do console do {{site.data.keyword.cloud_notm}}. Para obter mais informações sobre como atualizar as permissões, consulte [Configurando permissões de usuário para escala automática](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale).
{:note}


