---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

keywords: transient virtual servers, transient instances, transient offering, cost savings

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Servidores virtuais temporários
{: #about-vs-transient}
A oferta temporária {{site.data.keyword.BluVirtServers}} será uma boa opção se você tiver cargas de trabalho flexíveis e quiser economia de custo. Você economizará dinheiro ao executar sua carga de trabalho em um servidor virtual temporário. As instâncias temporárias são provisionadas quando há capacidade não usada disponível. Portanto, quando os recursos do data center são necessários para contas sob demanda integrais, também é possível perder esses recursos. As instâncias temporárias serão desprovidas em uma base primeiro a entrar, primeiro a sair quando esses recursos precisarem ser recuperados.   

Os servidores virtuais temporários oferecem a flexibilidade a seguir:

* **Disponibilidade global**

    A oferta de servidor virtual temporário está disponível em data centers em todo o mundo.

* **Economia de custo**

    Os servidores virtuais temporários são ideais para cargas de trabalho de não produção. Por exemplo, você pode usar uma instância temporária para testar e desenvolver aplicativos ou testar a escalabilidade em ambientes que não requerem tempo de atividade constante.

Instâncias temporárias são instâncias públicas que usam armazenamento suportado pela SAN. As seguintes famílias de instâncias públicas estão disponíveis para essa oferta.

| Famílias  | Descrição                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Balanceado](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Melhor para cargas de trabalho de nuvem comuns que requerem um balanceamento de desempenho e escalabilidade. Usa armazenamento conectado à rede.|
| [Cálculo](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Melhor para cargas de trabalho de trafego da web moderado a alto.|
| [Memória](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Melhor para cargas de trabalho de armazenamento em cache de memória e de analítica em tempo real. |
{: caption="Tabela 1. Seleções de família do servidor virtual público" caption-side="top"}

## Notificações
É possível usar o {{site.data.keyword.slapi_short}} para receber notificações quando os recursos estão disponíveis para uma instância temporária. Também será possível usar a API para provisionar programaticamente um servidor virtual temporário quando os recursos forem disponibilizados. Da mesma forma, será possível usar a API para parar programaticamente o fornecimento de instâncias quando os recursos se tornarem indisponíveis. Para obter mais informações, consulte [Configurando notificações automatizadas de recuperação](/docs/vsi?topic=virtual-servers-configuring-notifications-for-reclaims-of-transient-virtual-servers#configuring-notifications-for-reclaims-of-transient-virtual-servers).  

## Limitações
Considere as limitações a seguir antes de provisionar um servidor virtual temporário.

* O número de instâncias simultâneas suportadas faz parte de sua cota de dispositivo da conta. Para obter mais informações sobre limites de instância simultâneos, veja [Perguntas frequentes: servidores virtuais](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#faqs-virtual-servers).
* As instâncias temporárias não podem ser submetidas a upgrade ou downgrade.
* Os recursos podem ser recuperados a qualquer momento, sem notificação.
* As instâncias temporárias não podem usar armazenamento local.
* As instâncias temporárias não podem usar perfis baseados em GPU.


## Próximas Etapas

Depois de revisar e selecionar o perfil do servidor virtual, é hora de provisionar seu servidor virtual temporário. Para iniciar, consulte [Provisionando instâncias temporárias](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient).

