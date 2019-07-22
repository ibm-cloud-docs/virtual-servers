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

# Precificação do host dedicado
{: #dedicated-virtual-server-pricing}

A precificação para hosts dedicados é oferecida em um modelo por hora e mensal.
{:shortdesc}

A precificação do host dedicado é inclusiva de todos os componentes de vCPU, RAM, armazenamento local e de velocidade de porta de uplink conforme as instâncias são provisionadas em hosts dedicados. Para obter mais informações sobre precificação, consulte a [Calculadora de provisionamento de servidores virtuais ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

Com hosts dedicados, discos de armazenamento local adicionais estão disponíveis no primeiro, segundo, terceiro, quarto e quinto discos. Há também capacidade adicional de até 400 GB em cada disco secundário.

As instâncias por hora podem ser provisionadas em hosts por hora e mensal. As instâncias mensais podem ser provisionadas somente em hosts mensais.

| Configuração de host | vCPU	| RAM (GB) | Armazenamento Local (TB SSD) |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |  56 	|   242    |        	1,2	          |
| 56x484x1.2         |  56  |   484    |          1,2           |
{: caption="Tabela 1. Configurações de host dedicado" caption-side="top"}

A precificação varia por região.
{:note}

SAN (rede conectada), sistemas operacionais premium e complementos de SW são cobrados por hora ou mensalmente, pela instância, dependendo da instância provisionada no host dedicado. A precificação para esses componentes é consistente com a oferta existente em instâncias públicas e instâncias dedicadas. 

Por exemplo, uma instância dedicada provisionada em um host dedicado com a configuração a seguir não é cobrada pela instância. VCPU, RAM, armazenamento local e velocidades de porta de uplink são incluídos em encargos de host dedicado. 

* 8 vCPU
* 16 GB de RAM
* Primeiro disco SSD local de 100 GB
* Segundo disco SSD local de 400 GB
* Terceiro disco SSD local de 400 GB
* Uplinks de redes pública e privada de 1 Gbps (host dedicado) 

