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

# Memória
{: #memory}

Os perfis de memória são melhores para cargas de trabalho de memória intensiva, como cargas de trabalho de armazenamento em cache grandes, aplicativos de banco de dados intensivos ou cargas de trabalho analíticas na memória.

A oferta está disponível nos perfis a seguir:

<table>
<CAPTION>Tabela 1. Perfis de memória</CAPTION>
<THEAD>
<TR>
<th>Perfil</th>
<th>vCPU</th>
<th>RAM</th>
<th>Tipo de armazenamento</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>M1.1x8</td>
<td>1</td>
<td>8 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.2x16</td>
<td>2</td>
<td>16 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.4x32</td>
<td>4</td>
<td>32 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.8x64</td>
<td>8</td>
<td>64 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.16x128</td>
<td>16</td>
<td>128 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.30x240</td>
<td>30</td>
<td>240 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.48x384</td>
<td>48</td>
<td>384 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.56x448</td>
<td>56</td>
<td>448 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.64x512</td>
<td>64</td>
<td>512 GB</td>
<td>SAN</td>
</tr>
</TBODY>
</table>

**Notas de armazenamento:**
* Disco de inicialização primária SAN (25 ou 100 GB) com discos adicionais disponíveis, até 2 TB cada um (total de 5 discos permitidos).
* A precificação para servidores virtuais públicos usando o armazenamento SAN inclui CPU virtual, memória e disco de inicialização primário mínimo. Os preços de discos adicionais dependem do tamanho do disco e da quantidade selecionada.  

Os perfis de memória estão disponíveis em todos os data centers.

Todos os sistemas operacionais suportados (como RHEL, CentOS, Windows, Ubuntu e outros), bancos de dados suportados e complementos de software também estão disponíveis com esta oferta.  
