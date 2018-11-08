---
copyright:
  years: 2014, 2018
lastupdated: "2018-10-18"
---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# Scripts de provisionamento

Um script de provisionamento é um script que pode ser transferido por download ou transferido por download e executado em um dispositivo durante o processo de provisionamento. Para contas existentes, os scripts de provisionamento são gerenciados no {{site.data.keyword.slportal_full}}. Durante o processo de pedido, é possível inserir manualmente scripts para novas contas ou scripts que ainda não foram rastreados.

Como alternativa, é possível usar uma imagem ativada para cloud-init e fornecer os dados do usuário para
executar automaticamente as tarefas de configuração ou executar os scripts. Para obter informações adicionais, consulte
[Fornecimento
com uma imagem ativada para cloud-init](/docs/infrastructure/image-templates/image_cloud-init.html#provisioning-with-a-cloud-init-enabled-image).
{: tip}

Durante o processo de fornecimento, os scripts de fornecimento associados a uma URL de HTTP são
transferidos por download para o dispositivo. Após o provisionamento, um administrador deve executar o script manualmente no dispositivo. Os scripts associados a uma URL HTTPS são transferidos por download e executados automaticamente. Os scripts de provisionamento estão disponíveis atualmente nos sistemas operacionais padrão Linux (Cent, RHEL, Fedora, Debian ou Ubuntu), Windows e FreeBSD. Outros sistemas, como Vyatta, Netscaler, XenServer e VMware, não são suportados. O script de provisionamento pode ser qualquer tipo de arquivo executado pelo sistema operacional, incluindo arquivos binários combinados ou qualquer outro idioma suportado pelo S.O.

Para obter mais informações, consulte [Gerenciando um script de provisionamento](add-provisioning-script.html).
