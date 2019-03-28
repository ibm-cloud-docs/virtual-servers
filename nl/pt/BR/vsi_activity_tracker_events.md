---

copyright:
  years: 2016, 2018
lastupdated: "2018-11-06"

subcollection: virtual-servers

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Eventos de rastreador de atividade
{: #at_events}

Como um responsável pela segurança, um auditor ou um gerente, é possível usar o serviço
{{site.data.keyword.cloudaccesstrailfull}} para controlar como os usuários e os aplicativos interagem com
as instâncias de servidor virtual (VSI) no {{site.data.keyword.Bluemix}}. O proprietário da conta e os usuários
que estão vinculados à conta podem acionar os eventos do servidor virtual que estão com login efetuado no {{site.data.keyword.cloudaccesstrailshort}}.
{:shortdesc}

O serviço do {{site.data.keyword.cloudaccesstrailshort}} registra as atividades iniciadas pelo usuário que
mudam o estado de um serviço no {{site.data.keyword.Bluemix_notm}}. Para obter mais informações, consulte [Sobre o {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov ).

Para começar a monitorar as ações do usuário, consulte [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started-with-cla#getting-started-with-cla).

Um inicializador pode ser um usuário, um serviço ou um aplicativo. Para que um usuário gere eventos, ele deve ter acesso aos recursos de **Infraestrutura** no console do {{site.data.keyword.Bluemix}}.
{: tip}

## Eventos de instância de servidor virtual
{: #vsi}

É possível auditar uma instância de servidor virtual (VSI) por meio de seu ciclo de vida, usando o serviço do {{site.data.keyword.cloudaccesstrailshort}}.

A tabela a seguir lista as ações que geram um evento:

| Ação | Descrição |
|----------|---------|
| `audit-log.vsi.provision`             | Um evento é gerado quando um inicializador fornece uma VSI.  |
| `audit-log.vsi-port.disable`          | Um evento é gerado quando um inicializador desativa uma porta em uma VSI. |
| `audit-log.vsi-port.enable`           | Um evento é gerado quando um inicializador ativa uma porta em uma VSI. |
| `audit-log.vsi-port-speed.update`     | Um evento é gerado quando um inicializador atualiza a velocidade da porta em uma VSI. |
| `audit-log.vsi-image-template.create` | Um evento é gerado quando um inicializador cria um modelo de imagem para uma VSI.  |
| `audit-log.vsi.power-off`             | Um evento é gerado quando um iniciador desliga uma VSI.  |
| `audit-log.vsi.soft-power-off`        | Um evento é gerado quando um inicializador faz desligamento suave em uma VSI. |
| `audit-log.vsi.force-power-off`       | Um evento é gerado quando um inicializador faz um desligamento forçado em uma VSI. |
| `audit-log.vsi.reboot`                | Um evento é gerado quando um inicializador reinicializa uma VSI. |
| `audit-log.vsi.soft-reboot`           | Um evento é gerado quando um inicializador faz uma reinicialização suave em uma VSI. |
| `audit-log.vsi.hard-reboot`           | Um evento é gerado quando um inicializador faz uma reinicialização forçada em uma VSI. |
| `audit-log.vsi.power-on`              | Um evento é gerado quando um inicializador liga uma VSI. |
| `audit-log.vsi.rename`                | Um evento é gerado quando um inicializador renomeia uma VSI. |
| `audit-log.vsi.rescue`                | Um evento é gerado quando um inicializador resgata uma VSI. |
| `audit-log.vsi-security-group.add`    | Um evento é gerado quando um inicializador inclui um grupo de segurança em uma VSI. |
| `audit-log.vsi-security-group.remove` | Um evento é gerado quando um inicializador remove um grupo de segurança de uma VSI. |
| `audit-log.vsi.reload`                | Um evento é gerado quando um inicializador executa um recarregamento do sistema operacional (S.O.) para uma VSI. |
| `audit-log.vsi.boot`                  | Um evento é gerado quando um inicializador inicializa uma VSI de uma imagem. |
| `audit-log.vsi.reclaim`               | Um evento é gerado quando um inicializador cancela uma VSI. |
| `audit-log.vsi.pause`                 | Um evento é gerado quando um inicializador pausa uma VSI. |
{: caption="Tabela 2. Ações da VSI" caption-side="top"}



## Visualizando eventos
{: #ui}

Os eventos do {{site.data.keyword.cloudaccesstrailshort}} estão disponíveis no **domínio
da conta** do {{site.data.keyword.cloudaccesstrailshort}} que
está disponível na região do {{site.data.keyword.Bluemix_notm}} em que os eventos são gerados. Para obter mais informações, consulte [Visualizando eventos
de conta](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events).

Os eventos do {{site.data.keyword.cloudaccesstrailshort}} são encaminhados automaticamente para o serviço
do {{site.data.keyword.cloudaccesstrailshort}} na mesma região em que a ação acontece.
