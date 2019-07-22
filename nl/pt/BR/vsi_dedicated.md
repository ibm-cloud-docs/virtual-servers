---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# Sobre servidores virtuais dedicados
{: #dedicated-virtual-servers}

A oferta de host dedicado da infraestrutura do {{site.data.keyword.Bluemix}} é um servidor virtualizado, dedicado e de locatário único. Ele fornece a você o controle máximo sobre as opções de posicionamento de carga de trabalho e pós-fornecimento flexível. É possível decidir em qual data center predeterminado do {{site.data.keyword.cloud_notm}} seus servidores virtuais serão colocados e poderão ter a capacidade assegurada alocando seus hosts diretamente em sua conta.
{:shortdesc}

A oferta inclui os recursos a seguir:

* Afinidade e antiafinidade. É possível especificar os relacionamentos de host para servidor virtual e de servidor virtual para servidor virtual que devem permanecer, que são conhecidos como regras de afinidade e antiafinidade. Essas regras ajudam a assegurar que suas cargas de trabalho sejam colocadas de forma apropriada com base em seus requisitos de carga de trabalho.
* Gerenciamento pós-implementação. É possível migrar servidores virtuais entre hosts dedicados com base em seus requisitos de carga de trabalho.
* Visibilidade de carga de trabalho. É possível visualizar o consumo de recursos — núcleo, RAM e armazenamento local — para cada host, fornecendo o controle máximo sobre seu gerenciamento de carga de trabalho.

Você tem a opção de dois modelos de implementação: hosts dedicados e instâncias dedicadas. Os hosts dedicados ajudam com o controle sobre o posicionamento de carga e as instâncias dedicadas oferecem isolamento de locatário único.

Instâncias dedicadas não fornecem alguns dos recursos de controle oferecidos por hosts dedicados.  Veja a tabela a seguir para obter mais detalhes.
{:note}

| Recurso de servidor virtual dedicado | Instâncias de hosts Dedicados | Instâncias dedicadas |
| ------- | ------- | ------- |
| Isolamento de locatário único | ![Ícone de visto](../../icons/checkmark-icon.svg) | ![Ícone de visto](../../icons/checkmark-icon.svg) |
| Controle de posicionamento de servidor virtual | ![Ícone de visto](../../icons/checkmark-icon.svg) |   |
| Visibilidade de recurso | ![Ícone de visto](../../icons/checkmark-icon.svg) |   |
| Faturamento de instância |   | ![Ícone de visto](../../icons/checkmark-icon.svg) |
| Faturamento de host<sup>(1)</sup> | ![Ícone de visto](../../icons/checkmark-icon.svg) |   |
| Controle pós-implementação | ![Ícone de visto](../../icons/checkmark-icon.svg) |   |
| Reservas de capacidade | ![Ícone de visto](../../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="Tabela 1. Recursos de controle" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup>A precificação de host é inclusiva de núcleo, RAM, SSD local e velocidades de rede. Sistema operacional Premium (OS), armazenamento de rede de área de armazenamento (SAN) e complementos de software serão precificados por instância com a precificação e o licenciamento existentes em um modelo por hora ou mensal.

Tenha em mente o seguinte quando você estiver pedindo um host dedicado e instâncias de host dedicado:

* O tamanho do host é determinado pelas cargas de trabalho em você executará nele. O padrão é 56 núcleos X 242 GB de RAM X 1,2 TB, mas é possível escolher entre configurações adicionais.
* É possível pedir somente dois hosts por vez. Por exemplo, se você precisar de seis hosts, será necessário colocar três ordens separadas.
* Cada host precisará de seu próprio nome exclusivo e será possível designar automaticamente seu POD.

## Próximas Etapas

Depois de ter revisado e decidido sobre suas opções de implementação, é hora de provisionar seu servidor virtual. Para iniciar, veja [Provisionando hosts dedicados e instâncias](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated).
