---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

keywords: public virtual servers, network traffic, virtual server deployment, profile

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Perfis
{: #about-virtual-server-profiles}

Quando você provisiona instâncias de servidor virtual do {{site.data.keyword.cloud}}, é possível selecionar entre famílias suportadas de perfis. Um perfil é uma combinação de vCPU e RAM que pode ser instanciado rapidamente para iniciar uma instância de servidor virtual. No console do {{site.data.keyword.cloud_notm}}, é possível escolher entre configurações de perfil populares ou selecionar em uma lista de perfis que melhor se ajustam às suas necessidades.
{:shortdesc}

As seguintes famílias de instância de servidor virtual estão disponíveis.

Dependendo de seu tipo de instância, algumas famílias podem não estar disponíveis.
{:note}

| Famílias  | Descrição                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Balanceado](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Melhor para cargas de trabalho de nuvem comuns que requerem um balanceamento de desempenho e escalabilidade. Usa armazenamento conectado à rede. |
| [Armazenamento local balanceado](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage) | Melhor para cargas de trabalho de banco de dados grandes que requerem alto desempenho de E/S com latência muito baixa. |
| [Cálculo](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Melhor para cargas de trabalho de trafego da web moderado a alto. |
| [Memória](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Melhor para cargas de trabalho de armazenamento em cache de memória e de analítica em tempo real. |
| [GPU](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#gpu)  | Melhor para cargas de trabalho de alto desempenho. |
{: caption="Tabela 1. Seleções de família do servidor virtual público" caption-side="top"}

Algumas dessas famílias também estão disponíveis para o IBM Cloud Virtual Servers for VPC. Para obter mais informações, consulte [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen).
{:tip}

## Balanceado
{: #balanced}

Os perfis balanceados (com armazenamento conectado à rede) são ideais para cargas de trabalho de nuvem comuns que requerem um balanceamento de desempenho e escala. O desempenho da rede varia de padrão a premium.

A oferta está disponível nos perfis a seguir:

| Perfil   | vCPU    | RAM     | Tipo de armazenamento |
| --------- | ------- | ------- | ------------ |
| B1.1x2    | 1       | 2 GB    | SAN          |
| B1.1x4    | 1       | 4 GB    | SAN          |
| B1.2x4    | 2       | 4 GB    | SAN          |
| B1.2x8    | 2       | 8 GB    | SAN          |
| B1.4x8    | 4       | 8 GB    | SAN          |
| B1.4x16   | 4       | 16 GB   | SAN          |
| B1.8x16   | 8       | 16 GB   | SAN          |
| B1.8x32   | 8       | 32 GB   | SAN          |
| B1.16x32  | 16      | 32 GB   | SAN          |
| B1.16x64  | 16      | 64 GB   | SAN          |
| B1.32x64  | 32      | 64 GB   | SAN          |
| B1.32x128 | 32      | 128 GB  | SAN          |
| B1.48x192 | 48      | 192 GB  | SAN          |
{: caption="Tabela 2. Perfis balanceados com armazenamento conectado à rede" caption-side="top"}

### Notas de armazenamento

* Disco de inicialização primário da SAN (25 ou 100GB) com discos adicionais disponíveis, até 2 TB cada (cinco discos totais permitidos).
* A precificação para servidores virtuais públicos usando o armazenamento SAN inclui CPU virtual, memória e disco de inicialização primário mínimo. Os preços de discos extras dependem do tamanho do disco e da quantidade que você seleciona.  

Os perfis balanceados (com o armazenamento conectado à rede) estão disponíveis em todos os data centers.

Todos os sistemas operacionais suportados (como RHEL, CentOS, Windows, Ubuntu e outros), bancos de dados suportados e complementos de software também estão disponíveis com esta oferta. 

## Armazenamento local balanceado
{: #balanced-local-storage}

Os perfis de armazenamento local balanceados são principalmente para cargas de trabalho de banco de dados grandes que requerem alto desempenho de E/S com latência muito baixa. O desempenho da rede varia de padrão a premium.

A oferta está disponível em vários perfis e data centers, com as opções de armazenamento local a seguir:

* [HDD local ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#HDD)
* [SSD local ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#SSD)

### HDD local
{: #HDD}
 
<table>
<CAPTION>Tabela 3. Perfis de armazenamento local balanceados usando HDD local</CAPTION>
<THEAD>
<TR>
<th>Perfil</th>
<th>vCPU</th>
<th>RAM</th>
<th>Discos secundários<sup>(*)</sup></th>
<th>Tipo de armazenamento</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>HDD local</td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>HDD local</td>
</tr>
</TBODY>
</table>

#### Notas de armazenamento
* <sup>(*)</sup>Os perfis locais balanceados vêm automaticamente com um disco de inicialização de armazenamento local de 100 GB. Em seguida, é possível selecionar um segundo disco (opções mostradas na Tabela 3). Quaisquer discos locais adicionais são opcionais. Se forem requeridos mais de 500 GB, dois discos adicionais serão necessários (por exemplo, 8 núcleos requerem 2 x 250 GB de armazenamento local).
*	O armazenamento local máximo é limitado pelos núcleos. 
*	O armazenamento local balanceado está disponível globalmente, no entanto, o tipo de armazenamento (SSD local ou HDD local) depende do local do data center. 
*	Não é possível remover discos primários ou secundários.

Os data centers a seguir suportam servidores virtuais de armazenamento local balanceados com HDD local:

| Data centers disponíveis - HDD local |       |
| ---------------------- | ----- |
| Dallas (DAL01)         | Dallas (DAL05)   |
| Dallas (DAL06)         | Houston (HOU02)  |
| Seattle (SEA01)        | San José (SJC01) |
| Washington, DC (WDC01) |                  |
{: class="simple-tab-table"}
{: caption="Tabela 4. Data centers disponíveis (HDD local) - Américas" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd1}
{: tab-title="Americas"}

| Data centers disponíveis - HDD local |
| ---------------------- |
| Amsterdã (AMS01)      |
{: class="simple-tab-table"}
{: caption="Tabela 5. Data centers disponíveis (HDD local) - Europa" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd2}
{: tab-title="Europe"}

| Data centers disponíveis - HDD local |
| ---------------------- |
| Hong Kong (HKG02)      | 
| Singapura (SNG01)      |
{: class="simple-tab-table"}
{: caption="Tabela 6. Data centers disponíveis (HDD local) - Ásia-Pacífico" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd3}
{: tab-title="Asia-Pacific"}

Todos os sistemas operacionais suportados (como RHEL, CentOS, Windows, Ubuntu e outros), bancos de dados suportados e complementos de software também estão disponíveis com esta oferta.  

### SSD local 
{: #SSD}

<table>
<CAPTION>Tabela 7. Perfis de armazenamento local balanceados usando SSD local</CAPTION>
<THEAD>
<TR>
<th>Perfil</th>
<th>vCPU</th>
<th>RAM</th>
<th>Discos secundários<sup>(*)</sup></th>
<th>Tipo de armazenamento</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>SSD local</td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>SSD local</td>
</tr>
</TBODY>
</table>

#### Notas de armazenamento
* <sup>(*)</sup>Os perfis locais balanceados vêm automaticamente com um disco de inicialização de armazenamento local de 100 GB. Em seguida, é possível selecionar um segundo disco (opções mostradas na tabela acima). Quaisquer discos locais adicionais são opcionais. Se forem requeridos mais de 500 GB, dois discos adicionais serão necessários (por exemplo, 8 núcleos requerem 2 x 250 GB de armazenamento local).
*	O armazenamento local máximo é limitado pelos núcleos. 
*	O armazenamento local balanceado está disponível globalmente, no entanto, o tipo de armazenamento (SSD local ou HDD local) depende do local do data center. 
*	Não é possível remover discos primários ou secundários.

Os data centers a seguir suportam servidores virtuais de armazenamento local balanceados com SSD local:

| Data centers disponíveis - SDD Local |        |
| ---------------------------------- | ------ |
| Dallas (DAL09)                     | Dallas (DAL10)         |
| Dallas (DAL12)                     | Dallas (DAL13)         |
| Queretaro (MEX01)                  | Montreal (MON01)       |
| São Paulo (SAO01)                  | San José (SJC03)       |
| San José (SJC04)                   | Toronto (TOR01)        |
| Washington, DC (WDC04)             | Washington, DC (WDC06) |
| Washington, DC (WDC07)             |                        |
{: class="simple-tab-table"}
{: caption="Tabela 8. Data centers disponíveis (SDD local) - Américas" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd1}
{: tab-title="Americas"}

| Data centers disponíveis - SDD Local |       |
| ---------------------------------- | ----- |
| Amsterdã (AMS03)                  | Frankfurt (FRA02) |
| Londres (LON02)                     | Londres (LON04)    |
| Londres (LON06)                     | Milão (MIL01)     |
| Oslo (OSL01)                       | Paris (PAR01)     |
{: class="simple-tab-table"}
{: caption="Tabela 9. Data centers disponíveis (SDD local) - Europa" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd2}
{: tab-title="Europe"}

| Data centers disponíveis - SDD Local |       |
| ---------------------------------- | ----- |
| Chennai (CHE01)                    | Melbourne (MEL01) |
| Seul (SEO01)                      | Sydney (SYD01)    |
| Sydney (SYD04)                     | Tóquio (TOK02)     |
{: class="simple-tab-table"}
{: caption="Tabela 10. Data centers disponíveis (SDD local) - Ásia-Pacífico" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd3}
{: tab-title="Asia-Pacific"}

Todos os sistemas operacionais suportados (como RHEL, CentOS, Windows, Ubuntu e outros), bancos de dados suportados e complementos de software também estão disponíveis com esta oferta.

## Computação
{: #compute}

Os perfis de cálculo são melhores para cargas de trabalho com demandas de CPU intensivas, como cargas de trabalho de tráfego da web alto, processamento em lote de produção e servidores da web de front-end.

A oferta está disponível nos perfis a seguir:

| Perfil      | vCPU     | RAM       | Tipo de armazenamento |
| ------------ | -------- | --------- | ------------ |
| C1.1x1       | 1        | 1 GB      | SAN          |
| C1.2x2       | 2        | 2 GB      | SAN          |
| C1.4x4       | 4        | 4 GB      | SAN          |
| C1.8x8       | 8        | 8 GB      | SAN          |
| C1.16x16     | 16       | 16 GB     | SAN          |
| C1.32x32     | 32       | 32 GB     | SAN          |
{: caption="Tabela 11. Perfis de cálculo" caption-side="top"}

### Notas de armazenamento
* Disco de inicialização primária SAN (25 ou 100 GB) com discos adicionais disponíveis de até 2 TB cada (cinco discos totais permitidos).
* A precificação para servidores virtuais públicos usando o armazenamento SAN inclui CPU virtual, memória e disco de inicialização primário mínimo. Os preços de discos extras dependem do tamanho do disco e da quantidade que você seleciona.  

Os perfis de cálculo estão disponíveis em todos os data centers.

Todos os sistemas operacionais suportados (como RHEL, CentOS, Windows, Ubuntu e outros), bancos de dados suportados e complementos de software também estão disponíveis com esta oferta.

## Memória
{: #memory}

Os perfis de memória são melhores para cargas de trabalho de memória intensiva, como cargas de trabalho de armazenamento em cache grandes, aplicativos de banco de dados intensivos ou cargas de trabalho analíticas na memória.

A oferta está disponível nos perfis a seguir:

| Perfil      | vCPU     | RAM       | Tipo de armazenamento |
| ------------ | -------- | --------- | ------------ |
| M1.1x8       | 1        | 8 GB      | SAN          |
| M1.2x16      | 2        | 16 GB     | SAN          |
| M1.4x32      | 4        | 32 GB     | SAN          |
| M1.8x64      | 8        | 64 GB     | SAN          |
| M1.16x128    | 16       | 128 GB    | SAN          |
| M1.30x240    | 30       | 240 GB    | SAN          |
| M1.48x384    | 48       | 384 GB    | SAN          |
| M1.56x448    | 56       | 448 GB    | SAN          |
| M1.64x512    | 64       | 512 GB    | SAN          |
{: caption="Tabela 12. Perfis de memória" caption-side="top"}

### Notas de armazenamento
* Disco de inicialização primária SAN (25 ou 100 GB) com discos adicionais disponíveis, até 2 TB cada um (total de 5 discos permitidos).
* A precificação para servidores virtuais públicos usando o armazenamento SAN inclui CPU virtual, memória e disco de inicialização primário mínimo. Os preços de discos adicionais dependem do tamanho do disco e da quantidade selecionada.  

Os perfis de memória estão disponíveis em todos os data centers.

Todos os sistemas operacionais suportados (como RHEL, CentOS, Windows, Ubuntu e outros), bancos de dados suportados e complementos de software também estão disponíveis com esta oferta.

## GPU
{: #gpu}

Os perfis de GPU são melhores para cargas de trabalho de alto desempenho que requerem mais densidade de cálculo para reduzir o gerenciamento de recursos e os custos. Os perfis de GPU são ideais para os processos de inteligência
artificial, para os aplicativos gráficos e de dados intensos ou para o desenvolvimento de novos aplicativos que requerem desempenho rápido.

Desenvolvidos com GPUs NVDIA Tesla, tanto o perfil “ac1” quanto o "ac2" do {{site.data.keyword.cloud_notm}} Accelerated Compute oferecem armazenamento de bloco e SSD local. Os perfis de GPU a seguir estão disponíveis para sua escolha:  

<table>
<CAPTION>Tabela 13. Perfis de GPU P100</CAPTION>
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

Os perfis de GPU P100 estão disponíveis nos data centers _DAL13_, _LON06_ e _WDC07_.
{: note}

<table>
<CAPTION>Tabela 14. Perfis de GPU V100</CAPTION>
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

Os perfis da GPU V100 estão disponíveis nos data centers _DAL10_, _DAL12_, _LON04_ e _WDC07_.
{: note}

### Pré-requisitos de GPU
Revise os pré-requisitos de GPU a seguir.

1. Os servidores virtuais dos perfis de GPU estão disponíveis apenas em um sistema operacional que suporte o modo de inicialização Hardware Virtual Machine (HVM). Consulte a lista a seguir para os sistemas operacionais que suportam o modo de inicialização do HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Drivers NVIDIA e software apropriados devem ser instalados. Para obter mais informações sobre software e drivers NVIDIA, veja [Instalando drivers GPU e pacotes de software](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages).  

O software que você instala pode ter software obrigatório e configurações específicas do sistema operacional.
{: note}

### Incluindo ou removendo GPUs 
É possível mudar o número de GPUs em seu servidor virtual após seu pedido inicial. Mas, isso depende de quantos GPUs você provisionou. Você tem uma das opções a seguir.

- Se um GPU estiver provisionado, será possível incluir outro GPU ou
- Se dois GPUs estiverem provisionados, será possível efetuar fallback para um GPU

