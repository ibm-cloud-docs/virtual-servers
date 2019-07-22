---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-14"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurando permissões de usuário para escala automática
{: #user-permissions-required-to-use-auto-scale}

O acesso às opções de escala automática requer uma permissão de usuário especial, além da capacidade de solicitar e gerenciar {{site.data.keyword.virtualmachinesshort}}. Para acessar os recursos de escala automática, deve-se ter permissão para gerenciar todos os servidores virtuais na conta, além de qualquer dispositivo virtual futuro incluído.

Se você for o administrador de conta e desejar conceder aos usuários permissão para acessar as opções de escala automática, conclua as etapas a seguir:

1. Efetue login na página [Acesso (IAM) ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/iam#/users){: new_window} no console do {{site.data.keyword.cloud}}. 
2. Na guia **Usuários**, selecione **Visualizar por: meus usuários de infraestrutura clássica**.
3. Selecione um usuário e, em seguida, clique na guia **Infraestrutura clássica**.
4. Expanda a categoria **Dispositivos** na guia **Permissões** e selecione **Gerenciar grupos de escala automática**.
5. Clique em **Aplicar**.

## Próximas Etapas

Depois de ter permissão para acessar e usar as opções de escala automática, você está pronto para usar o recurso. Para iniciar, revise as informações a seguir:

1. [Gerenciando aumentos de tráfego com o ajuste automático de escala baseado em planejamento](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling)
2. [Gerenciando aumentos de tráfego com o ajuste automático de escala baseado em recurso](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling)
3. [FAQs: escala automática](/docs/vsi?topic=virtual-servers-faqs-auto-scale)

