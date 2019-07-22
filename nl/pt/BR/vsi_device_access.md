---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Gerenciando o acesso ao dispositivo
{: #managing-device-access}

Para acessar e gerenciar os detalhes de um dispositivo específico, deve-se ter as permissões corretas concedidas para a sua conta do usuário.  Depois que o administrador de conta concede à sua conta do usuário acesso a um dispositivo, é possível visualizar os detalhes do dispositivo usando o console do {{site.data.keyword.cloud}} ou usando o {{site.data.keyword.slapi_short}}. As informações ou ações que você vê dependem do tipo de dispositivo, bem como das permissões que são concedidas à sua conta do usuário.
{:shortdesc}

Se a sua conta tiver dispositivos para os quais você não tenha recebido acesso, você verá um nome "Dispositivo desconhecido" ao tentar acessar esses dispositivos.
{:note}

É possível designar acesso ao dispositivo para quaisquer usuários em sua conta, mas não para si mesmo. Somente o administrador de uma conta tem acesso a todos os dispositivos em sua conta do cliente e pode configurar o acesso para todos os outros usuários em sua conta. 

Deve-se ter as permissões a seguir para acessar os detalhes do dispositivo para servidores virtuais públicos ou servidores virtuais dedicados.

* **Visualizar detalhes dos servidores virtuais** - Permite visualizar os endereços IP, o tipo de sistema operacional, as senhas e mais para um determinado servidor virtual.  Também permite atualizar senhas do servidor virtual no portal. Deve-se ter esse acesso para visualizar instâncias públicas, instâncias dedicadas e instâncias de host dedicadas.

* **Visualizar detalhes do host dedicado virtual** - Permite visualizar os endereços IP, o tipo de sistema operacional, as senhas e mais para um determinado host dedicado.  Permite também migrar instâncias dedicadas para um host dedicado diferente. Deve-se ter esse acesso para visualizar os hosts dedicados.


## Incluindo permissões para seus usuários
Se você for o administrador de conta e desejar conceder aos usuários permissão para visualizar os detalhes do servidor virtual e do host dedicado, conclua as etapas a seguir.

1. Efetue login na página [Acesso (IAM) ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/iam#/users){: new_window} no console do {{site.data.keyword.cloud}}. 
2. Na guia **Usuários**, selecione **Visualizar por: meus usuários de infraestrutura clássica**.
3. Selecione um usuário e, em seguida, clique na guia **Infraestrutura clássica**.
4. Expanda a categoria **Dispositivos** na guia **Permissões** e selecione **Visualizar detalhes do servidor virtual** e **Visualizar detalhes do host dedicado virtual**.
5. Clique em **Aplicar**.

### Incluindo permissões de nível de dispositivo específicas
Se você desejar fornecer aos usuários acesso a um nível de dispositivo específico, conclua as etapas a seguir.

1. Na guia **Usuários**, selecione **Visualizar por: meus usuários de infraestrutura clássica**. 
2. Selecione um usuário e, em seguida, clique na guia **Infraestrutura clássica**.
3. Na seção **Selecionar tipo**, na guia **Dispositivos**, selecione a permissão apropriada: **Todos os servidores bare metal**, **Todos os hosts dedicados** ou **Todos os servidores virtuais**. 
4. Na seção **Ativar acesso futuro** na guia **Dispositivos**, selecione a permissão apropriada: **Acesso automático do servidor bare metal**, **Acesso automático ao host dedicado** ou **Acesso automático ao servidor virtual**. Essa permissão permite que seus usuários sempre tenham acesso ao tipo de dispositivo quando novos dispositivos forem incluídos.
5. Clique em **Configurar** para aplicar as novas permissões.

## Incluindo permissões para os usuários no Portal do Cliente
Se você for o administrador de conta e desejar conceder aos usuários permissão para visualizar os detalhes do servidor virtual e do host dedicado, conclua as etapas a seguir.

1. Acesse o [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.
2. Selecione **Conta > Usuários** na barra de navegação para acessar a tela Usuários.
3. Clique no nome do usuário relevante para acessar o Perfil do usuário.
4. Clique no ícone **Permissões do portal** para acessar a tela Permissões do portal.
5. Na guia **Dispositivo**, selecione **Visualizar detalhes do servidor virtual** e **Visualizar detalhes do host dedicado virtual** para incluir essas permissões no perfil do usuário.

### Incluindo permissões de nível de dispositivo específicas no Portal do Cliente
Para fornecer acesso em um nível de dispositivo específico, continue com as etapas a seguir.

1. Clique no ícone **Acesso ao dispositivo** para acessar a tela Acesso ao dispositivo.
2. Clique na guia **Acesso rápido**. 
3. Na lista suspensa **Tipo de dispositivo**, selecione **Todos os servidores virtuais** e **Todos os hosts dedicados**.
4. Selecione a caixa de seleção **Conceder acesso automaticamente quando novos dispositivos forem incluídos** se o usuário associado deverá sempre ter acesso a esse tipo de dispositivo.
5. Verifique se os dispositivos corretos estão selecionados.
6. Clique em **Atualizar acesso ao dispositivo**.

Também é possível usar o serviço de API SoftLayer_User_Customer::addBulkDedicatedHostAccess para fornecer a um usuário acesso a um ou mais hosts dedicados. Para obter mais informações, consulte [Incluindo Bulk Dedicated Host Access ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/reference/services/SoftLayer_User_Customer/addBulkDedicatedHostAccess/){: new_window}.  
{:note}

## Próximas Etapas
As permissões de usuário são atualizadas imediatamente após as mudanças serem enviadas. Se permissões tiverem sido concedidas, o usuário poderá visualizar ou interagir com os recursos selecionados. Se as permissões tiverem sido removidas, o usuário não poderá mais visualizar ou interagir com os recursos selecionados. As permissões podem ser atualizadas novamente a qualquer momento.

