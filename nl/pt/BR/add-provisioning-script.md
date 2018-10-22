---
copyright:
  years: 2014, 2018
lastupdated: "2018-04-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gerenciando um script de provisionamento

Use os scripts de provisionamento para especificar uma URL para um script a ser executado em um dispositivo recentemente provisionado. Você não tem restrições para o nome do script; no entanto, usar uma convenção de nomenclatura semelhante para cada script torna mais fácil a identificação. Os scripts de provisionamento devem ser associados a um nome completo do domínio e devem ser acessíveis usando os protocolos HTTP ou HTTPS. O tipo de protocolo que é usado afeta a resposta automatizada do sistema quando o script de provisionamento é transferido por download para o dispositivo.

* O uso do **Protocolo HTTP** requer que um administrador execute o script manualmente após ser transferido por download.
* O uso do **Protocolo HTTPS** faz download e executa o script automaticamente, quando possível. Se a URL não estiver associada a um script executável, o script será transferido por download e nenhuma ação adicional deverá ser executada.

## Acessando a tela de scripts de provisões
1. Entre no [{{site.data.keyword.slportal_full}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} com suas credenciais exclusivas.
2. Selecione **Dispositivos > Gerenciar > Scripts de provisionamento** na navegação para acessar a tela de scripts de provisionamento.


## Incluindo um script de fornecimento

1. Na tela **Scripts de provisionamento** no {{site.data.keyword.slportal}}, clique em **Incluir script de provisionamento** na parte superior da tela.
* Insira um **nome de identificação** para o script de provisionamento no campo **Nome**.
* Insira o **nome completo do domínio** que está associado ao script no campo **URL**.
* Clique em **Incluir** para incluir o script de provisionamento na conta. Clique em **Cancelar** para cancelar a ação.

## Editando detalhes do script de provisionamento

1. Na tela **Scripts de provisionamento** no {{site.data.keyword.slportal}}, clique em qualquer lugar na coluna **Nome** ou **URL** do script de provisionamento para abrir o script para edições.
3. Atualize o nome ou a URL.
  * **Observação:** quando você atualiza uma URL, deve-se usar um nome completo do domínio ou a mudança não será salva.
4. Clique em qualquer lugar na tela para salvar a edição.

## Próximas Etapas

Os scripts de provisionamento que estão associados a uma conta podem ser modificados ou removidos a qualquer momento. Os scripts de provisionamento são salvos no {{site.data.keyword.slportal}} até que sejam removidos e podem ser associados a qualquer novo dispositivo solicitado por meio do {{site.data.keyword.slportal}}. Se o script estiver associado a uma URL HTTP, ele será transferido por download para o novo dispositivo durante o provisionamento. Os scripts que estão associados a URLs HTTPS são transferidos por download e, quando aplicável, executados no novo dispositivo.

Depois de editar um script, as atualizações válidas são exibidas na tela imediatamente. Mudanças feitas nos scripts de provisionamento existentes não afetam os dispositivos já provisionados.
