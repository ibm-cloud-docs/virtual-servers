---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gerenciando scripts de provisionamento
{: #managing-a-provisioning-script}

É possível usar os scripts de provisionamento para especificar uma URL para um script que é executado em um dispositivo recém-provisionado. Os scripts de provisionamento podem ser qualquer arquivo que o sistema operacional (S.O.) possa executar, incluindo arquivos binários combinados ou qualquer idioma suportado pelo S.O. Você não tem restrições para o nome do script; no entanto, usar uma convenção de nomenclatura semelhante para cada script torna mais fácil a identificação. Os scripts de provisionamento devem ser associados a um nome completo do domínio e devem ser acessíveis usando os protocolos HTTP ou HTTPS. O tipo de protocolo que é usado afeta a resposta automatizada do sistema quando o script de provisionamento é transferido por download para o dispositivo.  
{:shortdesc}

* O uso do **Protocolo HTTP** requer que um administrador execute o script manualmente após ser transferido por download.
* O uso do **Protocolo HTTPS** faz download e executa o script automaticamente, quando possível. Se a URL não estiver associada a um script válido, o script será transferido por download e nenhuma ação adicional deverá ser executada.

## Antes de iniciar
Primeiro, navegue para o menu de dispositivos e assegure-se de ter as permissões de conta corretas para concluir as tarefas. 

* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assegure-se de ter quaisquer permissões de conta necessárias e de ter acesso ao dispositivo. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões. 

Para obter mais informações sobre permissões, veja [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Incluindo um script de fornecimento
{: #add-provisioning-script}

1. No menu **Dispositivos**, selecione **Gerenciar > Scripts de provisionamento**.
2. Selecione **Incluir script de provisionamento**. 
3. Insira um nome de identificação para o script de provisionamento no campo **Nome**.
4. Insira o nome completo do domínio associado ao script no campo **URL**.
5. Clique em **Incluir** para incluir o script de provisionamento na conta. 

## Editando detalhes do script de provisionamento
{: #edit-provisioning-script-details}

1. No menu **Dispositivos**, selecione **Gerenciar > Scripts de provisionamento**.
2. Clique em qualquer lugar na coluna **Nome** ou **URL** do script de provisionamento para abrir o script para edições.
3. Atualize o nome ou a URL.
   Ao atualizar uma URL, deve-se usar um nome completo do domínio ou a mudança não será salva.
   {:note}
4. Clique em qualquer lugar na tela para salvar a edição.

## Próximas Etapas

Os scripts de provisionamento que estão associados a uma conta podem ser modificados ou removidos a qualquer momento. Os scripts de provisionamento são salvos no console do {{site.data.keyword.cloud_notm}} até que sejam removidos e possam ser associados a qualquer novo dispositivo pedido por meio do console do {{site.data.keyword.cloud_notm}}. Se o script estiver associado a uma URL de HTTP, ele será transferido por download para o novo dispositivo durante o provisionamento e o administrador deverá efetuar login no dispositivo e executar o script manualmente. Os scripts associados a URLs de HTTPS são transferidos por download e, quando aplicável, são executados no novo dispositivo sem interação adicional necessária. 

Se você editar um script, as atualizações válidas serão exibidas na tela imediatamente. Mudanças feitas nos scripts de provisionamento existentes não afetam os dispositivos já provisionados.

