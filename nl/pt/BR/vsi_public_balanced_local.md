---



copyright:
  years: 2017
lastupdated: "2017-11-08"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Armazenamento local balanceado
Os tipos de armazenamento local balanceado são principalmente para clusters de bancos de dados grandes que requerem desempenho de E/S de latência alta ou baixa. Essa oferta tem maior desempenho porque os recursos não são sobrecarregados. O desempenho da rede varia de padrão a premium.

A oferta está disponível em vários tipos e data centers, com as opções de armazenamento local a seguir:

* [HDD local](vsi_public_balanced_local.html#HDD)
* [SSD local](vsi_public_balanced_local.html#SSD)

## HDD local {: #HDD}
 
<table>
<CAPTION>Tabela 1. Tipos de armazenamento local balanceado usando HDD local</CAPTION>
<THEAD>
<TR>
<th>Tipo</th>
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

**Notas de armazenamento:**
* <sup>(*)</sup>Os tipos locais balanceados vêm automaticamente com um disco de inicialização de armazenamento local de 100 GB. Em seguida, é possível selecionar um segundo disco (opções mostradas na tabela acima). Quaisquer discos locais adicionais são opcionais. Se forem requeridos mais de 500 GB, dois discos adicionais serão necessários (por exemplo, 8 núcleos requerem 2 x 250 GB de armazenamento local).
*	O armazenamento local máximo é limitado pelos núcleos. 
*	O armazenamento local balanceado está disponível globalmente, no entanto, o tipo de armazenamento (SSD local ou HDD local) depende do local do data center. 
*	Não é possível remover discos primários ou secundários.

Os data centers a seguir suportam servidores virtuais de Armazenamento Local Balanceado com HDD local:

|Data Centers (HDD Local) |        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   | 
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02        |        |  
{: caption="Tabela 1. Data centers suportados (HDD Local)" caption-side="top"}

Todos os sistemas operacionais suportados (como RHEL, CentOS, Windows, Ubuntu e outros), bancos de dados suportados e complementos de software também estão disponíveis com esta oferta.  

## SSD local {: #SSD}
<table>
<CAPTION>Tabela 1. Tipos de armazenamento local balanceado usando SSD local</CAPTION>
<THEAD>
<TR>
<th>Tipo</th>
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

**Notas de armazenamento:**
* <sup>(*)</sup>Os tipos locais balanceados vêm automaticamente com um disco de inicialização de armazenamento local de 100 GB. Em seguida, é possível selecionar um segundo disco (opções mostradas na tabela acima). Quaisquer discos locais adicionais são opcionais. Se forem requeridos mais de 500 GB, dois discos adicionais serão necessários (por exemplo, 8 núcleos requerem 2 x 250 GB de armazenamento local).
*	O armazenamento local máximo é limitado pelos núcleos. 
*	O armazenamento local balanceado está disponível globalmente, no entanto, o tipo de armazenamento (SSD local ou HDD local) depende do local do data center. 
*	Não é possível remover discos primários ou secundários.

Os data centers a seguir suportam servidores virtuais de Armazenamento Local Balanceado com SSD local:

|Data Centers (SSD Local) |        |         |
|------- |------  |------ | 
|AMS03   |LON06   |SJC03  |
|CHE01   |MEL01   |SJC04  | 
|DAL09   |MEX01   |SYD01  |
|DAL10   |MIL01   |SYD04  |
|DAL12   |MON01   |TOK02  |       
|DAL13   |OSL01   |TOR01  |
|FRA02   |PAR01   |WDC04  |
|LON02   |SAO01   |WDC06  |
|LON04   |SEO01   | WDC07 | 
{: caption="Tabela 2. Data centers suportados (SSD Local)" caption-side="top"}

Todos os sistemas operacionais suportados (como RHEL, CentOS, Windows, Ubuntu e outros), bancos de dados suportados e complementos de software também estão disponíveis com esta oferta.  
