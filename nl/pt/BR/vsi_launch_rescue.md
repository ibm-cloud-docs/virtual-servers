---



copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Ativando um kernel de resgate 
{: #launching-rescue}

Rescue Kernel é um ambiente de resgate em tempo real, projetado para fornecer aos clientes a capacidade de colocar um servidor bare metal ou servidor virtual on-line para solucionar problemas do sistema que normalmente seriam resolvidos somente por meio do Recarregamento de OS. O Rescue Kernel deve ser iniciado no {{site.data.keyword.slportal_full}}. Use as etapas a seguir para ativar o Rescue Kernel para um dispositivo.
{:shortdesc}

## Ativar Rescue Kernel

1. Acesse o [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) usando suas credenciais exclusivas.
2. Na Lista de dispositivos, clique no nome do dispositivo que você deseja resgatar.
3. Clique na lista suspensa *Ações* no canto superior direito e selecione **Resgatar**. (Como alternativa, é possível clicar na guia *Gerenciamento remoto* e selecionar **Resgatar**).
4. Clique no botão **Sim** para executar a transição de seu dispositivo para o Rescue Kernel imediatamente. Clique no botão **Não** para cancelar a ação.

## No Windows VSI

1. Acesse o [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) usando suas credenciais exclusivas.
2. Na Lista de dispositivos, clique no nome do dispositivo que você deseja resgatar.
3. Clique na lista suspensa *Ações* no canto superior direito e selecione **Inicialização por meio da imagem**.
4. Selecione **Inicialização por meio dessa imagem** ao lado da imagem pública, *WindowsRescueStandalone.iso*.


## Próximas Etapas
Após ativar o Rescue Kernel, o dispositivo é desligado e reinicializado no kernel de resgate para o sistema operacional do dispositivo. Isso pode levar vários minutos.

O acesso remoto ao dispositivo está disponível por meio do endereço IP do dispositivo. É possível acessar o dispositivo no Rescue Kernel usando as credenciais raiz ou do administrador para os dispositivos que são registrados no {{site.data.keyword.slportal}}. Ao usar o Rescue Kernel, é possível solucionar problemas, descobrir problemas e resolver problemas como você faria em um dispositivo regularmente inicializado. Se necessário, é possível montar unidades no OS do Rescue Kernel. Para sair do Rescue Kernel e retornar o dispositivo para seu ambiente regular, reinicialize o dispositivo no {{site.data.keyword.slportal}} ou reinicialize no SO do Rescue Kernel.

Para obter mais informações sobre como reinicializar um dispositivo, consulte [Gerenciando Servidores Virtuais](../vsi/vsi_managing.html).

