---



copyright: years: 2017 lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Gerenciando o acesso ao dispositivo
{: #managing-device-access}

Para acessar e gerenciar os detalhes para um dispositivo específico, deve-se ter as permissões certas concedidas à sua conta do usuário.  Após o administrador de conta conceder seu acesso à conta do usuário para um dispositivo, é possível visualizar os detalhes do dispositivo usando o {{site.data.keyword.slportal_full}} ou usando a API. As informações ou ação que você vê dependem do tipo de dispositivo, bem como as permissões que são concedidas para sua conta do usuário.
{:shortdesc}

**Nota:** se sua conta tiver dispositivos para os quais o acesso não foi concedido, você verá um nome "Dispositivo Desconhecido" quando tentar acessar esses dispositivos.

É possível designar acesso ao dispositivo para quaisquer usuários em sua conta, mas não para si mesmo. Somente o administrador de uma conta tem acesso a todos os dispositivos em sua conta do cliente e pode configurar o acesso para todos os outros usuários em sua conta. 

Deve-se ter as permissões a seguir para acessar os detalhes do dispositivo para servidores virtuais públicos ou servidores virtuais dedicados.

**Visualizar detalhes de servidores virtuais**

Permite visualizar os endereços IP, tipo de sistema operacional, senhas e muito mais para um servidor virtual fornecido.  Também permite atualizar senhas do servidor virtual no portal. Um usuário deve ter esse acesso para visualizar as instâncias públicas, instâncias dedicadas e instâncias de host dedicado.

**Visualizar detalhes do host dedicado virtual**

Permite visualizar os endereços IP, tipo de sistema operacional, senhas e muito mais para um determinado host dedicado.  Permite também migrar instâncias dedicadas para um host dedicado diferente. Um usuário deve ter esse acesso para visualizar hosts dedicados.

## Incluindo permissão para visualizar instâncias de servidor virtual
Use as etapas a seguir para incluir permissões *Visualizar detalhes do servidor virtual* para qualquer um de seus usuários filhos. Somente o administrador de uma conta pode conceder permissões para outros usuários em sua conta.  

1. Acesse o [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.
2. Selecione **Conta > Usuários** na barra de navegação para acessar a tela Usuários.
3. Clique no nome do usuário relevante para acessar o Perfil do usuário.
4. Clique no ícone **Permissões do portal** para acessar a tela Permissões do portal.
5. Na guia *Dispositivo*, selecione **Visualizar detalhes do servidor virtual** para incluir essa permissão no perfil do usuário.

Para fornecer acesso em um nível de dispositivo específico, continue com as etapas a seguir.

1. Clique no ícone **Acesso ao dispositivo** para acessar a tela Acesso ao dispositivo.
2. Clique na guia **Acesso rápido**. 
   Nota: outra opção é selecionar um dispositivo individual.
3. Na lista suspensa *Tipo de dispositivo*, selecione **Todos os servidores virtuais**.
4. Selecione a caixa de seleção **Conceder acesso automaticamente quando novos dispositivos forem incluídos** se o usuário associado deverá sempre ter acesso a esse tipo de dispositivo.
5. Verifique se os dispositivos corretos estão selecionados.
6. Clique em **Atualizar acesso ao dispositivo**.

## Incluindo permissão para visualizar hosts dedicados
Use as etapas a seguir para incluir permissões *Visualizar detalhes do host dedicado virtual* para qualquer um de seus usuários filhos. Somente o administrador de uma conta pode conceder permissões para outros usuários em sua conta.

1. Acesse o [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.
2. Selecione **Conta > Usuários** na barra de navegação para acessar a tela Usuários.
3. Clique no nome do usuário relevante para acessar o Perfil do usuário.
4. Clique no ícone **Permissões do portal** para acessar a tela Permissões do portal.
5. Na guia *Dispositivo*, selecione **Visualizar detalhes do host dedicado virtual** para incluir essa permissão no perfil do usuário.

Para fornecer acesso em um nível de dispositivo específico, continue com as etapas a seguir.

1. Clique no ícone **Acesso ao dispositivo** para acessar a tela Acesso ao dispositivo.
2. Clique na guia **Acesso rápido**. 
   Nota: outra opção é selecionar dispositivos individuais.
3. Na lista suspensa *Tipo de dispositivo*, selecione **Todos os hosts dedicados**.
4. Selecione a caixa de seleção **Conceder acesso automaticamente quando novos dispositivos forem incluídos** se o usuário associado deverá sempre ter acesso a esse tipo de dispositivo.
5. Verifique se os dispositivos corretos estão selecionados.
6. Clique em **Atualizar acesso ao dispositivo**.

**Nota:** também é possível usar o serviço da API SoftLayer_User_Customer::addBulkDedicatedHostAccess para fornecer um acesso de usuário para um ou mais hosts dedicados. Para obter mais informações, veja [Incluindo acesso ao host dedicado em massa ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://sldn.softlayer.com/reference/services/softlayer_user_customer/addbulkdedicatedhostaccess){: new_window}.  

## Próximas Etapas
As permissões de usuário são atualizadas imediatamente após as mudanças serem enviadas. Se permissões tiverem sido concedidas, o usuário poderá visualizar ou interagir com os recursos selecionados. Se as permissões tiverem sido removidas, o usuário não poderá mais visualizar ou interagir com os recursos selecionados. As permissões podem ser atualizadas novamente a qualquer momento.
