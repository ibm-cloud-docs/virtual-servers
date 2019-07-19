---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-29"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Rétromigration des vitesses de port
{: #downgrading-port-speeds}

Vous pouvez temporairement rétromigrer les vitesses de port pour votre instance de serveur virtuel sans avoir à ouvrir un ticket. Vous pouvez uniquement rétromigrer, déconnecter ou reconnecter à un maximum qui correspond à ce que vous payez. Vous ne pouvez pas effectuer une mise à niveau à partir de cette option. Les changements restent dans la console jusqu'à ce qu'un nouveau changement ait lieu. Aucun changement n'est effectué au niveau de la facturation et la rétromigration temporaire de votre serveur ne réduit pas votre facture. Si vous avez besoin d'une modification permanente de votre vitesse, vous devez ouvrir un ticket de vente.
{:shortdesc}

## Avant de commencer
Tout d'abord, accédez au menu Unité et assurez-vous de disposer des droits de compte appropriés pour exécuter la tâche. 

* Accédez au menu Unité de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des droits de compte et accès aux unités requis. Seul le propriétaire de compte ou un utilisateur disposant de droit d'infrastructure classique **Gérer les utilisateurs** peut modifier les droits. 

Pour plus d'informations sur les droits, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux unités](/docs/vsi?topic=virtual-servers-managing-device-access).

## Rétromigration des vitesses de port
Pour rétromigrer les vitesses de port, procédez comme suit.

1. Dans le menu **Unités**, sélectionnez **Liste des unités**.
2. Sélectionnez le serveur que vous souhaitez mettre à jour.
3. Dans l'onglet **Vue d'ensemble**, accédez à **Détails du réseau.**
4. Sélectionnez la liste déroulante dans **Vitesse** (pour réseau public ou privé) pour rétromigrer ou déconnecter la vitesse de port.

Lorsque vous changez les vitesses de port ou déconnectez vos ports pour une raison ou pour une autre, vous devez changer le serveur manuellement.
{:tip}
