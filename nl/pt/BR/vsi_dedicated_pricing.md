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

# Precificação de servidor virtual dedicado
{: #dedicated-virtual-server-pricing}

A precificação para hosts dedicados será oferecida em um modelo por hora e mensal.
{:shortdesc}

A precificação do host dedicado pode ser vista abaixo e será inclusiva de todos os componentes de vCPU, RAM, armazenamento local e de velocidade da porta de uplink pois as instâncias são provisionadas para hosts dedicados.

Com hosts dedicados, discos de armazenamento local adicionais estarão disponíveis no primeiro, segundo, terceiro, quarto e quinto discos. Há também a capacidade adicional até 400 GB em cada disco secundário.

As instâncias por hora podem ser provisionadas em hosts por hora e mensal. As instâncias mensais podem ser provisionadas somente em hosts mensais.

| Configuração de host | vCPU	| RAM (GB) | Armazenamento Local (TB SSD) |	Preço por hora | Preço mensal |
| ------------------ | ---- | -------- | ---------------------- | ------------ | ------------- |
| 56x242x1.2TB	     |  56 	|   242    |        	1,2	          |     $ 3,164   | 	$ 2.099,00    |
{: caption="Tabela 1. Precificação de host dedicado" caption-side="top"}

Observe que o preço varia por região.

A SAN (rede conectada), os OSs premium e os complementos de SW serão cobrados por hora ou mensalmente, pela instância, dependendo da instância provisionada no host dedicado. A precificação para esses componentes é consistente com a oferta existente em instâncias públicas e instâncias dedicadas.

Por exemplo, uma instância dedicada provisionada em um host dedicado com a configuração a seguir não será cobrada pela instância. VCPU, RAM, armazenamento local e velocidades de porta de uplink são incluídos em encargos de host dedicado.

* 8 vCPU
* 16 GB de RAM
* Primeiro disco SSD local de 100 GB
* Segundo disco SSD local de 400 GB
* Terceiro disco SSD local de 400 GB
* Uplinks de redes pública e privada de 1 Gbps (host dedicado)
