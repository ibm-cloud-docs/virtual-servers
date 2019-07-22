---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-06"

keywords: virtual server, suspend billing feature, virtual server instances, suspend billing

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}

# Suspender faturamento
{: #requirements}

Ao desligar um servidor virtual que suporta o recurso de suspensão de faturamento, os custos
para determinados recursos de cálculo não são acumulados. O faturamento é interrompido automaticamente quando o servidor é desligado. O recurso de suspensão de faturamento ajuda a reduzir custos e impede que você precise reprovisionar um servidor virtual quando precisar dos recursos novamente.
{:shortdesc}

A maioria das instâncias de servidor virtual criadas antes de 1º de novembro de 2018 não suporta o recurso de
suspensão de faturamento. Para descobrir se a instância de servidor virtual suporta o recurso de suspensão de
faturamento, consulte [Visualizando o recurso de suspensão de faturamento](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature).

Esse recurso está disponível em data centers em todo o mundo. Para fornecer uma instância de servidor virtual que
suporte o recurso de suspensão de faturamento, a instância de servidor virtual deve ser definida com as seguintes
configurações:

* SAN por hora
* Perfis públicos de uma das famílias a seguir:
  * Balanceado
  * Computação
  * Memória

É possível usar o recurso de suspensão de faturamento como uma alternativa mais rápida ao fornecimento e à
recuperação de uma instância de servidor virtual.
{:tip}

O faturamento é suspenso apenas quando você desliga a instância de servidor virtual por meio do console do {{site.data.keyword.cloud}}, da CLI ou do {{site.data.keyword.slapi_short}}. Se você desligar a instância de servidor virtual diretamente por meio do S.O., o faturamento não será suspenso para essa instância.
{:note}

## Detalhes do fornecimento

É possível provisionar uma instância de servidor virtual que suporta o recurso de suspensão de faturamento por meio do catálogo do {{site.data.keyword.cloud_notm}} (cloud.ibm.com), da CLI ou do {{site.data.keyword.slapi_short}}. Não é possível provisionar uma instância de servidor virtual que suporta o recurso de suspensão de faturamento por meio do {{site.data.keyword.slportal}} (control.softlayer.com). Para
obter informações adicionais sobre o fornecimento de instâncias de servidor virtual públicas, consulte
[Fornecimento de instâncias públicas](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public).

Para o catálogo do {{site.data.keyword.cloud_notm}}, deve-se ter uma conta atualizada para solicitar
os servidores virtuais. Para obter mais informações sobre como fazer upgrade de sua conta, veja [Alternando para o IBMid](/docs/account?topic=account-unifyingaccounts#unifyingaccounts).
{:note}

### Fornecimento por meio da API do Softlayer
É possível fornecer uma instância de servidor virtual que suporte o recurso de suspensão de faturamento por meio do {{site.data.keyword.slapi_short}}. Para obter exemplos de API, consulte [Provisionando uma instância pública usando o objeto Place Order](/docs/vsi?topic=virtual-servers-api-rest-public#provisioning-a-public-instance-using-place-order-object).

Deve-se especificar o ID do pacote de suspensão de faturamento específico durante o processo de fornecimento. É possível consultar o {{site.data.keyword.slapi_short}} para obter o ID do pacote de suspensão de faturamento usando o keyName `SUSPEND_CLOUD_SERVER`. Para obter um exemplo sobre a procura por pacotes do servidor, consulte [Entendendo e construindo um pedido usando a {{site.data.keyword.slapi_short}} CLI de pedido ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/article/understanding-ordering/){: new_window}.

## Detalhes do faturamento

É importante entender quais custos param de acumular e quais custos persistem quando a instância de servidor virtual é desligada.

| Recurso                      | Faturamento interrompido   | Faturamento persistente |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          | ![Ícone de visto](../../icons/checkmark-icon.svg) |                  |
| RAM                           | ![Ícone de visto](../../icons/checkmark-icon.svg) |                  |
| Velocidade da porta                    | ![Ícone de visto](../../icons/checkmark-icon.svg) |                  |
| Licenças do sistema operacional     | ![Ícone de visto](../../icons/checkmark-icon.svg) |                  |
| Complementos de monitoramento          | ![Ícone de visto](../../icons/checkmark-icon.svg) |                  |
| Endereços IP públicos secundários |                   | ![Ícone de visto](../../icons/checkmark-icon.svg) |
| Armazenamento                       |                   | ![Ícone de visto](../../icons/checkmark-icon.svg) |
{: row-headers}
{: class="comparison-table"}
{: caption="Tabela 1. Detalhes do recurso de faturamento" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the resource. The column headers identify whether billing stops or persists when your instance is powered off. To understand whether billing stops or persists for a resource, navigate to the row in the table, and find the billing information you are interested in."}  

Quando você provisiona uma instância de servidor virtual que suporta o recurso de suspensão de faturamento, os tempos de uso são calculados por segundo para o tempo de uso e para o tempo de suspensão de sua instância de servidor virtual. Mesmo que você nunca inicie o recurso de suspensão de faturamento desligando sua instância, o faturamento é calculado por segundo do ciclo de vida da instância.
{:note}

### Encargo mínimo de uso
As instâncias de servidor virtual que suportam o recurso de suspensão de faturamento podem ter um encargo de uso
mínimo aplicado em alguns casos. Se o uso for maior que 25%, você será faturado por esse uso. Se o uso for menor que 25%, você será cobrado por 25% das horas em que a instância existiu dentro do ciclo de faturamento atual.

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

Ao suspender o faturamento em uma instância de servidor virtual, o faturamento para o armazenamento
associado persiste, mas não é possível acessar os dados armazenados enquanto a instância de servidor virtual está
desligada. Ao retomar o faturamento na instância, será possível acessar os dados novamente.

### Endereços IP

Todos os endereços IP públicos são retidos para você quando o faturamento é suspenso para sua instância de servidor virtual.

### Limitações

As instâncias de servidor virtual que são suspensas continuam a contar para a cota do dispositivo em toda a
conta. Para obter mais informações sobre os limites de instância, consulte [Perguntas frequentes: servidores virtuais](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#concurrent).

## Próximas Etapas
Após provisionar um servidor virtual que suporte a suspensão de faturamento, será possível começar a suspender e retomar o faturamento no dispositivo.

Quando o faturamento é suspenso em uma instância de servidor virtual, não é possível concluir todas as mesmas
ações na instância até que o faturamento para o dispositivo seja retomado. É possível visualizar se o seu dispositivo está parado, bem como a data relevante em que o status foi mudado, por meio do {{site.data.keyword.slapi_short}} ou acessando a página Detalhes do dispositivo no {{site.data.keyword.slportal}}.

Para suspender o faturamento em uma instância de servidor virtual, desligue o servidor virtual. Para obter mais informações, veja [Gerenciando servidores virtuais](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
