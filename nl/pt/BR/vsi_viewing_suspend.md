---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-28"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Visualizando o recurso de suspensão de faturamento
{: #viewing-suspend-billing-feature}

## Antes de iniciar
Primeiro, navegue para o menu de dispositivo e assegure-se de que tenha as permissões de conta corretas para concluir a tarefa. 

* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assegure-se de ter quaisquer permissões de conta necessárias e de ter acesso ao dispositivo. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões. 

Para obter mais informações sobre permissões, veja [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Visualizando o recurso de suspensão de faturamento 
Para determinar se a sua instância de servidor virtual suporta o recurso de suspensão de faturamento, use as etapas a seguir:

1. No menu **Dispositivos**, selecione **Lista de dispositivos**. 
2. Na **Lista de dispositivos**, clique no nome da instância de servidor virtual. 
3. Na seção **Detalhes da instância**, é possível visualizar se a instância de servidor virtual suporta o recurso de suspensão de faturamento. 

| Campo                                 | Valor                     |
| --------------------------------------| ------------------------- |
| Faturamento suspenso: ativado no desligamento | O recurso é suportado.     |
| Faturamento suspenso: indisponível          | O recurso não é suportado. |
{: caption="Tabela 1. Detalhes da suspensão de faturamento" caption-side="top"}

## Visualizando o recurso de suspensão de faturamento por meio da API do SoftLayer

O comando a seguir é uma solicitação de exemplo de verificação se a instância de servidor virtual suporta o recurso de suspensão de faturamento por meio do {{site.data.keyword.slapi_short}}.

A solicitação e a resposta JSON a seguir é um exemplo genérico.
{:note}

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
1. [Suspender faturamento](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [Gerenciando servidores virtuais](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

