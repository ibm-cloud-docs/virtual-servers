---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

keywords: public virtual servers, network traffic, virtual server deployment

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Acerca de los servidores virtuales públicos
{: #about-public-virtual-servers}

Las ofertas de {{site.data.keyword.BluVirtServers}} públicos son despliegues de servidor virtual multiarrendatario gestionados por IBM. Le permiten escalar el entorno rápidamente, resultan rentables con tamaños predefinidos que se ajustan a todos los requisitos empresarial y se configuran y activan rápidamente.  
{:shortdesc}

Los servidores virtuales públicos ofrecen muchas ventajas, incluidas las siguientes:

* **Disponibilidad global**

    La oferta de servidor virtual público está disponible en los centros de datos de todo el mundo.

* **Varias opciones de configuración, despliegue rápido y escalabilidad**

    La oferta de servidor virtual público ofrece opciones de servidor virtual pequeño o grande que se ajustan a diversos requisitos de carga de trabajo.

El tráfico en la red correspondiente a servidores virtuales públicos, que engloba VSI SAN y otro almacenamiento conectado a la red, no tiene garantía. Si el tráfico en la red de una instancia de servidor virtual comienza a tener un impacto negativo significativo en otros servidores virtuales, dicha instancia se puede reiniciar en un nuevo host o, en casos extremos, se puede inhabilitar por completo. Este impacto negativo se suele observar cuando los niveles de tráfico alcanzan entre 20.000 y 30.000 paquetes por segundo (PPS).  Para disponer de un sistema de red garantizado se recomienda utilizar la oferta de servidor virtual dedicado. Para obtener más información, consulte la oferta del entorno de un solo arrendatario [servidor virtual dedicado](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers).

Las instancias públicas residen en un hipervisor que se comparte con otros clientes; sin embargo, los procesadores y la memoria están dedicados al servidor virtual, por lo que el rendimiento del servidor es muy fiable.

Dispone de los siguientes servidores virtuales públicos.

| Servidores virtuales públicos  | Descripción                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- |
| [Equilibrado](/docs/vsi?topic=virtual-servers-balanced#balanced) | Adecuado para cargas de trabajo comunes de la nube que requieren un equilibrio entre rendimiento y escalabilidad. Utiliza almacenamiento conectado a red.|
| [Almacenamiento local equilibrado](/docs/vsi?topic=virtual-servers-balanced-local-storage#balanced-local-storage) | Adecuado para grandes clústeres de bases de datos que requieren alto rendimiento de E/S de latencia baja.|
| [Cálculo](/docs/vsi?topic=virtual-servers-compute#compute) | Adecuado para cargas de trabajo con un tráfico en la web entre moderado y alto.|
| [Memoria](/docs/vsi?topic=virtual-servers-memory#memory)  | Adecuado para cargas de trabajo con colocación en memoria caché y análisis en tiempo real. |
| [GPU](/docs/vsi?topic=virtual-servers-gpu#gpu)  | Adecuado para cargas de trabajo de alto rendimiento.
{: caption="Tabla 1. Servidores virtuales públicos admitidos" caption-side="top"}

Algunas de estas familias también están disponibles para IBM Cloud Virtual Servers for VPC. Para obtener más información, consulte [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen).
{:tip}

## Siguientes pasos

Después de revisar y decidir el tipo de servidor virtual, es hora de suministrar el servidor virtual público. Para empezar, revise la información siguiente:
1. [Selecciones de suministro](/docs/vsi?topic=virtual-servers-provisioning-selections)
2. [Suministro de instancias públicas](/docs/vsi?topic=virtual-servers-ordering-vs-public)
