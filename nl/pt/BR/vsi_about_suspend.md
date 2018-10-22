---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-08"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Sobre a suspensão de faturamento (Beta)
{: #requirements}

Quando você desliga um servidor virtual que suporta o recurso de suspensão de faturamento, você não acumula custos para determinados recursos de cálculo. O faturamento é interrompido automaticamente quando o servidor é desligado. O recurso de suspensão de faturamento ajuda a reduzir custos e impede que você precise reprovisionar um servidor virtual quando precisar dos recursos novamente. A suspensão de faturamento é suportada somente em novas provisões, não em instâncias existentes.
{:shortdesc}

Esse recurso está disponível em data centers em todo o mundo. Para ter acesso ao recurso de suspensão de faturamento, deve-se provisionar a nova instância de servidor virtual usando o {{site.data.keyword.slapi_short}} para especificar o pacote de suspensão de faturamento. A nova instância de servidor virtual deve ser definida com as seguintes configurações:

* SAN por hora
* Tipos públicos de uma das famílias a seguir:
  * Balanceado
  * Computação
  * Memória

É possível usar o recurso de suspensão de faturamento como uma alternativa mais rápida para provisionar e desprovisionar uma instância de servidor virtual.
{:tip}

**Nota:** o faturamento é suspenso apenas quando você desliga a instância de servidor virtual por meio do {{site.data.keyword.slportal_full}}, da CLI ou do {{site.data.keyword.slapi_short}}. Se você desligar a instância de servidor virtual diretamente por meio do S.O., o faturamento não será suspenso para essa instância.

## Fornecimento

Para o beta, para provisionar uma instância de servidor virtual que suporte o recurso de suspensão de faturamento, deve-se usar o {{site.data.keyword.slapi_short}}. Para obter exemplos de API, consulte [Provisionando uma instância pública usando o objeto Place Order](../vsi/vsi_provision_api.html#provisioning-a-public-instance-using-place-order-object). 

Também se deve especificar o ID do pacote específico de suspensão de faturamento durante o processo de provisionamento. É possível consultar o {{site.data.keyword.slapi_short}} para obter o ID do pacote de suspensão de faturamento usando o keyName `SUSPEND_CLOUD_SERVER`. Para obter um exemplo sobre a procura por pacotes do servidor, consulte [Entendendo e construindo um pedido usando a {{site.data.keyword.slapi_short}} CLI de pedido ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Detalhes do faturamento

É importante entender quais custos param de acumular e quais custos persistem quando a instância de servidor virtual é desligada.

| Recurso                      | Faturamento interrompido   | Faturamento persistente |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          |          P        |                  |
| RAM                           |          P        |                  |
| Velocidade da porta                    |          P        |                  |
| Licenças do sistema operacional     |          P        |                  |
| Complementos de monitoramento          |          P        |                  |
| Endereços IP públicos secundários |                   |         P        |
| Armazenamento                       |                   |         P        |
{: caption="Tabela 1. Detalhes do recurso de faturamento" caption-side="top"}   

**Observação:** quando você provisiona uma instância de servidor virtual que suporta o recurso de suspensão de faturamento, os tempos de uso são calculados por minuto, tanto para o tempo de uso quanto para o tempo de suspensão da instância de servidor virtual. Mesmo que você nunca inicie o recurso de suspensão de faturamento ao desligar a sua instância, o faturamento será calculado por minuto do ciclo de vida da instância. 

### Encargo mínimo de uso
As instâncias de servidor virtual que suportam o recurso de suspensão de faturamento têm um encargo mínimo de uso por mês. Se o uso for maior que 25%, você será faturado por esse uso. Se o uso for menor que 25%, você será cobrado por 25% das horas em que a instância existiu dentro do ciclo de faturamento atual. 

### Fatura de cobrança
Ao suspender o faturamento em um servidor virtual, você verá algumas mudanças em sua fatura de cobrança. Os encargos relevantes agora aparecem como detalhes baseados em uso. Por exemplo, é possível ver as seguintes adições que refletem horas disponíveis, horas usadas e o número total de horas cobradas:

```
Computing instance usage...
RAM usage...
Operating system usage...
```
{:screen}

## Detalhes do recurso

### Armazenamento

Ao suspender o faturamento em uma instância de servidor virtual, o armazenamento associado persiste, mas não é possível acessar os dados enquanto a instância de servidor virtual está desligada. Ao retomar o faturamento na instância, será possível acessar seus dados e o faturamento normal começará novamente.

### Endereços IP

Todos os endereços IP públicos são retidos para você quando o faturamento é suspenso para sua instância de servidor virtual.

É possível visualizar se o seu dispositivo está parado, bem como a data relevante em que o status foi mudado, por meio do {{site.data.keyword.slapi_short}} ou acessando a página Detalhes do dispositivo no {{site.data.keyword.slportal_full}}.

### Limitações

O número de instâncias simultâneas suportadas faz parte de sua cota de dispositivo da conta. Para obter mais informações sobre limites de instância simultâneos, veja [Perguntas frequentes: servidores virtuais](vsi_faqs_vs.html#concurrent).

## Próximas Etapas
Após provisionar um servidor virtual que suporte a suspensão de faturamento, será possível começar a suspender e retomar o faturamento no dispositivo.
Quando o faturamento está suspenso em uma instância de servidor virtual, não é possível concluir todas as mesmas ações na instância até que você retome o faturamento para o dispositivo.

Para suspender o faturamento em uma instância de servidor virtual, desligue o servidor virtual. Para obter mais informações, veja [Gerenciando servidores virtuais](vsi_managing.html).
