---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-07"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gerenciando aumentos de tráfego com o ajuste automático de escala baseado em recurso
{: #managing-resourced-based-auto-scaling}

Lançar um novo produto ou fazer uma venda de um produto existente pode causar um aumento no tráfego em seu website. Um aumento no tráfego pode afetar seu tempo de resposta, o que afeta a experiência de seus clientes com seu website. A escala automática do {{site.data.keyword.cloud}} permite responder automaticamente aos aumentos de tráfego. É possível usar o ajuste automático de escala baseado em recurso para controlar esses aumentos de tráfego.
{:shortdesc}

## Antes de iniciar
Primeiro, navegue para o menu de dispositivos e assegure-se de ter as permissões de conta corretas para concluir as tarefas.

* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assegure-se de ter quaisquer permissões de conta necessárias e de ter acesso ao dispositivo. Se você não for o administrador da conta, a sua conta do usuário deverá incluir permissão para usar a escala automática. Para obter mais informações sobre como atualizar as permissões para usar a escala automática, consulte [Configurando permissões de usuário para a escala automática](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale). Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões. 

Para obter mais informações sobre permissões, veja [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Incluindo um grupo de escala automática
{: #adding-auto-scale-group}

Por exemplo, um Dallas, o website de e-commerce baseado no Texas requer que três servidores virtuais estejam on-line o tempo todo. Os negócios aumentam entre os horários de 9h e 17h todos os dias da semana quando a companhia mantém vendas on-line. Para ajudar a sustentar os tempos de resposta do website, mais três servidores virtuais são necessários durante esses horários. Além disso, quando a média de tráfego de entrada pública for superior a 5 MB por segundo em todos os servidores virtuais por 10 minutos, mais dois servidores virtuais deverão ser provisionados. Quando o tráfego cai abaixo de 5 MB por segundo, esses servidores virtuais extras devem ser cancelados e removidos. O objetivo é ter no máximo cinco servidores virtuais manipulando o pico de tráfego, o que impede os servidores virtuais de dias úteis de serem impactados pelo tráfego extra de dias úteis. As etapas a seguir acompanham você na configuração da escala automática para suportar o ajuste de escala baseado em recursos.

1. No menu **Dispositivos**, selecione **Escala automática**.
2. Selecione **Incluir grupo de escala automática**.
3. Configure um grupo de escala automática primeiro inserindo um **Nome do grupo**, por exemplo, Grupo de escala de fim de semana e, em seguida, selecione o data center.
4. Selecione a política de finalização do servidor. Por exemplo, se você escolher **Mais antigo**, o servidor com a data mais antiga provisionada será selecionado ao reduzir a escala.
5. Indique se o seu grupo deve ser um grupo de escalas de múltiplas VLANs e como equilibrar a escala nos pares de VLAN configurados
6. Selecione as VLANs públicas e privadas nas quais você deseja seus servidores provisionados. Se os servidores forem acessados por meio da Internet pública (se a VLAN estiver executando servidores da web), deixe **Rede privada somente** desmarcado.
7. Configure o **Mínimo de contagens de membros** como 3 e **Máximo de contagens de membros** como 6. Configure o **Tempo de espera** como 0. Como isso é um ajuste de escala baseado em planejamento, não há estatísticas reunidas para acionar ações de ajuste de escala.

## Definindo a configuração do membro para seu grupo
{: #defining-member-configuration}

1. Localize **Configuração do membro** e insira um **Nome do host** e um **Domínio** para o servidor de ajuste de escala. Os servidores subsequentes incluídos no grupo possuem sufixos exclusivos que são anexados ao nome do host.
2. Especifique a configuração de hardware das instâncias de computação (núcleos, RAM e assim por diante.)
3. Selecione um sistema operacional se você desejar instalar o sistema operacional mínimo. Também é possível usar uma **Imagem pública** ou **Imagem privada** para provisionar suas instâncias.
4. Se as instâncias exigirem etapas extras para instalar software adicional, especifique a URL de um **Script de pós-instalação** para instalar o software. (Se você usar um balanceador de carga para o grupo, os scripts pós-instalação serão executados antes que um membro seja colocado atrás de um balanceador de carga).

## Configurando políticas
{: #setting-up-policies}

No cenário, o website de e-commerce está usando o ajuste de escala baseado em recurso. Duas políticas são necessárias: uma para ter uma ação de escala relativa de +3 para o prazo de tempo necessário e uma segunda para ter uma ação de dispensa de 3 quando o aumento acabar. A primeira política é incluir os recursos.

1. Role para baixo até **Políticas** e clique em **Incluir política**. Insira o **Nome da política**, (Aumento de escala de dia da semana).
2. Selecione a opção de espera do grupo para o **Tempo de espera**.
3. Clique em **Incluir acionador** e especifique um acionador de repetição selecionando **Toda** no primeiro menu suspenso e, em seguida, destaque **Segunda-feira, Terça-feira, Quarta-feira, Quinta-feira** e **Sexta-feira** e **14h**\* nas caixas suspensas subsequentes. (A caixa de seleção **Edição avançada** permite que você insira a frequência do acionador na notação semelhante a crontab.)
4. Clique na caixa suspensa **Escala por** em **Ação** e selecione **Exato**. Insira 3 no campo **Membros**.
5. Clique em **Incluir política** novamente para especificar a segunda política que remove os servidores todas as tardes. O tempo de espera é o mesmo que a espera do grupo. O acionador é a cada segunda-feira, terça-feira, quarta-feira, quinta-feira e sexta-feira às 22h\*, com uma ação de escala exata de 3. O horário inserido no campo **Acionadores** é baseado no horário UTC, razão pela qual você precisa selecionar 14h para 9h (Horário de Verão Central) e 22h para 17h (Horário de Verão Central). Durante o Horário Padrão Central, os horários seriam 13h e 21h, porque o UTC/GMT não reconhece o Horário de Verão. Consulte o site [World Time Server ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://www.worldtimeserver.com/current_time_in_UTC.aspx){: new_window} para obter um conversor de tempo.
6. Configure outro grupo com o resfriamento de 0, denominado, por exemplo, Grupo de burst de tráfego, com uma contagem de membros mínima de 0 e um máximo de 5. Use as mesmas configurações para a configuração do grupo e do membro como o grupo do Aumento de escala de dia útil, exceto para o nome do grupo.
7. Clique em **Incluir política** para incluir a segunda política que controla os dois servidores adicionais quando o tráfego de entrada público é de média de 5 MB por segundo em todos os servidores virtuais por 10 minutos.
8. Insira o **Nome da política**, por exemplo, Grupo de burst de tráfego.
9. Selecione a opção de espera do grupo para o **Tempo de espera**.
10. Clique em **Incluir acionador**. Deixe o padrão **Se meu** na primeira caixa e selecione **Rede Pública de Entrada Mbps** para a segunda caixa. Deixe o padrão > sinal na terceira caixa. Na quarta caixa, insira **5** (5 MB), insira **600** na quinta caixa e selecione **Segundos** na última caixa para representar 10 minutos.
11. Clique na caixa suspensa **Escalar por** em **Ação** e selecione **Relativo**. Insira 2 no campo **Membros**.
12. Clique em **Incluir política** novamente para especificar a segunda política que remove os servidores quando o tráfego tiver diminuído para menos de 5 Mbps\*O tempo de espera será o mesmo que o resfriamento do grupo. O acionador é Se a minha rede pública de entrada Mbps for menor que 5 (5 Mbps) por um período de 600 segundos (10 minutos).

Quando os dois grupos são criados, o grupo Aumento de escala de dia de semana cria três servidores (o mínimo). Nos dias da semana, às 9h do Horário Central, mais três servidores são incluídos e, às 17h do Horário Central, os servidores são removidos. Não há outra maneira para os membros serem incluídos ou removidos desse grupo. Em um Grupo de Distribuição de Tráfego completamente separado, dois servidores são incluídos para cada 10 minutos em que o tráfego público de entrada em todos os membros tem média de 5 MB por segundo, até atingir o máximo de cinco do grupo. Após o tráfego público de entrada ficar sob esse valor durante 10 minutos, todos os servidores nesse grupo são removidos.

