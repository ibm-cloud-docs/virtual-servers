---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Foire aux questions : Auto Scale
{: #faqs-auto-scale}

## Auto Scale prend-t-il en charge les instances Auto Scale Bare Metal ?
{: faq}

Actuellement, Auto Scale ne prend pas en charge les instances Bare Metal Auto Scale.

## Auto Scale fonctionne-t-il avec des équilibreurs de charge ?
{: faq}

Oui, Auto Scale fonctionne actuellement avec des équilibreurs de charge locaux et utilise en partie l'API d'équilibreur de charge. Pour plus d'informations, voir [Etagement des équilibreurs de charge](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Quelles sont les différentes règles de résiliation de serveur Auto Scale ?
{: faq}

On distingue trois règles de résiliation de serveur Auto Scale : le plus récent, le plus ancien et le plus proche de la charge suivante. Elles décrivent comment le groupe choisit le membre à retirer lors d'une révision à la baisse des serveurs. Pour plus d'informations, voir [Règle de résiliation](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Qu'entend-on par règles Auto Scale ?
{: faq}

Une règle contient un ensemble d'actions et un ensemble de déclencheurs. Elles sont généralement composées de ces éléments : nom, transition, action et déclencheurs. Pour plus d'informations, voir [Règles](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Qu'est-ce que les déclencheurs Auto Scale ?
{: faq}

Les déclencheurs sont les commandes conditionnelles pouvant être satisfaites (uniquement si le groupe est actif). Il existe trois types de déclencheur : ponctuel, répétitif, et utilisation des ressources. Pour plus d'informations, voir [Déclencheurs](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Quel est le nombre maximal d'instances de serveur virtuel ?
{: faq}

Ceci indique le nombre maximal de membres pouvant être présents dans un groupe. Pour plus d'informations, voir [Nombre maximal d'instances de serveur virtuel](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Quel est le nombre minimal d'instances de serveur virtuel ?
{: faq}

Ceci indique le nombre minimal de membres pouvant être présents dans un groupe. Pour plus d'informations, voir [Nombre minimal d'instances de serveur virtuel](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Qu'est-ce qu'un actif Auto Scale ?
{: faq}

Un actif est un membre fixe d'un groupe qui n'est pas pris en compte dans le nombre de membres et qui n'est contrôlé automatiquement d'aucune manière. L'actif est présent pour fournir des informations supplémentaires aux déclencheurs de règle. Par exemple, un actif peut être pris en compte dans le pourcentage d'UC de tout le groupe si ce pourcentage est utilisé comme déclencheur. Actuellement un groupe ne peut avoir que des actifs de type invité virtuel et leur nombre n'est pas limité. En outre, un groupe n'est pas obligatoire.

## Qu'est-ce qu'un groupe Auto Scale ?
{: faq}

Un groupe (groupe de mise à l'échelle) est une collection spécifique d'actifs, de membres, d'équilibreurs de charge, de réseaux locaux virtuels et de règles au niveau d'un groupe. Un groupe possède tous les paramètres de mise à l'échelle, y compris les limites du nombre de membres et les modèles de membre de l'instance de serveur virtuel mis à l'échelle. 

## Qu'est-ce qu'un membre Auto Scale ?
{: faq}

Un membre est une unité mise à l'échelle dans un groupe. Les membres sont automatiquement mis à disposition ou libérés compte tenu des actions de la règle. Actuellement, tous les membres sont des instances de serveur virtuel. Dans un groupe actif, le nombre de membres ne peut jamais être inférieur au minimum ou supérieur au maximum fixés. Bien que les membres soient généralement ajoutés par les actions d'une règle, ils peuvent également être ajoutés manuellement par un utilisateur.
