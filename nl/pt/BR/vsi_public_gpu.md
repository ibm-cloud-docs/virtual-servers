---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
{: #gpu}

Os perfis de GPU são melhores para cargas de trabalho de alto desempenho que requerem mais densidade de cálculo para reduzir o gerenciamento de recursos e os custos. Os perfis de GPU são ideais para os processos de inteligência
artificial, para os aplicativos gráficos e de dados intensos ou para o desenvolvimento de novos aplicativos que requerem desempenho rápido.

Desenvolvidos pelas GPUs da NVDIA Tesla, os tipos “ac1” e "ac2" do {{site.data.keyword.cloud_notm}}
Accelerated Compute oferecem armazenamento em bloco e SSD local. Os perfis de GPU a seguir estão disponíveis para sua escolha:  

  <table>
<CAPTION>Tabela 1. Perfis de GPU P100</CAPTION>
<THEAD>
<TR>
<th>Perfil</th>
<th>GPU</th>
<th>RAM de GPU (GB)</th>
<th>vCPU</th>
<th>RAM de vCPU (GB)</th>
<th>Tipo de armazenamento</th>
<th>Disco de inicialização (GB)</th>
<th>Discos secundários (2 e 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Bloco (SAN)</td>
<td>25</td>
<td>Nenhum</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD local ou SAN</td>
<td>100</td>
<td>Nenhum (SAN)<br>300 (local)</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Bloco (SAN)</td>
<td>25</td>
<td>Nenhum</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD local ou SAN</td>
<td>100</td>
<td>Nenhum (SAN)<br>600 (local)</td></tr>

</TBODY>
</table>

**Nota:** os perfis de GPU P100 estão disponíveis nos data centers _DAL13_, _LON06_ e _WDC07_.

<table>
<CAPTION>Tabela 2. Perfis de GPU V100</CAPTION>
<THEAD>
<TR>
<th>Perfil</th>
<th>GPU</th>
<th>RAM de GPU (GB)</th>
<th>vCPU</th>
<th>RAM de vCPU (GB)</th>
<th>Tipo de armazenamento</th>
<th>Disco de inicialização (GB)</th>
<th>Discos secundários (2 e 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Bloco (SAN)</td>
<td>25</td>
<td>Nenhum</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD local ou SAN</td>
<td>100</td>
<td>Nenhum (SAN)<br>300 (local)</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Bloco (SAN)</td>
<td>25</td>
<td>Nenhum</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD local ou SAN</td>
<td>100</td>
<td>Nenhum (SAN)<br>600 (local)</td></tr>

</TBODY>
</table>

**Nota:** os perfis de GPU V100 estão disponíveis nos data centers _DAL10_, _DAL12_, _LON04_ e _WDC07_.


## Antes de iniciar
Revise os pré-requisitos de GPU a seguir.

1. Os servidores virtuais dos perfis de GPU estão disponíveis apenas em um sistema operacional que suporte o modo de inicialização Hardware Virtual Machine (HVM). Consulte a lista a seguir para os sistemas operacionais que suportam o modo de inicialização do HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Drivers NVIDIA e software apropriados devem ser instalados. Para obter mais informações sobre software e drivers NVIDIA, veja [Instalando drivers GPU e pacotes de software](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages).  
**Nota:** o software instalado pode ter software obrigatório e configurações específicas do sistema operacional.

## Incluir ou remover GPUs
É possível mudar o número de GPUs em seu servidor virtual após seu pedido inicial. Mas, isso depende de quantos GPUs você provisionou. Você tem uma das opções a seguir.

- Se um GPU estiver provisionado, será possível incluir outro GPU ou
- Se dois GPUs estiverem provisionados, será possível efetuar fallback para um GPU
