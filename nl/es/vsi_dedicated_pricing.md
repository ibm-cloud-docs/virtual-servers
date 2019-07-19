---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-22"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Precios de los hosts dedicados
{: #dedicated-virtual-server-pricing}

El establecimiento de precios para hosts dedicados se ofrece en un modelo por hora o mensual.
{:shortdesc}

El establecimiento de precios de host dedicado incluye todos los componentes de vCPU, RAM, almacenamiento local y velocidad de puerto de enlace ascendente, ya que las instancias se suministran en hosts dedicados. Para obtener información sobre los precios, consulte la
[Calculadora de suministro de servidores virtuales
![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

Con hosts dedicados, dispondrá de almacenamiento local adicional en el primero, segundo, tercero, cuarto y quinto disco. También hay capacidad adicional de hasta 400 GB en cada disco secundario.

Las instancias por hora se pueden suministrar en hosts por hora y mensuales. Las instancias mensuales solo se pueden suministrar en hosts mensuales.

| Configuración host | vCPU	| RAM (GB) | Almac. local (TB SSD) |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |  56 	|   242    |        	1,2	          |
| 56x484x1.2         |  56  |   484    |          1,2           |
{: caption="Tabla 1. Configuraciones de host dedicado" caption-side="top"}

Los precios varían según la región.
{:note}

Los complementos SAN (conectado a red), SO premium y SW se facturan por hora o al mes, por instancia, en función de la instancia suministrada en el host dedicado. Los precios para estos componentes dependerá de la oferta existente en las instancias públicas y en las instancias dedicadas. 

Por ejemplo, una instancia dedicada suministrada en un host dedicado con la siguiente configuración no se facturará por instancia. vCPU, RAM, almacenamiento local y velocidades de puerto de enlace ascendente se incluyen en los cargos del host dedicado. 

* 8 vCPU
* 16 GB de RAM
* 100 GB de SSD local primer disco
* 400 GB de SSD local segundo disco
* 400 GB de SSD local tercer disco
* 1 Gbps de enlaces ascendentes de red pública y privada (host dedicado) 

