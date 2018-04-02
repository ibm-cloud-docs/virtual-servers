---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Gerenciando servidores virtuais
{: #managing-virtual-servers}

Na Lista de dispositivos, é possível gerenciar servidores virtuais e outros dispositivos, como servidores bare metal e firewalls VLAN.
{:shortdesc}

Na lista de dispositivos, os servidores virtuais têm um tipo de dispositivo *Virtual*. Os servidores bare metal são indicados com o tipo de dispositivo *Servidor*. Os hosts dedicados têm um tipo de dispositivo *Host virtual dedicado*. Muitas interações disponíveis para os dispositivos são semelhantes, mas cada tipo de dispositivo também tem interações específicas do dispositivo.

As tarefas de gerenciamento de servidor virtual a seguir estão disponíveis para você na lista de dispositivos:
* Reinicializar - desligar imediatamente um dispositivo e, depois, ligá-lo novamente.
* Ligar/Desligar - ligar ou desligar remotamente um dispositivo.
* Renomear - mudar ou atualizar um nome de dispositivo.
* Cancelar - terminar o uso de um dispositivo. Os dispositivos podem ser cancelados imediatamente ou em um aniversário de faturamento. Depois de confirmar o cancelamento de seu dispositivo, a ação não pode ser desfeita. Reembolsos não podem ser fornecidos para cancelamentos imediatos.

Conclua as etapas a seguir para executar tarefas de gerenciamento para seus servidores virtuais na Lista de dispositivos no Portal do Cliente:  
1. Efetue login no [{{site.data.keyword.slportal_full}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas. 
2. No menu **Dispositivos**, selecione **Lista de dispositivos**.
3. Clique em **Ações** para o dispositivo que você deseja gerenciar e selecione a tarefa de gerenciamento desejada.

**Dicas:** 
* É possível interagir com servidores no {{site.data.keyword.slportal}} na visualização Captura Instantânea (um resumo de seu dispositivo) e na tela Detalhes do Dispositivo (uma lista totalmente detalhada). Para visualizar e interagir com seu servidor na Visualização de captura instantânea, clique na seta ao lado do Nome do dispositivo para expandir a visualização. Para visualizar e interagir com seu servidor na tela Detalhes do dispositivo, clique no Nome do dispositivo do servidor.
* É possível incluir notas em um dispositivo a qualquer momento na guia **Configuração**. As notas podem ajudar a identificar detalhes sobre o dispositivo, seu uso e ações que foram tomadas no dispositivo.

## O que acontece em seguida
* **Reinicalização**

    Uma reinicialização é uma das ações de dispositivo mais básicas. A reinicialização de um dispositivo resulta na desativação e ativação imediatas de seu dispositivo e é feita por muitas razões, muitas vezes específicas para as necessidades do dispositivo ou de negócios do usuário individual. As reinicializações de dispositivo podem ocorrer da Lista de dispositivos e da Visualização do dispositivo de um dispositivo individual. Os Servidores virtuais podem ser reinicializados a qualquer momento.  

* **Ligar/Desligar**

    Se o dispositivo foi desligado, o dispositivo permanece no estado desligado e deve ser ligado manualmente repetindo as etapas acima. Os usuários não podem interagir com um dispositivo quando um dispositivo é desligado. Se o dispositivo foi ligado, pode ocorrer uma interação normal. Ele permanecerá ligado até que uma ação adicional seja tomada.

* **Renomear**

  Depois de renomear o dispositivo, o nome será atualizado automaticamente no {{site.data.keyword.slportal}}. Ao executar uma procura no {{site.data.keyword.slportal}}, use o novo nome do dispositivo ao tentar localizar o conteúdo associado a ele. Repita as etapas anteriores para renomear o dispositivo novamente a qualquer momento.

* **Cancelar**

  Depois de confirmar o cancelamento, o processo de cancelamento do dispositivo começará. Se um cancelamento imediato foi solicitado, o dispositivo será cancelado imediatamente. Se um cancelamento de aniversário de faturamento foi solicitado, o dispositivo continuará ativo até o próximo aniversário de faturamento. Após seu cancelamento, o dispositivo não aparecerá mais na Lista de Dispositivos no {{site.data.keyword.slportal}}. Os itens de faturamento também serão removidos das faturas quando todos os saldos pendentes forem pagos no dispositivo, se houver. Para perguntas sobre uma fatura para um dispositivo cancelado, abra um chamado e selecione Solicitação de Contabilidade como o assunto do chamado. Reembolsos não podem ser fornecidos para cancelamentos imediatos.
  
## Próximas Etapas
Se você precisar reconfigurar um servidor virtual existente, veja [Reconfigurando um servidor virtual existente](../vsi/vsi_reconfigure.html).

