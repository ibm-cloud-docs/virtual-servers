---

copyright:
  years: 2014, 2019
lastupdated: "2019-02-06"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Ridimensionamento automatico con Apache Brooklyn
{: #auto-scale-with-apache-brooklyn}

## Introduzione 

Una società che fornisce quotidianamente i dati dei consumatori critici a più di un miliardo di utenti mobili ci ha chiesto di fornire la funzionalità per creare gruppi di server con ridimensionamento automatico su una rete privata. Un requisito chiave era l'elasticità per cui, in base alle esigenze dei carico di lavoro e al tempo di risposta dell'esperienza dell'utente, i sistemi eseguono automaticamente un ingrandimento o una riduzione in base a politiche predeterminate.

Il ridimensionamento automatico è basato sull'utilizzo della CPU. Se l'utilizzo della CPU medio dei server in un gruppo è superiore alla soglia massima, o evento di trigger, è necessario eseguire il provisioning di ulteriori risorse oppure un loro ampliamento. Se l'utilizzo della CPU medio dei server in un gruppo è inferiore alla soglia minima, o evento di trigger, le risorse devono essere ridotte. Il cliente aveva i seguenti requisiti:

1. Capacità di specificare i seguenti parametri:
  * Numero iniziale di server nel gruppo
  * Numero minimo e massimo di server nel gruppo
  * Soglie della CPU superiore e inferiore
  * Numero di ulteriori server oggetto dell'ampliamento o della riduzione in caso di evento di trigger
2. Integrare il DNS (Domain Name System) 
  * Dopo l'esecuzione del provisioning o dell'ingrandimento di un server nel gruppo, e dopo che è disponibile, è necessario creare per esso un appropriato record DNS. 
  * Quando il server viene ridotto, il record DNS per esso deve essere rimosso. 
3. Integrare un programma di bilanciamento del carico
  * Dopo l'esecuzione del provisioning o dell'ingrandimento di un server nel gruppo, e dopo che è disponibile, il record del server deve essere aggiunto all'appropriato programma di bilanciamento del carico NetScaler e associato all'appropriato gruppo di bilanciamento del carico.
  * Quando il server viene ridotto, la sua associazione al gruppo di bilanciamento del carico deve essere annullata e il record del server deve essere rimosso da NetScaler. 
4. Integrare Chef
  * Dopo l'esecuzione del provisioning o dell'ingrandimento di un server nel gruppo, e dopo che è disponibile, il client Chef deve essere eseguito e deve registrare il nodo presso il server Chef.
  * Quando il server viene ridotto, il record del client e del nodo del server deve essere rimosso dal server Chef.
5. Requisiti di provisioning del server
  * Il provisioning di tutti i server nel gruppo deve essere eseguito come VM (Virtual machine), con uplink solo privati, una velocità di porta di 1.000 Mbps e una VLAN privata specificata. 
  * Il provisioning delle VM deve essere eseguito dal template standard a più dischi, creato dal cliente in {{site.data.keyword.cloud}}. 
6. Sistema operativo
  * CentOS 7.

In base ai requisiti del cliente, Apache Brooklyn è stato selezionato come strumento di ridimensionamento automatico per implementare la soluzione.

## Panoramica di Apache Brooklyn

Apache Brooklyn è un framework per la modellazione, il monitoraggio e la gestione delle applicazioni tramite blueprint autonomici. Per ulteriori informazioni, consulta il sito [Apache Brooklyn ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://brooklyn.incubator.apache.org/){: new_window}. 

### Concetti di Apache Brooklyn

La documentazione di Apache Brooklyn fornisce definizioni dei concetti di Apache Brooklyn quali

* Entità
* Applicazione
* Configurazione principale e adesione
* Sensori ed effettori
* Ciclo di vita e contesto di gestione
* Configurazione dipendente
* Ubicazione, politiche
* Esecuzione
* Implementazione

### Integrazione di Chef, NetScaler e DNS 

Apache Brooklyn fornisce una classe di base per personalizzare l'ubicazione, `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`, che contiene i metodi che consentono di creare ulteriori parametri quando viene eseguito il provisioning delle macchine. Le azioni possono essere eseguite dopo che è stato eseguito il provisioning di una macchina e prima e dopo che è stata rilasciata, quando è annullata. 

Abbiamo creato una nostra classe customizer dell'ubicazione che ha esteso il `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer` fornito da Brooklyn. Per questo esempio, fai riferimento ad esso come `brooklyn.location.jclouds.ProjectJcloudsLocationCustomizer`. 

Sono stati sovrascritti i seguenti tre metodi:

1. `public void customize(JcloudsLocation location, ComputeService computeService, TemplateOptions templateOptions)` - il metodo viene avviato prima di richiamare la API cloud per eseguire il provisioning di un server. Abbiamo abilitato la capacità di fornire delle proprietà di provisioning quali `privateNetworkOnly, primaryBackendNetworkComponentVlanId, portSpeed,` e altre.

* `public void customize(JcloudsLocation location, ComputeService computeService, JcloudsSshMachineLocation machine)` - il metodo viene avviato dopo che di una macchina è stato eseguito il provisioning e l'avvio; pertanto tutti i parametri del server, come l'indirizzo IP del server, sono disponibili. Il codice per aggiungere un server al DNS e il programma di bilanciamento del carico devono essere collocati in questo metodo. API REST NetScaler e DNS vengono utilizzati per creare i record DNS e associare il server a NetScaler. Abbiamo utilizzato un pacchetto fornito da `Brooklyn, brooklyn.util.http`, per inoltrare le chiamate REST a DNS e API NetScaler. 

* `public void preRelease(JcloudsSshMachineLocation machine)` - il metodo viene avviato all'annullamento della macchina prima che il server venga arrestato. Abbiamo aggiunto le chiamate REST al DNS e a NetScaler qui per rimuovere i record NetScaler e DNS e annullare l'associazione del server al gruppo di NetScaler. 

Non abbiamo avuto bisogno di eseguire operazioni specifiche per connettere il nuovo server a Chef. L'immagine che era stata utilizzata per eseguire il provisioning del server aveva un client Chef installato su di essa e uno script di avvio (lo script esegue il client Chef e lo connette al server Chef). Se preferisci, puoi utilizzare l'integrazione Brooklyn con Chef per creare i blueprint. 

Abbiamo anche aggiunto una chiamata REST al server Chef per rimuovere gli appropriati record di nodo e client.

### Blueprint dell'applicazione

Nel blueprint dell'applicazione, abbiamo personalizzato l'ubicazione, i parametri di raccolta delle metriche e le proprietà di ridimensionamento automatico dei server. I seguenti sono i comandi utilizzati per personalizzare ciascun componente. 

    name: Group1
    location:

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

    services:
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

### Ubicazione

Nella sezione relativa all'ubicazione (location) del blueprint, abbiamo specificato le proprietà di provisioning quali 

* Dove deve essere eseguito il provisioning del server (data center e VLAN)
* Se il provisioning del server verrà eseguito con privateNetworkOnly
* Un ID immagine dell'immagine flex o del template standard {{site.data.keyword.cloud_notm}}. 
* Velocità porta

Abbiamo specificato anche l'ID zona DNS, che viene utilizzato da `ProjectJcloudLocationCustomizer` per aggiungere ed eliminare record nella zona DNS e le informazioni NetScaler per l'associazione e l'annullamento dell'associazione del server da NetScaler. 

    location:

      jclouds:softlayer:tor01:
        customizerType: brooklyn.location.jclouds.ProjectJcloudLocationCustomizer
        privateNetworkOnly: true
        primaryBackendNetworkComponentVlanId: 12345
        portSpeed: 1000
        dnsZoneId: 12345
        netscalerGroup: app1
        netscalerGroupPort: 8080
        netscalerUrl: http://user:password@10.10.10.10/nitro/v1/

### Servizi

Nella sezione dei servizi (services) del blueprint, abbiamo specificato

* Che stavamo distribuendo un gruppo di server
* Quale Brooklyn era da installare su ciascun server
* In che modo dovevano essere raccolte e utilizzate le metriche CPU
* I parametri della politica di ridimensionamento automatico

#### Specifica delle applicazioni

    services:
    - type: brooklyn.entity.group.DynamicCluster #group of servers
      id: cluster
      name: dynamic cluster
      initialSize: 1 #number of servers initially created in the group

#### Specifica dei membri

È stata utilizzata la chiamata `brooklyn.entity.basic.EmptySoftwareProcess` perché Apache Brooklyn doveva eseguire solo il provisioning dei server da un'immagine e non era richiesta alcuna installazione o configurazione aggiuntiva. Questa sezione specificava anche un sensore - server.cpucount – che raccoglie periodicamente l'utilizzo della CPU dal server.

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

### Metriche

Nella sezione delle metriche (metric) del blueprint, vengono raccolte le metriche dai singoli server e la media viene assegnata al sensore a livello del cluster.

    brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $me0$brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average

### Politiche di ridimensionamento automatico

In questa sezione, vengono definite le proprietà della politica di ridimensionamento automatico:

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

Una volta distribuita la soluzione, gli utenti potevano eseguire senza interruzioni un ridimensionamento incrementale o decrementale delle loro applicazioni in modo tempestivo, registrare e annullare la registrazione dei record di sistema con il bilanciamento del carico, DNS e server Chef. 
