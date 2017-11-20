---



copyright:
  years: 2017
lastupdated: "2017-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

#  Rechargement du système d'exploitation
Vous pouvez recharger le système d'exploitation sur un terminal à tout moment pour restaurer un terminal à son état de fonctionnement d'origine ou pour reconfigurer un terminal avec un autre logiciel. Un rechargement du système d'exploitation supprime toutes les données du terminal et applique la configuration d'origine, comme cela est spécifié lors de la configuration du rechargement du système d'exploitation. Si les données ne sont pas sauvegardées avant le rechargement, elles seront définitivement supprimées et ne pourront pas être extraites car les rechargements du système d'exploitation retire toutes les données du terminal.
{:shortdesc}

**Important :** Si vous souhaitez conserver vos données, sauvegardez-les avant toute opération de rechargement.

## Rechargement
1. Dans la **Liste des unités**, cliquez sur le serveur pour lequel un rechargement du système d'exploitation est requis.
2. Dans le menu **Actions** dans la partie supérieure gauche de la page, sélectionnez **Rechargement du système d'exploitation**.
3. Déterminez si vous souhaitez recharger la configuration existante ou recharger le terminal avec une nouvelle configuration.

   <table>
   <CAPTION>Tableau 1. Options de rechargement du système d'exploitation</CAPTION>
   <THEAD>
   <TR>
   <th>Type de rechargement</th>
   <th>Procédure</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Si vous souhaitez recharger un utilisant une nouvelle configuration...</td>
   <td>
   <ol>
   <li>Cliquez sur <b>Editer</b> pour la catégorie à mettre à jour.</li>
   <li>Sélectionnez le nouveau logiciel à appliquer au terminal dans la liste déroulante <i>Sélectionner le logiciel</i>.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Si vous souhaitez effectuer un rechargement en utilisant la configuration existante...</td>
   <td>Passez à l'étape suivante.</td>
   </tr>
   </TBODY>
   </table>

4. Déterminez si un script de post-installation doit être appliqué après la mise à disposition du terminal.

   Si vous souhaitez appliquer un script de post-installation, sélectionnez le script dans la liste déroulante Script existant ou entrez l'URL complète du nouveau script.  Sinon, passez à l'étape suivante.

5. Pour les terminaux physiques, déterminez si des partitions installées doivent être ajoutées ou retirées ou si la configuration doit rester identique.
   
   <table>
   <CAPTION>Tableau 2. Options d'action de partition</CAPTION>
   <THEAD>
   <TR>
   <th>Action de partition</th>
   <th>Procédure</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Ajout de partitions installées...</td>
   <td>
   <ul>
   <li>Cliquez sur le lien <b>Ajouter autre partition</b>.</li>
   <li>Entrez le nom exact de la partition.</li>
   <li>Entrez la taille de la partition (en Go). Si vous le souhaitez, vous pouvez sélectionner Développer afin que la partition occupe l'espace restant.
   <p><b>Remarque :</b> Vous pouvez sélectionner une seule partition à la fois pour cette opération. Cette partition est plus importante que la taille indiquée et occupe toute la capacité disponible. La capacité de cette partition est calculée en soustrayant la taille de toutes les autres partitions de la capacité totale fournie dans la section des partitions installées.</p>
   </li>
   </ul>
   </td>
   </tr>
   <tr>
   <td>Suppression de partitions installées...</td>
   <td>Cliquez sur l'icône <b>Supprimer</b> pour supprimer la partition.</td>
   </tr>
   <tr>
   <td>Conservation de la configuration existante...</td>
   <td>Passez à l'étape suivante.</td>
   </tr>
   </TBODY>
   </table>
    
6. Déterminez le nombre de clés SSH à appliquer au terminal.

7. Sélectionnez les cases à cocher appropriées pour les options que vous souhaitez appliquer au terminal pendant ou après le rechargement du système d'exploitation.

   **Remarque :** Les options varient en fonction du terminal. Toutes les options ne sont pas disponibles pour chaque terminal.

8. Cliquez sur le bouton **Recharger configuration ci-dessus** pour accéder à la fenêtre en incrustation Vérifier. Cliquez sur le bouton **Annuler** pour annuler les modifications effectuées et quitter l'écran.

9. Vérifiez que les informations s'affichant dans la section Nouvelle configuration sont correctes.  

10. Cliquez sur le bouton **Confirmer le rechargement du système d'exploitation** pour confirmer le rechargement et effectuer cette opération. Cliquez sur le bouton **Annuler** pour annuler l'action.

## Etape suivante
Une fois l'opération de rechargement du système d'exploitation lancée, le terminal passe hors ligne et l'opération commence.
La durée du rechargement du système d'exploitation varie en fonction de la configuration en cours et de la nouvelle configuration du terminal.
Pendant la configuration, la durée minimale du rechargement du système d'exploitation s'affiche sur chaque écran.
Il s'agit d'une estimation effectuée par le système et mise gracieusement à votre disposition. Si le rechargement dure plus de 24 heures,
contactez notre équipe de support. Lorsque le terminal est à nouveau en ligne, il fonctionne comme cela a été défini dans la section Nouvelle configuration. Toutes les données précédemment sauvegardées sur le terminal sont perdues mais peuvent être restaurées si une sauvegarde a été effectuée avant le rechargement.
Dans le cas contraire, les données ne peuvent pas être extraites.
 
Pour enregistrer à nouveau votre terminal avec eVault, voir [Re-registering your device with eVault ![External link icon](../icons/launch-glyph.svg "External link icon")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
