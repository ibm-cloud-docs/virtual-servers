---



copyright:
  years: 2017, 2018
lastupdated: "2018-6-18"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
Os tipos GPU são melhores para cargas de trabalho de alto desempenho que requerem mais densidade de cálculo para reduzir o gerenciamento de recursos e os custos. Os tipos do GPU são ideais para aplicativos intensos de gráficos e de dados ou para desenvolver novos aplicativos que requerem desempenho rápido.

Desenvolvido com GPUs NVDIA Tesla P100, o tipo “ac1” de Cálculo acelerado do {{site.data.keyword.cloud_notm}} oferece armazenamento SSD tanto em bloco quanto local. Os tipos de GPU a seguir estão disponíveis para você escolher:  

  <table>
<CAPTION>Tabela 1. Tipos de GPU</CAPTION>
<THEAD>
<TR>
<th>Tipo</th>
<th>GPU</th>
<th>RAM de GPU (GB)</th>
<th>vCPU</th>
<th>RAM de vCPU (GB)</th>
<th>Tipo de armazenamento</th>
<th>Disco de inicialização (GB)</th>
<th>Disco secundário (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Bloco (SAN)</td>
<td>25 e 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD local</td>
<td>100</td>
<td>2 x 300</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Bloco (SAN)</td>
<td>25 e 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD local</td>
<td>100</td>
<td>2 x 600</td></tr>

</TBODY>
</table>

**Observação:** os tipos de GPU estão disponíveis nos data centers _DAL13_, _LON06_ e _WDC07_.

## Antes de iniciar
Revise os pré-requisitos de GPU a seguir.

1. Os servidores virtuais dos tipos do GPU estão disponíveis apenas em um sistema operacional que suporta o modo de inicialização Hardware Virtual Machine (HVM). Veja a lista a seguir para obter os sistemas operacionais que suportam o modo de inicialização HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Drivers NVIDIA e software apropriados devem ser instalados. Para obter mais informações sobre software e drivers NVIDIA, veja [Instalando drivers GPU e pacotes de software](../vsi/vsi_gpu_nvidia_drivers.html).  
**Nota:** o software instalado pode ter software obrigatório e configurações específicas do sistema operacional.

# Incluir ou remover GPUs
É possível mudar o número de GPUs em seu servidor virtual após seu pedido inicial. Mas, isso depende de quantos GPUs você provisionou. Você tem uma das opções a seguir. Na tela de pedido de provisionamento, você tem uma das opções a seguir
- Se um GPU estiver provisionado, será possível incluir outro GPU ou
- Se dois GPUs estiverem provisionados, será possível efetuar fallback para um GPU
