---
copyright:
  years: 2014, 2018
lastupdated: "2018-02-26"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Opções de armazenamento

Você tem a opção para SAN ou armazenamento local para cada servidor virtual. É possível complementar a SAN ou o armazenamento local com outros produtos de armazenamento conforme necessário. 

## Armazenamento local

O armazenamento local é construído em discos que são locais para o host do servidor virtual. O armazenamento local fornece melhor desempenho de leitura/gravação de disco. Os discos são construídos em uma configuração de Redundant Array of Independent Disks (RAID) para redundância, substituição de disco e monitoramento de funcionamento que é totalmente gerenciado pelo {{site.data.keyword.cloud}}. Em data centers mais recentes, esse armazenamento é toda unidade de estado sólido (SSD) para fornecer o melhor desempenho. 

## Armazenamento SAN
 
O armazenamento SAN é construído na infraestrutura SAN do {{site.data.keyword.cloud_notm}} em vez de no armazenamento de host local. Isso fornece maior resiliência no caso de uma falha de host e também pode suportar volumes muito maiores. No caso de uma falha de host, as instâncias de servidor virtual que usam o armazenamento baseado em SAN são migradas automaticamente para outros hosts e reiniciadas. 

Todos os discos secundários são conectados como armazenamento móvel. Na maioria dos casos, os discos podem ser removidos a qualquer momento para permitir que eles sejam movidos para outros servidores virtuais. 

**Exceção:** com servidores virtuais públicos que utilizam armazenamento local balanceado, não é possível remover discos primários ou secundários.

Os discos podem ser reconectados a outro servidor, contanto que a mudança não exceda a cota do disco ou o limite de tamanho máximo do volume do servidor virtual de destino.

**Nota:** o disco movido é convertido para o tipo de armazenamento do servidor de destino.

## Volumes de armazenamento móvel

Os volumes de armazenamento móvel são soluções de armazenamento auxiliar exclusivamente disponíveis nos {{site.data.keyword.BluVirtServers_short}}. Eles podem ser conectados a um servidor virtual de cada vez. Eles também serão uma solução ideal se você desejar transferir dados entre os servidores virtuais existentes em qualquer data center na rede do {{site.data.keyword.cloud_notm}}. Os volumes de armazenamento móvel são úteis para aplicativos de banco de dados que requerem acesso ao armazenamento em nível de bloco bruto e não formatado e para mover grandes conjuntos de dados entre os {{site.data.keyword.BluVirtServers_short}}.

Quando um volume de armazenamento móvel é anexado a um servidor virtual em um data center diferente do servidor virtual original, o sistema interno do {{site.data.keyword.cloud_notm}} copia o volume para a SAN no novo data center. O sistema verifica então a integridade do volume copiado e remove o volume móvel original da SAN do data center original.

## Limitações de LVM

O Logical volume management (LVM) não é suportado como um esquema de particionamento inicializável. Com o suporte e a configuração do sistema operacional adequados, os discos de servidor virtual secundário podem ser usados para partições LVM. No entanto, o LVM não é um sistema de arquivos suportado para Modelos de imagem ou Flex Images.

## Armazenamento suplementar

Os servidores virtuais são totalmente compatíveis com o armazenamento SAN de arquivo e bloco, bem como o armazenamento de objeto. Esses tipos de armazenamentos são recomendados para unidades de cluster, armazenamento de arquivo compartilhado, armazenamento de archive, requisitos de armazenamento grande ou requisitos de desempenho específicos.

Para obter mais informações sobre as opções de armazenamento adicional, consulte os recursos a seguir:

* [Introdução ao Block Storage](/docs/infrastructure/BlockStorage/index.html)
* [Introdução ao File Storage](/docs/infrastructure/FileStorage/index.html)
* [Introdução ao Object Storage](/docs/services/ObjectStorage/index.html)

## Próximas Etapas
Para obter mais informações sobre como usar os volumes de armazenamento móvel, veja as tarefas a seguir:
* [Acessando o armazenamento móvel](../storage/access-portable-storage-screen.html)
* [Editando a descrição do armazenamento móvel](../storage/edit-description-portable-storage-volume-psv.html)


