---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-05"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Considerações de recurso para instâncias de servidor virtual
{: #capacity-considerations}

## O que está acontecendo?

Ao provisionar um servidor virtual, é possível receber a mensagem de erro a seguir:

```
There is insufficient capacity to complete the request.
```
{:screen}

Quando o fornecimento falha, todas as instâncias de servidor virtual dessa solicitação específica falham.
{:tip}

## Por que isso está acontecendo?

Ocorre um erro quando há recursos insuficientes disponíveis no roteador ou no data center para atender à solicitação de serviço. Existem vários motivos pelos quais você pode receber esse erro. A disponibilidade de recurso muda frequentemente, portanto, você pode esperar e tentar novamente mais tarde.

## Como corrigi-lo

É possível tentar provisionar novamente usando as estratégias a seguir:

1. Provisionar especificando um roteador diferente.  
2. Provisão sem especificar um roteador.
3. Provisão em um data center diferente.
4. Provisionar menos instâncias.
5. Difundir instâncias provisionando para múltiplos data centers.
6. Provisionar tamanhos menores de instância.
7. Alterar o armazenamento VSI de SAN para LOCAL ou de LOCAL para SAN.
