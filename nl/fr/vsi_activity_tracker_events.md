---

copyright:
  years: 2016, 2018
lastupdated: "2018-11-06"

subcollection: virtual-servers

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Evénements du service Activity Tracker
{: #at_events}

En tant qu'agent de sécurité, auditeur ou gestionnaire, vous pouvez utiliser le service {{site.data.keyword.cloudaccesstrailfull}} pour contrôler la manière dont les utilisateurs et les applications interagissent avec les instances de serveur virtuel dans {{site.data.keyword.Bluemix}}. Le propriétaire du compte et les utilisateurs liés au compte peuvent déclencher des événements de serveur virtuel qui sont consignés dans {{site.data.keyword.cloudaccesstrailshort}}.
{:shortdesc}

Le service {{site.data.keyword.cloudaccesstrailshort}} enregistre les activités lancées par l'utilisateur qui modifient l'état d'un service dans {{site.data.keyword.Bluemix_notm}}. Pour en savoir plus, voir [A propos d'{{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov ).

Pour commencer à surveiller les actions de vos utilisateurs, veuillez vous reporter à [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started-with-cla#getting-started-with-cla).

L'initiateur peut être un utilisateur, un service ou une application. Pour qu'un utilisateur puisse générer des événements, il doit avoir accès aux ressources **d'infrastructure** dans la console {{site.data.keyword.Bluemix}}.
{: tip}

## Evénements de l'instance de serveur virtuel
{: #vsi}

Vous pouvez auditer une instance de serveur virtuel tout au long de son cycle de vie au moyen du service {{site.data.keyword.cloudaccesstrailshort}}.

Le tableau ci-dessous répertorie les actions qui génèrent un événement :

| Action | Description |
|----------|---------|
| `audit-log.vsi.provision`             | Un événement est généré lorsqu'un initiateur met à disposition une instance de serveur virtuel.  |
| `audit-log.vsi-port.disable`          | Un événement est généré lorsqu'un initiateur désactive un port dans une instance de serveur virtuel. |
| `audit-log.vsi-port.enable`           | Un événement est généré lorsqu'un initiateur active un port dans une instance de serveur virtuel. |
| `audit-log.vsi-port-speed.update`     | Un événement est généré lorsqu'un initiateur met à jour la vitesse de port dans une instance de serveur virtuel. |
| `audit-log.vsi-image-template.create` | Un événement est généré lorsqu'un initiateur crée un modèle d'image pour une instance de serveur virtuel.  |
| `audit-log.vsi.power-off`             | Un événement est généré lorsqu'un initiateur met hors tension une instance de serveur virtuel.  |
| `audit-log.vsi.soft-power-off`        | Un événement est généré lorsqu'un initiateur effectue une mise hors tension souple sur une instance de serveur virtuel. |
| `audit-log.vsi.force-power-off`       | Un événement est généré lorsqu'un initiateur effectue une mise hors tension forcée sur une instance de serveur virtuel. |
| `audit-log.vsi.reboot`                | Un événement est généré lorsqu'un initiateur redémarre une instance de serveur virtuel. |
| `audit-log.vsi.soft-reboot`           | Un événement est généré lorsqu'un initiateur effectue un redémarrage souple sur une instance de serveur virtuel. |
| `audit-log.vsi.hard-reboot`           | Un événement est généré lorsqu'un initiateur effectue un redémarrage forcé sur une instance de serveur virtuel. |
| `audit-log.vsi.power-on`              | Un événement est généré lorsqu'un initiateur effectue une mise sous tension sur une instance de serveur virtuel. |
| `audit-log.vsi.rename`                | Un événement est généré lorsqu'un initiateur renomme une instance de serveur virtuel. |
| `audit-log.vsi.rescue`                | Un événement est généré lorsqu'un initiateur récupère une instance de serveur virtuel. |
| `audit-log.vsi-security-group.add`    | Un événement est généré lorsqu'un initiateur ajoute un groupe de sécurité à une instance de serveur virtuel. |
| `audit-log.vsi-security-group.remove` | Un événement est généré lorsqu'un initiateur supprime un groupe de sécurité d'une instance de serveur virtuel. |
| `audit-log.vsi.reload`                | Un événement est généré lorsqu'un initiateur effectue un rechargement du système d'exploitation pour une instance de serveur virtuel. |
| `audit-log.vsi.boot`                  | Un événement est généré lorsqu'un initiateur démarre une instance de serveur virtuel à partir d'une image. |
| `audit-log.vsi.reclaim`               | Un événement est généré lorsqu'un initiateur annule une instance de serveur virtuel. |
| `audit-log.vsi.pause`                 | Un événement est généré lorsqu'un initiateur met en pause une instance de serveur virtuel. |
{: caption="Tableau 2. Actions sur l'instance de serveur virtuel" caption-side="top"}



## Affichage d'événements
{: #ui}

Les événements d'{{site.data.keyword.cloudaccesstrailshort}} sont disponibles dans le **domaine de compte** d'{{site.data.keyword.cloudaccesstrailshort}} disponible dans la région {{site.data.keyword.Bluemix_notm}} dans laquelle les événements sont générés. Pour plus d'informations, voir [Affichage des événements
de compte](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events).

Les événements d'{{site.data.keyword.cloudaccesstrailshort}} sont automatiquement renvoyés au service {{site.data.keyword.cloudaccesstrailshort}} dans la région dans laquelle l'action se produit.
