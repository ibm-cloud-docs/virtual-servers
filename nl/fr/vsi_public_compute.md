---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Compute
{: #compute}

Les profils Compute sont recommandés pour les charges de travail avec des demandes d'unité centrale importantes, comme les fortes charges de travail de trafic Web, le traitement de lots de production et les serveurs Web frontaux.

L'offre est disponible dans les profils suivants :

<table>
<CAPTION>Tableau 1. Profils Compute</CAPTION>
<THEAD>
<TR>
<th>Profil</th>
<th>UC virtuelle</th>
<th>RAM</th>
<th>Type de stockage</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>C1.1x1</td>
<td>1</td>
<td>1 Go</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.2x2</td>
<td>2</td>
<td>2 Go</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.4x4</td>
<td>4</td>
<td>4 Go</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.8x8</td>
<td>8</td>
<td>8 Go</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.16x16</td>
<td>16</td>
<td>16 Go</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.32x32</td>
<td>32</td>
<td>32 Go</td>
<td>SAN</td>
</tr>
</TBODY>
</table>

**Remarques sur le stockage :**
* Disque d'amorçage principal SAN (25 ou 100 Go) avec des disques supplémentaires disponibles, jusqu'à 2 To chacun (5 disques autorisés au total).
* La tarification des serveurs virtuels publics utilisant le stockage SAN inclut l'unité centrale virtuelle, la mémoire et un disque d'amorçage principal. Le prix des disques supplémentaires dépend de la taille du disque et de la quantité sélectionnée.  

Les profils Compute sont disponibles dans tous les centres de données.

Tous les systèmes d'exploitation pris en charge (RHEL, CentOS, Windows, Ubuntu et autres), les bases de données prises en charge et les modules logiciels complémentaires sont également disponibles avec cette offre.  
