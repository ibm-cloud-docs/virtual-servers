---

copyright:
  years: 2017
lastupdated: "2017-10-23"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Affichage et gestion des moniteurs
{: #viewing-and-managing-monitors}

La surveillance d'un terminal permet aux utilisateurs de lancer des commandes ping de service et des commandes ping lentes afin de garantir que le terminal est en ligne et qu'il répond.
{:shortdesc}

Si aucun écho n'est reçu pendant la période allouée (1 seconde pour les commandes ping de service, 5 secondes pour les commandes ping lentes), une alerte est envoyée à
l'adresse électronique du compte. La mention **ACTIF** dans la zone **Statut** indique qu'un écho a été reçu alors que la mention **INACTIF**
indique le contraire. Si vous avez déjà configuré un moniteur de base, vous pouvez suivre la procédure ci-dessous pour afficher et gérer la surveillance d'un terminal.

   <table>
   <CAPTION>Tableau 1. Affichage et gestion de la surveillance de terminal</CAPTION>
   <THEAD>
   <TR>
   <th>Action</th>
   <th>Procédure</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Affichage des moniteurs</td>
   <td>
   <ol>
   <li>Dans la liste des unités, cliquez sur le <b>Nom de l'unité</b> pour accéder à cet élément.</li>
   <li>Cliquez sur l'onglet <b>Surveillance</b>. Toutes les demandes ping ne sont pas visibles sur la page d'arrivée. (L'onglet <b>Surveillance</b> est visible uniquement si au moins un moniteur est configuré.)</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Ajout d'un moniteur</td>
   <td>
   <ol>
   <li>Sur l'onglet <b>Surveillance</b> de la page Détails de l'unité, cliquez sur <b>Gérer les superviseurs</b> sur le côté droit de la page pour gérer les moniteurs associés à ce terminal.</li>
   <li>Sur la page Moniteurs, cliquez sur l'onglet <b>Ajouter moniteur</b>.</li>
   <li>Sélectionnez l'adresse IP à surveiller dans la liste déroulante <b>Adresse IP</b>.</li>
   <li>Sélectionnez le type de moniteur dans la liste déroulante <b>Type de moniteur</b>.</li>
   <li>Configurez les options de notification. Dans la liste déroulante <b>Avertir ?</b>, sélectionnez <b>Notifier les Utilisateurs</b> pour signaler les problèmes aux utilisateurs ou <b>Ne rien faire</b> pour ne pas générer de notification utilisateur.</li>
   <li>Sélectionnez le délai d'envoi de notification utilisateur dans la liste déroulante <b>Notifier attente</b>.</li>
   <li>Cliquez sur le bouton <b>Ajouter moniteur</b> afin d'ajouter le moniteur pour le terminal. Le nouveau moniteur s'affiche dans la section <b>Editer les superviseurs existants</b> de l'écran.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Edition d'un moniteur existant</td>
   <td>
   <ol>
   <li>Sur la page Moniteurs sous l'en-tête <b>Editer les superviseurs existants</b>, cliquez sur des détails de moniteur pour ouvrir le moniteur afin de pouvoir l'éditer.</li>
   <li>Mettez à jour une des zones suivantes : Type de moniteur, Notifier, Notifier attente.</li>
   <li>Cliquez sur le bouton <b>Mettre à jour</b> pour mettre à jour les détails. Cliquez sur le bouton <b>Annuler</b> pour annuler l'édition.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Suppression d'un moniteur</td>
   <td>
   <ol>
   <li>Sur la page Moniteurs sous l'en-tête <b>Editer les superviseurs existants</b>, cliquez sur l'icône Supprimer en regard des détails du moniteur.</li>
   <li>Cliquez sur le bouton <b>Oui</b> pour supprimer le moniteur. Cliquez sur le bouton <b>Non</b> pour annuler l'action.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Etapes suivantes

- Si un nouveau moniteur a été ajouté, le moniteur apparaît sur l'onglet **Surveillance**. Le moniteur envoie une demande ping au terminal toutes les cinq minutes, attendant une réponse en fonction du type de demande ping sélectionnée. Si la réponse attendue n'est pas reçue, un message électronique est envoyé pendant la période définie à l'adresse de notification correspondant au compte (dans le cas où la notification a été sélectionnée).
- Si un moniteur a été édité, le moniteur continue de fonctionner comme cela est défini dans les détails du moniteur. Si le type est modifié, la période avant la réception de la commande ping attendue est différente. En cas de modification des options de notification, la façon dont les utilisateurs sont avertis des tentatives infructueuses sont modifiées en fonction des nouvelles sélections. Le moniteur reste accessible dans l'onglet **Surveillance**.
- Si un moniteur est supprimé, ce dernier ne fonctionne plus pour le terminal. Toutes les opérations de surveillance associées au moniteur supprimé s'arrêtent et le moniteur ne s'affiche plus sur l'onglet **Surveillance**.
