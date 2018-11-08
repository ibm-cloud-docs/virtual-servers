---



copyright:
  years: 2018
lastupdated: "2018-10-30"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Visualizando o recurso de suspensão de faturamento
É possível visualizar se a instância de servidor virtual suporta o recurso de suspensão de faturamento no
{{site.data.keyword.slportal_full}} ou por meio do {{site.data.keyword.slapi_short}}.

## Visualizando o recurso de suspensão de faturamento no portal do cliente
Para determinar se a instância de servidor virtual suporta o recurso de suspensão de faturamento no
{{site.data.keyword.slportal}}, use as etapas a seguir:

1. Efetue login no [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas. 
2. No menu **Dispositivos**, selecione **Lista de dispositivos**. 
3. Na **Lista de dispositivos**, clique no nome da instância de servidor virtual. 
4. Na guia **Configuração**, na seção **Sistema**, é possível
visualizar se a instância de servidor virtual suporta o recurso de suspensão de faturamento. 

| Campo                                 | Valor                     |
| --------------------------------------| ------------------------- |
| Suspensão de faturamento: ativado no desligamento | O recurso é suportado.     |
| Suspensão de faturamento: indisponível | O recurso não é suportado. |
{: caption="Tabela 1. Detalhes da suspensão de faturamento" caption-side="top"}

## Visualizando o recurso de suspensão de faturamento por meio da API do Softlayer

O comando a seguir é uma solicitação de exemplo para verificar se a instância de servidor virtual suporta o
recurso de suspensão de faturamento no {{site.data.keyword.slapi_short}}.

**Nota**: a solicitação e a resposta JSON a seguir é um exemplo genérico. 

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

O exemplo da resposta JSON para a solicitação é o seguinte:

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

Para obter mais informações, consulte a
[Documentação da API
SLDN ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}.

## Próximas Etapas

Para saber mais sobre o recurso de suspensão de faturamento, revise as seguintes informações:
1. [Sobre a suspensão de faturamento](vsi_about_suspend.html)
2. [Gerenciando servidores virtuais](vsi_managing.html)
