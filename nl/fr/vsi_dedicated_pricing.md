---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-22"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Tarification d'hôte dédié
{: #dedicated-virtual-server-pricing}

La tarification des hôtes dédiés s'effectue à l'heure ou au mois.
{:shortdesc}

La tarification des hôtes dédiés inclut l'unité centrale virtuelle, la mémoire RAM, le stockage local et la vitesse du port de liaison montante lorsque les instances sont mises à disposition sur les hôtes dédiés. Pour plus d'informations sur la tarification, voir [Calculateur de mise à disposition de serveurs virtuels ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

Avec des hôtes dédiés, des disques de stockage local supplémentaires sont disponibles sur le premier, le deuxième, le troisième, le quatrième et le cinquième disques. Il existe une capacité supplémentaire pouvant aller jusqu'à 400 Go sur chaque disque secondaire.

Les instances horaires peuvent être mises à disposition sur les hôtes horaires et mensuels. Les instances mensuelles peuvent uniquement être mises à disposition sur les hôtes mensuels.

| Configuration d'hôte | UC virtuelle	| Mémoire RAM (Go) | Stockage local (Unité SSD - To) |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |  56 	|   242    |        	1,2	          |
| 56x484x1.2         |  56  |   484    |     1,2
|
{: caption="Tableau 1. Configurations d'hôte dédié " caption-side="top"}

La tarification varie en fonction des zones géographiques.
{:note}

Le réseau de stockage SAN (lié par réseau), les systèmes d'exploitation Premium et les modules complémentaires logiciels sont facturés à l'heure ou au mois, en fonction de l'instance mise à disposition sur l'hôte dédié. La tarification de ces composants correspond à l'offre existante sur les instances publiques et les instances dédiées. 

Par exemple, une instance dédiée mise à disposition sur un hôte dédié avec la configuration suivante n'est pas facturée par l'instance. L'UC virtuelle, la mémoire RAM, le stockage local et les vitesses de port de liaison montante sont inclus dans les frais d'hôte dédiés. 

* 8 UC virtuelles
* 16 Go de mémoire RAM
* Unité SSD locale 100 Go - premier disque
* Unité SSD locale 400 Go - deuxième disque
* Unité SSD locale 400 Go - troisième disque
* Liaisons réseau montantes publiques et privées 1 Gbps (hôte dédié) 

