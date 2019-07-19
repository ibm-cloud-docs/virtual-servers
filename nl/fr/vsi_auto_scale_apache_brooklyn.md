---

copyright:
  years: 2014, 2019
lastupdated: "2019-02-06"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Mise à l'échelle automatique avec Apache Brooklyn
{: #auto-scale-with-apache-brooklyn}

## Introduction

Une entreprise qui fournit chaque jour des données consommateur critiques à plus d'un milliard d'utilisateurs mobiles nous a demandé de lui fournir une fonctionnalité permettant de créer des groupes de mise à l'échelle automatique des serveurs situés sur un réseau privé. Une exigence clé était l'élasticité où, compte tenu des demandes de la charge de travail et des temps de réponse rencontrés par l'utilisateur, les systèmes devraient automatiquement se dilater ou se contracter en fonction de règles prédéterminées.

La mise à l'échelle automatique est basée sur l'utilisation de l'UC. Si l'utilisation moyenne de l'UC des serveurs d'un groupe est supérieure au seuil plafond, ou à un événement déclencheur, des ressources supplémentaires ont besoin d'être mises à disposition (augmentation). Si l'utilisation moyenne de l'UC des serveurs d'un groupe est inférieure au seuil le plus bas, ou à un événement déclencheur, les ressources ont besoin d'être diminuées. Les exigences suivantes s'appliquent au client :

1. Possibilité de spécifier les paramètres suivants :
  * Nombre initial de serveurs dans le groupe
  * Nombre minimal et maximal de serveurs dans le groupe
  * Valeur plafond et valeur plancher pour l'UC
  * Nombre de serveurs supplémentaires à rajouter ou retrancher en cas d'événement déclencheur
2. Intégration de système de noms de domaine (DNS)
  * Après qu'un serveur dans la groupe ait été mis à disposition, ou rajouté, et devient disponible, un enregistrement DNS approprié doit être créé pour celui-ci.
  * Lorsqu'un serveur est retiré, l'enregistrement DNS correspondant doit être supprimé.
3. Intégration d'un équilibreur de charge
  * Après qu'un serveur dans la groupe ait été mis à disposition, ou rajouté, et devient disponible, son enregistrement doit être ajouté à l'équilibreur de charge NetScaler approprié et lié au groupe d'équilibrage de charge adéquat.
  * Lorsqu'un serveur est retiré, sa liaison au groupe d'équilibrage de charge doit être annulée et son enregistrement supprimé de NetScaler.
4. Intégration de Chef
  * Après qu'un serveur dans la groupe ait été mis à disposition, ou rajouté, et devient disponible, le client Chef doit l'exécuter et enregistrer le noeud auprès du serveur Chef.
  * Lorsqu'un serveur est retiré, le noeud sur le serveur et l'enregistrement client doivent être supprimés du serveur Chef.
5. Exigences pour la mise à disposition de serveurs
  * Tous les serveurs du groupe doivent être mis à disposition sous forme de machines virtuelles (VM) avec liaisons montantes uniquement privées, vitesse de port de 1000 Mbit/s et un VLAN privé spécifié.
  * Les machines virtuelles doivent être mises à disposition d'après le modèle standard multi-disques créé par le client dans {{site.data.keyword.cloud}}.
6. Système d'exploitation
  * CentOS 7.

Compte tenu des exigences du client, Apache Brooklyn a été sélectionné comme outil de mise à l'échelle automatique pour implémenter la solution.

## Présentation d'Apache Brooklyn

Apache Brooklyn est une structure de modélisation, de suivi et de gestion d'applications via des plans directeurs autonomes. Pour plus d'informations, consultez le site [Apache Brooklyn ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://brooklyn.incubator.apache.org/){: new_window}.

### Concepts Apache Brooklyn

La documentation d'Apache Brooklyn fournit des définitions des concepts Apache Brooklyn tels que :

* Entités
* Application
* Configuration de parent et d'appartenance
* Capteurs et effecteurs
* Cycle de vie et contexte de gestion
* Configuration dépendante
* Emplacement, règles
* Exécution
* Implémentation

### Intégration de DNS, NetScaler et Chef

Apache Brooklyn fournit une classe de base pour personnalisation de l'emplacement, `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`, qui contient des méthodes permettant la création de paramètres supplémentaires lors de la mise à disposition de machines. Les actions peuvent être exécutées après qu'une machine ait été mise à disposition, et avant et après qu'elle ait été libérée une fois annulée.

Nous avons créé notre propre classe de personnaliseur d'emplacement qui étend le `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer` fourni par Brooklyn. Pour cet exemple, nous le désignons comme `brooklyn.location.jclouds.ProjectJcloudsLocationCustomizer`.

Les trois méthodes suivantes ont été redéfinies :

1. `public void customize(JcloudsLocation location, ComputeService computeService, TemplateOptions templateOptions)` - La méthode est démarrée avant l'appel de l'API cloud pour mettre à disposition un serveur. Nous avons activé la possibilité de soumettre des propriétés de mise à disposition comme `privateNetworkOnly, primaryBackendNetworkComponentVlanId, portSpeed,` et d'autres.

* `public void customize(JcloudsLocation location, ComputeService computeService, JcloudsSshMachineLocation machine)` - La méthode est démarrée après qu'une machine ait été mise à disposition et démarrée. De la sorte, tous les paramètres du serveur, comme l'adresse IP du serveur, sont disponibles. Le code pour ajouter un serveur au DNS et à l'équilibreur de charge doit être placé dans cette méthode. Le DNS et l'API REST NetScaler sont utilisés pour créer les enregistrements DNS et lier le serveur à NetScaler. Nous avons utilisé un package fourni par `Brooklyn, brooklyn.util.http` pour soumettre des appels REST au DNS et aux API NetScaler.

* `public void preRelease(JcloudsSshMachineLocation machine)` - La méthode est démarrée lors de l'annulation d'une machine avant que le serveur ne soit arrêté. Nous avons ajouté ici des appels REST au DNS et à NetScaler pour supprimer les enregistrements DNS et NetScaler et annuler la liaison du serveur au groupe NetScaler.

Nous n'avons rien fait de spécifique pour connecter le nouveau serveur à Chef. L'image utilisée pour mettre à disposition le serveur comportait un client Chef installé, ainsi qu'un script de démarrage (le script exécute le client Chef et le connecte au serveur Chef). Si vous préférez, vous pouvez utiliser l'intégration Brooklyn avec Chef pour créer des plans directeurs.

Nous avons également ajouté un appel REST au serveur Chef pour supprimer les enregistrements de client et de noeud concernés.

### Plan directeur d'application

Dans le plan directeur d'application, nous avons personnalisé l'emplacement, les paramètres de collecte de métriques, et les propriétés de mise à l'échelle automatique des serveurs. Les commandes suivantes sont utilisées pour personnaliser chaque composant.

    Nom : Group1
    emplacement :

      jclouds:softlayer:tor01:
      customizerType: brooklyn.location.jclouds.ProjectJcloudLocationCustomizer
      privateNetworkOnly: true
      primaryBackendNetworkComponentVlanId: 12345
      portSpeed: 1000
      imageId: 123456
      dnsZoneId: 12345
      netscalerGroup: app1
      netscalerGroupPort: 8080
      netscalerUrl: http://user:password@10.10.10.10/nitro/v1/

    services :
    - type: brooklyn.entity.group.DynamicCluster
      id: cluster
      name: dynamic cluster
      initialSize: 1
      memberSpec:
        $brooklyn:entitySpec:
        name: VMinSL
        type: brooklyn.entity.basic.EmptySoftwareProcess
        brooklyn.initializers:
        - type: brooklyn.entity.software.ssh.SshCommandSensor
          brooklyn.config:
            name: server.cpucount
            command: "LANG=en_US.UTF-8 sar -u 1 1|grep Average | awk '{print 100 - $8}'"
            targetType: java.lang.Double
            period: 10s
          brooklyn.config:
            post.launch.command: "sudo apt-get install -y sysstat"

      brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $brooklyn:sensor("server.cpucount")
          enricher.targetSensor: $brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average
        brooklyn.policies:
        - policyType: brooklyn.policy.autoscaling.AutoScalerPolicy
        brooklyn.config:
          metric: $brooklyn:sensor("server.cpucount.averaged")
          metricLowerBound: 10
          metricUpperBound: 60
          minPoolSize: 1
          maxPoolSize: 5

### Emplacement

Dans la section emplacement du plan directeur, nous avons spécifié des propriétés de mise à disposition comme :

* Emplacement où mettre à disposition le serveur (centre de données et réseau local virtuel)
* Emplacement où mettre à disposition le serveur avec privateNetworkOnly
* ID d'image du modèle standard {{site.data.keyword.cloud_notm}} ou de l'image Flex
* Vitesse de port

Nous avons également spécifié l'ID de zone DNS, laquelle est utilisée par `ProjectJcloudLocationCustomizer` pour ajouter et supprimer des enregistrements dans la zone DNS et par les informations NetScaler pour liaison du serveur à NetScaler ou annulation de cette liaison.

    emplacement :

      jclouds:softlayer:tor01:
        customizerType: brooklyn.location.jclouds.ProjectJcloudLocationCustomizer
        privateNetworkOnly: true
        primaryBackendNetworkComponentVlanId: 12345
        portSpeed: 1000
        dnsZoneId: 12345
        netscalerGroup: app1
        netscalerGroupPort: 8080
        netscalerUrl: http://user:password@10.10.10.10/nitro/v1/

### Services

Dans la section services du plan directeur, nous avons spécifié

* Que nous déployons un groupe de serveurs
* Que Brooklyn doit être installé sur chaque serveur
* Comment collecter et utiliser les métriques de l'UC
* Les paramètres de la règle de mise à l'échelle automatique

#### Spécifications pour l'application

    services :
    - type: brooklyn.entity.group.DynamicCluster #group of servers
      id: cluster
      name: dynamic cluster
      initialSize: 1 #number of servers initially created in the group

#### Spécifications pour les membres

L'appel `brooklyn.entity.basic.EmptySoftwareProcess` a été utilisé vu qu'Apache Brooklyn avait uniquement besoin de mettre à disposition des serveurs à partir d'une image et qu'aucune installation ou configuration supplémentaire n'était requise. Cette section spécifiait également un capteur - server.cpucount – collectant périodiquement des informations sur l'utilisation de l'UC sur le serveur.

    memberSpec:
      $brooklyn:entitySpec:
      name: VMinSL
      type: brooklyn.entity.basic.EmptySoftwareProcess
      brooklyn.initializers:
      - type: brooklyn.entity.software.ssh.SshCommandSensor
        brooklyn.config:
          name: server.cpucount
          command: "LANG=en_US.UTF-8 sar -u 1 1|grep Average | awk '{print 100 - $8}'"
          targetType: java.lang.Double
          period: 10s
      brooklyn.config:
        post.launch.command: "sudo apt-get install -y sysstat"

### Métriques

Dans la section métriques du plan directeur, des métriques de serveurs individuels sont collectées et la moyenne est affectée au capteur au niveau du cluster.

    brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $me0$brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average

### Stratégies de mise à l'échelle automatique

Les propriétés de la règle de mise à l'échelle automatique sont définies dans cette section :

    brooklyn.policies:
    - policyType: brooklyn.policy.autoscaling.AutoScalerPolicy
      brooklyn.config:
        metric: $brooklyn:sensor("server.cpucount.averaged")
        metricLowerBound: 10
        metricUpperBound: 60
        minPoolSize: 1
        maxPoolSize: 5
        minPeriodBetweenExecs: 10m
        resizeUpIterationIncrement: 2
        resizeUpIterationMax: 2
        resizeDownIterationIncrement: 2
        resizeDownIterationMax: 2

Une fois la solution déployée, les utilisateurs pouvaient renforcer ou réduire le nombre de serveurs de leurs applications en temps opportun et de manière transparente, en enregistrant ou annulant les enregistrements du système auprès de l'équilibreur de charge, du DNS et des serveurs Chef.
