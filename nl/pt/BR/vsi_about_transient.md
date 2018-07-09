---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Servidores virtuais temporários
A oferta temporária {{site.data.keyword.BluVirtServers}} será uma boa opção se você tiver cargas de trabalho flexíveis e quiser economia de custo. Você economizará dinheiro ao executar sua carga de trabalho em um servidor virtual temporário. As instâncias temporárias são provisionadas quando há capacidade não usada disponível. Portanto, quando os recursos do data center são necessários para contas sob demanda integrais, também é possível perder esses recursos. As instâncias temporárias serão desprovidas em uma base primeiro a entrar, primeiro a sair quando esses recursos precisarem ser recuperados.   

Os servidores virtuais temporários são ideais para cargas de trabalho de não produção. Por exemplo, você pode usar uma instância temporária para testar e desenvolver aplicativos ou testar a escalabilidade em ambientes que não requerem tempo de atividade constante.

## Requisitos
Para aproveitar as instâncias temporárias, deve-se provisionar usando as seleções de servidores virtuais públicos a seguir:
* Temporário
* Seu local de host; é possível selecionar entre os data centers a seguir:
    * MEX01 
    * SEO01
    * PAR01

Instâncias temporárias são instâncias públicas que usam armazenamento suportado pela SAN.

## Notificações
É possível usar o {{site.data.keyword.slapi_short}} para receber notificações quando os recursos estão disponíveis para uma instância temporária. Também será possível usar a API para provisionar programaticamente um servidor virtual temporário quando os recursos forem disponibilizados. Da mesma forma, será possível usar a API para parar programaticamente o fornecimento de instâncias quando os recursos se tornarem indisponíveis. Para obter mais informações, consulte [Configurando notificações automatizadas de recuperação](configuring-automated-reclaim-notifications.html).

## Limitações
Considere as limitações a seguir antes de provisionar um servidor virtual temporário.

* O número de instâncias simultâneas suportadas faz parte de sua cota de dispositivo da conta. Para obter mais informações sobre limites de instância simultâneos, veja [Perguntas frequentes: servidores virtuais](../vsi/vsi_faqs_vs.html#concurrent).
* As instâncias temporárias não podem ser submetidas a upgrade ou downgrade.
* Os recursos podem ser recuperados a qualquer momento, sem notificação.
* As instâncias temporárias não podem usar armazenamento local.
* As instâncias temporárias usam apenas o armazenamento suportado pela SAN (balanceado, de cálculo, de memória).
* As instâncias temporárias não podem usar tipos baseados na GPU.


## Próximas Etapas

Depois de revisar e selecionar seu tipo de servidor virtual, é hora de provisionar seu servidor virtual temporário. Para iniciar, revise as informações a seguir:
1. [Seleções de fornecimento](../vsi/vsi_public_selections.html)
2. [Provisionando instâncias temporárias](../vsi/vsi_provision_transient.html)
