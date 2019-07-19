---

copyright:
  years: 2014, 2019
lastupdated: "2019-02-06"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Escalado automático con Apache Brooklyn
{: #auto-scale-with-apache-brooklyn}

## Introducción

Una empresa que proporciona diariamente datos críticos de consumidor a más de mil millones de usuarios móviles nos pidió que les proporcionáramos la funcionalidad para crear grupos de servidores de escalado automático que se encuentran en una red privada. Un requisito clave era la elasticidad; donde, en función de las demandas de carga de trabajo y del tiempo de respuesta de la experiencia de usuario, los sistemas escalan hacia arriba y hacia abajo automáticamente en función de las políticas predeterminadas.

El escalado automático se basa en el uso de CPU. Si el promedio de uso de CPU de los servidores de un grupo es mayor que el umbral más alto, o del suceso desencadenante, es necesario suministrar o escalar hacia arriba más recursos. Si el promedio de uso de CPU de los servidores de un grupo es inferior que el umbral más bajo, o del suceso desencadenante, es necesario que los recursos se escalen hacia abajo. El cliente ha de cumplir los requisitos siguientes:

1. Posibilidad de especificar los parámetros siguientes:
  * Número inicial de servidores en el grupo
  * Número mínimo y número máximo de servidores en el grupo
  * Umbrales de CPU alto y bajo
  * Número de servidores adicionales que se van a escalar hacia arriba y hacia abajo en un suceso desencadenante
2. Integrar el sistema de nombres de dominio (DNS)
  * Después de que se suministre o se escale hacia arriba un servidor del grupo y de que esté disponible, se debe crear un registro de DNS adecuado para el mismo.
  * Cuando el servidor se escala hacia abajo, se elimina el registro de DNS para el mismo.
3. Integrar un Equilibrador de carga
  * Después de que se suministre o se escale hacia arriba un servidor del grupo y esté disponible, se debe añadir el registro del servidor al equilibrador de carga de NetScaler adecuado y se debe enlazar al grupo de equilibrio de carga adecuado.
  * Cuando el servidor se escala hacia abajo, se tiene que desenlazar del grupo de equilibrio de carga y el registro del servidor se tiene que eliminar de NetScaler.
4. Integrar Chef
  * Después de que se suministre o se escale hacia arriba un servidor del grupo y esté disponible, se debe ejecutar el cliente de Chef y se debe registrar el nodo en el servidor de Chef.
  * Cuando el servidor se escala hacia abajo, se elimina el registro de clientes y el nodo del servidor del servidor de Chef.
5. Requisitos de suministro del servidor
  * Todos los servidores del grupo se tienen que suministrar como máquinas virtuales (VM) con enlaces ascendentes solo privados, con una velocidad de puerto de 1.000 Mbps y con una VLAN privada especificada.
  * Las máquinas virtuales se van a suministrar desde la plantilla estándar de varios discos, creada por el cliente en {{site.data.keyword.cloud}}.
6. Sistema operativo
  * CentOS 7.

Basándose en los requisitos del cliente, Apache Brooklyn se ha seleccionado como la herramienta de escalado automático para implementar la solución.

## Visión general de Apache Brooklyn

Apache Brooklyn es una infraestructura para modelar, supervisar y gestionar aplicaciones a través de blueprints autonómicos. Para obtener más información, consulte el sitio de [Apache Brooklyn ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://brooklyn.incubator.apache.org/){: new_window}.

### Conceptos de Apache Brooklyn

La documentación de Apache Brooklyn proporciona definiciones de los conceptos de Apache Brooklyn como, por ejemplo,

* Entidades
* Aplicación
* Configuración de padre y miembro
* Sensores y efectores
* Contexto de gestión y de ciclo de vida
* Configuración dependiente
* Ubicación, políticas
* Ejecución
* Implementación

### Integración de DNS, NetScaler y Chef

Apache Brooklyn proporciona una clase base para la personalización de la ubicación, `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer`, que contiene métodos que permiten crear parámetros adicionales cuando se suministran las máquinas. Las acciones se pueden ejecutar después de que se suministre una máquina y antes y después de que se haya liberado cuando se cancele.

Hemos creado nuestra propia clase de personalizador de ubicación que ha ampliado la clase `brooklyn.location.jclouds.BasicJcloudsLocationCustomizer` proporcionado por Brooklyn. Para este ejemplo, nos referiremos a la misma como `brooklyn.location.jclouds.ProjectJcloudsLocationCustomizer`.

Se han alterado temporalmente los tres métodos siguientes:

1. `public void customize(JcloudsLocation location, ComputeService computeService, TemplateOptions templateOptions)`: el método se inicia antes de llamar a la API de nube para suministrar un servidor. Hemos habilitado la capacidad de suministrar propiedades de suministro como, por ejemplo, `privateNetworkOnly, primaryBackendNetworkComponentVlanId, portSpeed,` etc.

* `public void customize(JcloudsLocation location, ComputeService computeService, JcloudsSshMachineLocation machine)`: el método se inicia después de suministrar e iniciar una máquina, por lo que todos los parámetros del servidor, como la dirección IP del servidor, están disponibles. El código para añadir un servidor al DNS y el equilibrador de carga tiene que colocarse en este método. Se utiliza DNS y la API REST de NetScaler para crear registros de DNS y enlazar el servidor a NetScaler. Hemos utilizado un paquete proporcionado por `Brooklyn, brooklyn.util.http`, para enviar llamadas REST al DNS y a las API de NetScaler.

* `public void preRelease(JcloudsSshMachineLocation machine)`: el método se inicia cuando se cancela la máquina antes de que el servidor se detenga. Hemos añadido llamadas de REST a DNS y NetScaler aquí para eliminar registros los registros de DNS y de NetScaler y para desenlazar el servidor del grupo de NetScaler.

No hemos hecho nada específico para conectar el nuevo servidor a Chef. La imagen, que se utilizó para suministrar el servidor, tenía instalado un cliente de Chef en el mismo y el script de inicio (el script ejecuta el cliente Chef y lo conecta al servidor Chef). Si lo prefiere, puede usar la integración de Brooklyn con Chef para crear blueprints.

También hemos añadido una llamada REST al servidor de Chef para eliminar los registros de cliente y de nodo adecuados.

### Blueprint de aplicación

Dentro del blueprint de aplicación, hemos personalizado la ubicación, los parámetros de recopilación de métricas y las propiedades de escalado automático de los servidores. Se utilizan los mandatos siguientes para personalizar cada componente.

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

### Ubicación

En la sección location de blueprint, hemos especificado propiedades de suministro como, por ejemplo,

* Dónde se debe proporcionar el servidor (centro de datos y VLAN)
* Si el servidor se suministrará o no con privateNetworkOnly
* Un ID de imagen de la plantilla estándar de {{site.data.keyword.cloud_notm}} o de la imagen Flex
* Velocidad de puerto

También hemos especificado el ID de zona del DNS, que `ProjectJcloudLocationCustomizer` utiliza para añadir y suprimir registros en la zona DNS, y la información de NetScaler para enlazar y desenlazar el servidor de NetScaler.

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

### Servicios

En la sección services del blueprint, hemos especificado

* Que estábamos desplegando un grupo de servidores
* Lo que Brooklyn tenía que instalar en cada servidor
* Cómo se tienen que recopilar y utilizar las métricas de CPU
* Los parámetros de la política de escalado automático

#### Especificación de aplicación

    services:
    - type: brooklyn.entity.group.DynamicCluster #group of servers
      id: cluster
      name: dynamic cluster
      initialSize: 1 #number of servers initially created in the group

#### Especificación de miembro

Se ha utilizado la llamada `brooklyn.entity.basic.EmptySoftwareProcess` porque Apache Brooklyn solo necesitaba suministrar servidores a partir de una imagen y no se necesitaba ninguna instalación ni configuración adicional. Esta sección también ha especificado un sensor - server.cpucount – que recopila periódicamente la utilización de CPU desde el servidor.

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

### Métricas

En la sección metrics del blueprint, se recopilan las métricas de servidores individuales y se asigna el promedio al sensor de nivel de clúster.

    brooklyn.enrichers:
      - type: brooklyn.enricher.basic.Aggregator
        brooklyn.config:
          enricher.sourceSensor: $me0$brooklyn:sensor("server.cpucount.averaged")
          enricher.aggregating.fromMembers: true
          transformation: average

### Políticas de escalado automático

En esta sección, se definen las propiedades de política de escalado automático:

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

Una vez desplegada la solución, los usuarios pudieron escalar hacia arriba y hacia abajo automáticamente y de forma transparente sus aplicaciones de forma oportuna, registrando y eliminando el registro de los registros del sistema con el equilibrio de carga, DNS y los servidores de Chef.
