---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestion des pics de trafic avec mise à l'échelle automatique basée planning
{: #managing-schedule-based-auto-scaling}

Les pics de trafic Web ont du bon et du mauvais. D'un côté, ils signifient une plus grande affluence sur votre site, de l'autre, une pointe de l'activité peut affecter vos temps de réponse. La mise à l'échelle automatique {{site.data.keyword.cloud}} vous permet de revoir automatiquement vos serveurs à la hausse ou à la baisse compte tenu de vos besoins métier. Vous pouvez utiliser la mise à l'échelle automatique basée planning pour contrôler ces pics de trafic.
{:shortdesc}

## Avant de commencer
Tout d'abord, accédez au menu Unité et assurez-vous de disposer des droits de compte appropriés pour exécuter les tâches.

* Accédez au menu Unité de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des droits de compte et accès aux unités requis. Si vous n'êtes pas l'administrateur du compte, votre compte d'utilisateur doit inclure le droit d'utiliser la mise à l'échelle automatique. Pour en savoir plus sur la mise à jour des droits pour utiliser la mise à l'échelle automatique, voir [Configuration des droits utilisateur pour la mise à l'échelle automatique](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale).
Seul le propriétaire de compte ou un utilisateur disposant de droit d'infrastructure classique **Gérer les utilisateurs** peut modifier les droits. 

Pour plus d'informations sur les droits, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux unités](/docs/vsi?topic=virtual-servers-managing-device-access).

## Ajout d'un groupe Auto Scale
{: #add-auto-scale-group}

Dans ce scénario, un site Web social basé à Dallas, Texas, connaît des pics d'activité le week-end. Deux serveurs virtuels au minimum sont requis par le site du lundi au vendredi. Par contre, deux serveurs virtuels supplémentaires sont nécessaires chaque week-end en raison de l'augmentation du trafic. Les étapes suivantes décrivent comment configurer Auto Scale pour gérer une mise à l'échelle automatique basée planning.

1. Dans le menu **Unités**, sélectionnez **Mise à l'échelle auto**.
2. Sélectionnez **Ajouter groupe de mise à l'échelle auto**.
3. Configurez un groupe Auto Scale en renseignant d'abord **Group Name** (par exemple, Weekend Scale Up Group), puis sélectionnez le centre de données. 
4. Sélectionnez la règle de résiliation de serveur. Par exemple, si vous sélectionnez **Oldest**, le serveur avec la date de mise à disposition la plus ancienne est sélectionné pour réduire le nombre de serveurs.
5. Indiquez si votre groupe doit être un groupe avec réseaux locaux virtuels multiples et comment répartir le redimensionnement à la baisse entre les paires de réseau local virtuel configurées.
6. Sélectionnez les réseaux locaux virtuels publics et privés sur lesquels mettre à disposition vos serveurs. Si l'accès aux serveurs est effectué depuis l'internet public (si le réseau local virtuel exécute des serveurs Web), ne cochez pas la case **Réseau privé uniquement**.
7. Définissez **Minimum Member Counts** à 2 et **Maximum Member Counts** à 4. Définissez **Cooldown Period** à 0. Comme nous utilisons une mise à l'échelle basée planning, des statistiques ne sont pas collectées pour déclencher des actions de mise à l'échelle.

## Définition de la configuration de membres pour votre groupe
{: #define-member-configuration}

1. Localisez **Member Configuration** et renseignez les zones **Hostname** et **Domain** pour le serveur de mise à l'échelle. Des suffixes uniques seront ajoutés au nom d'hôte des serveurs ajoutés ultérieurement au groupe.
2. Spécifiez la configuration matérielle des instances de calcul (coeurs, mémoire RAM, etc.)
3. Sélectionnez un système d'exploitation si vous désirez installer le système d'exploitation minimal. Vous pouvez également utiliser une image publique ou privée pour mettre à disposition vos instances.
4. Si les instances requièrent des étapes supplémentaires pour ajouter d'autres logiciels, spécifiez l'URL d'un script de post-installation pour installer ces logiciels. Si vous utilisez un équilibreur de charge pour le groupe, les scripts de post-installation doivent être exécutés avant de placer un membre derrière l'équilibreur de charge.

## Configuration de règles
{: #set-up-policies}

Dans ce scénario, le site Web social utilise une mise à l'échelle basée planning. Deux règles sont nécessaires : l'une pour renforcer les serveurs le vendredi après-midi, l'autre pour les diminuer le samedi soir. La première règle consiste à revoir les serveurs à la hausse.

1. Localisez **Policies** et cliquez sur **Add Policy**. Renseignez la zone **Policy Name**, (Friday Scale Up).
2. Sélectionnez l'option de délai de transition du groupe pour **Cooldown Period**.
3. Cliquez sur **Add Trigger** et spécifiez un déclencheur répétitif en sélectionnant **Every** dans la première liste déroulante, puis sélectionnez **Friday** et **10:00 PM**\* dans les menus déroulants suivants. La case à cocher **Advanced Edit** vous permet d'indiquer la fréquence du déclencheur sous forme de notation de tâche périodique.
4. Cliquez sur la liste déroulante **Scale By** sous **Action** et sélectionnez **Relative**. Entrez 2 dans la zone **Members**.
5. Cliquez à nouveau sur **Add Policy** pour spécifier la seconde règle qui réduit le nombre de serveurs le samedi. La période de transition est la même que celle du groupe. Le déclencheur sera activé chaque samedi à 1h00, avec une action de mise à l'échelle relative de -2.
6. L'heure entrée dans la zone **Triggers** est basée sur l'heure UTC, c'est pourquoi vous devez sélectionner 10:00 PM pour 5:00 PM Central Daylight Time et 1:00 AM pour 8:00 PM Central Daylight Time. Pour l'heure du centre des Etats-Unis, ceci correspondrait à 9:00 AM et 12:00 AM puisque le fuseau UTC/GMT ignore l'heure d'été. Voir le site [World Time Server ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} pour obtenir un convertisseur de fuseaux horaires.

## Ajout d'un équilibreur de charge

Si vous avez configuré un équilibreur de charge, vous pouvez l'utiliser pour équilibrer la charge sur votre groupe Auto Scale.

1. Localisez **Local Load Balancers** et cliquez sur **Add Load Balancer**.
2. Cliquez sur **View VIP Settings** (s'ouvre dans une page séparée) pour examiner les équilibreurs de charge locaux disponibles dans votre compte et commandez-en un nouveau en cas de besoin. Un équilibreur de charge doit avoir un groupe de services associé pour pouvoir être utilisé avec un groupe Auto Scale. Assurez-vous que l'équilibreur de charge est implanté dans le centre de données de votre groupe Auto Scale.
3. Cliquez sur **Add Load Balancer** sur la page **Add Auto Scale Group**, puis cliquez sur la flèche vers le bas en regard de Virtual IP et sélectionnez votre équilibreur de charge.
4. Cliquez sur les flèches vers le bas en regard de **Service Group**, **Service Port** et **Service Health Check Type** et sélectionnez les valeurs appropriées.
5. Cliquez sur **Add Group** pour enregistrer votre groupe.
6. Si tous vos centres de données, réseaux, etc., ont été spécifiés correctement, votre groupe Auto Scale est créé. Cliquez sur le groupe dans l'écran **View All Groups** pour examiner ses informations.

La configuration d'une mise à l'échelle basée planning entraîne la mise à disposition automatique de deux membres pour se conformer à l'exigence minimum du site Web. Le vendredi à 17h00 (heure du centre des Etats-Unis), deux membres supplémentaires sont automatiquement mis à disposition au déclenchement de la première règle. Puis, le samedi à 20h00 (heure du centre des Etats-Unis), deux membres sont libérés grâce au déclenchement de la seconde règle. Si vous spécifiez un équilibreur de charge, tous les membres ajoutés à sa création, ou le vendredi, résident derrière l'équilibreur de charge une fois le script de post-installation exécuté.
