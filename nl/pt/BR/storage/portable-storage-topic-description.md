---
copyright: years: 1994, 2017 lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Sobre volumes de armazenamento móvel

Os volumes de armazenamento móvel são soluções de armazenamento auxiliar exclusivamente disponíveis nos {{site.data.keyword.BluVirtServers_short}}. Eles podem ser conectados a um servidor virtual de cada vez. Eles também serão uma solução ideal se você desejar transferir dados entre os servidores virtuais existentes em qualquer data center na rede do {{site.data.keyword.cloud}}. Os volumes de armazenamento móvel são úteis para aplicativos de banco de dados que requerem acesso ao armazenamento em nível de bloco bruto e não formatado e para mover grandes conjuntos de dados entre os {{site.data.keyword.BluVirtServers_short}}.

Quando um volume de armazenamento móvel é anexado a um servidor virtual em um data center diferente do servidor virtual original, o sistema interno do {{site.data.keyword.cloud}} copia o volume para a SAN no novo data center. O sistema verifica então a integridade do volume copiado e remove o volume móvel original da SAN do data center original.

## Próximas Etapas
Para obter mais informações sobre como usar os volumes de armazenamento móvel, veja as tarefas a seguir:
* [Acessando o armazenamento móvel](../storage/access-portable-storage-screen.html)
* [Editando a descrição do armazenamento móvel](../storage/edit-description-portable-storage-volume-psv.html)
