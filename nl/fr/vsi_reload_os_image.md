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

# Nouveau chargement du système d'exploitation en utilisant un modèle d'image
Tout comme un rechargement de système d'exploitation standard, le rechargement d'un terminal à partir d'un modèle d'image permet aux utilisateurs de restaurer ou de reconfigurer un terminal en fonction d'un modèle d'image préexistant associé au compte du portail client utilisé. Lors du processus de rechargement du système d'exploitation standard, les options de configuration du terminal peuvent être sélectionnées individuellement alors que la fonction Charger à partir d'une image charge la configuration exacte du modèle d'image. Vous pouvez toujours ajouter des fonctions facultatives avant d'effectuer le rechargement.
Procédez comme suit pour effectuer un rechargement de système d'exploitation à partir d'un modèle d'image en utilisant la fonction Charger à partir d'une image dans le portail client.
{:shortdesc}

## Exécution d'un rechargement à partir d'un modèle d'image
1. Sauvegardez toutes les données du terminal.
  
   **Remarque :** Les rechargements de système d'exploitation provoquent la suppression de toutes les données du disque dur. Si les données ne sont pas sauvegardées avant le début du rechargement du système d'exploitation, elles ne peuvent pas être extraites. Bluemix (Softlayer) ne sauvegarde pas les données stockées sur les terminaux client et n'est aucunement responsable des pertes de données découlant du rechargement de système d'exploitation.
  
2. Sur la page Liste des unités, sélectionnez **Charger à partir d'une image** dans le menu **Actions** pour le terminal souhaité.

3. Sélectionnez la case à cocher du modèle d'image souhaité pour sélectionner le modèle d'image qui sera chargé sur le terminal.

   **Remarque :** Avant le rechargement, le modèle d'image est copié dans le centre de données contenant le terminal, s'il ne s'y trouve pas déjà. Si le modèle d'image doit être copié dans le centre de données approprié, des frais supplémentaires peuvent être appliqués si le modèle n'est pas supprimé de l'emplacement après le rechargement du système d'exploitation.
  
4. Déterminez si vous souhaitez ajouter des fonctions supplémentaires. Toute fonction supplémentaire sélectionnée est ajoutée au terminal lors du processus de rechargement.
   
   <table>
   <CAPTION>Tableau 1. Fonctions facultatives</CAPTION>
   <THEAD>
   <TR>
   <th>Fonctions facultatives</th>
   <th>Procédure</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   </tr>
   <tr>
   <td>Oui, je souhaite ajouter des fonctions facultatives.</td>
   <td>
   <ol>
   <li>Cliquez sur <b>Charger Image Sélectionnée</b>.</li>
   <li>Consultez la configuration de l'image et continuez ou annulez cette action.</li>
   <li>Cliquez sur <b>Confirmer le rechargement du système d'exploitation</b> pour confirmer l'action et commencer le processus de rechargement du système d'exploitation.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Non, je ne souhaite pas ajouter de fonctions facultatives.</td>
   <td>Cliquez sur <b>Afficher Fonctions En Option</b>.</td>
   </tr>
   </TBODY>
   </table>

5. Configurez des options supplémentaires, en fonction de vos besoins. Pour plus de détails, consultez les informations suivantes.
   
   <dl>
   <dt>Script de Post-Installation</dt>
   <dd>Ajoute un script de post-installation (existant ou nouveau).</dd>
   <dt>Clé SSH</dt>
   <dd>Ajoute une clé SSH au terminal lors de l'action de rechargement. </dd>
   <dt>Réinitialiser Mot de passe IPMI</dt>
   <dd> Cette option est disponible uniquement pour les terminaux physiques. </dd>
   <dt>Appliquer les mises à jour du BIOS de la carte mère</dt>
   <dd>Cette option est disponible uniquement pour les terminaux physiques. </dd>
   <dt>Appliquer les mises à jour du microcode pour tous les disques durs</dt>
   <dd>Cette option est disponible uniquement pour les terminaux physiques.</dd>
   <dt>Ajouter au pool de secours après le rechargement du système d'exploitation</dt>
   <dd>Cette option est disponible uniquement sur les disques physiques et doit être approuvée en interne avant d'être disponible sur un compte.</dd>
   <dt>Effacer tous les disques durs</dt>
   <dd> Cette option est disponible uniquement sur les terminaux physiques et requiert des droits utilisateur spéciaux définis par l'administrateur de compte.</dd>
   <dt>Rechargement du système d'exploitation avec préservation du disque</dt>
   <dd>Conserve toutes les données sur le disque principal pendant le processus de rechargement de système d'exploitation. Cette conservation provoque la conversion de l'unité principale en terminal de stockage portable. Cette option est disponible uniquement sur les terminaux virtuels et génère des frais supplémentaires en fonction des modèles de facturation (horaire ou mensuel) du terminal. Les frais peuvent être annulés en annulant le terminal de stockage portable à tout moment après sa création.</dd>
   </dl>

6. Cliquez sur **Charger Image Sélectionnée**.

7. Vérifiez la configuration de l'image puis cliquez sur **Suivant** pour passer à l'écran suivant ou sur **Annuler** pour annuler l'action.

   **Remarque :** Une fois que vous avez cliqué sur **Suivant**, tous les ports réseau du terminal sont systématiquement arrêtés et le terminal devient indisponible pendant une durée maximale de 15 minutes. Pendant cette période, l'action peut être annulée à tout moment en cliquant sur **Annuler**. Vous disposez de 15 minutes après avoir cliqué sur **Suivant** pour l'étape suivante, sinon il est nécessaire d'effectuer à nouveau la procédure. Il s'agit d'une mesure de sécurité permettant de garantir qu'aucune donnée supplémentaire n'est ajoutée à un terminal entre la confirmation de la configuration et le lancement du rechargement du système d'exploitation.

8. Cliquez sur **Confirmer le rechargement du système d'exploitation** pour confirmer l'action et commencer le processus de rechargement du système d'exploitation. Cliquez sur **Annuler** pour annuler l'action.

## Etape suivante
Une fois l'opération de rechargement du système d'exploitation lancée, le terminal passe hors ligne et l'opération commence.
La durée du rechargement du système d'exploitation varie en fonction de la configuration en cours et de la nouvelle configuration du terminal.
Si le rechargement dure plus de 24 heures, contactez notre équipe de support. Lorsque le terminal est à nouveau en ligne, il fonctionne comme cela a été défini dans la section Nouvelle configuration. Toutes les données précédemment sauvegardées sur le terminal sont perdues mais peuvent être restaurées si une sauvegarde a été effectuée avant le rechargement. Dans le cas contraire, les données ne peuvent pas être extraites.

 Pour enregistrer à nouveau votre terminal avec eVault, voir [Re-registering your device with eVault ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
