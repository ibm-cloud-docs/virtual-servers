---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Establecimiento de precios del servidor virtual dedicado
{: #dedicated-virtual-server-pricing}

El establecimiento de precios para hosts dedicados se ofrecerá en un modelo por hora o mensual.
{:shortdesc}

Puede ver a continuación el establecimiento de precios de host dedicado, que incluye todos los componentes de vCPU, RAM, almacenamiento local y velocidad de puerto de enlace ascendente, ya que las instancias se suministran en hosts dedicados.

Con hosts dedicados, dispondrá de almacenamiento local adicional en el primero, segundo, tercero, cuarto y quinto disco. También hay capacidad adicional de hasta 400 GB en cada disco secundario.

Las instancias por hora se pueden suministrar en hosts por hora y mensuales. Las instancias mensuales solo se pueden suministrar en hosts mensuales.

| Configuración host | vCPU	| RAM (GB) | Almac. local (TB SSD) |	Precio/hora | Precio mensual |
| ------------------ | ---- | -------- | ---------------------- | ------------ | ------------- |
| 56x242x1,2TB	     |  56 	|   242    |        	1,2	          |     3,164$   | 	2.099,00 $    |
{: caption="Tabla 1. Establecimiento de precios de host dedicado" caption-side="top"}

Tenga en cuenta que el precio varía según la región.

Los complementos SAN (conectado a red ), SO premium y SW se facturarán por hora o al mes, por instancia, en función de la instancia suministrada en el host dedicado. Los precios para estos componentes dependerá de la oferta existente en las instancias públicas y en las instancias dedicadas.

Por ejemplo, una instancia dedicada suministrada en un host dedicado con la siguiente configuración no se facturará por instancia. vCPU, RAM, almacenamiento local y velocidades de puerto de enlace ascendente se incluyen en los cargos del host dedicado.

* 8 vCPU
* 16 GB de RAM
* 100 GB de SSD local primer disco
* 400 GB de SSD local segundo disco
* 400 GB de SSD local tercer disco
* 1 Gbps de enlaces ascendentes de red pública y privada (host dedicado)
