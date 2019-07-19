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


# Considérations relatives aux ressources pour les instances de serveur virtuel 
{: #capacity-considerations}

## Quel est le problème ?

Lorsque vous mettez à disposition un serveur virtuel, le message d'erreur suivant peut s'afficher :

```
There is insufficient capacity to complete the request.
```
{:screen}

Lorsque la mise à disposition échoue, toutes les instances de serveur virtuel faisant partie de cette demande spécifique échouent.
{:tip}

## Pourquoi ?

Une erreur se produit lorsque le nombre de ressources disponibles est insuffisant dans le routeur ou dans le centre de données pour répondre à la demande de service. Il existe une série de raisons pour lesquelles cette erreur peut se produire. La disponibilité des ressources change fréquemment, et il est donc conseillé d'attendre et de réessayer plus tard.

## Comment résoudre le problème ?

Vous pouvez tenter une nouvelle mise à disposition à l'aide des stratégies suivantes :

1. Spécifiez un routeur différent lors de la mise à disposition.  
2. Ne spécifiez aucun routeur lors de la mise à disposition.
3. Effectuez la mise à disposition dans un centre de données différent.
4. Mettez à disposition un nombre d'instances plus réduit.
5. Répartissez les instances en effectuant une mise à disposition vers plusieurs centres de données.
6. Mettez à disposition des tailles d'instances plus réduites.
7. Faites passer le stockage VSI de SAN à LOCAL ou de LOCAL à SAN.
