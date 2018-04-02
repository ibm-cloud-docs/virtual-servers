---



copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Incluindo um script de fornecimento customizado 
{: #adding-post-script}

Os scripts de fornecimento customizado permitem que os usuários especifiquem uma URL para um script que é executado em um dispositivo recentemente provisionado. É possível postar e gerenciar scripts de fornecimento customizado no {{site.data.keyword.slportal_full}}.
{:shortdesc}

Ao pedir um dispositivo, será possível selecionar um script de fornecimento customizado se ele tiver sido postado na tela Scripts de Fornecimento do {{site.data.keyword.slportal}}. Se um script não tiver sido incluído, será possível fornecer uma URL. Os scripts de fornecimento podem ser qualquer arquivo que o sistema operacional (OS) possa executar, incluindo arquivos binários combinados ou qualquer idioma suportado pelo OS. Use as etapas a seguir para incluir um script de fornecimento customizado no {{site.data.keyword.slportal}}.

**Nota:** esse recurso está disponível atualmente somente para sistemas operacionais baseados no Linux e Unix.

## Incluindo um script de fornecimento

1. No menu **Dispositivos** no [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window}, selecione **Gerenciar** > **Scripts de Fornecimento**.
2. Clique em **Incluir script de fornecimento**.
4. No campo Nome, insira um nome de script exclusivo.
5. No campo URL, insira a URL exata a ser associada ao script.
6. Clique em ** Adicionar**.

## Próximas Etapas
Após uma ordem que contém um script de fornecimento ser enviada, o dispositivo é provisionado de forma semelhante a qualquer outro dispositivo. Antes que o dispositivo fique disponível, o script especificado é transferido por download para o dispositivo. A origem do script de fornecimento determina o comportamento durante esta última etapa do processo de fornecimento. Se o script for fornecido por meio de uma URL HTTPS, o script será transferido por download e executado sem interação adicional necessária do usuário. Se o script for fornecido por HTTP, o script será somente transferido por download. Para scripts fornecidos por HTTP, o administrador deve efetuar login no dispositivo e executar o script manualmente.
