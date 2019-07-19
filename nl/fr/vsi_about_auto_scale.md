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

# A propos d'Auto Scale
{: #about-auto-scale}

Les instances de serveur virtuel Auto Scale pour {{site.data.keyword.cloud}} vous permettent d'automatiser le processus manuel de mise à l'échelle associé à l'ajout ou au retrait d'instances épaulant vos applications métier. Cela vous permet de configurer automatiquement de nouvelles instances à mesure que davantage de ressources sont nécessaires, puis ces instances sont arrêtées et supprimées lorsque la charge supplémentaire diminue. Auto Scale utilise des groupes contenant les règles qui régissent l'expansion ou la contraction de votre environnement. Ces règles utilisent des actions pour ajouter ou supprimer un serveur virtuel en fonction de votre activité et des besoins de l'application. 
{:shortdesc}

La mise à l'échelle automatique active les fonctionnalités suivantes : 

* Une mise à l'échelle automatique et transparente d'instances lorsque des ressources supplémentaires sont requises en présence d'une demande accrue
* Une rétromigration automatique et transparente d'instances par la suppression des ressources inutiles en cas de baisse de la demande (économies d'argent)
* Déclencheurs de mise à l'échelle flexibles : pourcentage d'UC, bande passante sortante publique et privée, bande passante entrante publique et privée 
* Des mises à jour quasi en temps réel du statut de l'activité de mise à l'échelle des groupes 
* Une intégration facultative de réseaux locaux virtuels et d'équilibreurs de charge locaux

La mise à l'échelle peut être appliquée dans deux solutions métier courantes :

| Solution | Description |
| -------- | ----------- |
| [Mise à l'échelle basée planning](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling) | Utilisez la mise à l'échelle basée planning pour définir des règles pour les pics d'utilisation ponctuels (par exemple, les week-ends ou les jours fériés). La mise à l'échelle basée planning peut être utilisée lorsqu'une en entreprise prévoit des pics du trafic, par exemple un site de réseau social qui nécessite des ressources supplémentaires en fonction d'un calendrier. |
| [Mise à l'échelle basée ressources](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling) |Utilisez la mise à l'échelle basée ressources pour définir des règles pour les pics d'utilisation irréguliers en fonction de l'utilisation des ressources. Des pics de trafic irréguliers peuvent se produire en cas d'efforts pour la mise sur le marché d'un produit ou lorsqu'un site de commerce électronique procède à des soldes et que des ressources sont requises pour soutenir les temps de réponse. |
{: caption="Tableau 1. Solutions de mise à l'échelle automatique" caption-side="top"}

Si vous n'êtes pas l'administrateur du compte, votre compte d'utilisateur doit inclure le droit d'utiliser la mise à l'échelle automatique. L'administrateur du compte peut accorder le droit d'utilisateur à partir de la console {{site.data.keyword.cloud_notm}}. Pour en savoir plus sur la mise à jour des droits, voir [Configuration des droits utilisateur pour la mise à l'échelle automatique](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale).
{:note}


