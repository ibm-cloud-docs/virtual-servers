---



copyright:
  years: 2017, 2018
lastupdated: "2018-2-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
Os tipos GPU são melhores para cargas de trabalho de alto desempenho que requerem mais densidade de cálculo para reduzir o gerenciamento de recursos e os custos. GPUs são ideais para aplicativos gráficos e de dados intensos ou para desenvolver novos aplicativos que requerem desempenho rápido.

Desenvolvido com GPUs NVDIA Tesla P100, a família “ac1” de Cálculo acelerado do {{site.data.keyword.cloud_notm}} oferece armazenamento de bloco (ac1) e de SSD local (acl1). Os tipos de GPU a seguir estão disponíveis para você escolher:  

<table>

<caption>Tabela 1. Tipos de GPU</caption>

  
<thead>
<td rowspan="4"></td>
  <th colspan="4">Tipos de GPU</th>
<tr>
  <th>ac1.8x60</th>
  <th>acl1.8x60</th>
  <th>ac1.16x120</th>
  <th>acl1.16x120</th>
</tr>
</thead>
<TBODY>
<tr>
  <th><b>GPU</b></th>
  <td>1 x P100</td>
  <td>1 x P100</td>
  <td>2 x P100</td>
  <td>2 x P100</td>
</tr>
<tr>
  <th><b>RAM de GPU (GB)</b></th>
  <td>16</td>
  <td>16</td>
  <td>32</td>
  <td>32</td>
</tr>

<tr>
  <th><b>vCPU</b></th>
  <td>8</td>
  <td>8</td>
  <td>16</td>
  <td>16</td>
</tr>

<tr>
  <th><b>RAM de vCPU (GB)</b></th>
  <td>60</td>
  <td>60</td>
  <td>120</td>
  <td>120</td>
</tr>

<tr>
  <th><b>Tipo de armazenamento</b></th>
  <td>Bloco (SAN)</td>
  <td>SSD local</td>
  <td>Bloco (SAN)</td>
  <td>SSD local</td>
</tr>

<tr>
  <th><b>Disco de inicialização (GB)</b></th>
  <td>25 e 100</td>
  <td>100</td>
  <td>25 e 100</td>
  <td>100</td>
</tr>

<tr>
  <th><b>Disco secundário (GB)</b></th>
  <td>4 x 2000</td>
  <td>2 x 300</td>
  <td>4 x 2000</td>
  <td>2 x 300</td>
</tr>

</TBODY>
</table>


**Nota:** os tipos de GPU estão disponíveis no data center _DAL13_.

## Antes de iniciar
Revise os pré-requisitos de GPU a seguir.

1. Os servidores virtuais da Família GPU estão disponíveis apenas em um sistema operacional que suporta o modo de inicialização Hardware Virtual Machine (HVM). Veja a lista a seguir para obter os sistemas operacionais que suportam o modo de inicialização HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Windows 2012 R2
  - Windows 2016

2. Drivers NVIDIA e software apropriados devem ser instalados. Para obter mais informações sobre software e drivers NVIDIA, veja [Instalando drivers GPU e pacotes de software](../vsi/vsi_gpu_nvidia_drivers.html).

**Nota:** o software instalado pode ter software obrigatório e configurações específicas do sistema operacional.


