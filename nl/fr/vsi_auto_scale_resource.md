---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestion des pics de trafic avec mise à l'échelle automatique basée ressources
{: #managing-resourced-based-auto-scaling}

Le lancement d'un nouveau produit ou des soldes sur un produit existant peuvent générer un pic du trafic sur votre site Web. Ce pic peut affecter vos temps de réponse, ce qui a un impact sur l'expérience client sur votre site Web. {{site.data.keyword.cloud}} Auto Scale vous permet de répondre automatiquement aux pics de trafic. Vous pouvez utiliser la mise à l'échelle automatique basée ressources pour contrôler ces pics de trafic.
{:shortdesc}

## Avant de commencer
Tout d'abord, accédez au menu Unité et assurez-vous de disposer des droits de compte appropriés pour exécuter les tâches.

* Accédez au menu Unité de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des droits de compte et accès aux unités requis. Si vous n'êtes pas l'administrateur du compte, votre compte d'utilisateur doit inclure le droit d'utiliser la mise à l'échelle automatique. Pour en savoir plus sur la mise à jour des droits pour utiliser la mise à l'échelle automatique, voir [Configuration des droits utilisateur pour la mise à l'échelle automatique](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale).
Seul le propriétaire de compte ou un utilisateur disposant de droit d'infrastructure classique **Gérer les utilisateurs** peut modifier les droits. 

Pour plus d'informations sur les droits, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux unités](/docs/vsi?topic=virtual-servers-managing-device-access).

## Ajout d'un groupe Auto Scale
{: #adding-auto-scale-group}

Par exemple, un site Web d'e-commerce basé à Dallas, Texas, requiert que trois serveurs virtuels soient en ligne en tout temps. Des pointes de l'activité sont constatées entre 9h00 et 17h00 chaque jour de la semaine lorsque l'entreprise propose des soldes en ligne. Pour maintenir les temps de réponse du site Web, trois autres serveurs virtuels sont requis pendant ces périodes. En outre, lorsque le trafic entrant public moyen sur tous les serveurs virtuels dépasse 5 Mo par seconde pendant 10 minutes, deux autres serveurs virtuels devraient également être déployés. Lorsque le trafic redescend au-dessous de 5 Mo par seconde, ces serveurs virtuels supplémentaires devraient être annulés et retirés. L'objectif est de se limiter à cinq serveurs virtuels pour traiter la hausse du trafic et d'éviter que les serveurs virtuels des semaines ordinaires ne soient impactés par le trafic additionnel durant ces périodes. Les étapes suivantes décrivent comment configurer Auto Scale pour gérer une mise à l'échelle automatique basée ressources.

1. Dans le menu **Unités**, sélectionnez **Mise à l'échelle auto**.
2. Sélectionnez **Ajouter groupe de mise à l'échelle auto**.
3. Configurez un groupe Auto Scale en renseignant d'abord **Group Name** (par exemple, Weekend Scale Up Group), puis sélectionnez le centre de données. 
4. Sélectionnez la règle de résiliation de serveur. Par exemple, si vous sélectionnez **Oldest**, le serveur avec la date de mise à disposition la plus ancienne est sélectionné pour réduire le nombre de serveurs.
5. Indiquez si votre groupe doit être un groupe avec réseaux locaux virtuels multiples et comment répartir le redimensionnement à la baisse entre les paires de réseau local virtuel configurées.
6. Sélectionnez les réseaux locaux virtuels publics et privés sur lesquels mettre à disposition vos serveurs. Si l'accès aux serveurs est effectué depuis l'internet public (si le réseau local virtuel exécute des serveurs Web), ne cochez pas la case **Réseau privé uniquement**.
7. Définissez **Minimum Member Counts** à 3 et **Maximum Member Counts** à 6. Définissez **Cooldown Period** à 0. Comme nous utilisons une mise à l'échelle basée planning, des statistiques ne sont pas collectées pour déclencher des actions de mise à l'échelle.

## Définition de la configuration de membres pour votre groupe
{: #defining-member-configuration}

1. Localisez **Member Configuration** et renseignez les zones **Hostname** et **Domain** pour le serveur de mise à l'échelle. Des suffixes uniques seront ajoutés au nom d'hôte des serveurs ajoutés ultérieurement au groupe.
2. Spécifiez la configuration matérielle des instances de calcul (coeurs, mémoire RAM, etc.)
3. Sélectionnez un système d'exploitation si vous désirez installer le système d'exploitation minimal. Vous pouvez également utiliser une **image publique** ou une **image privée** pour mettre à disposition vos instances.
4. Si les instances requièrent des étapes supplémentaires pour ajouter d'autres logiciels, spécifiez l'URL d'un **Script de post-installation** pour installer ces logiciels. Si vous utilisez un équilibreur de charge pour le groupe, les scripts de post-installation doivent être exécutés avant de placer un membre derrière l'équilibreur de charge.

## Configuration de règles
{: #setting-up-policies}

Dans le scénario, le site Web de commerce électronique utilise une mise à l'échelle basée ressources. Deux règles sont nécessaires : une pour disposer d'une action de mise à l'échelle relative de +3 pour la période requise et une autre pour une action d'absolution de 3 lorsque le pic est passé. La première règle consiste à ajouter les ressources.

1. Défilez jusqu'à **Policies** et cliquez sur **Add Policy**. Renseignez la zone **Policy Name**, (Weekday Scale Up).
2. Sélectionnez l'option de délai de transition du groupe pour **Cooldown Period**.
3. Cliquez sur **Add Trigger** et spécifiez un déclencheur répétitif en sélectionnant **Every** dans la première liste déroulante, puis sélectionnez **Monday, Tuesday, Wednesday, Thursday,** **Friday** et **2:00 PM**\* dans les listes déroulantes ultérieures. La case à cocher **Advanced Edit** vous permet d'indiquer la fréquence du déclencheur sous forme de notation de tâche périodique.
4. Cliquez sur la liste déroulante **Scale By** sous **Action** et sélectionnez **Exact**. Entrez 3 dans la zone **Members**.
5. Cliquez à nouveau sur **Add Policy** pour spécifier la seconde règle qui retire les serveurs chaque après-midi. La période de transition est la même que celle du groupe. Le déclencheur opère chaque lundi, mardi, mercredi, jeudi et vendredi à 22h00, avec une action de mise à l'échelle exacte définie à 3. L'heure qui est entrée dans **Triggers** est basée sur l'heure UTC, c'est pourquoi vous devez sélectionner 2:00 PM pour 9:00 AM (Heure du centre des Etats-Unis) et 10:00 PM pour 5:00 PM (Heure du centre des Etats-Unis). Sous l'heure du centre des Etats-Unis, les horaires deviendraient 1:00 PM et 9:00 PM vu que UTC/GMT ignore l'heure d'été. Voir le site [World Time Server ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} pour obtenir un convertisseur de fuseaux horaires.
6. Configurez un autre groupe avec un délai de transition défini à 0, nommé par exemple Traffic Burst Group, avec un nombre de membres minimum de 0 et maximum 5. Utilisez les mêmes paramètres pour la configuration du groupe et des membres que ceux du groupe Weekday Scale Up, à part le nom du groupe.
7. Cliquez sur **Add Policy** pour ajouter la seconde règle qui régit les deux serveurs supplémentaires lorsque le trafic public entrant moyen dépasse 5 Mo par seconde entre tous les serveurs virtuels pendant 10 minutes.
8. Renseignez la zone **Policy Name**, par exemple : Traffic Burst Group.
9. Sélectionnez l'option de délai de transition du groupe pour **Cooldown Period**.
10. Cliquez sur **Add Trigger**. Conservez la valeur par défaut, **If my**, dans la première zone et sélectionnez **Public Network Incoming Mbps** pour la seconde. Conservez le signe par défaut, >, dans la troisième zone. Dans la quatrième zone, entrez **5** (5 Mo), entrez **600** dans la cinquième zone et sélectionnez **Seconds** dans la dernière, pour correspondre à 10 minutes.
11. Cliquez sur la liste déroulante **Scale By** sous **Action** et sélectionnez **Relative**. Entrez 2 dans la zone **Members**.
12. Cliquez à nouveau sur **Add Policy** pour spécifier la seconde règle qui retire les serveurs une fois que le trafic est redescendu à moins de 5 Mbit/s. La période de transition sera la même que celle du groupe. Le déclencheur sera : trafic sur mon réseau public entrant inférieur à 5 (5 Mbit/s) sur une période de 600 secondes (10 minutes).

Lorsque les deux groupes ont été créés, le groupe Weekday Scale Up crée trois serveurs (le minimum). Les jours de semaine, trois serveurs sont ajoutés à 9h00 (heure du centre des Etats-Unis) et sont retirés à 17h00. Ceci est la seule méthode pour ajouter des membres au groupe ou pour en retirer. Dans un groupe Traffic Burst Group complètement indépendant, deux serveurs sont ajoutés, quand pendant 10 minutes, le trafic public entrant moyen entre tous les membres atteint 5 Mbit par seconde, à concurrence du nombre maximal pour le groupe (5). Une fois que le volume du trafic public entrant reste sous ce seuil pendant 10 minutes, tous les serveurs de ce groupe sont retirés.

