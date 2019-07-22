---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Gerenciando servidores virtuais
{: #managing-virtual-servers}

É possível gerenciar servidores virtuais, juntamente com outros dispositivos, por meio da lista de detalhes do dispositivo.
{:shortdesc}


## Antes de iniciar
Primeiro, navegue para o menu de dispositivos e assegure-se de ter as permissões de conta corretas para concluir as tarefas.

* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assegure-se de ter quaisquer permissões de conta necessárias e de ter acesso ao dispositivo. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões.

Para obter mais informações sobre permissões, veja [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Tipos de dispositivos
A lista de detalhes do dispositivo mostra os tipos de dispositivo a seguir:

| Dispositivo  | Tipo de dispositivo  |
| ------  | ------------ | 
| Servidores Virtuais | Virtual |
| Servidores bare metal | Servidor |
| Hosts dedicados | Host virtual dedicado | 
{: caption="Tabela 1. Tipos de dispositivo" caption-side="top"}

As ações que você vê dependem do tipo de dispositivo, bem como das permissões que são concedidas à sua conta do usuário.

Conclua as etapas a seguir para executar as tarefas de gerenciamento para os servidores virtuais.

1. No menu **Dispositivos**, selecione **Lista de dispositivos**.
2. Clique em **Ações** para o dispositivo que você deseja gerenciar e selecione a tarefa relevante.

* É possível interagir com servidores no console do {{site.data.keyword.cloud_notm}} na visualização de captura instantânea (um resumo de seu dispositivo) e na página de detalhes do dispositivo (uma lista totalmente detalhada). Para visualizar e interagir com seu servidor na visualização de captura instantânea, clique na seta ao lado de Nome do dispositivo para expandir a visualização. Para visualizar e interagir com seu servidor na página de detalhes do dispositivo, clique no Nome do dispositivo do servidor.

* É possível incluir notas em um dispositivo a qualquer momento na guia **Configuração**. As notas podem ajudar a identificar detalhes sobre o dispositivo, seu uso e ações que foram tomadas no dispositivo.
 {:tip}

## Reinicializar
Uma reinicialização é uma das ações de dispositivo mais básicas. A reinicialização de um dispositivo resulta na desativação e ativação imediatas de seu dispositivo e é feita por muitas razões, muitas vezes específicas para as necessidades do dispositivo ou de negócios do usuário individual. As reinicializações de dispositivo podem ocorrer da Lista de dispositivos e da Visualização do dispositivo de um dispositivo individual. Os Virtual Servers podem ser reinicializados a qualquer momento.

Uma reinicialização é muito útil ao enfrentar um problema no qual o servidor não pode ser inicializado para o sistema operacional devido a um problema de configuração.  Também é possível inicializar no kernel de resgate. Após a inicialização no Rescue Kernel, é possível montar a unidade/unidades de seu servidor e, em seguida, corrigir o problema de configuração. Depois que o problema foi corrigido, apenas reinicialize o servidor por meio da linha de comandos e o servidor será reinicializado no kernel padrão para seu servidor.
{:tip}

## Ligar/Desligar
Se o dispositivo foi desligado, o dispositivo permanece no estado desligado e deve ser ligado manualmente repetindo as etapas acima. Os usuários não podem interagir com um dispositivo que está desligado. Se o servidor virtual suportar o recurso de suspensão de faturamento, o faturamento será suspenso para alguns recursos de cálculo. Não será possível concluir todas as ações de gerenciamento em uma instância até que o faturamento seja retomado. Para obter mais informações, consulte [Suspensão de faturamento](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing). Para descobrir se a instância de servidor virtual suporta o recurso de suspensão de faturamento, consulte [Visualizando o recurso de suspensão de faturamento](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature#viewing-suspend-billing-feature). Se o dispositivo tiver sido ligado, a interação normal poderá ocorrer. Ele permanecerá ligado até que uma ação adicional seja tomada.

## Renomear
Depois de renomear o dispositivo, o nome é atualizado automaticamente no console do {{site.data.keyword.cloud_notm}}. Ao executar uma procura dentro do console do {{site.data.keyword.cloud_notm}}, use o novo nome do dispositivo ao tentar localizar o conteúdo associado a ele. Repita as etapas anteriores para renomear o dispositivo novamente a qualquer momento.

## Cancelar
Se você cancelar um dispositivo, encerrará o uso desse dispositivo. Os dispositivos podem ser cancelados imediatamente ou em um aniversário de faturamento. Depois de confirmar o cancelamento de seu dispositivo, a ação não pode ser desfeita. Reembolsos não podem ser fornecidos para cancelamentos imediatos.

Depois de confirmar o cancelamento, o processo de cancelamento do dispositivo começará. Se um cancelamento imediato foi solicitado, o dispositivo será cancelado imediatamente. Se um cancelamento de aniversário de faturamento foi solicitado, o dispositivo continuará ativo até o próximo aniversário de faturamento. Após seu cancelamento, o dispositivo não aparecerá mais na Lista de dispositivos no console do {{site.data.keyword.cloud_notm}}. Os itens de faturamento também serão removidos das faturas quando todos os saldos pendentes forem pagos no dispositivo, se houver. Para perguntas sobre uma fatura para um dispositivo cancelado, abra um chamado e selecione Solicitação de Contabilidade como o assunto do chamado. Reembolsos não podem ser fornecidos para cancelamentos imediatos.

## Próximas Etapas
Se você precisar reconfigurar um servidor virtual existente, veja [Reconfigurando um servidor virtual existente](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).
