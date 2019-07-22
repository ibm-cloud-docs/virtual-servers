---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gerenciando aumentos de tráfego com o ajuste automático de escala baseado em planejamento
{: #managing-schedule-based-auto-scaling}

Aumentos de tráfego da web podem ser uma coisa boa e ruim. Os aumentos são bons no sentido de que mais pessoas estão usando seu site; eles podem ser ruins devido a como um pico na atividade pode afetar os seus tempos de resposta. A escala automática do {{site.data.keyword.cloud}} fornece a capacidade de aumentar ou diminuir a escala de seus servidores automaticamente para suportar suas necessidades de negócios. É possível usar o ajuste automático de escala baseada em planejamento para controlar esses aumentos de tráfego.
{:shortdesc}

## Antes de iniciar
Primeiro, navegue para o menu de dispositivos e assegure-se de ter as permissões de conta corretas para concluir as tarefas.

* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assegure-se de ter quaisquer permissões de conta necessárias e de ter acesso ao dispositivo. Se você não for o administrador da conta, a sua conta do usuário deverá incluir permissão para usar a escala automática. Para obter mais informações sobre como atualizar as permissões para usar a escala automática, consulte [Configurando permissões de usuário para a escala automática](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões. 

Para obter mais informações sobre permissões, veja [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Incluindo um grupo de escala automática
{: #add-auto-scale-group}

Nesse cenário, um website social baseado em Dallas, Texas experimenta aumentos de atividade durante os fins de semana. Dois servidores virtuais são o mínimo necessário pelo site de segunda a sexta-feira; no entanto, mais dois servidores virtuais são necessários a cada fim de semana para contabilizar o tráfego aumentado. As etapas a seguir conduzem você pela configuração da escala automática para suportar o ajuste de escala baseado em planejamento.

1. No menu **Dispositivos**, selecione **Escala automática**.
2. Selecione **Incluir grupo de escala automática**.
3. Configure um grupo de escala automática primeiro inserindo um **Nome do grupo**, por exemplo, Grupo de escala de fim de semana e, em seguida, selecione o data center.
4. Selecione a política de finalização do servidor. Por exemplo, se você escolher **Mais antigo**, o servidor com a data mais antiga provisionada será selecionado ao reduzir a escala.
5. Indique se o seu grupo deve ser um grupo de escalas de múltiplas VLANs e como equilibrar a escala nos pares de VLAN configurados.
6. Selecione as VLANs públicas e privadas nas quais você deseja seus servidores provisionados. Se os servidores forem acessados por meio da Internet pública (se a VLAN estiver executando servidores da web), deixe **Rede privada somente** desmarcado.
7. Configure o **Mínimo de contagens de membros** como 2 e o **Máximo de contagens de membros** como 4. Configure o **Tempo de espera** como 0. Como isso é um ajuste de escala baseado em planejamento, não há estatísticas reunidas para acionar ações de ajuste de escala.

## Definindo a configuração do membro para seu grupo
{: #define-member-configuration}

1. Localize **Configuração do membro** e insira um **Nome do host** e um **Domínio** para o servidor de ajuste de escala. Os servidores subsequentes incluídos no grupo possuem sufixos exclusivos que são anexados ao nome do host.
2. Especifique a configuração de hardware das instâncias de computação (núcleos, RAM e assim por diante.)
3. Selecione um sistema operacional se você desejar instalar o sistema operacional mínimo. Também é possível usar uma imagem pública ou imagem privada para provisionar suas instâncias.
4. Se as instâncias exigirem etapas extras para instalar software adicional, especifique a URL de um script de pós-instalação para instalar o software. (Se você usar um balanceador de carga para o grupo, os scripts pós-instalação serão executados antes que um membro seja colocado atrás de um balanceador de carga).

## Configurando políticas
{: #set-up-policies}

Neste cenário, o website social está usando o ajuste de escala baseado em planejamento. Duas políticas são necessárias: uma para aumentar a capacidade dos servidores nas tardes de sexta-feira e um segundo para diminuir a escala dos servidores em noites de domingo. A primeira política é para aumentar a escala dos servidores.

1. Localize **Políticas** e clique em **Incluir política**. Insira o **Nome da política**, (Aumento de escala na sexta-feira).
2. Selecione a opção de espera do grupo para o **Tempo de espera**.
3. Clique em **Incluir acionador** e especifique um acionador de repetição selecionando **Todos** no primeiro menu suspenso e, em seguida, selecione **Sexta-feira** e **22h**\* nos menus suspensos subsequentes. (A caixa de seleção **Edição avançada** permite que você insira a frequência do acionador na notação semelhante a crontab.)
4. Clique na caixa suspensa **Escalar por** em **Ação** e selecione **Relativo**. Insira 2 no campo **Membros**.
5. Clique em **Incluir política** novamente para especificar a segunda política que reduz a escala dos servidores nas noites de domingo. O tempo de espera é o mesmo que a espera do grupo. O acionador é todo domingo à 1h*, com uma ação de escala relativa de -2.
6. O horário inserido no campo **Acionadores** é baseado no horário UTC, que é o motivo pelo qual você precisa selecionar 22h para 5h Horário de Verão Central e 1h para 20h Horário do Horário de Verão Central. Durante o Horário Padrão Central, os horários seriam 9h e 12h, porque o UTC/GMT não reconhece o Horário de Verão. Consulte o site [World Time Server ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} para obter um conversor de tempo.

## Incluindo um balanceador de carga local

Se você tiver um balanceador de carga local configurado, poderá usá-lo para balanceamento de carga de seu grupo de escala automática.

1. Localize os **Balanceadores de carga locais** e clique em **Incluir balanceador de carga**.
2. Clique em **Visualizar configurações de VIP** (abre uma página separada) para ver os balanceadores de carga locais disponíveis em sua conta e solicite um novo, se necessário. Um balanceador de carga precisa ter um grupo de serviços associado para ser usado com um grupo de escala automática. Certifique-se de que o balanceador de carga esteja localizado no data center de seu grupo de escala automática.
3. Clique em **Incluir balanceador de carga** na página **Incluir grupo de escala automática**, clique na seta suspensa para o IP Virtual e selecione seu balanceador de carga.
4. Clique nas setas suspensas para **Grupo de serviços**, **Porta de serviço** e **Tipo de verificação de funcionamento do serviço** e selecione os valores apropriados.
5. Clique em **Incluir grupo** para salvar seu grupo.
6. Se todos os seus data centers, redes, e assim por diante, estiverem especificados corretamente, seu grupo de escala automática foi criado. Clique no grupo na tela **Visualizar todos os grupos** para ver os detalhes do grupo.

O resultado de configurar um ajuste de escala baseado em planejamento é que dois membros são provisionados automaticamente para atender ao requisito mínimo do website. Às sextas-feiras às 17h no Horário Central, mais dois membros são provisionados automaticamente quando o primeiro ativador de política é disparado. Então, aos domingos às 20h no Horário Central, dois membros são recuperados graças ao segundo ativador de política. Se você especificar um balanceador de carga, todos os membros criados na criação, ou na sexta-feira, estarão atrás do balanceador de carga depois de executar o script de pós-instalação customizado.
