---

copyright:
  years: 2014, 2019
lastupdated: "2019-02-06"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Automatische Skalierung mit Apache Brooklyn
{: #auto-scale-with-apache-brooklyn}

## Einleitung

Ein Unternehmen, das täglich kritische Verbraucherdaten für über eine Milliarde Mobilfunkbenutzer zur Verfügung stellt, hat uns gebeten, Funktionen zur Erstellung von Servergruppen für die automatische Skalierung zu erstellen, die sich in einem privaten Netz befinden. Eine zentrale Anforderung war hierbei die Elastizität. Dabei sollten die Systeme anhand vordefinierter Richtlinien und basierend auf den Workloadanforderungen und der Antwortzeit für die Benutzer automatisch mit einem Scale-up oder Scale-down nach oben bzw. unten skaliert werden.

Die automatische Skalierung basiert auf der CPU-Auslastung. Wenn die durchschnittliche CPU-Auslastung der Server einer Gruppe den obersten Schwellenwert überschreitet oder wenn die Bedingungen für das Auslöserereignis erfüllt sind, müssen weitere Ressourcen bereitgestellt werden oder es muss ein Scale-up durchgeführt werden. Ist die durchschnittliche CPU-Auslastung der Server einer Gruppe niedriger als der niedrigste Schwellenwert oder werden die Bedingungen für das Auslöserereignis nicht erfüllt, dann muss für die Ressourcen ein Scale-down durchgeführt werden. Der Kunde hat die folgenden Anforderungen formuliert:

1. Möglichkeit zur Angabe der folgenden Parameter:
  * Ursprüngliche Anzahl der Server in der Gruppe
  * Minimale und maximale Anzahl der Server in der Gruppe
  * Obere und untere CPU-Schwellenwerte
  * Anzahl der zusätzlichen Server, die bei Auftreten eines Auslöserereignisses mit einem Scale-up oder Scale-down erhöht oder reduziert wird
2. Integration des Domain Name System (DNS)
  * Nach Bereitstellung eines Servers in der Gruppe (Scale-up) und dessen Verfügbarkeit muss für diesen Server ein entsprechender DNS-Datensatz erstellt werden.
  * Nach einem Scale-down für den Server muss der zugehörige DNS-Datensatz wieder entfernt werden.
3. Integration einer Lastausgleichsfunktion
  * Nach Bereitstellung eines Servers in der Gruppe (Scale-up) und dessen Verfügbarkeit muss der Serverdatensatz zur entsprechenden NetScaler-Lastausgleichsfunktion hinzugefügt werden und es muss eine Bindung zur entsprechenden Lastausgleichsgruppe hergestellt werden.
  * Nach einem Scale-down für den Server muss die Bindung des Servers zur Lastausgleichsgruppe aufgehoben werden und der Serverdatensatz muss aus NetScaler entfernt werden.
4. Integration von Chef
  * Nach Bereitstellung eines Servers in der Gruppe (Scale-up) und dessen Verfügbarkeit muss der Chef-Client ausgeführt werden und der Knoten muss auf dem Chef-Server registriert werden.
  * Nach einem Scale-down für den Server müssen der Serverknoten und der Clientdatensatz vom Chef-Server entfernt werden.
5. Voraussetzungen für Serverbereitstellung
  * Alle Server in der Gruppe müssen als virtuelle Maschinen (VMs) mit rein privaten Uplinks, 1.000 Mb/s Portgeschwindigkeit und einem angegebenen privaten VLAN bereitgestellt werden.
  * VMs sollen auf Basis einer Standardvorlage für mehrere Platten bereitgestellt werden, die vom Kunden in {{site.data.keyword.cloud}} erstellt wurde.
6. Betriebssystem
  * CentOS 7.

Basierend auf den Anforderungen des Kunden wurde Apache Brooklyn als Tool für die automatische Skalierung zur Implementierung der Lösung ausgewählt.

## Übersicht zu Apache Brooklyn

Apache Brooklyn ist ein Framework für die Modellierung, Überwachung und Verwaltung von Anwendungen durch autonome Blueprints. Weitere Informationen hierzu finden Sie auf der Site für [Apache Brooklyn ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://brooklyn.incubator.apache.org/){: new_window}.

### Apache Brooklyn-Konzepte

Die Apache Brooklyn-Dokumentation enthält Definitionen der folgenden Apache Brooklyn-Konzepte:

* Entitäten
* Anwendung
* Konfiguration übergeordneter Elemente und Konfiguration der Zugehörigkeit
* Sensoren und Effektoren
* Lebenszyklus- und Verwaltungskontext
* Abhängige Konfiguration
* Standort, Richtlinien
* Ausführung
* Implementierung

### Integration von DNS, NetScaler und Chef durchführen

Apache Brooklyn stellt eine Basisklasse zur Anpassung des Standorts (`brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`) bereit, in der Sie Methoden finden, die die Erstellung zusätzlicher Parameter ermöglichen, wenn Systeme bereitgestellt werden. Nach der Bereitstellung eines Systems können Aktionen ausgeführt werden. Außerdem können Aktionen auch ausgeführt werden, bevor und nachdem das System bei einem Abbruch freigegeben wird.

Es wurde eine eigene Standortanpassungsklasse erstellt, die die von Brooklyn bereitgestellte Klasse `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer` ergänzt. Im vorliegenden Beispiel wird sie als `brooklyn.location.jclouds.ProjectJcloudsLocationCustomizer` bezeichnet.

Die folgenden drei Methoden wurden überschrieben:

1. `public void customize(JcloudsLocation location, ComputeService computeService, TemplateOptions templateOptions)` - Die Methode wird gestartet, bevor die Cloud-API zur Bereitstellung eines Servers aufgerufen wird. Darüber hinaus wurde die Möglichkeit geschaffen, Bereitstellungseigenschaften wie beispielsweise `privateNetworkOnly, primaryBackendNetworkComponentVlanId, portSpeed` und ähnliche Komponenten anzubieten.

* `public void customize(JcloudsLocation location, ComputeService computeService, JcloudsSshMachineLocation machine)` - Die Methode wird gestartet, nachdem ein System bereitgestellt und gestartet wurde. Aus diesem Grund sind alle Serverparameter (z. B. die Server-IP-Adresse) verfügbar. Der Code zum Hinzufügen eines Servers zum DNS und zur Lastausgleichsfunktion muss in dieser Methode platziert werden. Die REST-APIs für DNS und NetScaler werden zum Erstellen der DNS-Datensätze und zum Binden des Servers an NetScaler verwendet. Zum Übergeben von REST-Aufrufen an die DNS- und NetScaler-APIs wurde ein Paket von `Brooklyn, brooklyn.util.http` verwendet.

* `public void preRelease(JcloudsSshMachineLocation machine)` - Die Methode wird beim Systemabbruch gestartet, bevor der Server gestoppt wird. Es wurden REST-Aufrufe für DNS und NetScaler hinzugefügt, um die DNS- und NetScaler-Datensätze zu entfernen und die Bindung des Servers zur NetScaler-Gruppe aufzuheben.

Es wurden keine speziellen Maßnahmen zur Herstellung der Verbindung des neuen Server zu Chef ausgeführt. In dem Image, das zur Bereitstellung des Servers verwendet wurde, ist ein Chef-Client sowie ein Startscript installiert, das zur Ausführung des Chef-Clients und zur Herstellung der Verbindung zum Chef-Server dient. Bei Bedarf kann die Brooklyn-Integration mit Chef zur Erstellung von Blueprints verwendet werden.

Des Weiteren wurde ein REST-Aufruf an den Chef-Server hinzugefügt, um entsprechende Client- und Knotendatensätze zu entfernen.

### Anwendungsblueprint

Im Anwendungsblueprint wurden der Standort, die Parameter zur Erfassung von Metriken sowie die Eigenschaften für die automatische Skalierung der Server angepasst. Zur Anpassung der einzelnen Komponenten werden die folgenden Befehle verwendet.

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

### Standort (location)

Im Abschnitt 'location' des Blueprints wurden folgende Bereitstellungseigenschaften angegeben:

* Position für die Bereitstellung des Servers (Rechenzentrum und VLAN)
* Angabe, ob der Server mit 'privateNetworkOnly' bereitgestellt wird
* Image-ID der {{site.data.keyword.cloud_notm}}-Standardvorlage oder des entsprechenden Flex Images
* Portgeschwindigkeit

Des Weiteren wurde die DNS-Zonen-ID angegeben, die von `ProjectJcloudLocationCustomizer` zum Hinzufügen und Löschen von Datensätzen in der DNS-Zone verwendet wird, und es wurden NetScaler-Informationen für die Serverbindung und das Aufheben der Serverbindung zu NetScaler bereitgestellt.

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

### Services (services)

Im Abschnitt 'services' des Blueprints wurden folgende Informationen angegeben:

* Angabe zur Bereitstellung einer Servergruppe
* Angabe zu den von Brooklyn auf den einzelnen Servern zu installierenden Komponenten
* Angabe zur Vorgehensweise bei der Erfassung und Verwendung von CPU-Metriken
* Parameter der Richtlinie für die automatische Skalierung

#### Anwendungsspezifikation

    services:
    - type: brooklyn.entity.group.DynamicCluster #group of servers
      id: cluster
      name: dynamic cluster
      initialSize: 1 #number of servers initially created in the group

#### Mitgliederspezifikation

Der Aufruf `brooklyn.entity.basic.EmptySoftwareProcess` wurde verwendet, weil Apache Brooklyn nur Server auf Basis eines Images bereitstellen musste und keine zusätzlichen Installations- oder Konfigurationsmaßnahmen erforderlich waren. Dieser Abschnitt enthält auch einen Sensor (server.cpucount), der zur regelmäßigen Erfassung der CPU-Auslastung auf dem Server verwendet wird.

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

### Metriken (metrics)

Im Abschnitt 'metrics' des Blueprints werden Metriken einzelner Server erfasst und der Durchschnitt wird dem Sensor auf Clusterebene zugeordnet.

    brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $me0$brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average

### Richtlinien für automatische Skalierung

In diesem Abschnitt werden die Eigenschaften für die Richtlinien für die automatische Skalierung definiert:

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

Nach Bereitstellung der Lösung können Benutzer reibungslos und zeitnah ein Scale-up oder Scale-down für ihre Anwendungen durchführen, die Systemdatensätze registrieren und deren Registrierung bei der Lastausgleichsfunktion, im DNS und auf den Chef-Servern wieder aufheben.
