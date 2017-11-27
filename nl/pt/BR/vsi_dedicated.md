---



copyright: years: 2017 lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Servidores virtuais dedicados
A oferta de host dedicado da infraestrutura do {{site.data.keyword.Bluemix}} é um servidor virtualizado, dedicado e de locatário único. Ele fornece a você o controle máximo sobre as opções de posicionamento de carga de trabalho e pós-fornecimento flexível. É possível decidir em qual data center predeterminado do {{site.data.keyword.cloud}} seus servidores virtuais serão colocados e poderão ter a capacidade assegurada alocando seus hosts diretamente em sua conta.
{:shortdesc}

A oferta inclui os recursos a seguir: 

* Afinidade e antiafinidade. É possível especificar os relacionamentos de host para servidor virtual e de servidor virtual para servidor virtual que devem permanecer, que são conhecidos como regras de afinidade e antiafinidade. Essas regras ajudam a assegurar que suas cargas de trabalho sejam colocadas de forma apropriada com base em seus requisitos de carga de trabalho.
* Gerenciamento pós-implementação. É possível migrar servidores virtuais entre hosts dedicados com base em seus requisitos de carga de trabalho.
* Visibilidade de carga de trabalho. É possível visualizar o consumo de recursos — núcleo, RAM e armazenamento local — para cada host, fornecendo o controle máximo sobre seu gerenciamento de carga de trabalho.

Você tem a opção de dois modelos de implementação: hosts dedicados e instâncias dedicadas. Os hosts dedicados ajudam com o controle sobre o posicionamento de carga e as instâncias dedicadas oferecem isolamento de locatário único. 

**Nota:** as instâncias dedicadas não fornecem alguns dos recursos de controle oferecidos por hosts dedicados.  Veja a tabela a seguir para obter mais detalhes. 
<table>
<CAPTION>Tabela 1. Recursos de controle</CAPTION>
<THEAD>
<TR>
<th>Recurso de servidor virtual dedicado</th>
<th>Instâncias de hosts Dedicados</th>
<th>Instâncias dedicadas</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>Isolamento de locatário único</td>
<td>P</td>
<td>P</td>
</tr>
<tr>
<td>Controle de posicionamento de servidor virtual</td>
<td>P</td>
<td></td>
</tr>
<tr>
<td>Visibilidade de recurso</td>
<td>P</td>
<td></td>
</tr>
<tr>
<td>Faturamento de instância</td>
<td></td>
<td>P</td>
</tr>
<tr>
<td>Faturamento de host<sup>(1)</sup></td>
<td>P</td>
<td></td>
</tr>
<tr>
<td>Controle pós-implementação</td>
<td>P</td>
<td></td>
</tr>
<tr>
<td>Reservas de capacidade</td>
<td>P</td>
<td></td>
</tr>
</TBODY>
</table>


<sup>(1)</sup>A precificação de host é inclusiva de núcleo, RAM, SSD local e velocidades de rede. Sistema operacional Premium (OS), armazenamento de rede de área de armazenamento (SAN) e complementos de software serão precificados por instância com a precificação e o licenciamento existentes em um modelo por hora ou mensal.

Tenha em mente o seguinte quando você estiver pedindo um host dedicado e instâncias de host dedicado:

* Seu local de host; é possível selecionar nos data centers do {{site.data.keyword.cloud_notm}} a seguir:
      
| Data centers          ||
| ------------ | ------- | 
|AMS01         |  MON01  |
|AMS03         |  OSL01  |
|CHE01         |  PAR01  |
|DAL05         |  SAO01  |
|DAL06         |  SEO01  |
|DAL09         |  SJC01  |
|DAL10         |  SJC03  |
|DAL12         |  SJC04  |
|DAL13         |  SNG01  | 
|FRA02         |  SYD01  |
|HKG02         |  SYD04  |
|HOU02         |  TOK02  |
|LON02         |  TOR01  |
|LON04         |  WDC01  |
|MEL01         |  WDC04  |
|MEX01         |  WDC06  |
|MIL01         |  WDC07  |
{: caption="Tabela 2. Data centers suportados" caption-side="top"}

* O tamanho do host é determinado pelas cargas de trabalho em você executará nele. O padrão é 56 Núcleos X 242 GB de RAM X 1,2 TB. 
* É possível pedir somente dois hosts por vez. Por exemplo, se você precisar de seis hosts, será necessário colocar três ordens separadas.
* Cada host precisará de seu próprio nome exclusivo e será possível designar automaticamente seu POD.

## Próximas Etapas

Depois de ter revisado e decidido sobre suas opções de implementação, é hora de provisionar seu servidor virtual. Para iniciar, veja [Provisionando hosts dedicados e instâncias](../vsi/vsi_provision_dedicated.html).



  
