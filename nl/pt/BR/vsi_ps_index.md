---
copyright:
  years: 2014, 2018
lastupdated: "2018-02-20"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Scripts de provisionamento

Um script de provisionamento é um script que pode ser transferido por download ou transferido por download e executado em um dispositivo durante o processo de provisionamento. Para contas existentes, os scripts de provisionamento são gerenciados no {{site.data.keyword.slportal_full}}. Durante o processo de pedido, é possível inserir manualmente scripts para novas contas ou scripts que ainda não foram rastreados.

Durante o processo de provisionamento, os scripts que estão associados a uma URL HTTP são transferidos por download para o dispositivo. Após o provisionamento, um administrador deve executar o script manualmente no dispositivo. Os scripts associados a uma URL HTTPS são transferidos por download e executados automaticamente. Os scripts de provisionamento estão disponíveis atualmente nos sistemas operacionais padrão Linux (Cent, RHEL, Fedora, Debian ou Ubuntu), Windows e FreeBSD. Outros sistemas, como Vyatta, Netscaler, XenServer e VMware, não são suportados. O script de provisionamento pode ser qualquer tipo de arquivo executado pelo sistema operacional, incluindo arquivos binários combinados ou qualquer outro idioma suportado pelo S.O.

Para obter mais informações, consulte [Gerenciando um script de provisionamento](add-provisioning-script.html).
