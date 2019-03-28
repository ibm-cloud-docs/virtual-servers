---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Tarification de serveur virtuel dédié
{: #dedicated-virtual-server-pricing}

La tarification des hôtes dédiés s'effectue à l'heure ou au mois.
{:shortdesc}

La tarification des hôtes dédiés est présentée ci-dessous et inclut l'unité centrale virtuelle, la mémoire RAM, le stockage local et la vitesse du port de liaison montante lorsque les instances sont mises à disposition sur les hôtes dédiés.

Avec des hôtes dédiés, des disques de stockage local supplémentaires sont disponibles sur le premier, le deuxième, le troisième, le quatrième et le cinquième disque. Il existe une capacité supplémentaire pouvant aller jusqu'à 400 Go sur chaque disque secondaire.

Les instances horaires peuvent être mises à disposition sur les hôtes horaires et mensuels. Les instances mensuelles peuvent uniquement être mises à disposition sur les hôtes mensuels.

| Configuration d'hôte | Unité centrale virtuelle	| Mémoire RAM (Go) | Stockage local (Unité SSD - To) |	Prix horaire | Prix mensuel |
| ------------------ | ---- | -------- | ---------------------- | ------------ | ------------- |
| 56 x 242 x 1,2 To	     |  56 	|   242    |        	1,2	          |     3,164 USD   | 	2 099 USD    |
{: caption="Tableau 1. Tarification d'hôte dédié" caption-side="top"}

Prenez en compte le fait que les prix varient en fonction des zones géographiques.

Le réseau de stockage SAN (lié par réseau), les systèmes d'exploitation Premium et les modules logiciels complémentaires sont facturés à l'heure ou au mois, en fonction de l'instance mise à disposition sur l'hôte dédié. La tarification de ces composants correspond à l'offre existante sur les instances publiques et les instances dédiées.

Par exemple, une instance dédiée mise à disposition sur un hôte dédié avec la configuration suivante ne sera pas facturée par l'instance. L'UC virtuelle, la mémoire RAM, le stockage local et les vitesses de port de liaison montante sont inclus dans les frais d'hôte dédiés.

* 8 UC virtuelles
* 16 Go de mémoire RAM
* Unité SSD locale 100 Go - premier disque
* Unité SSD locale 400 Go - deuxième disque
* Unité SSD locale 400 Go - troisième disque
* Liaisons réseau montantes publiques et privées 1 Gbps (hôte dédié)
