---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-06"

subcollection: virtual-servers

---

{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Opções de armazenamento
{: #storage-options}

Existe a opção de armazenamento SAN (SAN móvel) ou local para cada servidor virtual. É possível complementar a SAN ou o armazenamento local com outros produtos de armazenamento conforme necessário.

## Armazenamento local

O armazenamento local é construído em discos que são locais para o host do servidor virtual. O armazenamento local fornece melhor desempenho de leitura/gravação de disco. Os discos são construídos em uma configuração de Redundant Array of Independent Disks (RAID) para redundância, substituição de disco e monitoramento de funcionamento que é totalmente gerenciado pelo {{site.data.keyword.cloud}}. Em data centers mais recentes, esse armazenamento é toda unidade de estado sólido (SSD) para fornecer o melhor desempenho.

## Armazenamento SAN móvel

Os volumes de armazenamento móvel são soluções de armazenamento auxiliar exclusivamente disponíveis nos {{site.data.keyword.BluVirtServers_short}}.  A SAN móvel é construída em todos os clusters de armazenamento flash do {{site.data.keyword.cloud_notm}} em vez de no armazenamento do host local. Essa infraestrutura fornece maior resiliência no caso de uma falha do host e também
pode suportar volumes muito maiores. Se houver uma falha do host, as instâncias de servidor virtual que usam armazenamento baseado em SAN serão migradas automaticamente para outros hosts e reiniciadas.

O armazenamento móvel é uma solução ideal se você deseja transferir dados entre servidores virtuais existentes em qualquer data center na rede do {{site.data.keyword.cloud_notm}}. Os volumes de armazenamento móvel são úteis para aplicativos de banco de dados que requerem acesso ao armazenamento em nível de bloco bruto e não formatado e para mover grandes conjuntos de dados entre os {{site.data.keyword.BluVirtServers_short}}.

Todos os discos secundários são conectados como armazenamento móvel. Na maioria dos casos, esses discos secundários podem ser separados a qualquer momento para permitir que sejam movidos para outros servidores virtuais.

Com os servidores virtuais públicos que usam armazenamento local balanceado, não é possível remover discos primários ou secundários.
{:important}

Os discos podem ser reconectados a outro servidor, contanto que a mudança não exceda a cota do disco ou o limite de tamanho máximo do volume do servidor virtual de destino.

O disco movido é convertido para o tipo de armazenamento do servidor de destino.
{:note}

Quando um volume de armazenamento móvel é anexado a um servidor virtual em um data center diferente do servidor virtual original, o sistema interno do {{site.data.keyword.cloud_notm}} copia o volume para a SAN no novo data center. O sistema verifica então a integridade do volume copiado e remove o volume móvel original da SAN do data center original.

## Limitações de LVM

O Logical volume management (LVM) não é suportado como um esquema de particionamento inicializável. Com o suporte e a configuração do sistema operacional adequados, os discos de servidor virtual secundário podem ser usados para partições LVM. No entanto, o LVM não é um sistema de arquivos suportado para Modelos de imagem ou Flex Images.

## Armazenamento suplementar

Os servidores virtuais são totalmente compatíveis com o {{site.data.keyword.filestorage_short}}, o {{site.data.keyword.blockstorageshort}} e o {{site.data.keyword.cos_full}}. Esses tipos de armazenamentos são recomendados para unidades de cluster, armazenamento de arquivo compartilhado, armazenamento de archive, requisitos de armazenamento grande ou requisitos de desempenho específicos.

Para obter mais informações sobre as opções de armazenamento adicional, consulte os recursos a seguir:

* [Introdução ao Block Storage](/docs/infrastructure/BlockStorage?topic=BlockStorage-getting-started)
* [Introdução ao File Storage](/docs/infrastructure/FileStorage?topic=FileStorage-getting-started)
* [Introdução ao Object Storage](/docs/services/cloud-object-storage?topic=cloud-object-storage-getting-started)

## Próximas Etapas
Para obter mais informações sobre como usar os volumes de armazenamento móvel, veja as tarefas a seguir:
* [Gerenciando o armazenamento móvel](/docs/vsi?topic=virtual-servers-accessing-portable-storage#accessing-portable-storage)
* [Editando uma descrição de armazenamento móvel](/docs/vsi?topic=virtual-servers-editing-a-portable-storage-description#editing-a-portable-storage-description)
