---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-30"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Gestion des serveurs virtuels
{: #managing-virtual-servers}

Dans la liste des terminaux, vous pouvez gérer des serveurs virtuels et d'autres terminaux, tels que des serveurs Bare Metal et des pare-feu VLAN.
{:shortdesc}

Dans la liste de terminaux, le type des serveurs virtuels est *Virtuel*. Les serveurs Bare Metal sont indiqués avec le type *Serveur*. Les hôtes dédiés sont de type *Hôtes virtuels dédiés*. Un grand nombre d'interactions disponibles pour les terminaux sont similaires, mais pour chaque type de terminal, il existe des interactions spécifiques.

Les tâches de gestion de serveur virtuel suivantes sont disponibles dans la liste des terminaux :
* Réinitialisation -  Mise hors tension immédiate d'un terminal puis remise sous tension.
* Mise sous tension/hors tension - Mise sous tension ou hors tension d'un terminal à distance.
* Attribution d'un nouveau nom - Modification ou mise à jour d'un nom de terminal.
* Annulation - Fin d'utilisation d'un terminal. Les terminaux peuvent être annulés immédiatement ou au moment d'un anniversaire de facturation. Une fois l'annulation de votre terminal confirmée, l'action ne peut plus être annulée. Aucun remboursement n'est effectué pour les annulations immédiates.

Procédez comme suit afin d'effectuer les tâches de gestion pour vos serveurs virtuels à partir de la liste des terminaux dans le portail client :  
1. Connectez-vous au portail [{{site.data.keyword.slportal_full}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques. 
2. Dans le menu **Unités**, sélectionnez **Liste d'unités**.
3. Cliquez sur **Actions** pour le terminal à gérer et sélectionnez la tâche de gestion souhaitée.

**Astuces :** 
* Vous pouvez interagir avec les serveurs dans le portail {{site.data.keyword.slportal}} soit dans la vue Instantané (récapitulatif de votre terminal), soit dans l'écran Détails de l'unité (liste détaillée complète). Pour afficher votre serveur et interagir avec ce dernier dans la vue Instantané, cliquez sur la flèche en regard du nom du terminal pour développer la vue. Pour afficher votre serveur et interagir avec ce dernier dans l'écran Détails de l'unité, cliquez sur le nom de terminal du serveur.
* Vous pouvez ajouter des remarques à un terminal à tout moment à partir de l'onglet **Configuration**. Les remarques vous permettent d'identifier des détails sur le terminal, son utilisation et les actions effectuées sur ce dernier.

## Que se passe-t-il ensuite ?
* **Réamorçage**

    Le réamorçage est l'une des actions les plus simples réalisées sur un terminal. Le réamorçage d'un terminal entraîne la mise hors tension immédiate du terminal, suivie d'une mise sous tension. Il est réalisé pour différentes raisons qui dépendent du terminal et des besoins professionnels de chaque utilisateur. Les réamorçages de terminaux peuvent s'effectuer à partir de la liste des unités ou à partir de l'affichage des unités d'un terminal spécifique. Les serveurs virtuels peuvent être réamorcés à tout moment.  

* **Mise sous tension/hors tension**

    Si le terminal a été mis hors tension, il reste à cet état et doit être mis sous tension manuellement à l'aide de la procédure ci-dessus. Les utilisateurs ne peuvent pas interagir avec un terminal lorsque ce dernier est hors tension. Si le serveur virtuel prend en charge la fonction d'interruption de facturation, la facturation est interrompue pour certaines ressources de traitement. Vous ne pouvez pas exécuter toutes les actions de gestion sur une instance tant que la facturation n'a pas repris. Pour plus d'informations, voir [A propos de l'interruption de facturation (bêta)](vsi_about_suspend.html). Pour savoir si votre instance de serveur virtuel prend en charge la fonction d'interruption de facturation, voir [Affichage de la fonction d'interruption de facturation](vsi_viewing_suspend.html). Si le terminal a été mis sous tension, les utilisateurs peuvent interagir avec lui normalement. Il reste sous tension jusqu'à ce qu'une action soit effectuée.

* **Attribution d'un nouveau nom**

  Une fois le terminal renommé, le nom est automatiquement mis à jour dans le portail {{site.data.keyword.slportal}}. Lorsque vous effectuez une recherche dans le portail {{site.data.keyword.slportal}}, utilisez le nouveau nom de terminal pour rechercher le contenu associé. Répétez les étapes précédentes pour renommer le terminal une nouvelle fois.

* **Annulation**

  Une fois l'annulation confirmée, le processus d'annulation du terminal commence. Si une annulation immédiate est demandée, le terminal est annulé immédiatement. Si l'annulation d'une date anniversaire de facturation a été demandée, le terminal reste actif jusqu'à la date anniversaire de facturation suivante. Dès son annulation, le terminal disparaît de la liste des terminaux du portail {{site.data.keyword.slportal}}. Les éléments de facturation sont également retirés des factures lorsque les soldes restants sont payés sur le terminal, le cas échéant. Si vous avez des questions sur la facture d'un terminal annulé, ouvrez un ticket et sélectionnez Demande de comptabilité en objet. Aucun remboursement n'est effectué pour les annulations immédiates.
  
## Etapes suivantes
Si vous avez besoin de configurer à nouveau un serveur virtuel existant, voir [Nouvelle configuration d'un serveur virtuel existant](../vsi/vsi_reconfigure.html).

