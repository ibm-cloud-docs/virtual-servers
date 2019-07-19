---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-17"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mise à disposition d'instances publiques
{: #ordering-vs-public}

## Avant de commencer
Il existe deux méthodes de mise à disposition de vos instances de serveur virtuel public. Vous pouvez utiliser soit la console {{site.data.keyword.cloud}}, soit {{site.data.keyword.slportal}}. Des ID de connexion uniques sont requis pour la console et {{site.data.keyword.slportal}}. Vous ne pouvez pas utiliser le nom d'utilisateur et le mot de passe de votre console pour vous connecter au portail et inversement.
{:shortdesc}

Pour la console {{site.data.keyword.cloud_notm}}, vous devez posséder un compte mis à niveau afin de commander des serveurs virtuels. Pour plus d'informations sur la mise à niveau de votre compte, voir [Compte Paiement à la carte](/docs/account?topic=account-accounts#paygo).
{:note}

Avant de commencer, passez en revue les conditions requises présentées ci-dessous.

  1. Consultez les options de déploiement disponibles. Pour plus d'informations, voir [Serveurs virtuels publics](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers).

  2. Vérifiez les considérations sur la capacité des instances de serveur virtuel.  Pour plus d'informations, voir [Considérations relatives aux ressources pour les instances de serveur virtuel](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).
  
  3. Ouvrez la page d'[instance de serveur virtuel ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} à partir de la console {{site.data.keyword.cloud_notm}}.

## Mise à disposition d'une instance de serveur virtuel public  
{: #ordering-public-instance}

Pour mettre à disposition une instance de serveur virtuel, vous devez prendre en compte les informations suivantes. 

Vous devez être connecté pour voir toutes les options disponibles.
{:tip}

### Instance publique

| Zone    | Détails    |
| -------- | ----------- |
| Facturation  | En fonction de votre instance de serveur virtuel, vous pouvez sélectionner une facturation horaire ou mensuelle. La principale différence (outre le coût) réside dans le fait qu'aucune allocation de bande passante n'est incluse pour les instances facturées à l'heure. A la fin d'une période de facturation, l'utilisation de la bande passante et le nombre d'heures pendant lesquelles chaque instance a été active sur le compte sont calculés. Par exemple, si vous annulez une instance facturée à l'heure après 10 jours, vous payez uniquement les heures correspondant à ces 10 jours. Si vous annulez une instance facturée au mois après 10 jours, vous payez pour le mois entier. Si la fonctionnalité d'interruption de facturation, qui est disponible uniquement pour les instances horaires, vous intéresse, reportez-vous à la rubrique [A propos de l'interruption de facturation](/docs/vsi?topic=virtual-servers-about-suspend-billing). |
| Nom d'hôte | Peut contenir des libellés composés de caractères alphanumériques et de tirets, séparés par des points. Les libellés ne peuvent pas être uniquement composés de caractères numériques, débuter ou se terminer par un tiret et comporter des tirets ou des points consécutifs.|
| Domaine |Doit contenir au moins deux libellés pouvant être composés de caractères alphanumériques et de tirets, séparés par des points. Les libellés ne peuvent pas commencer ni se terminer par un tiret, ni comporter des tirets ou des points consécutifs. Le dernier libellé doit être uniquement composé de lettres.|
| Groupe de placement | Vous pouvez sélectionner un groupe de placement pour votre instance. Si vous ajoutez un groupe de placement, la règle "propagation" signifie que les instances se trouvent sur un matériel physique différent. Pour plus d'informations, voir [Groupes de placement](/docs/vsi?topic=virtual-servers-placement-groups).|
| Emplacement  |Les emplacements sont composés de régions (zones géographiques spécifiques) et de zones (centres de données à tolérance de pannes dans une région). Sélectionnez l'emplacement où vous souhaitez créer votre instance de serveur virtuel. |
| Profils populaires | Pensez à sélectionner des configurations de profil populaires prenant en charge les cas d'utilisation les plus courants. Les profils contiennent des instances préconfigurées prêtes à être utilisées en quelques minutes. |
| Tous les profils | Pour plus d'informations sur les options de profil disponibles pour les instances publiques, voir [Serveurs virtuels publics](/docs/vsi?topic=virtual-servers-about-public-virtual-servers). |
| Clés SSH     | Les clés SSH permettent d'accéder à une instance sans utiliser de mot de passe des clients correspondants pour chaque clé publique implémentée sur l'instance. Si vous décidez d'ajouter une clé SSH, fournissez une clé publique de votre clé SSH, que vous pourrez utiliser pour vous connecter à votre instance après sa mise en service. |
| Image        |  Une image est le système d'exploitation déployé pour votre instance. Vous pouvez sélectionner certaines options gratuites, telles CentOS et Ubuntu. Certains systèmes payants, tels Windows Server et Red Hat Enterprise Linux (RHEL), sont également disponibles. Il est important de noter que Windows requiert un disque principal de 100 Go. |
{: caption="Tableau 1. Options d'instance publique" caption-side="top"}

### Modules complémentaires d'instance publique  

Si vous choisissez des modules complémentaires de système d'exploitation, de panneau de commande ou de logiciel, ils doivent être compatibles avec votre image pour éviter les erreurs lors de la commande de votre instance. Par exemple, vous ne pouvez pas installer une image RedHat avec une base de données Microsoft.
{:important}

| Zone     | Détails     |
| --------- | ----------- |
| Modules complémentaires de système d'exploitation | Si vous sélectionnez la facturation mensuelle, vous pouvez sélectionner les modules complémentaires d'image suivants :<br><br> **R1Soft Server Backup Manager** fournit une sauvegarde haute performance de serveur de disque à disque et un référentiel de gestion et de données centralisé. Si vous sélectionnez le module complémentaire R1Soft, vous devez acheter un pack R1Soft Backup Agent, à savoir un module complémentaire CDP dans la section **Services**. La sélection de l'un sans l'autre provoque une erreur de votre commande. Pour plus d'informations sur R1Soft et IBM Cloud, voir [R1Soft Server Backup Manager ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/cloud/backup-and-restore?mhq=R1Soft%20Server%20Backup%20Manager&mhsrc=ibmsearch_a){: new_window}.<br><br>**Veeam Backup and Replication** associe une sauvegarde automatisée à des fonctions de restauration et de réplication. Veeam fournit également une surveillance avancée, des rapports et une planification des capacités. Pour plus d'informations sur Veeam Backup and Replication, voir [Veeam Backup and Replication with IBM storage ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www-356.ibm.com/partnerworld/gsd/solutiondetails.do?solution=54724&lc=en&stateCd=P&tab=2){: new_window}.<br><br>**VMware vCenter** automatise le déploiement des couches VMware vSphere et VMware vCenter Server sous-jacentes dont vous avez besoin pour une solution VMware flexible et personnalisable. Pour plus d'informations sur vCenter on IBM Cloud, voir [About vCenter Server on IBM Cloud ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/downloads/cas/L7RKPZND?mhq=vmware%20vcenter&mhsrc=ibmsearch_a){: new_window}.|
| Logiciel du panneau de commande | Si vous sélectionnez la facturation mensuelle, vous pouvez ajouter un panneau de commande pour l'hébergement Web. |
|  Logiciel de base de données     | Vous pouvez sélectionner un logiciel de base de données à installer. {{site.data.keyword.cloud_notm}} prend en charge tous les logiciels de base de données déployés au cours du processus de mise à disposition. Vous pouvez également installer votre propre logiciel de base de données une fois le serveur déployé.|
| Services | Certains services sont automatiquement sélectionnés pour vous, en fonction de vos sélections de facturation et d'image. Vous pouvez choisir l’un des modules complémentaires de service restants pour votre instance. |
| Script de mise à disposition |Les scripts de mise à disposition sont généralement utilisés pour appliquer à un serveur une configuration spécifique à un client et pour faciliter l'automatisation de la mise à l'échelle. Tout fichier pouvant être exécuté par le système d'exploitation incluant notamment les fichiers binaires combinés ou les langues prises en charge par le système d'exploitation, peut être un script de mise à disposition. Les scripts de mise à disposition ne peuvent pas être utilisés sur des images cloud-init. Pour plus d'informations, voir [Scripts de mise à disposition](/docs/vsi?topic=virtual-servers-provisioning-scripts). |
| Données utilisateur     |Vous pouvez ajouter des données utilisateur qui effectuent automatiquement des tâches de configuration courantes ou exécutent des scripts. Les données utilisateur peuvent être utilisées sur des images cloud-init et non-cloud-init. |
{: caption="Tableau 2. Modules complémentaires d'instance publique " caption-side="top"}

### Disques de stockage connectés

Si vous avez besoin de davantage de stockage, vous pouvez connecter des disques de stockage à votre instance. Le type de disque de stockage disponible dépend du profil sélectionné. Par exemple, les profils locaux équilibrés et quelques profils GPU utilisent des disques sauvegardés localement. Si vous sélectionnez la facturation mensuelle, vous pouvez ajouter {{site.data.keyword.backup_notm}} et choisir l'option qui correspond le mieux à vos besoins. Pour plus d'informations, voir [Services {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-getting-started).

### Interface réseau

| Zone    | Détails     |
| -------- | ----------- |
| Vitesses de port pour la liaison montante |Vous pouvez sélectionner la vitesse de liaison montante pour votre instance, jusqu'à 1 Go/s. Ces liaisons montantes virtuelles dépendent de liaisons montantes physiques redondantes vers les réseaux dédiés et publics IBM. La vitesse dédiée et publique est toujours identique lors de la commande, avec la possibilité de mettre à niveau ou de rétrograder une liaison, si nécessaire. |
| Groupe de sécurité privé et public  | Vous pouvez utiliser des groupes de sécurité pour promulguer un ensemble de règles de filtre d'adresse IP qui définissent comment gérer le trafic entrant et sortant entre les interfaces publiques et privées de votre instance. Pour plus d'informations, voir [A propos des groupes de sécurité IBM](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups). |
| VLAN privé et public | Par défaut, votre instance de serveur virtuel est placée sur un VLAN attribué automatiquement. Vous pouvez choisir un autre VLAN si vous en avez déjà un dans votre centre de données sélectionné. Pour plus d'informations, voir [A propos des VLAN](/docs/infrastructure/vlans?topic=vlans-about-vlans). |
| Sous-réseau privé et public | La sélection d'un sous-réseau est facultative et doit uniquement avoir lieu si vous souhaitez que votre terminal utilise une adresse IP appartenant au sous-réseau. Si vous sélectionnez un sous-réseau, vérifiez que vous avez suffisamment d'adresses IP pour répondre à la demande. Si vous n'avez pas assez d'adresses IP pour votre sous-réseau, votre commande peut être retardée ou annulée. Pour plus d'informations, voir [A propos des sous-réseaux et des adresses IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
{: caption="Tableau 3. Options d'interface réseau " caption-side="top"}

### Modules complémentaires d'interface réseau 

| Zone    | Détails     |
| -------- | ----------- |
| Bande passante | 250 Go sont inclus avec les instances mensuelles qui ont une liaison montante publique. Vous pouvez acheter des allocations plus importantes à un coût réduit. |
| Pare-feux matériels et logiciels | Les services de pare-feu empêchent le trafic indésirable sur vos serveurs, réduisent le risque d'attaque et permettent aux ressources de votre serveur d'être dédiées à l'usage auquel elles sont destinées. |
| Adresse IP principale | Une adresse IP principale est automatiquement attribuée à votre instance. |
| Adresses IP publiques secondaires | Vous êtes propriétaire de ces sous-réseaux pendant la durée de votre instance de serveur virtuel. Vous pouvez annuler le sous-réseau séparément, mais si vous annulez votre instance, le sous-réseau est également supprimé. Pour plus d'informations, voir [A propos des sous-réseaux et des adresses IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
| Adresses IPv6 et IPv6 statiques publiques  | Vous pouvez sélectionner une adresse IPv6 ou des adresses IPv6 statiques publiques pour votre instance. |
| Gestion de réseau privé virtuel| Cette option est automatiquement sélectionnée pour votre instance avec un nombre illimité d'utilisateurs VPN SSL. Pour plus d'informations, voir [A propos de la connexion VPN](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn). |
{: caption="Tableau 4. Modules complémentaires d'interface réseau " caption-side="top"}


## Mise à disposition d'une instance publique via le portail client
Pour mettre à disposition votre instance de serveur virtuel publique via le portail {{site.data.keyword.slportal}}, procédez comme suit :

  1. Connectez-vous au portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
  2. Localisez la section **Commande** et cliquez sur **Unités**.
  3. Sur la page Unités, cliquez sur **SAN horaire**, **Local horaire**, **Mensuel** ou **Transitoire** correspondant aux offres de Serveur virtuel.
  4. Sur la page de configuration de votre serveur Cloud**, indiquez les informations pertinentes.
  5. Cliquez sur **Ajouter à la commande** pour continuer.
  6. Confirmez ou modifiez les informations de domaine pour le serveur.
  7. Cliquez sur les cases à cocher **Conditions des services Cloud** et **Contrat de service tiers**.
  8. Confirmez ou entrez vos informations de paiement, puis cliquez sur **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

## Etapes suivantes
Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page *Détails de l'unité* une fois que vous êtes connecté à {{site.data.keyword.Bluemix_notm}}. 

Une fois que votre serveur virtuel est mis à disposition et est disponible pour être utilisé, vous pouvez configurer vos serveurs virtuels à l'aide de la console {{site.data.keyword.cloud_notm}} ou de {{site.data.keyword.slapi_short}}. Pour plus d'informations, voir [Configuration des serveurs virtuels](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
