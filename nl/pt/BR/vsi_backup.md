---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Serviços de backup
{: #back-up-services}

## IBM Cloud Backup

O {{site.data.keyword.backup_full}} é um sistema automatizado de backup baseado em agente que é gerenciado por meio do utilitário de gerenciamento baseado em navegador WebCC do {{site.data.keyword.backup_notm}}, fornecendo aos usuários um método para fazer backup de dados entre servidores em um ou mais data centers na rede do {{site.data.keyword.BluSoftlayer}}.  Os administradores podem configurar backups para seguir um planejamento por hora, diário, semanal ou customizado que é destinado a sistemas integrais, diretórios específicos ou mesmo arquivos individuais.  Plug-ins adicionais permitem compatibilidade com software como o Microsoft Exchange e Microsoft SQL, bem como outros tipos de software de terceiros e permite que os usuários executem uma Restauração bare metal, quando necessário.

Para obter mais informações sobre os serviços do {{site.data.keyword.backup_notm}}, consulte [Introdução aos serviços do {{site.data.keyword.backup_notm}}](/docs/infrastructure/Backup?topic=Backup-gettingstarted#gettingstarted).

## CDP R1Soft

Proteção Contínua de Dados (CDP) é um software de backup de alto desempenho criado pelo R1Soft que permite o backup de dispositivos físicos e virtuais. O Idera CDP consiste em três componentes principais: o servidor CDP, o agente e os plug-ins de banco de dados, que estão disponíveis para compra separadamente nos dois primeiros componentes.  Como o CDP R1Soft é uma solução de backup de terceiros, as interações com o CDP ocorrem completamente fora das interfaces proprietárias do {{site.data.keyword.Bluemix_short}}; no entanto, as senhas do R1Soft CDP podem ser rastreadas e armazenadas no {{site.data.keyword.slportal}}.  Todas as outras interações com o CDP R1Soft estão documentadas no website R1Soft.

Para obter mais informações sobre os serviços de backup CDP do R1Soft, consulte [Documentação do R1Soft ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://wiki.r1soft.com/display/ServerBackupManager/Home){: new_window}.
